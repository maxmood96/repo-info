## `drupal:10-apache-bookworm`

```console
$ docker pull drupal@sha256:1fc27e7982d1d6430c15f514c8ed8f5f49b2355fc9790da6395e8cadb1fd7f9a
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
$ docker pull drupal@sha256:4f63a225c8e826a3ccac56c92c721bd7cd72a3702835cef531ed3bdcfaeacebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201233769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c25356c6c61d9b36b3e7aa9bce0b8981d9c06c3ea200d4be4189343788642d6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73912981f01d465fad5d795434f1fe2351568e1a1c7589504ca584da52aa6e9`  
		Last Modified: Tue, 04 Feb 2025 04:37:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125af08412c173ba3c4065d50e69ee57f1c22b1ea95915923d04ff541eb6d71`  
		Last Modified: Tue, 04 Feb 2025 04:37:48 GMT  
		Size: 104.3 MB (104345428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffddd7eb5e6b8e6d05cd3306a4970ac764afa082bdd81eefa03cf968abdab17a`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b3e392321920ca03abf1f287089f0705b075ca1e4787ec38013263b144d9ba`  
		Last Modified: Tue, 04 Feb 2025 04:37:46 GMT  
		Size: 20.1 MB (20123825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54b93702d85932125a6384d578952b42e671e06aceeb84f5adebe3bea3ea1bb`  
		Last Modified: Tue, 04 Feb 2025 04:37:46 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e742feb4c8c73c323b7323ba8b2daf6d967d9353759ef964775a92b9d61a3`  
		Last Modified: Tue, 04 Feb 2025 04:37:46 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40acf0a8fd4f344198279a4a4317d3b5dc1a293c8d321ccd1b5eb0880f99f03`  
		Last Modified: Tue, 04 Feb 2025 04:37:47 GMT  
		Size: 12.7 MB (12673263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a625eb80489d190915a081a0270f12fe4c1ac28388ffe508617199b591d2824c`  
		Last Modified: Tue, 04 Feb 2025 04:37:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2870b4f65cfc40e64d97b38096c14e70dba263fb8d22f4b9cf7a1eec536e4a`  
		Last Modified: Tue, 04 Feb 2025 04:37:47 GMT  
		Size: 11.7 MB (11655336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7681d77b64a1816ff0149e937407e6e66e3917be24d80d3aeb5db79b407662c0`  
		Last Modified: Tue, 04 Feb 2025 04:37:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b771f4085e2b5b47a02991e7b2a495c2ec937f9b069da325c8ac246012897ca3`  
		Last Modified: Tue, 04 Feb 2025 04:37:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f31d377d0366828767d6080eb61608488b00a223cdc8574c9f6140aec60df2`  
		Last Modified: Tue, 04 Feb 2025 04:37:48 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a47c8141a88c733dae1cff36358c1b1b5f79d310028a3a96089426bfc3dfa8`  
		Last Modified: Tue, 04 Feb 2025 05:23:12 GMT  
		Size: 2.0 MB (1999845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dee765661b5de557ca7b318695eb8aa1a4a70ad1464d4b2fe9990583f22354`  
		Last Modified: Tue, 04 Feb 2025 05:23:12 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadde05cdc24af2f6115a7fb0bbe3a5edc9e36aa528d9f5606266f8ec99f35da`  
		Last Modified: Tue, 04 Feb 2025 05:23:12 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d504232f87ac1e297d6482724806e585158cfd7587fceccd15a9a16639539412`  
		Last Modified: Tue, 04 Feb 2025 05:23:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02f363786005e1935c6c3e0783124abaa0fbd6a9afc6fae0702b1940de9950`  
		Last Modified: Tue, 04 Feb 2025 05:23:13 GMT  
		Size: 21.5 MB (21477519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ba1e833715267c8b6a3ec4c850b85772710a90d5758fcdb99e35b583a37e2189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6882074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec02b18d62903fe254adc1c028bce80efd82ff38014f93d294e78671a727fbed`

```dockerfile
```

-	Layers:
	-	`sha256:9d7bfacf217ead40fe5dfb93eb1aa0fff2a47cc7a08c53f57640125e91670bcc`  
		Last Modified: Tue, 04 Feb 2025 05:23:12 GMT  
		Size: 6.8 MB (6841031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c1651035b1b970b03309b74b15c7e961256402795f004c27f41e07d328f847`  
		Last Modified: Tue, 04 Feb 2025 05:23:11 GMT  
		Size: 41.0 KB (41043 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6560aaea6cf63b4ce1f5a993a2b347a57af0a56c8add6626f2b3b092d68ae9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165228612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4406247c3c0418e0aadb409a784758ba943328a3d938b39ed1111d820a620860`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d546b00afb4b9d040080c0bcc406bf33316623067156773fc2c6b01571dc5c3`  
		Last Modified: Tue, 14 Jan 2025 02:49:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbadf9d833fbe1e5f7e579b22da5a224c4248d4c38649c1535310aa87b326e8`  
		Last Modified: Tue, 14 Jan 2025 02:49:20 GMT  
		Size: 76.2 MB (76162940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827c0e6243599ec0c52a40858b85fe86d2ce54a4d77185b826e94ce33c26525`  
		Last Modified: Tue, 14 Jan 2025 02:49:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d718ae00362fa1531399a71a0605a8c1022220e646f4e54cecb15f8249ef8649`  
		Last Modified: Tue, 14 Jan 2025 02:53:30 GMT  
		Size: 18.9 MB (18857361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411786d2746e941cb797557cd9c2285f527461bc4a2045d6bfbb0a73450ca28b`  
		Last Modified: Tue, 14 Jan 2025 02:53:28 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12ab02075e9800e9ff53812946d5404f8ddf60c94c5674950ae3f5bce341b47`  
		Last Modified: Tue, 14 Jan 2025 02:53:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fa9ceb81ad9fe5cbef84e3d3732b5394b3550a5749df41adfc71bce4bdde5d`  
		Last Modified: Fri, 17 Jan 2025 01:40:07 GMT  
		Size: 12.7 MB (12671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0757c6697df2995b22d1f1629a4ce62a0ef5c6170e1cfb205606f409e1ce251`  
		Last Modified: Fri, 17 Jan 2025 01:40:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d869e9126c873ee8b4a0849fe27999c20692836ac415ce62447ee781f3f610bb`  
		Last Modified: Fri, 17 Jan 2025 01:40:07 GMT  
		Size: 10.0 MB (10043574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef7b6ab5a45b190455e3934cbea82d1f7245579217ed14312a874c9632ce827`  
		Last Modified: Fri, 17 Jan 2025 01:40:06 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8113dd86166b113f16cb459e2ddfecae4bbeb52fc2b6f18a2a46cb87dd5709c3`  
		Last Modified: Fri, 17 Jan 2025 01:40:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8609d96cdea47a39da6091fe48cbde54dc4a777c0fafe608356e575f19b41c`  
		Last Modified: Fri, 17 Jan 2025 01:40:07 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae2ab51b4236bee84f186015f8cb75db0ea5af9f59fad63217ba88ad60f5967`  
		Last Modified: Fri, 17 Jan 2025 02:34:24 GMT  
		Size: 1.4 MB (1355157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9376c63234e0159b68b26eddb15e6fcf1c4b934801486993fd7f8eec69aef42`  
		Last Modified: Fri, 17 Jan 2025 02:34:23 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b096e1f632ca2a32bba2d40f37c5d70ce19ec3d5970efea9c4def31ff960a76`  
		Last Modified: Wed, 22 Jan 2025 00:28:39 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfbd22fe0b37d0f59829ade82c5ebe773c243dff30de3817475eb9ed61f5001`  
		Last Modified: Wed, 22 Jan 2025 00:28:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0156993515a26a327b80d4d09147dbe72559e9477f2fe25dce350886d9f84547`  
		Last Modified: Wed, 22 Jan 2025 00:37:06 GMT  
		Size: 21.5 MB (21477580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:38184d79db9505ba55c2d65e6f3fd12f2ece5cb4f1ebcec1486ed2a994628856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6707486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1adce933acca85a7ece49b68712a29b8ab7b123496348802787b01b18b910b`

```dockerfile
```

-	Layers:
	-	`sha256:f37b9895665c2f8bf745d84da188f255564ce976a94f29784421282592c9ecbb`  
		Last Modified: Wed, 22 Jan 2025 00:37:04 GMT  
		Size: 6.7 MB (6666213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635f22b2f3001f5f45abeaaae1bc90d5718ec8cf49db4750e160310c15026006`  
		Last Modified: Wed, 22 Jan 2025 00:37:03 GMT  
		Size: 41.3 KB (41273 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c7676474b5d059e4829b04bd3144bc761ab4f0627213a6f67f075022bf980c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195096163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d1f823095b0c5a5ff61a92c3a3dbad3959f8767b290db649f06db6fe4c3923`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48015c6e07faccdd2a54d1e2ccecbd028511c6c5d8cf9a4f84b8d4d42d775ba8`  
		Last Modified: Tue, 14 Jan 2025 03:14:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f6eaa105a9e29cbbbc0157f5082daabecac6d65df1a6be8e50afa6dd8b23a3`  
		Last Modified: Tue, 14 Jan 2025 03:14:38 GMT  
		Size: 98.1 MB (98130619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f24c5a85b79cc5db518b237cd81340b2b5649ed577353635cba0aa5362458`  
		Last Modified: Tue, 14 Jan 2025 03:14:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b226d860afc85e06f588b3f648963225616fb252f0f4d759999b9378e564e8`  
		Last Modified: Tue, 14 Jan 2025 03:18:21 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc75481d6ff5615af00c9aa8f15d5ee5354ad284d2a792301107bdea3b78816`  
		Last Modified: Tue, 14 Jan 2025 03:18:19 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596177a782ea080f91870a2b548372f3d7dc9e0c7cb3069ea29c796c4f94d314`  
		Last Modified: Tue, 14 Jan 2025 03:18:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501a5f7f16a2d6582ce6dbddccf9c0029d8ae972b402a5c7f53e5713636c5e`  
		Last Modified: Fri, 17 Jan 2025 01:31:40 GMT  
		Size: 12.7 MB (12673014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783f81a0d40d3714eb0efc5caa1be37f1dc34e985cc45b50d056d4e5c80c9959`  
		Last Modified: Fri, 17 Jan 2025 01:31:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad6427349967c1f0286381864da6f4960a0dde4bb37aebc6119ba51a6c5efa`  
		Last Modified: Fri, 17 Jan 2025 01:31:41 GMT  
		Size: 11.6 MB (11647038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973d4fe8f60777ea79ee8588ad9d2aaf78ec3e9b5beb53af046a4f192474c4e`  
		Last Modified: Fri, 17 Jan 2025 01:31:40 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3bf1fac613ab2528a3a606eab5ccf3cc5c7a4d1baea110c8cc9a192c8a1afd`  
		Last Modified: Fri, 17 Jan 2025 01:31:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd158ba2109743673047ff8abd5f2e0f6c42fe93382e29ca0858b84174a1722`  
		Last Modified: Fri, 17 Jan 2025 01:31:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac577369fbd6cf74225769061ab8205b2a2d8d3f828e46d820b9c4f7b93c4ad1`  
		Last Modified: Fri, 17 Jan 2025 02:51:16 GMT  
		Size: 2.3 MB (2259697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a76240fd47dbb0c307c19a721f69b47cf474871506ebebd969ed599e88db32a`  
		Last Modified: Fri, 17 Jan 2025 02:51:16 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fd2ebb57b90b9ed8f7ffd2c4fc9fdb3a941b49e5955283815a8cef446300c5`  
		Last Modified: Wed, 22 Jan 2025 00:27:49 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29f774a84854bda978087c96a112e4632e6e95165b1fdf7564a71379f28ce51`  
		Last Modified: Wed, 22 Jan 2025 00:27:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1dca57bd14ab68cc7dccf1e4af5531c979c75749e184e569e4dced977b29e4`  
		Last Modified: Wed, 22 Jan 2025 00:34:59 GMT  
		Size: 21.5 MB (21477598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4c88ede6e9617cfc6a19aa2561a967877543d0459e6ad756c332c8bee50e7134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6921076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e08b8f632c72d88b0ffcb7ced6ed227efa11ad7d3d982d73798942f9ed626d`

```dockerfile
```

-	Layers:
	-	`sha256:32603a1f3cc86abc12028ef46e66836fbbb2c206d6cb92c0a781a5494256ae06`  
		Last Modified: Wed, 22 Jan 2025 00:34:57 GMT  
		Size: 6.9 MB (6879711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3ea4f9b161f2ec9a30f82fac95668230aa7e9b8c355422ab3645318b2f7f08`  
		Last Modified: Wed, 22 Jan 2025 00:34:56 GMT  
		Size: 41.4 KB (41365 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:bd830673d59b397c3ac1d0c433737b79cfa368496dc6bb535542ea24601cfd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200161315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64155b0bf451d11dd63a55c6e6126fb5ae2e52fb169659bf03a339ec670d902`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679520630c1119c6d5ed8f586ed4e3add8abb1239ca96890d7e7f56e132903ce`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1900402a9d5100ac5f8ce80a5f47f236e58d5b6cbc040caef36e05532bc8b3b5`  
		Last Modified: Tue, 04 Feb 2025 04:37:39 GMT  
		Size: 101.5 MB (101514284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc22770b6701d4071e3424e53e3bbbdaf545f9fdc8c6a6a3bbd75d36210a6d1`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ff05914b1a23525e49c5251ce70c5e0400fbf205aa01507d19f1b94cc7d94`  
		Last Modified: Tue, 04 Feb 2025 04:37:37 GMT  
		Size: 20.6 MB (20638489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22968474b51014c1204f2ed693635100efafc5d6c52c168c6b327423893b8`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bff96e732879827d08be1a66e0465f27f21f3042bb65e98c5d207acde79ce4`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157536fe17d346a1247eda1f0a847cbbc849ae11ce85625aa95ffc87775e8f2`  
		Last Modified: Tue, 04 Feb 2025 04:37:38 GMT  
		Size: 12.7 MB (12672207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b048a8842a0c348b46601407f16d781cd0faae3f29ae62652241d359c738d4`  
		Last Modified: Tue, 04 Feb 2025 04:37:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb5a150fcf42fc4edb97e4855ad3353083013c68c0fc27a4a3a7e52530a8276`  
		Last Modified: Tue, 04 Feb 2025 04:37:39 GMT  
		Size: 11.9 MB (11872637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329a81d7ed20aed830ccccbe675a8c7577ef60e50901d8260750f9e1c9c0472`  
		Last Modified: Tue, 04 Feb 2025 04:37:38 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d7c913ef647dbffed0dfd3d84cc6caf1466d269f276f8e851acc04351a18a9`  
		Last Modified: Tue, 04 Feb 2025 04:37:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d2ddd462726eb6fd174809f61424ab2a249294c63cfa112e552ac3c9946be9`  
		Last Modified: Tue, 04 Feb 2025 04:37:39 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1deffd0bd732510e73e17687079419892f8da9ee6ea3e281a528d9d239c8c6`  
		Last Modified: Tue, 04 Feb 2025 05:16:45 GMT  
		Size: 2.1 MB (2052614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaf6f0428bce4dad9745d3a63ef6860f4401b8cffed5df6e1465bcc7c04cbb3`  
		Last Modified: Tue, 04 Feb 2025 05:16:45 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9421433e29ff7d371cad3495fb2a39e833b359cca59c7fe629dd461fbee59a0`  
		Last Modified: Tue, 04 Feb 2025 05:16:45 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1f4bd0b7c586438fcd46cfb763d728ec73580a1249ff6f1c14e89c4ac1ae69`  
		Last Modified: Tue, 04 Feb 2025 05:16:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78325a3ff6a159ef0fde7393ba6137732f6bd1380969d2d75103a34e6327592`  
		Last Modified: Tue, 04 Feb 2025 05:16:47 GMT  
		Size: 21.5 MB (21477391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bdb5b4493a545900e08883ff83a74a7c3a31718d9d91e547294307cb71ec30c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6862161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cad5e2fcd689037c03b2fcedc03198a9dc94615fb322d5d2439de66ef50581`

```dockerfile
```

-	Layers:
	-	`sha256:2001254f8d39f0f8cb284ad7319409175ebddf6aa2ac88f3acb1a535d65a1a3e`  
		Last Modified: Tue, 04 Feb 2025 05:16:46 GMT  
		Size: 6.8 MB (6821232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6342f6bb5ecf9465a17b03cfad0a1f418720b6684657931cbd62a6493eb6ae3`  
		Last Modified: Tue, 04 Feb 2025 05:16:45 GMT  
		Size: 40.9 KB (40929 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:88d2240f94dbd23c27585f74a7bd28dc8764d95ee1c2fb8dcc529150ff41efda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205500651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fcb5576fa3a87259ea37b1c21d9d6a523228914bb8179486df8306e1f84a7e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 05:12:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 05:12:53 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 05:12:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5218c0aca3f23dfaf27a513c2d06daa612d2386294a53d81f7ddbaba9d45ee`  
		Last Modified: Tue, 04 Feb 2025 05:17:45 GMT  
		Size: 21.3 MB (21308399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e7b8f37e12d934578444c6271234e36e9309afc271390ee87415e245ca5b87`  
		Last Modified: Tue, 04 Feb 2025 05:17:44 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca689848e7e5a26455cede87aec423ec507686f316f5ae1d8789563c816b887a`  
		Last Modified: Tue, 04 Feb 2025 05:17:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3207b15700af30303fc01444c2c82341e4d65ea622e1acf4def510ef72dfc9`  
		Last Modified: Tue, 04 Feb 2025 06:06:41 GMT  
		Size: 12.7 MB (12672735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1118d66ecc0c81e290769d5134ec440b132aaa95c047abda409b97c8f48e98a`  
		Last Modified: Tue, 04 Feb 2025 06:06:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a223afb62ed8ccba454869761de27fb33ca00e32d1f4a5700313612a89107d9`  
		Last Modified: Tue, 04 Feb 2025 06:06:41 GMT  
		Size: 12.1 MB (12070524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f562c2134c2e4f9426d482e275bfa509bb9170e6a2901a34681eb03b86a8cfc`  
		Last Modified: Tue, 04 Feb 2025 06:06:40 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee31c75acadf55ed694f6f9465b5c6c06ee02569395821366724674b78db7e9`  
		Last Modified: Tue, 04 Feb 2025 06:06:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28ada74699f0c515168f4ba8e58b15f37b592fcc1f5777872d97890d8fb1798`  
		Last Modified: Tue, 04 Feb 2025 06:06:41 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58101db9eb01b61c358cc8fa31f96c2658304a1ffe936bbb681610345a9a44d`  
		Last Modified: Tue, 04 Feb 2025 15:55:13 GMT  
		Size: 1.9 MB (1856297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e093f5ea2fb0c26d1842eb968fbf98311e4aafe5d73058d6a3ab5cc6388d9c`  
		Last Modified: Tue, 04 Feb 2025 15:55:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df012f4c20436262278011062584055def0b8fbfee620c8c9b73f52b19c58a92`  
		Last Modified: Tue, 04 Feb 2025 15:55:13 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfe6358c7f7257af35145c83abd4bd8c80b6358d76d4b55f93c6d91053703e5`  
		Last Modified: Tue, 04 Feb 2025 15:55:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ec40723b074350b615e691374176206100197984a12e7e0e74a2c45fdf49fb`  
		Last Modified: Tue, 04 Feb 2025 16:01:19 GMT  
		Size: 21.5 MB (21477652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:226e5b2eac5ddc2bb7178a32028506724868856892fa7396c02022bdcc25e7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902a7d24892b58a8b166a6d4885c8049f00f066c295301014d93e0ef7a7ea914`

```dockerfile
```

-	Layers:
	-	`sha256:cdf1ff8c213e9256cfb3c6a49e48a1270588ef735148772e772ec03419c14235`  
		Last Modified: Tue, 04 Feb 2025 16:01:18 GMT  
		Size: 6.8 MB (6828229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e01ef627558af0450ed678f97b1df16b7460683948e115f43de5d1df20bc0a3`  
		Last Modified: Tue, 04 Feb 2025 16:01:18 GMT  
		Size: 41.2 KB (41185 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:05d8a081c9fe66e97a0e85eb346df877fd6e97dcbff897361fa4d731bf9c887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174895926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ace93a951927dd61aa09848f39a8e065d46596ab47cf39393b1013de904ecc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 Jan 2025 04:57:29 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Jan 2025 04:57:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Jan 2025 04:57:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_VERSION=8.3.16
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Jan 2025 04:57:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Jan 2025 04:57:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /var/www/html
# Tue, 07 Jan 2025 04:57:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Jan 2025 04:57:29 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 05:16:13 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8253988c6a24fa76feaf6e34729bf23e9a788e7438b3da6a7db669f072c5ab9e`  
		Last Modified: Tue, 04 Feb 2025 05:23:18 GMT  
		Size: 19.9 MB (19895180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82684711048482eb8cc4b2f6548b4d6e7ece37d508c1ea3a12ab8f229f29fda`  
		Last Modified: Tue, 04 Feb 2025 05:23:17 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5cab685c9f3203c43aafec691ac532f2bd71706ad37119783a03535a44ba2a`  
		Last Modified: Tue, 04 Feb 2025 05:23:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75395b3c4347b39b2b9a80157704b6f66cfd082e176299c67f08aad81ffbd0a2`  
		Last Modified: Tue, 04 Feb 2025 06:12:50 GMT  
		Size: 12.7 MB (12671608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cb94f07a54aee56a250c94a756b299d1f8393c8f7902ed1878d0cc3e70c9d3`  
		Last Modified: Tue, 04 Feb 2025 06:12:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b819120b63451c38a32fde8d2f32e61bd27e26a2c598e68d55a0056f3c692`  
		Last Modified: Tue, 04 Feb 2025 06:12:51 GMT  
		Size: 10.9 MB (10875761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1ed24c5a00c5915f551958761a13334fc5df992458b17c31411e707ab2e84c`  
		Last Modified: Tue, 04 Feb 2025 06:12:50 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab52bf9e4d2f61c93b30ca6fd91c8cea7d68e9124cd03ad0c2e65935dc88b20`  
		Last Modified: Tue, 04 Feb 2025 06:12:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2d5e195b1f6273f6204ecd6a4434509aaede50cc58c7ae6d27bfe0a6df044`  
		Last Modified: Tue, 04 Feb 2025 06:12:51 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421b948828fac257640a11b261fb5a0ca40e250b72746a6a86aabbc3308b3f42`  
		Last Modified: Tue, 04 Feb 2025 11:46:55 GMT  
		Size: 1.6 MB (1553812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43923da78113f953cfe772a0d88d342f5dbfaec2cf6703eeea1d30aebdc38d8e`  
		Last Modified: Tue, 04 Feb 2025 11:46:55 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e923e2b4258779a77d4358f8c293e1b6b7aa9fa490d3b77c0e69c9e4d5c7c6`  
		Last Modified: Tue, 04 Feb 2025 11:46:55 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d100892449e04dfa32292846f531afd629d482144aa3c2f0effbb7386da3508f`  
		Last Modified: Tue, 04 Feb 2025 11:46:55 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fb5213b911087b984347dbe9c54139858bc0dfc19cf6f843ed4b366a051d1`  
		Last Modified: Tue, 04 Feb 2025 11:55:49 GMT  
		Size: 21.5 MB (21477457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:39c8fe803fd6e07f45840d9f926a5c9790328b6fd281dba2f133ea3954c08a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db921f7fa6c1f003dd40482d9bab88bfae46b3030db498194f896d80cb812aa6`

```dockerfile
```

-	Layers:
	-	`sha256:75f0c6300ecfdab244e54bc58ec6f214ae11b21c9dacb15f6078c9ebb5819a68`  
		Last Modified: Tue, 04 Feb 2025 11:55:48 GMT  
		Size: 6.7 MB (6692555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014f38ea929651deb7d3dc74130dcf14d9d831039ca3f9672b3c8c07ccac5517`  
		Last Modified: Tue, 04 Feb 2025 11:55:48 GMT  
		Size: 41.0 KB (41037 bytes)  
		MIME: application/vnd.in-toto+json
