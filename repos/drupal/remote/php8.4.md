## `drupal:php8.4`

```console
$ docker pull drupal@sha256:8be7fc5bc04f2c957e42c9c9f28dcaa927e22109b704216aec6ca8077a402971
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

### `drupal:php8.4` - linux; amd64

```console
$ docker pull drupal@sha256:113e9abdeb20549217928b52e22956f1f44607893057d1fcd403b0613a9ccad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203445262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe02e72e098b1341f0b4baf7a46c20130f63dcd383a5bf9e68fa4bdac71e4ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccdcb705a77aabd7829e7a2ab1a74391d241147a56a06453a52f82044ea0922`  
		Last Modified: Tue, 04 Feb 2025 09:00:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6eea6d4777a96c3233f01e7b4e4a0e8c1e9e9e92e467cd24127f5423c673e7`  
		Last Modified: Tue, 04 Feb 2025 09:01:03 GMT  
		Size: 104.3 MB (104345493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f3f460766db51f3c434927f14199fba8450d0a89b4ed7abbf5a581f3f4a9`  
		Last Modified: Tue, 04 Feb 2025 09:14:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db757b18230f56cd624d4ab7877369e0a37b1c69b215f0126c15c9b3deb0d1b`  
		Last Modified: Tue, 04 Feb 2025 09:17:52 GMT  
		Size: 20.1 MB (20123771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df1c4345cb9338a66b465da86ec097f830f79574954b1d779f53e1867e4010`  
		Last Modified: Tue, 04 Feb 2025 09:20:59 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf432328c30ca5763416cef4fa340fec936e95cd53967ebca24fbe3a7d0eedbc`  
		Last Modified: Tue, 04 Feb 2025 09:04:03 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ee054a0220cbe3e745cdfbd7476fffdf819929c3551fefab10e2dd963c963`  
		Last Modified: Tue, 04 Feb 2025 09:01:01 GMT  
		Size: 13.7 MB (13699074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d4bd31e823f347cf4012f44de09bc2d507e01cb5c5b5a8a72974f5b37ca15d`  
		Last Modified: Tue, 04 Feb 2025 09:09:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eab40ab3013a218aa407395b210a4f6c203627c6130ac3ff4cd1111f1119b`  
		Last Modified: Tue, 04 Feb 2025 09:00:18 GMT  
		Size: 14.1 MB (14140153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94ea33dae5ff86bacf9f06008851bf22d6c537d46c469b101e76f001df17c8`  
		Last Modified: Tue, 04 Feb 2025 09:15:39 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33586a0f5b8cdda0827e40aa83675ffe91dc8e927909d827cd04ad02bf3ca439`  
		Last Modified: Tue, 04 Feb 2025 09:02:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a5f3fa8877f42df832bdb7ad0cc3bcd1a6930ef1e9f7967c5d918c8696039`  
		Last Modified: Tue, 04 Feb 2025 09:20:49 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a0a83ae94d4e7df62e4f6137386ba43b8c20188d0579257661ef862fa7d7e9`  
		Last Modified: Wed, 12 Feb 2025 21:01:17 GMT  
		Size: 2.1 MB (2116973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bb1802f7dd7ece34cf0fc18ef89d83f358cd6fb8f3929cb25842869f4aad7d`  
		Last Modified: Wed, 12 Feb 2025 21:03:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3294d74c73c5f3d741785538fea66439a81b02805f320f73c05610ea8f8f9db`  
		Last Modified: Wed, 12 Feb 2025 20:29:30 GMT  
		Size: 740.4 KB (740355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d9d185f8a3b080a1feaab1cdf76d99ea7ece2d799c323c200846f56da7dc86`  
		Last Modified: Wed, 12 Feb 2025 20:51:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333dc7b02abdb70e2d51966c5bfd07f9ef851f736054f78f150e483d8b659b1`  
		Last Modified: Wed, 12 Feb 2025 20:51:29 GMT  
		Size: 20.1 MB (20061245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:7a79f56cf2362d1399369c6bcab11af703a2ace1e56d739f9fb9f1695471c46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6883181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c770bb00436a3431f5c51e9365853c833cf816625f4173e104c4cc83dad6c5`

```dockerfile
```

-	Layers:
	-	`sha256:a43b15907c2466f8a152b1d4bb539039b552fb7c6be8c99c7b9003ab6a0874fa`  
		Last Modified: Wed, 12 Feb 2025 17:30:41 GMT  
		Size: 6.8 MB (6843991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3014cab8bbafc4c030b266c36d49bfe0f705af3313a7baf2cb9cfd20dd1c6e47`  
		Last Modified: Wed, 12 Feb 2025 17:30:41 GMT  
		Size: 39.2 KB (39190 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4` - linux; arm variant v7

```console
$ docker pull drupal@sha256:903218444dfa863b6423fd2b5b2ac05b5e96475289676e5aaa4e9b4eb76a9f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167075923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afadeacd866aa38a400703d4a5e2bd6c91ea846a5bb8c254f7cae3b9867228fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3121bf0a9ad47be9cd9230d76c59964a3c5c2ad428f1f2d5e0ea10c439534`  
		Last Modified: Tue, 04 Feb 2025 16:46:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e514983dd1fb84c6ee305b52a5a3c4aa50f60f471002066ed6c1fc22642b`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 76.2 MB (76162605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2400437b25b5d1b02d62a06166a2fb642e727da4868737aedeb7e86797c34448`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db855c0ccbd5449d40ab70032bf7b56fb3cfea2bade47fc7c1bda6c7772901`  
		Last Modified: Tue, 04 Feb 2025 09:33:29 GMT  
		Size: 18.9 MB (18857283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe7af15f7e5d8a84ddc0ee0c05a5748052ebb16cdf52e6db919f2bc9e48d4d0`  
		Last Modified: Tue, 04 Feb 2025 09:17:04 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb55ddf2b979059029229318166cb34829e074c9b4af0504b65ac6066e9e0fc`  
		Last Modified: Tue, 04 Feb 2025 09:33:28 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4465e50abcaaf028d083ee8e43ee906c7ef318f0ed68f769cb8a3f5fa825f47`  
		Last Modified: Wed, 05 Feb 2025 08:34:31 GMT  
		Size: 13.7 MB (13697053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439fbdbf2860fc2aaf7ebbd81f244fc1162244d8699554ec89e94c692519d41d`  
		Last Modified: Wed, 05 Feb 2025 02:41:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1ebcccf8b8e4df27aa398b7e7cf4309ce4113e199efcc00107069750164a8e`  
		Last Modified: Wed, 05 Feb 2025 01:08:33 GMT  
		Size: 12.3 MB (12271891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c67235a0dcf1899c9342f8864db6a4884de7456c5a8a7265a35cfe62144c5`  
		Last Modified: Wed, 05 Feb 2025 06:17:21 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca80679fc97137d2f5ba2155f8dffc580488299c086883e488646e95c13e84f9`  
		Last Modified: Thu, 06 Feb 2025 00:28:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04015fd30c315d6159ef571cf9ccd565a5472ff86432943ff8702eab1cfa0d8f`  
		Last Modified: Tue, 04 Feb 2025 12:03:12 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1121b73ba86f1e376712aa599327328849c82875ed6b8db222b5123ad11b3c30`  
		Last Modified: Thu, 13 Feb 2025 09:06:26 GMT  
		Size: 1.4 MB (1365142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca669bd741ba8c83ccec06ef13ea3cc09a0304ad2b119ec9ee4dd5a9e55d2c7`  
		Last Modified: Thu, 13 Feb 2025 09:06:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2352482cf5473b8af4d0ab1f54c6c0691a710f6615512f33b19e01f8b6842`  
		Last Modified: Wed, 12 Feb 2025 20:29:14 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7f3bf98242bb3c4ffc0a9362eb64b5afede70522f9f471d06d819c268c53f5`  
		Last Modified: Thu, 13 Feb 2025 09:06:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b264e22aebca3894a9092262ae5b9e0650c50e87fce89cbdaa8f6d82c7fcf59`  
		Last Modified: Wed, 12 Feb 2025 17:31:58 GMT  
		Size: 20.1 MB (20061159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:3e32a84f8029f00991ed3b8a8e73365b0b23b2cd8b74a680ad5f3eba0b706e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6709695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c591ab77cd50f6c423f8c30cf71549ad9f5be512bf1d8adddca281e5127ff9`

```dockerfile
```

-	Layers:
	-	`sha256:773e542d5fd02ba2d92aac1c3f99cf16abb272b94feb94c508680fbd6abfa307`  
		Last Modified: Wed, 12 Feb 2025 17:31:56 GMT  
		Size: 6.7 MB (6670323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725717e17f2c7d3747ec887195e6382c733c9089eac7cf282f71cf01ac0985c0`  
		Last Modified: Wed, 12 Feb 2025 17:31:56 GMT  
		Size: 39.4 KB (39372 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6b4cd4ec4b1a0695b76d6cae3c3726cda98c84ceb25500c409b1bdf77bf76293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196573515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762ab2cf679000b8ed51b1450a3c3f743f410c7da467cf59657f2d081848d3e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16d737fb0a30c662d9b2adf51f2dff7d89c28971aed9f2463503588644f91d`  
		Last Modified: Tue, 04 Feb 2025 09:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8571b79e8caaac6ec73bed43c061c8744cd39e18a67d9cd17dd79b0d6ea2e1`  
		Last Modified: Tue, 04 Feb 2025 08:59:42 GMT  
		Size: 98.1 MB (98130343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f74dc117b0b71ab00cf12fe8d534cbeab80ebf367380080264b1ddede90d92`  
		Last Modified: Tue, 04 Feb 2025 08:49:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349801e0b439bb7399adf1a3bad741322f9e25c3d7095d77525bb3d33598bde0`  
		Last Modified: Tue, 04 Feb 2025 09:11:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfb56ebf305e8086f08b1a2decda71f875642031182c450dfa65bc15d26a02e`  
		Last Modified: Tue, 04 Feb 2025 09:19:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6d105874122db2dfaacc1f9637c71272786724301db52dff0c0738d2155a94`  
		Last Modified: Tue, 04 Feb 2025 09:09:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2dbedf0e1bfe4e4d452abfa6fb568a80d4972258863b5d86fc266b4cad3b9f`  
		Last Modified: Tue, 04 Feb 2025 10:21:18 GMT  
		Size: 13.7 MB (13698846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48848b554bd1aaee38ce11645885fc981243e9b4d5e1970cfc53071a6e2047ea`  
		Last Modified: Tue, 04 Feb 2025 09:57:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2890b646f350b06e29eb68bd2c0509d9a67c4439678b30d40043af453366d`  
		Last Modified: Tue, 04 Feb 2025 10:04:25 GMT  
		Size: 13.8 MB (13758246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d751cb2c4005ab1b06d5f8124f28d5f1ea56086162d06513e9e43a46896943`  
		Last Modified: Tue, 04 Feb 2025 09:33:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b089af2c17a934f5412d943f1d7c9f1d4561840a64f9440f1447cf85da276cc0`  
		Last Modified: Tue, 04 Feb 2025 09:33:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10ab8ac4e1fc36cc83b15ce004e63c7c30887b317c1c199350a8f9b070b1f10`  
		Last Modified: Tue, 04 Feb 2025 09:15:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d9b05e13ba169fadefebc302c845817e4788f6c3b20bc20c2ffdb15f7c550`  
		Last Modified: Wed, 12 Feb 2025 21:13:56 GMT  
		Size: 2.0 MB (2016827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b5e003bbd9e5fd04b61c7ff61f660c5ad6f633dd0cb031198a60d33804c93b`  
		Last Modified: Wed, 12 Feb 2025 21:16:09 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc661fd2fd5dfc929e5e0c03e59c2de8d260d4e5780cf9e8739e0e25bdc35f84`  
		Last Modified: Wed, 12 Feb 2025 20:32:25 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11c2bd74660d1ce4ce479c3deb2d11c2d5505975638350dfd9f01d70bce594e`  
		Last Modified: Wed, 12 Feb 2025 21:13:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a86f942efd8364504f7e1f6977757516b4d16457f49f70bf62caba27bab54c5`  
		Last Modified: Wed, 12 Feb 2025 21:16:13 GMT  
		Size: 20.1 MB (20061186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:86a2605a97cc8200e69182b9da67569ae2d13fe1eef7e426972c1953caf4ce30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6923237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db418c3f9a53a1363b934a25eba09581d4fa06bc5c7753e97e7243e5467ac6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0a0918640b28c857bb74a4ea3326027396aab967546a9eba2b7667f75c561fd`  
		Last Modified: Wed, 12 Feb 2025 17:31:16 GMT  
		Size: 6.9 MB (6883797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1aecbf3a001cd53be185014fd6aab0f3f57c0a8c7c2a47691f40ca30f296e4f`  
		Last Modified: Wed, 12 Feb 2025 17:31:16 GMT  
		Size: 39.4 KB (39440 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4` - linux; 386

```console
$ docker pull drupal@sha256:18e6d331b433ec58a1590bc399ea0f7a1e7b9c7b09619eca8b20d5a445a6870d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202486383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b3b2e83d578e299c7340c3f7aa1b1514384f67c87b962d9f20328fe37e2a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7c77c81e129b42a96b4092472647dc8f7293487b714eb22fb20d2556b5524c`  
		Last Modified: Thu, 06 Feb 2025 02:03:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08d17fdf6e84e73294d7f36a7f5164c2f6128d945459984f44a15c2541a6699`  
		Last Modified: Wed, 05 Feb 2025 01:34:25 GMT  
		Size: 101.5 MB (101513092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea77627ee16bb80267d06e2c22ddab28319d4845e99a76dc8d84738e9723db17`  
		Last Modified: Tue, 04 Feb 2025 12:05:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d343b1d4eab9784344bbcb3a85d037db2f096fdbfb1f72f4d7bf2bd295a5d2`  
		Last Modified: Thu, 06 Feb 2025 02:04:01 GMT  
		Size: 20.6 MB (20638467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4824d53f7e5663c8ee8a87fbd6114d3c6d023ff342552ce46c3043b84dd6b`  
		Last Modified: Wed, 05 Feb 2025 06:27:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3283fd8479333c2dd7a4cd234d381695b81716146845fee07ca10516aa2b9d0b`  
		Last Modified: Thu, 06 Feb 2025 02:04:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05672602d3271741a874785ce270649a73f0c042ac63b3e3af180d732c957ba`  
		Last Modified: Tue, 04 Feb 2025 12:05:04 GMT  
		Size: 13.7 MB (13698108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f906d44dc95b7a2f2b29e88d26884320b474e63bc0a11e19c96f02aa59a6f`  
		Last Modified: Thu, 06 Feb 2025 02:04:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006fa2a1ccf081c58bee7fd830f9b26e8bd3e4ec4aa117119d4810c283ecc848`  
		Last Modified: Thu, 06 Feb 2025 02:04:07 GMT  
		Size: 14.4 MB (14432567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707d3027eb46910dff2b385769e753683e15357588eb2799099dc2ce2a9a1e18`  
		Last Modified: Thu, 06 Feb 2025 02:04:08 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b3606f44bb71bb2e85f08c604d97c6c1c4abfae56768632a204c7f9456fe0`  
		Last Modified: Wed, 05 Feb 2025 01:34:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0280e24bc35c8393ff40aa4b88a2dea57218c056b9f926cc49ba0c18e7c72a4`  
		Last Modified: Thu, 06 Feb 2025 02:04:09 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0254ff1d8a2091ac06a48f151d1438a92be814d7ebdaa40a9983c5758922efc3`  
		Last Modified: Wed, 12 Feb 2025 17:31:00 GMT  
		Size: 2.2 MB (2209194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4ff386ba2edf15d31384ad751d4b5f8e13116ab2e08756459e3981c8314ebc`  
		Last Modified: Wed, 12 Feb 2025 17:31:00 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320f8246fc3d9aa111b7f07983c81d9c7efa630264b076a01911910701083747`  
		Last Modified: Wed, 12 Feb 2025 20:29:11 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0520119149c0761ef16cb9da9f4dac6e12db88bd9921c47f64d66c043b4cef`  
		Last Modified: Wed, 12 Feb 2025 17:31:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d0c40ae74c51dd248d6a3b985bd213f9630e699f33e97d044ebc88b1fddcd`  
		Last Modified: Wed, 12 Feb 2025 17:31:02 GMT  
		Size: 20.1 MB (20061254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:ca2ee925550398de5b991a0d4f16c0a0de0d95fd345a0e22b1aeb2b3e837f85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1618fa797019e525dab8bfb3171d6aa86cfb030b7a07a2c50762824b779d128`

```dockerfile
```

-	Layers:
	-	`sha256:f989c346f1dfa1b7b57de3c8a3e2c19c10f18eccff95148f8d20651665a52a85`  
		Last Modified: Wed, 12 Feb 2025 17:31:00 GMT  
		Size: 6.8 MB (6824222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d251e62160ec4abbe9878118c4270b1c1bf7b0bac3471236093a9ce690208c`  
		Last Modified: Wed, 12 Feb 2025 17:31:00 GMT  
		Size: 39.1 KB (39107 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4` - linux; ppc64le

```console
$ docker pull drupal@sha256:fedc5dc60b3319d24fbc3251e6379bee3364a494fe02c76d39ce811929f18883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207619157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b889b2e921bab6d46a11be1b5b845356ab1e467a063114d6069fd54673b1b499`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 09:24:12 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 23:02:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5218c0aca3f23dfaf27a513c2d06daa612d2386294a53d81f7ddbaba9d45ee`  
		Last Modified: Tue, 04 Feb 2025 09:33:32 GMT  
		Size: 21.3 MB (21308399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e7b8f37e12d934578444c6271234e36e9309afc271390ee87415e245ca5b87`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca689848e7e5a26455cede87aec423ec507686f316f5ae1d8789563c816b887a`  
		Last Modified: Tue, 04 Feb 2025 23:02:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a142501c800a3e0c1a86f8dc9b9c68e6eb5822af88762f700e777fda8465c51b`  
		Last Modified: Thu, 06 Feb 2025 02:04:30 GMT  
		Size: 13.7 MB (13698591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a13e8c518149a1f3646caf57c9bc08b2a9520b40d7e6fe55424367a13ffced`  
		Last Modified: Wed, 05 Feb 2025 02:41:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b59f21315415912172700488b07ac495c01429694283541899498c101e4261`  
		Last Modified: Thu, 06 Feb 2025 02:04:33 GMT  
		Size: 14.6 MB (14565025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba89e5d4fd3917648fba94f93b748da799a3262fad035f03fb4472e20ba089b`  
		Last Modified: Thu, 06 Feb 2025 02:04:34 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e83d7ffad9c1068fb727b693861b6d0e4482274aa7816f09b47daf12d356072`  
		Last Modified: Tue, 04 Feb 2025 12:03:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746da4bb4767f7597d2d1d140ac409b4af4184589f8d7afd60c624fbc9ed667a`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39b83f15d852231c1c9fe7a39803b7bd8929e17d1d2d73c278006f2d3c9070`  
		Last Modified: Thu, 13 Feb 2025 09:06:18 GMT  
		Size: 1.9 MB (1870862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c87d49358e5e17416839bada8f49220b4d6d5585ca815bbe25df27a9bc96be3`  
		Last Modified: Thu, 13 Feb 2025 09:06:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28f31230f9ab14393783682b12c4ca7a38a29c8df84753d17f3270111773f83`  
		Last Modified: Wed, 12 Feb 2025 20:28:31 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f67e2fae60891613614ac35974432ff7e7ad548c33ff1a58f29512730b9f33`  
		Last Modified: Thu, 13 Feb 2025 09:06:19 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b24fa67d3ed0f4542a6b91bf387a40aea9483a492e877e4dbe1f18b7442f055`  
		Last Modified: Wed, 12 Feb 2025 17:32:01 GMT  
		Size: 20.1 MB (20061229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:1af64aedf287495db3b21117207a77407bac7222a43a241e3c770ce7a25b3e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6871646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c0afdca77ce1f0dc577cfc7526078d8a7ed3c6d2039e7ddbeb398f74bfaabd`

```dockerfile
```

-	Layers:
	-	`sha256:43379148ef1510bd651af2bd017a75d85da6654a64de56aa409b3664bca988d7`  
		Last Modified: Wed, 12 Feb 2025 17:31:59 GMT  
		Size: 6.8 MB (6832351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec382b15194de4e1dc4e7e99309cb26307e9edc720dc20af39ca81ada5306c1`  
		Last Modified: Wed, 12 Feb 2025 17:31:58 GMT  
		Size: 39.3 KB (39295 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4` - linux; s390x

```console
$ docker pull drupal@sha256:50a2735eedf9b9aea01401d33ec60673fc6dc8e3d469d4dbda53937cf918b356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177168685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170696a6b2e3c43b8ce8f2a9bf7da69c77d559a267e42ecc99fd6a98d2156090`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 12:11:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 09:33:36 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 16:01:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8253988c6a24fa76feaf6e34729bf23e9a788e7438b3da6a7db669f072c5ab9e`  
		Last Modified: Tue, 04 Feb 2025 11:21:40 GMT  
		Size: 19.9 MB (19895180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82684711048482eb8cc4b2f6548b4d6e7ece37d508c1ea3a12ab8f229f29fda`  
		Last Modified: Wed, 05 Feb 2025 00:01:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5cab685c9f3203c43aafec691ac532f2bd71706ad37119783a03535a44ba2a`  
		Last Modified: Tue, 04 Feb 2025 23:09:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da428e1625fee48d36398a6b96a83758fb1a46be6dd3e6f717f560dda79e6b4`  
		Last Modified: Wed, 05 Feb 2025 06:43:02 GMT  
		Size: 13.7 MB (13697502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb601e7ed0879c438798534ff640ac322da96ccc755c6ef790c665af4bd840`  
		Last Modified: Wed, 05 Feb 2025 06:43:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312ff8713c424b41a8109b796d6e4e06c9fc0f1a5b885a1f56bb8e18b3a266d`  
		Last Modified: Tue, 04 Feb 2025 16:47:20 GMT  
		Size: 13.5 MB (13528082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095a19a739d5c2745cc4461310dbacf87a240f3c9df62d78ee6e88fd0e3e7ef1`  
		Last Modified: Thu, 06 Feb 2025 02:04:46 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84087def673fbddf84c8e793881a8896765b773b83dd10a836954c3ba94f848`  
		Last Modified: Thu, 06 Feb 2025 02:04:47 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbdc431f86f6da8c69f47fdea486987ce983bf970f9d4b48bf2ecdeda160db7`  
		Last Modified: Wed, 05 Feb 2025 02:41:19 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a418f51d1ed433939b73be7a4e5b17d16ea6ffaad6ee19088f7d9ed26ce495`  
		Last Modified: Wed, 12 Feb 2025 17:34:52 GMT  
		Size: 1.6 MB (1564579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e14c2a1b3741f41d10ba5ff7eec7b80b9499ecf9dd476fe065108c204b66e8`  
		Last Modified: Wed, 12 Feb 2025 17:34:52 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288bae4b5f004f36b732936231f3c723f8db2eb1ff647d02d55ffa4b68b1d66`  
		Last Modified: Wed, 12 Feb 2025 17:34:52 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae55f080b453d3ff1962c4e25afa0df46fcd902b88323b26ee1daed28c6d2e20`  
		Last Modified: Wed, 12 Feb 2025 17:34:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b58bb9ab9faa45995e7815bd64d02721be4338b20d44a95fe3d280fbfbddfa`  
		Last Modified: Wed, 12 Feb 2025 17:34:53 GMT  
		Size: 20.1 MB (20061242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4` - unknown; unknown

```console
$ docker pull drupal@sha256:82825628fbec938c8148375daa37479997e5e61ea878600094890e849138f6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6735896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d167fd54c97d032ec26c5b4e333c12ba74fe9c65432fbcd671d6294a927e696`

```dockerfile
```

-	Layers:
	-	`sha256:e31bce1a8236fb0b389ccac499fcd1c830f83293253ccc790af65ddb928f7e13`  
		Last Modified: Wed, 12 Feb 2025 17:34:51 GMT  
		Size: 6.7 MB (6696713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69d4fa0bcdecb1f5dd3a0e1df2e616540d0ac77eeca156a06b5346a05c815f4`  
		Last Modified: Wed, 12 Feb 2025 17:34:51 GMT  
		Size: 39.2 KB (39183 bytes)  
		MIME: application/vnd.in-toto+json
