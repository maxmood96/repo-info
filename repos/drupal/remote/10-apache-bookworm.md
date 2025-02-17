## `drupal:10-apache-bookworm`

```console
$ docker pull drupal@sha256:773f7704b77a2de4871fdbdaea7ccf173815bc4c02bc53a5f3f4d9bb9c46e68f
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
$ docker pull drupal@sha256:b5b3cdac1b44ef2eb422e99965cdb4a5dee811da6b45bbccfb0f356d4762433d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201229761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a00396e5650c3689061fffc10c474fe28e4c97573b9ff887464afb979bd4ec9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a75c3e6a3090db961f187e726d4f8d9470d109873ea82676d20418337fa99`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fb56484a65ab530ed3a13c37c0d4490e5b20d60544117d1355bc924ca741f0`  
		Last Modified: Fri, 14 Feb 2025 05:08:29 GMT  
		Size: 104.3 MB (104345484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a8c28e2a6462b881346f671a6a138b8939b522b6a59f1df9dc3b47a373d513`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4b52ba138f07eb5a43b4e999ad5d9732f80424c1146edfe4506f9d400dc234`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2801a0b661a741cda5801c08a9760b5e2b6b8ff90aeea85213a9aa76beb55f7`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abaaa7aab0e297aa578b9ffc188ad34b99d5f908a418db4a09c0fcaab0e102f`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624140c5bee349372ea34fcb86cab39f68ec4c3c923bc58c70374b7ef5dc9b8`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 12.7 MB (12669743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5250a5fbf9003989ed0004e7b3806c9c589b17fb8b9ff5272292e0eea114218d`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0765d0c88fa1531a15a2fe8c98660619acdc1d236f7c94ceeeb2c25c31ab5d1`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 11.7 MB (11653066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872b33dacafd826ad0d6eb2e2b26976f2bdb354884cdaa6c2e93a7371101c67`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bca8216293d7220363a34e35012c4b87555e8f4fed4d41ca0399c210db629`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54cdbe7b63b97c4f159133a93e51d5eb96a937eef274224cf47f3ab474c4590`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4677023df9cce055939e16248027ab37a4b2fd7263ec12e8b052f0658e8cd72`  
		Last Modified: Fri, 14 Feb 2025 23:55:23 GMT  
		Size: 2.0 MB (1999482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67514b3894f20ad8a1a2abec782fb0e137c8bd1906c430fdee8cc80e1a8bfc04`  
		Last Modified: Fri, 14 Feb 2025 23:55:21 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fdea730bef5fbe7a2348b5fef739c4cb5ddd3b06ce7ded963f1d5c450de19`  
		Last Modified: Fri, 14 Feb 2025 23:55:20 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4ff62214cedb0a990a7aecd0a76618e8440dec226f5e51c835d693388bfca7`  
		Last Modified: Fri, 14 Feb 2025 23:55:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e7c4da35d1561f85a4fcbe205d9cf751c614845d5c956cc1d97967693c7758`  
		Last Modified: Fri, 14 Feb 2025 23:55:28 GMT  
		Size: 21.5 MB (21479672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:5e97181a9d17423681a1d07d0b35ea70c1c824446cf22a28c3ae9120d6b74b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6882073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c7ef5fbf1cd8a75e8caf9696c6141c46f2082af782d74850a9ac7a22bd9b86`

```dockerfile
```

-	Layers:
	-	`sha256:40457664b5faaac2775366339a3361d0cc0477e01d7f28223a7b5d80274658e6`  
		Last Modified: Fri, 14 Feb 2025 23:53:23 GMT  
		Size: 6.8 MB (6841031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e16c28ba8a6224e6658eec2ae888c7f3bdbf2cd6ddf902469987291611b1aa2`  
		Last Modified: Fri, 14 Feb 2025 23:53:23 GMT  
		Size: 41.0 KB (41042 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:864b6acae84030d297be9607a8b42d1bf199ebb18a511f8b3c1c7b55ee443109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165227193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a8b19ac7a6779436b9dbd7d61ca8b56b0eb617437efbaa76d0240c90a85230`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
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
	-	`sha256:5a0061a65af18d1f444ddce2a9c5adcda383e392b43f907d4f1cfccbdd86eb7b`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 12.7 MB (12667938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ddeea63a4ce930814517c148050885a1dcc675b49b9a0cb215c1a5071d783`  
		Last Modified: Fri, 14 Feb 2025 08:30:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cf17c9822fbc25061c1bedf52d2fe828e813acc20b155300c96059e2c8cdcb`  
		Last Modified: Fri, 14 Feb 2025 08:30:09 GMT  
		Size: 10.0 MB (10044324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103242c028fb3f94e70f6aad3a8acb02c3609e9f161c59a0d3fac14a123b22`  
		Last Modified: Fri, 14 Feb 2025 08:30:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d287db14ec7ae0af84306be48a164ec40227a26eb34dc1c91b7bb34998758007`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a2185f46b047a9c314d2de357f5c8fc7686a6e3f1debb4f977571569477d91`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8289b19739d4c72bcbb1beab2f4c3fa7b1e1a4706716bee0d57b28e7b3cd40d9`  
		Last Modified: Fri, 14 Feb 2025 14:48:25 GMT  
		Size: 1.4 MB (1354721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f463b094768bc92118d58b3521d6e03029b116e6718a69d85701afdf96338db1`  
		Last Modified: Fri, 14 Feb 2025 14:48:24 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a43f9e622adb1d9a9641c52a5324655ce0fa6b7cf2fcbfd8cfa847a62aa6f9`  
		Last Modified: Fri, 14 Feb 2025 08:33:54 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f81f157b397b7034a74f2327f5dcfb7a9e3c3c885390716ed287388fd143134`  
		Last Modified: Fri, 14 Feb 2025 14:48:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6379895207095664d5c418f0d2e7cb951aa48600b9604b872b5907ec64bf441`  
		Last Modified: Fri, 14 Feb 2025 15:53:52 GMT  
		Size: 21.5 MB (21479534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:75a151af4dbf2ab5a492ce13d577593b03792df58effbb0f7dd273ef2f7aacc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6707485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff1ae4f7e1efaaab1c3c915b7886ee5a7370dc53224e3f5d60d7d287eb8b3c8`

```dockerfile
```

-	Layers:
	-	`sha256:4d97581e4e2478f12ff6c3a7a6f85d9edec36addd938d88d733ef35e09dd73cf`  
		Last Modified: Sat, 15 Feb 2025 20:53:19 GMT  
		Size: 6.7 MB (6666213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67f7d829f41a37444d54dee9e9c8129d70969c35a96dd0b145b123f2d288682`  
		Last Modified: Sat, 15 Feb 2025 20:53:19 GMT  
		Size: 41.3 KB (41272 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:9883faff7db5bbcbba83c192e78799b9edc98edb91e5bd97178d73f34f56e581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195096788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a33218cf19745c8b477b118dd6a9d90187a16654ba4207fc57b8d90dd6b8108`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
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
	-	`sha256:21196ec8e1c1dfd80024f57b05b04a0eaf34e114f8127bd370edc9a9aa9dd22b`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 12.7 MB (12669564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1bcbcbb81b84139eeae4d92fd2035ea91bbb53ae2efe44ff97031cfb95d5db`  
		Last Modified: Fri, 14 Feb 2025 05:13:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a63caf847a0fabb747e47c1443cba52008580717256dbf524c7ffa4a55806`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 11.6 MB (11649823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e8a356a7a2cea4755c5b51fa8347428771002844d198bfdbee26c69bb645f`  
		Last Modified: Fri, 14 Feb 2025 05:13:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26402d45dda19b9f8fd7e95944a4978aaa74d560a4427455777573caf52c6979`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca75595b7a8267cee7228887aafbe6541d7d12a2ba80e86936f3d58baa134c`  
		Last Modified: Fri, 14 Feb 2025 05:13:14 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8806e6ca371e92d60d5939ac85a7bebb9c21c10e884baadd5cf01341b5165`  
		Last Modified: Fri, 14 Feb 2025 09:05:39 GMT  
		Size: 2.3 MB (2259168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e918ca99fe220e47b74a5fcf055f635a1aa26ffe33db4e635014702fc216d0`  
		Last Modified: Fri, 14 Feb 2025 09:05:33 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dff43454dcd0953df7c4e87f4e95ac73626783883a60ed1bbf5ba6ee92b34cb`  
		Last Modified: Fri, 14 Feb 2025 09:05:35 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8bff3353f25d8ed7fac50190711ee29fc5986f3141f7e5a9c165c8c83fe2b`  
		Last Modified: Fri, 14 Feb 2025 09:05:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb844d95432c57c5809928c061675d113fe45d1413c0bde7f5f3324b11178489`  
		Last Modified: Fri, 14 Feb 2025 09:05:46 GMT  
		Size: 21.5 MB (21479826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f4aed57d9ffbe7527c24edfe55c0919ca2f0ed2f90ac8cdb5dadcfe67dec67c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6921075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bd91f17d03071bf085b1a9b2ebedd60ed39caa1bd56f2c636613d5e59af72d`

```dockerfile
```

-	Layers:
	-	`sha256:447229678ffb015be350b3695e1636012e2784b77bd327b48fb078ef91907632`  
		Last Modified: Sat, 15 Feb 2025 11:53:24 GMT  
		Size: 6.9 MB (6879711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfeb61a7643e6f7cc213b1ad88a41654c98bcd228e520b4ec81b35c6b880e90`  
		Last Modified: Sat, 15 Feb 2025 11:53:24 GMT  
		Size: 41.4 KB (41364 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:0786ff953c1afe8dcda6ea48a8fbc4e36bad61016439ad2b2d11450be6697a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200162249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7fc9e3b38e6da6c278a526400751b068d7c95c3cda7fcfe035a83a4dc769de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b613625d23792fb714ed0ea23144c0605d29b6fed360bb76e054fde26d8c3866`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35610fb0fd5a6dcd1f7abbd6b925a39db37b185b165d2056a200f62c9d1d04`  
		Last Modified: Fri, 14 Feb 2025 05:08:42 GMT  
		Size: 101.5 MB (101513729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc9694c3bcfa66783af0c675abac303483f3e7ec83ee53e26f67929675bbcc`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f370c1b3f7740375abdfeea774005f34789be5d0e9a375b1518bfd8afbbdc990`  
		Last Modified: Fri, 14 Feb 2025 05:08:36 GMT  
		Size: 20.6 MB (20638450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4d0c6093b741980cfa89de6ed93898cf1a6303df104fcde6a387c0bc8c3d6`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be28fade995e8ec99823d90011a18c578f524f1027dcd5c73c855d449928c15`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506ecd4a857258c7c70be8d97489c05eef37a09f6a3b4d0803a419d83f1993ee`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 12.7 MB (12668927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf4c835ba433a1d172b9ba07f43f966f0eb05ee10284f09cfd882368bd2c8ca`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185d7363802500e0336fe058a83b8c6a8c64c0334680507fc5fdfca9d140a74`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 11.9 MB (11875658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68ed86d82217e240f5f70b173ae60912abaadd9bac6084fde125962c4b19781`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a33b761c64605c9d26198d448ac81df7b83abc67800d7fd4b8e6f259548f4e`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170694b4d37420e4e388ce3b55e04465a055748c58ae0a4730a838a63f435a5f`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c7c0f63fc97c02410db2b80157d6231ba81d251117e468b2a0893e94c6cec`  
		Last Modified: Fri, 14 Feb 2025 21:13:57 GMT  
		Size: 2.1 MB (2052334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49af225039119be6000b921b437c03fb6498d5dde38893e7e6159479e977e7a`  
		Last Modified: Fri, 14 Feb 2025 21:13:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b52aed8c93594f14f91844a3fa0bc36fafec0d412bd085d893171b1129f58b`  
		Last Modified: Fri, 14 Feb 2025 21:13:57 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261a79c50e76b1554699414460de2a3c0577d8a27f34ea1d478c48dfb1b1e478`  
		Last Modified: Fri, 14 Feb 2025 21:13:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b75c5da9a928d4026ec834290f0299ff0cce0321b8271b5a6c5f0973c1ecea7`  
		Last Modified: Fri, 14 Feb 2025 21:13:58 GMT  
		Size: 21.5 MB (21479440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:86787146f74da1255e6a382a5e00426bcf83281c6a05bd5f2104795b6a45f27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6862161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525ab6f500cf3ab4ed5f9baab034411394644eed24e248dff111feb0efb34597`

```dockerfile
```

-	Layers:
	-	`sha256:5c1224c72a26964568b32de85c8e86db11fd39aeb37eb6822f8cb2fad03d40be`  
		Last Modified: Fri, 14 Feb 2025 23:53:32 GMT  
		Size: 6.8 MB (6821232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377730cce7483d8324c893b4136eee352c54b443027ab8d44004a9ce49134d7d`  
		Last Modified: Fri, 14 Feb 2025 23:53:33 GMT  
		Size: 40.9 KB (40929 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:13ea06de52baeb9be921c7a5edd0ef3460882ab23027345992ac0792305f1e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205497485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2306715e7622752046550a88a98f4ba7d169f35c224342324c4207a104fbdaa7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
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
	-	`sha256:3d5d967f821ca1fb79746ae807f48942031ff2d439b9b9f9df26ed06c154b2f0`  
		Last Modified: Fri, 14 Feb 2025 05:44:43 GMT  
		Size: 12.7 MB (12669396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49214599fe5e44263b4f29eec79a048aec632a3a0c9ec9306cef90705e2c318e`  
		Last Modified: Fri, 14 Feb 2025 04:35:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70af670052714511036edba6a195ad4ac53e19472f619cf8af458c6a6055154e`  
		Last Modified: Fri, 14 Feb 2025 05:44:44 GMT  
		Size: 12.1 MB (12069363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcd0d7e9b95be4af021d09c6b8fe1941e9a9343a7257ecc5c313f88e67cacde`  
		Last Modified: Fri, 14 Feb 2025 04:35:38 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b08c890f85c486e806f894555738bb2681c8b2e582158fa9b947ff69ef6baeb`  
		Last Modified: Fri, 14 Feb 2025 05:44:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85e02e440d877c5e9601bfa96781c8574bff6ee1c23a7cbd6e4f18005b6768`  
		Last Modified: Fri, 14 Feb 2025 04:35:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2ebaf059f020267fc6e0b7389d42474a21d5b9b09c34aafc7d8132affc70d`  
		Last Modified: Mon, 17 Feb 2025 04:51:30 GMT  
		Size: 1.9 MB (1856037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647adcdba5f6b1b583397312996cb43eb32e31cdc8f89cbf2ac05064f5576d42`  
		Last Modified: Mon, 17 Feb 2025 04:51:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c116ac9bb3dd93df18b7c1e15579aaeb8748d292e9bc26a562872702b2c215`  
		Last Modified: Mon, 17 Feb 2025 04:51:31 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344be8cdec3b0ae9ef379053259e508ca944500ea5253fb7378cbe19d8f761e`  
		Last Modified: Mon, 17 Feb 2025 04:51:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087e104661526bee907bb0c296ac482e272cf976376b28d78f5f4c3c217d2c71`  
		Last Modified: Fri, 14 Feb 2025 05:32:33 GMT  
		Size: 21.5 MB (21479244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2a82473b2b4cb7b03fab0c1d8bf26a6c10d9ab356f2bd8ce14153d218b1f997a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef89030c32a6a49dd054a0c1f54abef578465e2950cac8891d6bf18a6f3eb4ee`

```dockerfile
```

-	Layers:
	-	`sha256:814b8bb22324d18410129c6514f25b9087b306dc518c67d46a5d4dc87a8cc863`  
		Last Modified: Sat, 15 Feb 2025 05:53:27 GMT  
		Size: 6.8 MB (6828229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c3b8d0546c64699657368c38d507d244538bcf68fa5c813a916cd84cbb1e9f`  
		Last Modified: Sat, 15 Feb 2025 05:53:28 GMT  
		Size: 41.2 KB (41184 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:188ad47dc76d133f97b560818735f0e16c8613c0976bdaec73395790370af55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174893392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291e30813b3eb32ba0bfbada559063f047778f24eb952fe36f82007d741d5e61`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 04:56:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
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
	-	`sha256:3f122e6df6f4a530391eafe96fd22f7a827680552569d20e74ceb44bb2feaaaf`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 12.7 MB (12668348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd33a4b2e38cc678b5373957e39c88c2ba6c28a5708a0b6e3ecd411f4cda46f`  
		Last Modified: Fri, 14 Feb 2025 09:10:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955870271e205902dd486313c7108103c880114c5080faba66a02d18c6c05fb6`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 10.9 MB (10874900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228daba1b2e4e648f074319bfe954f10e9e4ed702532264242c0265083326238`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450024d85b97e8263ff6f299351829d0b323d899830479d49ccd9e4038ec8888`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802c5dddb1c07139cf78fb9933e64dd90748f2c3e7c3e8071d393dc1136eb025`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef22e2f10329d6b0ff0c0ac077a4518b1db016860c325ea7fe405dc037cefe3`  
		Last Modified: Mon, 17 Feb 2025 04:51:43 GMT  
		Size: 1.6 MB (1553430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f29f2be2191fdde419e00b90efa7e9cb1dcf6f9f1e5e6376cca4c597ec1bc3`  
		Last Modified: Mon, 17 Feb 2025 04:51:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ded313d1a964579f50ece532d71ca7c3441f04c188ed7e6b7f8c5bf2cab3a`  
		Last Modified: Fri, 14 Feb 2025 12:25:06 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5941dda3a8a31fc1a0afa46202ec9fa0bf36af5e2f51ec34f3461e1b59192f`  
		Last Modified: Mon, 17 Feb 2025 04:51:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb183b16b3b98b38eed432aa1527b13299522e1a2b314d06b78f8383a07a7f`  
		Last Modified: Fri, 14 Feb 2025 10:36:02 GMT  
		Size: 21.5 MB (21479419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f26431ffd5b6419fa8fa8ea14306d10d49bb97635e4810fa6906701e6babbc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c999b3da94b8fa5157e3b4a0691d69460072b7100bf2a462e5c8e0378123a2`

```dockerfile
```

-	Layers:
	-	`sha256:49b865438a65b4e2a994bae856062f96cfeac31a08765675dd43a6f2cefa6af8`  
		Last Modified: Sat, 15 Feb 2025 14:53:30 GMT  
		Size: 6.7 MB (6692555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c13206aafad9ded1faa911761a7415633a7fa7f0d3eaf9fb306a39a3846b4f8`  
		Last Modified: Sat, 15 Feb 2025 14:53:31 GMT  
		Size: 41.0 KB (41035 bytes)  
		MIME: application/vnd.in-toto+json
