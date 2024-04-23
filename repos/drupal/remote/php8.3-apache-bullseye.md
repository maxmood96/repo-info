## `drupal:php8.3-apache-bullseye`

```console
$ docker pull drupal@sha256:cf4db8a672adb66587e4c8ee62b72b158ad824f52c6bb34cdb76c8de94e49e57
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

### `drupal:php8.3-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:256d925e38ed12534ed2cf9345b0e0847440945b11df375682c7c6aaf0de95e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188630820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26165cd02a6f4ab6f78da536f6809fc64489bd463d99eb64b4a69eab1ba442dd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a09bf591af6aa18ca1e47bf7fb6d5b8a94b361f49d572e22973eaffb9c61d3`  
		Last Modified: Wed, 10 Apr 2024 12:26:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63fe8cf3a3ac18fbbeb84a6bcfd82dca8f26e775dd8ff9b1042dbcccfb04f0`  
		Last Modified: Wed, 10 Apr 2024 12:27:09 GMT  
		Size: 91.6 MB (91640010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b92c4ecc2a1a38639ae53e2931c4b637365db397a7bb7bea09e097637979c69`  
		Last Modified: Wed, 10 Apr 2024 12:26:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c90252fcc0571c2b6e50c7fcbe629517ba0cf269a2c92b2171853719ad5026`  
		Last Modified: Wed, 10 Apr 2024 12:27:26 GMT  
		Size: 19.3 MB (19258377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32183726aaa5f55cd2ca3e3382900f1e3bc14c941ad90f91c7842283af025440`  
		Last Modified: Wed, 10 Apr 2024 12:27:23 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5347604417b38d526466b64f3e983028e59b63c1168a31f0e095afbd62b333`  
		Last Modified: Wed, 10 Apr 2024 12:27:23 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58aeee410248da0551fafd7b7c33d324e99df37144cfd53e5de3e03df1dc585`  
		Last Modified: Thu, 11 Apr 2024 19:42:45 GMT  
		Size: 12.8 MB (12808695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec1324c0009cde03fd8b2575dee6352d003ab3cb65e66530ffe3c7ac3c3dd5`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a08263592e9ed27f0007c5fa7564d1ec2d6bcf35c68ee52c8a30b04e52aa4c`  
		Last Modified: Thu, 11 Apr 2024 19:42:44 GMT  
		Size: 11.6 MB (11573598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaee8939b2752ca2bb944cfcfbc16bbe75dfc1a0094ffbee8b3cfb8bcd46691`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c5384923bd990af12fb29d057b74385c2cde6aab3699fb86115ff60bd7b1e`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00294aba7ed6b11e76e8769fe8c71b8aecf4e9ee0fe768e4c13e79d20584edeb`  
		Last Modified: Thu, 11 Apr 2024 19:42:43 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2a65baba3c5a0d47f9fddfd6f073271eca3ecf319413e10c9c18fb100698a9`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 1.9 MB (1930390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2108d33e4e25f577471bea8025fd0c93d94eb31b2a100bb2b7fbf1679c5e45b`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22f997db4fdfd2f132e67855eb67da7e62d4209ae2537b2243c181d2578cd`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 723.9 KB (723945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac8b449aac4a1e7e34eff9e56a44edf2260434c15b2ef4d9c01f8f8e6345586`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a227eba0dce33244261bbf2155276aa1f1d95e23a0027fb969443452f3bcc6`  
		Last Modified: Tue, 23 Apr 2024 17:54:48 GMT  
		Size: 19.3 MB (19262056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:fb9dea1c5e44378064d4e47c2a20349c8d68544163a812076a743e9fbe00dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7007455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69cec9641d987e6fc718c7cd7a42e1f72656bda2d9b6e1b275b65796a601ed8`

```dockerfile
```

-	Layers:
	-	`sha256:51b2b093c5b5ed0da634fa5e976a2fb42a6f18d1a037e69419bc243293da4ccb`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 7.0 MB (6967508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a3d205002544229c1e1ab922dc8927b29c526bed1841a16b5b053afd0f8779`  
		Last Modified: Tue, 23 Apr 2024 17:54:45 GMT  
		Size: 39.9 KB (39947 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:00b60838fb22ff26289e0c8ea3357ff017d2132c604aa963be42ed8de28b10fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158045704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283cec6b67f71cb918e5001a031b1cfaf0407c78cffa4c6517eed7fe7a5710b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a36d9891eefe34cc386e8f6e07bb4a652abb6889dba10af0d41e5bad62ec9`  
		Last Modified: Wed, 10 Apr 2024 15:50:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f4929d4ebe8a6444b4b3e2fecf310b784254e270c11226e566a981a274c59`  
		Last Modified: Wed, 10 Apr 2024 15:50:52 GMT  
		Size: 69.3 MB (69322863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df67edc88110a99e5baa75d813f45c5c4a65d0efa18a57773c1706349828a23f`  
		Last Modified: Wed, 10 Apr 2024 15:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9aeed1f01bb97573aa5b12b9cc36b65bcf60db555e6354e9ca32e196f8a970`  
		Last Modified: Wed, 10 Apr 2024 15:51:10 GMT  
		Size: 18.0 MB (18017614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d8b4e70f4b084437e788317a9cc992325122e8ea9722e63daad3ada7491c64`  
		Last Modified: Wed, 10 Apr 2024 15:51:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f7828acb96a4ac10db29925d8b4231aa21778d3b51367dc9c29d343a81cbdf`  
		Last Modified: Wed, 10 Apr 2024 15:51:07 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf3e278459bdf17bfdae75f852b27a157a614275dd0b250b4b610d679062dee`  
		Last Modified: Thu, 11 Apr 2024 21:36:04 GMT  
		Size: 12.8 MB (12807320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44aa9580335ebe254674677898e3eb95520f64ae61a0198c2d9a3af63925d976`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17f49d2f73e5d299d8e13c60772d055b3b8afb81e8357326153052db79344b0`  
		Last Modified: Thu, 11 Apr 2024 21:36:01 GMT  
		Size: 10.0 MB (10007892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1f59ff050a7076f52cf6b33d300ae1105e3b7e21877fdf8b472d120fc67d7a`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e53886dd7aae3aeffed3ba4f2cf8f4df6baaf6860a94a0e31bd3e750aef94`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde7581e764772c557edf9b6a4c29ed33719b2ff167999390f0fdb2822762b50`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4762fd4a7e91a7fc8d6b2950e5651a3ce31956ce79b7da71d78726e17e62ac`  
		Last Modified: Fri, 12 Apr 2024 10:37:48 GMT  
		Size: 1.3 MB (1311205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128e4942d78f25a0905d6582567e0d40d3dc23bd29239697368225ec0bd4af55`  
		Last Modified: Fri, 12 Apr 2024 10:37:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e06e5706f9252362b421a139de8f504b84d77f6cb6251698d18106e890aef33`  
		Last Modified: Tue, 23 Apr 2024 19:08:59 GMT  
		Size: 723.9 KB (723947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0de10856facb2431a24e43f9e51fb4df281e8deae51c2de3fedf7440f7d64`  
		Last Modified: Tue, 23 Apr 2024 19:08:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507f6d1def48599012837a52cfab420f8fd52777bc2d11e67583e345ff134fe3`  
		Last Modified: Tue, 23 Apr 2024 19:08:59 GMT  
		Size: 19.3 MB (19260378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8592982b699e66ff34184f2c572dadb517d6dbcfb00f7b976ea3a888c229f914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6812847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec70488f82e5a3af243451f859838a7f37f992277d2ee80d08f59ed8c6a9b24`

```dockerfile
```

-	Layers:
	-	`sha256:2045595560af1bc980941a8eac9ed261bf700a5920bd8900dac72adc0595e38f`  
		Last Modified: Tue, 23 Apr 2024 19:08:58 GMT  
		Size: 6.8 MB (6777170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d5b20373943ee7204eec12d5ab37b5ff844d10a7706482ea961728359f2cbd`  
		Last Modified: Tue, 23 Apr 2024 19:08:58 GMT  
		Size: 35.7 KB (35677 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:b915de1a0d243c78200b55de258ee886f7c0be4ccee0ec8d45855623ec7b80c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182821292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071d91c9a013c26a7a3742b672b9665ed0a2d604d54b555d417cd2330d6ea8fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f983756bc446d47a3a97837b5ea0e8046f50564b79a5b7970b6a2e5e3d1b1b3`  
		Last Modified: Wed, 10 Apr 2024 10:04:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a305e7c7a347e54af023228347ce29496e33846afcbe09efbad3f61836ddd133`  
		Last Modified: Wed, 10 Apr 2024 10:04:45 GMT  
		Size: 86.9 MB (86934737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4584f5143a2530480b9185a97ebe23a0277200e873d3df547cc345ff519741d4`  
		Last Modified: Wed, 10 Apr 2024 10:04:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a58e0161768545dc9c85cc708791abd398b7c460273b11747808b9f5991fff`  
		Last Modified: Wed, 10 Apr 2024 10:05:00 GMT  
		Size: 19.2 MB (19176456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92571c73b54051834edb8a4a59e5000b4525361669ec7fd686db7cb4e1b6b4ac`  
		Last Modified: Wed, 10 Apr 2024 10:04:58 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf203b2d2dcb85877524131f292851864dbbfe4bf5c983b5e415f47c9e7cda6`  
		Last Modified: Wed, 10 Apr 2024 10:04:58 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f232b9f856a5cbd876e2e15fa2540002ef95a6baab8f6c2c96709ba5a0799e7`  
		Last Modified: Thu, 11 Apr 2024 20:15:57 GMT  
		Size: 12.8 MB (12807927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851d456f25bd54d1d48588abc11fd85f00346b36014211f536337d3f1b7eedc9`  
		Last Modified: Thu, 11 Apr 2024 20:15:54 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acc213c2e76710d3c23938e4afa0aab3e09424b6a2bab9e5958589e9fd9650e`  
		Last Modified: Thu, 11 Apr 2024 20:15:56 GMT  
		Size: 11.6 MB (11639546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed5d7fa823221f64779aeede5e106b1bb7aa9ce42c381a02b61cb1c23395808`  
		Last Modified: Thu, 11 Apr 2024 20:15:54 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2b58d95ddb4d55d46cfe871e58340325fb0bb473018a5accb7e7354ae1197`  
		Last Modified: Thu, 11 Apr 2024 20:15:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c55bf8c730801b92364e994becdcbe49758f76826983bad81d50cf047bd6d`  
		Last Modified: Thu, 11 Apr 2024 20:15:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d095ca1d40ede0d900d1fbdd86bd42a4617f5af9d75e39c53ddae907e65a71`  
		Last Modified: Fri, 12 Apr 2024 03:52:05 GMT  
		Size: 2.2 MB (2194156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00a8fe2109f6106174ae9058eaa66be1072b56a6b67366795c2acaefebbb82`  
		Last Modified: Fri, 12 Apr 2024 03:52:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66ea432a7ff38aa1962b73d57c2c676a272b6f13c69a233b39b068f6130c22e`  
		Last Modified: Tue, 23 Apr 2024 18:27:01 GMT  
		Size: 723.9 KB (723943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eee331b538e31f150d7668952bfb7f2f7ceef8bb86c239c63dd233a29a9fb0d`  
		Last Modified: Tue, 23 Apr 2024 18:27:01 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28209f0b5c92c14e57d7c9561db8ed85a54b115da60e38848fdaca8ac43fa5b`  
		Last Modified: Tue, 23 Apr 2024 18:27:02 GMT  
		Size: 19.3 MB (19262214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5b24c3da1b5270b8d3feeed0b3582a857a84e501ef94d011995d5ec36689d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b14478df81cd0b8e78e8c7bb10aece0918dc42763cec3ab9f5c7718f5136abf`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e4abbef533d1382e020887307d4cf8c45d6f1ea01d7ee79596026efac7721`  
		Last Modified: Tue, 23 Apr 2024 18:27:01 GMT  
		Size: 7.0 MB (6970512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d4309dfda978dc5509de05fce050a8ab27e5331d7dbe33d559ae97966abceb`  
		Last Modified: Tue, 23 Apr 2024 18:27:00 GMT  
		Size: 35.6 KB (35575 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:8f7c75b86db97680de57dec28d5ab702df7c1ee33af95e0db4211633c79a80ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191466311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e219c95cc845b7500cc941d5edd205e6092957b4763bcf25da01cf660e5a6f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218ed3dadf1c21feb2ff16df18b571ba54145f46f3b6040b0ac6a1aad1b96653`  
		Last Modified: Wed, 10 Apr 2024 16:02:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b436e2a26ab5647f311e180cf02589b2fe37976e32a161d54e0967c7cb70fca`  
		Last Modified: Wed, 10 Apr 2024 16:03:01 GMT  
		Size: 92.7 MB (92721468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ee4d362949c5e7064e0dbfa8f04547e6aeb38cad32fecb6e2ae7ea7d75b70`  
		Last Modified: Wed, 10 Apr 2024 16:02:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e607cd004a82750f89d56d2efd473e4d30ded01833c0837c4c5612ff65d6598`  
		Last Modified: Wed, 10 Apr 2024 16:03:22 GMT  
		Size: 19.7 MB (19744236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189268e404872539b171f731b51d20f97896419264c7e256bec2ae65bcdaba23`  
		Last Modified: Wed, 10 Apr 2024 16:03:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec06a311c51dd4465e0e5b1f570b727f7cc52396a5f33fa8f75cdbcdccd71549`  
		Last Modified: Wed, 10 Apr 2024 16:03:18 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9d60acf9c8c586296a9b6a327b6b03eba403d7b393c1a18c6389835ae2685`  
		Last Modified: Thu, 11 Apr 2024 20:49:07 GMT  
		Size: 12.8 MB (12807971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5954b97e32dc23b7816837f62e20a690b4257d6495d9eac9440f317508ad44f`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f86177ab7b6bcd05e7def86d83fc12c289fbb415817b070b5b60f5db301d9`  
		Last Modified: Thu, 11 Apr 2024 20:49:08 GMT  
		Size: 11.8 MB (11789874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499470d7d2367ed3124a9a38267dc32038ab2abd0840d8b8537113d71d0a2758`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410d06a6fd1754e06d4a00ed8eb1e2d00b2d662bdecb6e001d717535978a3067`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bbbe4b31faf3540338f2775c22dce3664d16538324b9e20cb03b367e1e2bc5`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f025959ac3b0bb78e146fb1c89be8f282476dddd06a33b071965a32e2ffbd4`  
		Last Modified: Tue, 23 Apr 2024 17:54:52 GMT  
		Size: 2.0 MB (1997322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c90e172f47bea3b0c2b13c002f773025585790ebebbacac371b4f95dff263da`  
		Last Modified: Tue, 23 Apr 2024 17:54:52 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab6744b93089f3fe2cbe482edc6ed85398edcb3af88203f0a57a77d818b1dd`  
		Last Modified: Tue, 23 Apr 2024 17:54:52 GMT  
		Size: 723.9 KB (723942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff3af13691c2390aa0c52f41bce22ac31d87812cc46d90f6f610fe5ebf8036d`  
		Last Modified: Tue, 23 Apr 2024 17:54:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dd9bad52b8e4289fa842d2a130c42c14d8c39183e46a01942b42c22d074d01`  
		Last Modified: Tue, 23 Apr 2024 17:54:53 GMT  
		Size: 19.3 MB (19262076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7f1ebd7b8635c166d3f0f5ccbcfb91e34118953ec7d9105c767e68efe5ea0095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd162380d9abfbb96a5d22e807377caf0379e46e21c847cef0a9b965a1300d4`

```dockerfile
```

-	Layers:
	-	`sha256:3f9ea817872e54f93dc99a937e395227569cdd914ba9c10ea5f69c2d9bfd1dc1`  
		Last Modified: Tue, 23 Apr 2024 17:54:52 GMT  
		Size: 7.0 MB (6958610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc40e3e45ab5c11ae02842a3af78869abfdfc19e7849fde8ea449dc41358743c`  
		Last Modified: Tue, 23 Apr 2024 17:54:52 GMT  
		Size: 39.9 KB (39907 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:528cddb7f0354ba71260392685017267bc4f4f671464990af4ce83ba6126c67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189038500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498fa6680bd0b6b6674edcee4e168bc84d8402609cf26027ec2a19392490fb86`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7d55142cd3123552c44a0e1701f8cd168bc522175bc75c850189de125d70fb`  
		Last Modified: Wed, 10 Apr 2024 11:51:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddbd240e160e1289c6d6b5e93d65b6e60feada9d89fc02edf160b1a799b861b`  
		Last Modified: Wed, 10 Apr 2024 11:51:58 GMT  
		Size: 86.7 MB (86651989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debc3c4f90d609bdab9cc23403c78861d833f4e099e49befddd660674bf5e49e`  
		Last Modified: Wed, 10 Apr 2024 11:51:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e5b71e65c481447d08e87f77fbc81c15db0c24b77f03f27574cd7e850fd8a4`  
		Last Modified: Wed, 10 Apr 2024 11:52:19 GMT  
		Size: 20.5 MB (20473729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b313fb545912f5c440f81255801d291fc171b5d3fe66904af0badd13fdc3ce2b`  
		Last Modified: Wed, 10 Apr 2024 11:52:15 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d937caa7e434a76e8f5fc981bd308ce8b77f0c79791dd00ffe2171f530dbb3`  
		Last Modified: Wed, 10 Apr 2024 11:52:14 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477d9edd66b84988cf31d8aa13cc67d7cfc25b2cb4abb22e8cc70efbf5c7cd2c`  
		Last Modified: Thu, 11 Apr 2024 19:09:10 GMT  
		Size: 12.8 MB (12808612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e2f82b8a8df7050ff173cf6a9141eb1c8c7988d003a7729147bae13417a0cc`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b161e3c72cbbe18e2b642cf8404926dd62a88ed739a0d8b0ef1fbf799854871`  
		Last Modified: Thu, 11 Apr 2024 19:09:10 GMT  
		Size: 12.0 MB (12014027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8106c30e7916d20d3f9a24038746e10af94024e9d24fa4b90e749696e723eb2e`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caf7b1b74ed6eed444581197113856846dcea63460661604d6bdf2766d0cb22`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f82b01e3fd0c8720826073b556518520eeb23041437471513a771631e88dbe`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdb0b263e8d770d0cbec69f8007d955bb4ca5e43da6acbfb42c7582523aef18`  
		Last Modified: Fri, 12 Apr 2024 00:11:24 GMT  
		Size: 1.8 MB (1794674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9233e453db97d404218fc679d8191088f7e1daa1fd2f00145b7e8d6ce94ea`  
		Last Modified: Fri, 12 Apr 2024 00:11:24 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223158c97932e652d3e8cf2837dff21e5d5cecf723451bdaec64a1ab087f15b7`  
		Last Modified: Tue, 23 Apr 2024 18:31:41 GMT  
		Size: 723.9 KB (723943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936aa6a96528d540e780d6e27ac8109ed47025e8643e2fbb9e84c51a95767812`  
		Last Modified: Tue, 23 Apr 2024 18:31:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641d3873924b30285733402ae655d353a019833c36bc66a0fc39210ad489c5f`  
		Last Modified: Tue, 23 Apr 2024 18:31:42 GMT  
		Size: 19.3 MB (19261418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:6ee28797279924d033b3ebb04376e8c82a34fad6f6918bc0f9d1805bd6933898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b2f5988fe9cb2f3ad1a120f53eccb10ec488d5df0fac0eb2f5da69f08d7ab5`

```dockerfile
```

-	Layers:
	-	`sha256:a71c8a3811ec6d2192cf51e1f1716f064df7fe29fdeb740a9b9338e1ef67d004`  
		Last Modified: Tue, 23 Apr 2024 18:31:40 GMT  
		Size: 6.9 MB (6933447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f97dd883b3d10f275845fbf63c840f5bfe1e2ce87c40dcc7fd3c83f2c99706`  
		Last Modified: Tue, 23 Apr 2024 18:31:39 GMT  
		Size: 35.6 KB (35610 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:72aef1c63c0e61887a0d2ace21d80d45690ec0811b13f81a53ce3f25114ce379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165371003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa4f6702a46894769af16d22091d6daa167221757847a8eb5472a02094263eb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:173b309178d19f7fccea713c7c575233510e5f065fd2d92a5378f001a1d33846 in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.3.6
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:499f72f2d94381b6df4b58d8ad4918f9e03fc5d140cb0704842fd78e2e63e391`  
		Last Modified: Wed, 10 Apr 2024 01:49:00 GMT  
		Size: 29.7 MB (29666840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca506d7131291f914a2fe8e52815ff8bdd8c25bf45070ac9921895e8823c050`  
		Last Modified: Wed, 10 Apr 2024 16:55:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ab6e162507d3c1d7c1ae9da56b1b7f8c491011e2e9cb752fb2c0583c81953d`  
		Last Modified: Wed, 10 Apr 2024 16:55:38 GMT  
		Size: 71.6 MB (71639415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51c30516b20da53f1011e02fe706b3cb1f822dbdc3b77fccb2bf91362af999c`  
		Last Modified: Wed, 10 Apr 2024 16:55:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da72ea9be2505eb147b43891a05666be5445dc052b0ad75d4cb1ae1b68e184`  
		Last Modified: Wed, 10 Apr 2024 16:55:55 GMT  
		Size: 19.1 MB (19080398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128ade7838782e1dab46ed62687de5ca3718647310af5ea1b26a7195dd14a560`  
		Last Modified: Wed, 10 Apr 2024 16:55:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c03025e8aa39e77b5b4b9784ed1ec0f3a19cef75e1cbf7f4ade3132918197`  
		Last Modified: Wed, 10 Apr 2024 16:55:53 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a4590f1af3913d334e7a94b0aaa7ed8e3bcdf6c821ae351fdd9e65a867705d`  
		Last Modified: Thu, 11 Apr 2024 23:30:59 GMT  
		Size: 12.8 MB (12807791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1725a46b65dcf1a84ba7521641deea34da90ddff1783d82777b05f1da2926d4`  
		Last Modified: Thu, 11 Apr 2024 23:30:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cdd634ed3b85fbd32c09490e0af26c585d8349585d75dd2e6e32df06095583`  
		Last Modified: Thu, 11 Apr 2024 23:30:59 GMT  
		Size: 10.7 MB (10664320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de50de409b7aa7e0df24c97a0e1433cc9f02e04b067e172016b341d41583388e`  
		Last Modified: Thu, 11 Apr 2024 23:30:56 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d5f148b2aa3fd06d429c6cb7b250a7d3d13872136f79d16ee5af37789dec8`  
		Last Modified: Thu, 11 Apr 2024 23:30:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da8d791b5e4e84109e2fe2a21f8cc1f8ba80199c1cb556eb943e8ef4435c43`  
		Last Modified: Thu, 11 Apr 2024 23:30:56 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2631c3b7e29e7df23b642047d6f0a758b1d6d1162242522a16b753b7033858`  
		Last Modified: Sat, 13 Apr 2024 19:27:38 GMT  
		Size: 1.5 MB (1523542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2376e2a1ff38b6519fe672c580600cd16a7d5197db21ed19c27ec10bd07716`  
		Last Modified: Sat, 13 Apr 2024 19:27:39 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19854f08af0f79e156319f9513b8442b9259808978d43ce415ca2c5856b210`  
		Last Modified: Sat, 13 Apr 2024 19:27:38 GMT  
		Size: 722.2 KB (722248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0a90a6ab284f1555c6fabdac6dfeef81eb9d82895868aa503aba9129dc2516`  
		Last Modified: Sat, 13 Apr 2024 19:27:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a92a30773f56dbe8b6835974b3f41ac08b7cf5c83941450dc0b0f6794a96ff`  
		Last Modified: Sat, 13 Apr 2024 19:27:40 GMT  
		Size: 19.3 MB (19260436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ddde137882319de59d3f185768ea8ec863de2882b348b91d82e98c1de42c9d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6826327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1441de59e4466c723c57001deb6d611225c9c87655c121007c96958d933dbffa`

```dockerfile
```

-	Layers:
	-	`sha256:2367673319356f37130355fb7f5f697c5ffdc14346c25050d8532f0b0b07d380`  
		Last Modified: Sat, 13 Apr 2024 19:27:37 GMT  
		Size: 6.8 MB (6788659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1144cd6c036791c62a31a9ad22dfe7a8d60f2332b15a281d72b2e18fcd48b71`  
		Last Modified: Sat, 13 Apr 2024 19:27:37 GMT  
		Size: 37.7 KB (37668 bytes)  
		MIME: application/vnd.in-toto+json
