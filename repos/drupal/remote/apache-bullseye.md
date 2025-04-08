## `drupal:apache-bullseye`

```console
$ docker pull drupal@sha256:e703e31c28f27bc5db1f35425df49ed9c12c2f613aad6b6c5da98f7ecf723c13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:a36da8f703f10803abd371ec4d47d7b157c231b89498b4905804397ab4da2566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188013252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4032ae059236240a1332e0647f93b943c74e54d9916dc531900a5e5dffc0466`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 15:35:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bac74b9ac14001d49a17d12e2678c07742ece75c132f1b19816358b23c86911`  
		Last Modified: Tue, 08 Apr 2025 01:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d5ea90f11c3e52a7d93c53804b2617f37556c4e8726688b6909503dbfbbc6`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 91.7 MB (91653382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e7602a84c7c60ae839aebcbf26e7c77ecc81e43f9f6cf9b2e6bebdb28755b2`  
		Last Modified: Tue, 08 Apr 2025 01:21:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9cd7884fa0effe6ecd7e9ff74a7d6fb8bcc6305de64b240f1f0b4c7f2ca765`  
		Last Modified: Tue, 08 Apr 2025 01:21:36 GMT  
		Size: 19.1 MB (19064190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62c6fc56f8aad0da123f39ac0f7d7edb95122d8a35ddea86ea861e9171ff30b`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08ebb87d416e7cc2eca3a67ac03fd4c01f7047bc1b6b37c0b1c75c398fa4c3c`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df31dc1f41746059129eb8cd002068765adfca35299b8f5a4d3258ed38ac35`  
		Last Modified: Tue, 08 Apr 2025 01:21:38 GMT  
		Size: 12.7 MB (12685594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7321206b71f0ec0912cd897473a92dc5a1cf5cd04e2c101fcfd285e38b4c7ce`  
		Last Modified: Tue, 08 Apr 2025 01:21:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d04e3177988b06db63fb896db23a0331ddd22a8cef3c1db6f6cccc642f2669`  
		Last Modified: Tue, 08 Apr 2025 01:21:39 GMT  
		Size: 11.6 MB (11599273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8afeba741961a0deb52154a42f9775f27d68de1c6b7f7ba23e2b8dd6488766`  
		Last Modified: Tue, 08 Apr 2025 01:21:38 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd677d6bae2a44aef5793e9a5d587485b1e45cfe2c2f7404c5145148dc024049`  
		Last Modified: Tue, 08 Apr 2025 01:21:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6b95153b74944473f1106515dbc80e432e352d54f025c43b3c84cfb39d99f9`  
		Last Modified: Tue, 08 Apr 2025 01:21:39 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3253d199c3ab5dc2fdf8145ab635e34c48c18a55f63ac1f1907c00fa07d05c`  
		Last Modified: Tue, 08 Apr 2025 02:15:58 GMT  
		Size: 1.9 MB (1933075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d2fe9d1594c19bb774fe63c2648171b0189397e586a25adf0f8e7dbfaf749d`  
		Last Modified: Tue, 08 Apr 2025 02:15:57 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcf398ed98fe4523a64b51c11219263ba32cddc3b54047a0a939703425b68bf`  
		Last Modified: Tue, 08 Apr 2025 02:15:58 GMT  
		Size: 750.6 KB (750624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb7538265ddcd65effaea0a90d2a9af6a63d2812bfa4a1ae8ff6b35b3c094e`  
		Last Modified: Tue, 08 Apr 2025 02:15:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3351ee7f543e584b4808aae34db634b33f61521490de7505fdfb221bc8c66e`  
		Last Modified: Tue, 08 Apr 2025 02:15:58 GMT  
		Size: 20.1 MB (20063778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:9968878d5c4cb75c23687a3e4a4601510dbc4ba89ad9b3e54945685a306e3ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f8e7e77d7e8f6c449fd110c9b270d8f86ce88e5e8e1390f5889818cf30af56`

```dockerfile
```

-	Layers:
	-	`sha256:0edd0d1551040d044cd57403358754319287e7e7d8d98ba06d8d03434927b815`  
		Last Modified: Tue, 08 Apr 2025 02:15:58 GMT  
		Size: 7.0 MB (7038387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3e8a06bacb4efd7d6c37495ef6dbbd98387d887a87a8875fc408033d286c0d`  
		Last Modified: Tue, 08 Apr 2025 02:15:57 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:3fda233debb11fc3bbfe17d6d0d22a472e96a0372d0841daae154c036b54791b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157315781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b56df37dfdb21e2398942037f0688ca22b3952b9e2e525b86679b7429300a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 15:35:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
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
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1025fe025af769b6936ee3ed06b13f60f6c4df2ea57a88d17e56f673ea45b6`  
		Last Modified: Tue, 18 Mar 2025 06:34:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c44daab001583fce063841032bb6ea652620064ab9fbf7d880588eaf67c75b`  
		Last Modified: Tue, 18 Mar 2025 06:34:43 GMT  
		Size: 69.1 MB (69119208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff841f7831550381d69a8f1bf31c3b5a47d736c2f6a95a57f029a70b9f2ba3ea`  
		Last Modified: Tue, 18 Mar 2025 06:34:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3820dfc98d59eecfc435663aeef071e4cd3a185c11c95fb306b3541f07ea6ca8`  
		Last Modified: Tue, 18 Mar 2025 07:33:39 GMT  
		Size: 17.8 MB (17817117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5693b515125ea6a0aa248f7e033223d4b2967f70f5cf1be77e196aaf38331d`  
		Last Modified: Tue, 18 Mar 2025 07:33:38 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a3e2077b9803e8dce2ee34a6c0340efb25d0a1243736af5195b1a593c69fc5`  
		Last Modified: Tue, 18 Mar 2025 07:33:38 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70a649ce9dc0d9d02aebc4ada2d90e597fd89930be5d11d014d849acc77843`  
		Last Modified: Tue, 18 Mar 2025 10:58:06 GMT  
		Size: 12.7 MB (12684248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a55f004c1fb8398adbb6a9b1c6644587cecaaccd5a74d91a890331c8036034c`  
		Last Modified: Tue, 18 Mar 2025 10:58:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3086087a783ae9133ea5dac5389ed71bc0f2f0339a79567dd1926cd4431229a`  
		Last Modified: Tue, 18 Mar 2025 10:58:06 GMT  
		Size: 10.0 MB (10027612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c954631ec5034fb3d74d4dec7b2aecf20155b6345708abfa0385fc1f25d5df`  
		Last Modified: Tue, 18 Mar 2025 10:58:05 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9555b27fe97f9994db4e5543c248aebf7fe34833189cef43ff2968b708b74`  
		Last Modified: Tue, 18 Mar 2025 10:58:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04fc05cd0a1217b121bc3cf227612848b5b9807fdefb2d00a69ac5f30533b8`  
		Last Modified: Tue, 18 Mar 2025 10:58:06 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ce37f4bcf034596b7144939b1fadca1a0598de8a33f4eef7e1854a812e1b31`  
		Last Modified: Tue, 18 Mar 2025 15:25:57 GMT  
		Size: 1.3 MB (1312017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1228e5ce283033e5f0b2630b3f54c0103aad61d96f5665815d12f6b9842e3e`  
		Last Modified: Tue, 18 Mar 2025 15:25:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a4bb7d8c7f398a7107581366a49440c27515ff85000907fc1c2c6ba69c504`  
		Last Modified: Mon, 07 Apr 2025 18:48:39 GMT  
		Size: 750.6 KB (750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae43d910146288e16bae75425daa78d0296c51232447ac635e12baa9b50018d`  
		Last Modified: Mon, 07 Apr 2025 18:48:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140fb79b2b81e1853ba82602a3e12e99a6d9f3a3b4ff74109bc2f195cc6b10d`  
		Last Modified: Mon, 07 Apr 2025 18:48:40 GMT  
		Size: 20.1 MB (20063705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:fedafaae51facdb8ad14757c8508f4f4b180fe1ed147cd71467753434f4784ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6883580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15df9d1d0a4136f54e6bfdbb4f848576cd93e049b3faebf164f115fa5bf9804`

```dockerfile
```

-	Layers:
	-	`sha256:7e0f4efcc3d8854a5731d7346913d472be3a49546ad98c847764f5c0a1f60066`  
		Last Modified: Mon, 07 Apr 2025 18:48:39 GMT  
		Size: 6.8 MB (6845437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec15d77961b4fa83fe4eb039ca56d86211d4a329997d7ca68a0d91711811225`  
		Last Modified: Mon, 07 Apr 2025 18:48:40 GMT  
		Size: 38.1 KB (38143 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:a5e7b710ab50c33b719127783f43fa67afa570cb9616a9061ebc1d5eafc96cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181818180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fe7b1898e8757f43dbb2eb4d4de5dd4faacedb51d174a7c97c7c5c0872a5be`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 15:35:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30a4b98d6d9d341325155385916d7532526ea08768653b48f2722f278a8d43`  
		Last Modified: Tue, 18 Mar 2025 05:31:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb0e83a8ad79344475695e51f2489c2d8cf5877a26fcded29b10154759542f1`  
		Last Modified: Tue, 18 Mar 2025 05:31:09 GMT  
		Size: 86.7 MB (86734007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80f21d828c5691e64bf7ff33432f2bc2b409ac5eb2fbbdd42b81f7c20557c38`  
		Last Modified: Tue, 18 Mar 2025 05:31:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577adf86a70349470def3c36906fb60b4b5ddfffb961d43ffa7ac9aa4404c094`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 19.0 MB (18981509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd473bc5275ce03133dbd2c85f8a58dd5605e869a74f6730992e65b5e2db03`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4e8c4c72476e5f880737fb14a8a595975239ef8ad6a2ea5c6d4a25b73fe7b`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b1038c3df939fe6bf7a048f58ed5dcb489bab2b9732b6eb3e808aec0fec58`  
		Last Modified: Tue, 18 Mar 2025 05:31:09 GMT  
		Size: 12.7 MB (12684865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a5b5347166bc3094b30aaca910f4f1a1526e609cc216f642871b3b04b7e503`  
		Last Modified: Tue, 18 Mar 2025 05:31:09 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a568fc1b4b5da97d9a23bd984aadbb45962b900cba7eb6d4f85db19e1fad71`  
		Last Modified: Tue, 18 Mar 2025 05:31:10 GMT  
		Size: 11.7 MB (11655004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d31ef8dcf64483eacd3c13378b79adb764614154a95a5c16720e690ef96e7`  
		Last Modified: Tue, 18 Mar 2025 05:31:10 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f170358b89cbb3c9f14e788310e65795f1623cf37ab12e4cb9e1b7cd73a19c`  
		Last Modified: Tue, 18 Mar 2025 05:31:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6447901cf22637cafc608cf3e2e5fdb8a6f2c51ad88732bf4eba73551b913b3`  
		Last Modified: Tue, 18 Mar 2025 05:31:11 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbeeadc3db6d3efd4397915308059affefa1945b92210da185b7d83cb9770ab`  
		Last Modified: Tue, 18 Mar 2025 12:57:50 GMT  
		Size: 2.2 MB (2196477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d430e40b6b47ce28394914e10eedaff173b29d45125b1a1d21e48e82ccef03`  
		Last Modified: Wed, 19 Mar 2025 23:40:16 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e391e243c5a577eda89bfb4a843d2154bc0619e3b2f493d87fbd381d12f88f`  
		Last Modified: Mon, 07 Apr 2025 19:04:25 GMT  
		Size: 750.6 KB (750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31f9448de200c00d328037efa1cfef91e392efe9c9a0821b4cb68c405118e2a`  
		Last Modified: Mon, 07 Apr 2025 19:04:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9386cd54a93f1e3081f849238a6aec07c339dd646443256360a2d4d49febf4f`  
		Last Modified: Mon, 07 Apr 2025 19:04:26 GMT  
		Size: 20.1 MB (20063859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:47bc2d9418f661aa49a15ea5cc9efe29f653574301499387df89fb59c44597fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c610b2e9582f595a1fb34d4db002d549a0a588bddd27daecec169fb79151f4e3`

```dockerfile
```

-	Layers:
	-	`sha256:182f1c3ceb6bf62fedc136671ec059fd61dc51c33df246d34955b2ede3de91a6`  
		Last Modified: Mon, 07 Apr 2025 19:04:25 GMT  
		Size: 7.0 MB (7039353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc97e0ff6019f9c93ff0367ad336073029b9deea80f2880a8f05717e5bd5c781`  
		Last Modified: Mon, 07 Apr 2025 19:04:24 GMT  
		Size: 38.2 KB (38195 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:7a43597da3ef336d52036f9b4f908f5712da88793bd78d3774b75a63ee206b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190570150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a35f5629c08031c196dc82fa5d8b12d574ed5da04813d9e37f5fbd4683907`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 15:35:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 15:35:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157e07886443f1f9ea3618eb712416c4f7fb0d1476dc360770751436d7f4fb1`  
		Last Modified: Mon, 17 Mar 2025 23:30:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dba154b0633cb3676a8564ef6ff1411d055f50944c8eea2cc860de2009d292`  
		Last Modified: Mon, 17 Mar 2025 23:30:26 GMT  
		Size: 92.5 MB (92521346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeee77d304f7c9afafba02eb2d21e61fc74785590f36db650932dd93925a1ca3`  
		Last Modified: Mon, 17 Mar 2025 23:30:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b601e07b7177bef4393b478626177c19a4c7121f3d6cff4b05a1d722ebfbd0dd`  
		Last Modified: Mon, 17 Mar 2025 23:30:24 GMT  
		Size: 19.6 MB (19552782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac9b2a2b08fe7e1e1d3a409b4eb7e4eb9f00b2c12bb12bf9a59960153899278`  
		Last Modified: Mon, 17 Mar 2025 23:30:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2f614d2fd293a23233ec5566665d91bb69c683d587ac767bfc6af898654ad4`  
		Last Modified: Mon, 17 Mar 2025 23:30:24 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef1260cf2608ef82df8a21cdd64c918ea05749346d6ed3af91ca609805f3b9c`  
		Last Modified: Mon, 17 Mar 2025 23:30:25 GMT  
		Size: 12.7 MB (12684874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d2e01075654eb73ace8b608c64cf8569c5f96c443cababf3b2b5e91306a5f`  
		Last Modified: Mon, 17 Mar 2025 23:30:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2fe470adc7ca3c0d2cda0847a7e721889e79116a5d23fccd4c505c86527ac0`  
		Last Modified: Mon, 17 Mar 2025 23:30:26 GMT  
		Size: 11.8 MB (11812118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8314957035922d6689c25e0d6d238ef84a506b055672e827081e6deb5892ca1`  
		Last Modified: Mon, 17 Mar 2025 23:30:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd32d90fba0355e6b588f3f2ace84c945e39777a33f09caeb296c29ced3d8c2`  
		Last Modified: Mon, 17 Mar 2025 23:30:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dcbb28789d826833e5833add179f768f0bc75a589803529ef50ce48cf5453a`  
		Last Modified: Mon, 17 Mar 2025 23:30:27 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89881ed6900be119285a12b68eb23e79e8d1c3ed6ee4e9bddb49a5ce46ee421`  
		Last Modified: Mon, 07 Apr 2025 18:44:05 GMT  
		Size: 2.0 MB (1998337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233fc056c5276ec6730dae559934d9ec099c4575664ccd403e6378ad356c02c8`  
		Last Modified: Mon, 07 Apr 2025 18:44:05 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079f45176074723c76c7e4447238ce7d1d58b7e4118aa3d2316ba8fd9b0e98ae`  
		Last Modified: Mon, 07 Apr 2025 18:44:07 GMT  
		Size: 750.6 KB (750624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fa654333ca560a4beb48b9bf16a6cf2b18cf84600f6100d4014f0e2562176`  
		Last Modified: Mon, 07 Apr 2025 18:43:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4ccf0e7fefa278b3ee863454441df8d6fe19fa96d22514cb8f6c7342b5f39e`  
		Last Modified: Mon, 07 Apr 2025 18:44:07 GMT  
		Size: 20.1 MB (20063826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:6118a94b88bfc6b105fb732213483cd391589f42b9184fc704d65731af29215a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7065015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb84963461fad894743671c30565c7ba0dc80a034418ebfbc0bc419fc3e278`

```dockerfile
```

-	Layers:
	-	`sha256:e9301225312164d41360f0238377a4d61e339d61931254ad175fa66ca2de54b5`  
		Last Modified: Mon, 07 Apr 2025 18:44:05 GMT  
		Size: 7.0 MB (7027091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8914fdd3e39baf5b4aa009eda5e66057c930085f340f86e6286337609902fe20`  
		Last Modified: Mon, 07 Apr 2025 18:44:05 GMT  
		Size: 37.9 KB (37924 bytes)  
		MIME: application/vnd.in-toto+json
