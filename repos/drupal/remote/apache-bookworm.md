## `drupal:apache-bookworm`

```console
$ docker pull drupal@sha256:55a482497b193fb48667623954d4ba6147e9f7fe68b320395a7e509a4b883c2f
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
$ docker pull drupal@sha256:e1980885a00763c69be988671454400b778e9ce3cf205cff8f9857b7d495dd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f2688354b01d7e2df854696025ff23d019d7360883bfd48870bc90fd1e0ad1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:20:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:20:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:20:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:20:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:20:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:20:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:20:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:20:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:20:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:20:30 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:23:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:23:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:23:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:23:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:23:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:17 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:23:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:23:17 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:40:15 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:15 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:15 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:15 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378813deee69243cf04ee1a6481394d86f489b7bd656bd9cc61cb6b7e2d6ecbc`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8685c1a28010251c326af1ea730dec27b8595137d45a17fc7823d12b290c27d`  
		Last Modified: Tue, 04 Nov 2025 00:23:59 GMT  
		Size: 104.3 MB (104330651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd2626ff8621c5095307155de1569aff676630dc33ad200c68e5a91cd0bb2fa`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3c24131b291db4920bc63df0b6e841532ac9a7fc8cbf2d90f9d13c309fbb96`  
		Last Modified: Tue, 04 Nov 2025 00:23:50 GMT  
		Size: 20.1 MB (20131749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d76b38b8781e5f32fd3bb0f7ca4294a2c2a9029ff8f81778018fc1ecae64c1`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a433803a3088937bc8c631fa4f7d089e76821ef307e0bc8b462b8dc69e33ff8`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039c0f209bec7b811977a769e9c324d2dcf35ae7f2cd5e3b559890f3f60ec77`  
		Last Modified: Tue, 04 Nov 2025 00:23:49 GMT  
		Size: 13.8 MB (13773351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79de272dd8e5276ead109636c84db4dc311f62081acff2f92cf819dfa7e4f56c`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2228ad9e93e299f51eeea6b5e04d045dab8e82fef4cb913a1a150fe1bafbbae`  
		Last Modified: Tue, 04 Nov 2025 00:23:48 GMT  
		Size: 13.5 MB (13498587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fa1c6687ee0f8c0c59b0029b0d8f085dc7496f85a80ef3a5ec919d4c9f16c3`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19da57137c7b3ba436b50a73e74a5ab4619eca9fe5af29d8fe3f9f56051d8d`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18f374a494a2539d8cd44e1be8345bb66a32f955f9a5f7ddd8b31c4a2fd2fbe`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5faed854bfee041a532643991153bfc607437131adb1367ee44048dcab03418`  
		Last Modified: Tue, 04 Nov 2025 00:23:47 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c9eb68b83e696c58e3b65167939d0bb79973b26a51b0ff6dabc9b2934f257`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 1.6 MB (1574202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19533e5bd2dbdcf366dc2147bc4e7f65516a967b96765765d9f066042e476830`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a89c24b23eacd38d8f026ae9e8c13d026d727508678967071e520b03dd6e3a`  
		Last Modified: Fri, 07 Nov 2025 00:40:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40eda03a46d00c31424183cff3f7dc85d004ddce0d29810c06a9d49d3f8f45a`  
		Last Modified: Fri, 07 Nov 2025 00:40:49 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f703c6b65701dae135d09c28cff66ee5455f52404176db892c2d599b840d7577`  
		Last Modified: Fri, 07 Nov 2025 01:26:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd5ca1e1f9d974f861dbe79fa3387c5b82ba66913b89f1c24415a9483482d1b`  
		Last Modified: Fri, 07 Nov 2025 00:40:51 GMT  
		Size: 20.6 MB (20642986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:25ac143866fa85d00a7986c48b29331e9d2aeba7039efc895dc2f58919be1888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7098307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1fde7539ecae52f7a7a4088b924fbb02c59e1105ace7cfcb6280fcbb9bfbc4`

```dockerfile
```

-	Layers:
	-	`sha256:063109a6446c722848a131f520cee426515094bb612e76fc976aff7c50d00351`  
		Last Modified: Fri, 07 Nov 2025 02:56:57 GMT  
		Size: 7.1 MB (7054222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de6e6d37dd887bcdb1e3b304e24d433a790ff50fe132ae6628ab03ac79ae80`  
		Last Modified: Fri, 07 Nov 2025 02:56:58 GMT  
		Size: 44.1 KB (44085 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4ed9c51f8dd8b8327f2ce158ec1ba67df0ce54a6197a276a938abc6132f2e193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167012034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df19383fbda4566f77695a614c4b8b5ed45422fa86323afd86b9edede5492bb7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:16:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:16:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:16:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:16:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:16:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:16:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:16:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:16:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:16:52 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:17:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:17:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:19:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:19:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:19:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:19:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:19:36 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:36 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:19:36 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:19:36 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:40:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:27 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:27 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:27 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:35 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d75259e3cc7bf66e987106b258ca9f3341f6ba764a7da30b2fb6aed592c4f1c`  
		Last Modified: Tue, 04 Nov 2025 00:20:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4702cec7bcd70944085ed4d7479f4b9fe9a1d7de22faa17c97ea7a739bdbefc3`  
		Last Modified: Tue, 04 Nov 2025 00:20:16 GMT  
		Size: 76.1 MB (76148701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f722ea27b800b1c1dac4b32363cd322e2935b5418c92a86f7c1150ebc3c8d06e`  
		Last Modified: Tue, 04 Nov 2025 00:20:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeba8f2d387ae87c97d913321cf03b1e599ed1af20786e73d3ae04f0a2e30e70`  
		Last Modified: Tue, 04 Nov 2025 00:20:09 GMT  
		Size: 18.9 MB (18860014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67c880be1502b982d8fa1a5f8585c25dd6569193d27c197695d229861676bf`  
		Last Modified: Tue, 04 Nov 2025 00:20:05 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaee11b9071f780cc75a5958b3a44514ed5f663f16b21f387bf1c746a12131f`  
		Last Modified: Tue, 04 Nov 2025 00:20:05 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686c747dd410f45213ac26b30e1d43be8b4a5aef17cd9d6455f0a1a39cd23c0c`  
		Last Modified: Tue, 04 Nov 2025 00:20:06 GMT  
		Size: 13.8 MB (13770985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1492fe1a660a50c4f1d4f4d3c84cdd34ac19b3850c3870dc0518b452b4cdd1`  
		Last Modified: Tue, 04 Nov 2025 00:20:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a98cdb3e921c02a16c96bae8e8efd176011c884149afb6fb2bf5717d2ec4fb`  
		Last Modified: Tue, 04 Nov 2025 00:20:08 GMT  
		Size: 11.6 MB (11601472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9dcc3a691d03a9a3e904c89c606980d839ed7399e5167a98a8a09c58f88e2f`  
		Last Modified: Tue, 04 Nov 2025 00:20:07 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8fc07a8ac94afa872c0e681fe05b82dce68470fe5c7daeaf8d89d81ac50046`  
		Last Modified: Tue, 04 Nov 2025 00:20:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9719858ad0fdc48463f6d4ab52b15f115ac2e2f803a10a2590c5d1e95c42a877`  
		Last Modified: Tue, 04 Nov 2025 00:20:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9390a29a90c282a8ac24ef9387306793ee4648b1766bf77e7979971b9c09a462`  
		Last Modified: Tue, 04 Nov 2025 00:20:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea3d81b9380f612166760dca4704f3ac74960277b0dae915ed9ff618edf5fed`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 1.3 MB (1295073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fcfa5a9588a8cf340a08c75a3bb070aaffae137ebb3b962fe4e7802b57acf9`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347ea5f5ed516d7cf92246903c9a3e51244564d80d367883bc7ab1bf6dc5110d`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4606913094ed22e142b1734653184851a0ad1ba1b7b9bea11171a921d15e1870`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d3efd42975e73a111a3e41986642f50b0b40333778778ad4273ea635941665`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1461e1a2b6d9ca357ca5d2bc4701f29c6514aa7f4bfd297cd2c62f0b5a182593`  
		Last Modified: Fri, 07 Nov 2025 00:41:04 GMT  
		Size: 20.6 MB (20643780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f7f938976716dce41dfbffd86e06c32764a8e9f458f6df7d9016e3a0986c554f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6911841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9b5c5b94dace1bfa0ecabb11130ba563498f8da2fd156d419edcdb72b3b6bf`

```dockerfile
```

-	Layers:
	-	`sha256:fcd0577771112b7e081ef80f116499469a078e8059591c68a076506faa356a6f`  
		Last Modified: Fri, 07 Nov 2025 02:57:05 GMT  
		Size: 6.9 MB (6867590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63679a0bfbf81168a7fc0d1aa419800257dbfebac1c4bd55d5d6ee1cf539501`  
		Last Modified: Fri, 07 Nov 2025 02:57:06 GMT  
		Size: 44.3 KB (44251 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7b1c0c78407f3801b158ee0e7c5625c7853bb132b8166fd13c912f2e78c4a99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196306156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13705e7b3df375a8ee8969e19189bb285ffb30092b0245f7233206ed7b11ad2e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:20:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:20:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:20:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:20:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:20:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:20:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:20:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:20:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:20:39 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:20:39 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:23:35 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:23:35 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:35 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:23:35 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:23:35 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:41:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:41:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:41:32 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:41:32 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:41:32 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:41:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:41:32 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:41:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:41:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df3cfb9c379216becd09a6d5c94f023a734932160ae73086c95a5afd9f1970c`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb86b07548fa9207c92e89a9cf50a242947f454f4cdcb6f5333063f39323cdcc`  
		Last Modified: Tue, 04 Nov 2025 00:24:16 GMT  
		Size: 98.2 MB (98165816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6717ae970a5f62b02b53103b4ee86d9b6d2ca7d908dbe0af66379a8d788054f`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20cb9f397536962e0c8f598e88335339857dea1efcc536d75b1537836324fa0`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 20.2 MB (20159103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e2cd5c6478ef134b3860af2816a1ee1ce699bf820419a2c06f311f0ef099db`  
		Last Modified: Tue, 04 Nov 2025 00:24:03 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b51e53b773f16d5c60827f1ed02ba1f9745654c94b738a720c7f1c83f22f8`  
		Last Modified: Tue, 04 Nov 2025 00:24:03 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf936c79215bb9768a8bbbb6cf6c2f333c674b3178e7dcf315ea6ae90c862d9`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 13.8 MB (13772974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df554fd065c1b7d6ee3e1bc5556446f2aba871048bc37d3f31628b4c771398`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674c05476338c3eb1760918f7c3b14b14629ceeebd4db04f1ff1e31455b2f185`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 13.1 MB (13144631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f400bc0b4916fc69f5393c1d428a1b07228c29e4d67e60946f5a9d68273a5dd8`  
		Last Modified: Tue, 04 Nov 2025 00:24:03 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9cb0cb81285be030d9ac095442bd98f849523bcda914261c6ba297be6ef59a`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150e88f7538859429859ca2a9c1528d4ed5cb7a2c25b747ae7777d5952b4c5a`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec8723d8b4f73b8a890689878fb31cd460e103b1b8141a32be144c1ff194988`  
		Last Modified: Tue, 04 Nov 2025 00:24:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed39f5d6365994b2468174bca4db2cad66d596a11e107af760578a824b3efb`  
		Last Modified: Fri, 07 Nov 2025 00:42:03 GMT  
		Size: 1.6 MB (1559962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355f0993be95407e6f775d36b0b423865186c470c6c5a853a6b734d58886ad44`  
		Last Modified: Fri, 07 Nov 2025 00:42:03 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98614a39033bb1b52efe17984c307b9640747f87018b850888a415c7f8e6ca2`  
		Last Modified: Fri, 07 Nov 2025 00:42:05 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7c453d34881c1ab76c7b281687c87865fe7477377a8f45c0bcac35f51193b9`  
		Last Modified: Fri, 07 Nov 2025 00:42:03 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724be4805c8b81d52133343bd95c1714a7199d40f599b0a8ef13b4c6de1f7e8c`  
		Last Modified: Fri, 07 Nov 2025 00:42:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055bd7013d6872e5579cd5873f84224d9f147f345a03ef1793f152893f2f4bc`  
		Last Modified: Fri, 07 Nov 2025 00:42:05 GMT  
		Size: 20.6 MB (20643410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:07a454628e4d31e898c3b8f8c7b2e5d499b483d2ea7e6ea0c002e381e6e9e833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7126984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475822630c2a12e11e6d6abd3eeb0dc8708d8968b3df5550cf25fd49586ad926`

```dockerfile
```

-	Layers:
	-	`sha256:310c1b67991d9ab40dd6c8d50aa68fd7122c11d1c0792aff393a60f91b946122`  
		Last Modified: Fri, 07 Nov 2025 02:57:13 GMT  
		Size: 7.1 MB (7082683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593834901b6c6c29e7b68b915cb90c1cdbf576f299902f7f28c763eb0c779b6c`  
		Last Modified: Fri, 07 Nov 2025 02:57:14 GMT  
		Size: 44.3 KB (44301 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:3ecf4ad98de830fe02952cce053d387bbfb946836c17b8756ddb1462ca30f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (201994670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fce12550dc8f39ead51577684fb8433fff8dc3b8f15c6e51bfec63c36eb8da6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:17:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:17:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:17:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:17:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:17:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:17:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:17:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:17:31 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:17:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:17:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:20:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:20:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:22 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:20:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:20:22 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:40:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:35 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d6c898007b7581386fd5095822158822be3a8d9cca6cde5d465edbc6e4dfb`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713537d54a154a90d71d1dd45a46bfe9272e009d0bead10463c2371e488f03a2`  
		Last Modified: Tue, 04 Nov 2025 00:21:02 GMT  
		Size: 101.5 MB (101518570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c11b6cb2ce3b54f452288a7af91fd1db7574f696c736f3e2264656a1d21e42`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5931e8cb00b849d7d67d27da7c8392413c0e810f64770894a0ce026dc70d3134`  
		Last Modified: Tue, 04 Nov 2025 00:20:54 GMT  
		Size: 20.7 MB (20658337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b05abfbed9c8c141b72fe277758c3563c325f64af1d4facf0cf9b9be2b7c60e`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c305048691fed92487f4fc8988e530d9e22f3eabf941e3248fe7dd22b2ca037`  
		Last Modified: Tue, 04 Nov 2025 00:20:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71f3575ed9da0246c92b1839a8558b130ed6e377ed97e6a2deef5e15c6b11ad`  
		Last Modified: Tue, 04 Nov 2025 00:20:55 GMT  
		Size: 13.8 MB (13772283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d8a6bf9a2b274a0e19ac0dfb719b0005e8198d348f175de527cae5429da4d`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8668c48cb24f58e0d8d28f0b2802e84ec0472563dbafd5468ac65435bdee1a0c`  
		Last Modified: Tue, 04 Nov 2025 00:20:54 GMT  
		Size: 13.8 MB (13790724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22beb408f0c3280229ea7d2fa48f7ab304600a2108ce2c60c3249e52c580320`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c208d4c9eeb90c84ff821c60fda4ec8f0058b38257952834608928131b249e8`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dbce3b1653c05164b3f474f9d06b0b9d74272346f181bc9c01cc2a594db093`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ea5fe66ae871ba2d8701cb6e1829204f29ebc67d1001eeb52892a606ab963e`  
		Last Modified: Tue, 04 Nov 2025 00:20:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5031331fd9905f58301d290c847bed775e48e67a56d3fe0242c936ccd05241`  
		Last Modified: Fri, 07 Nov 2025 00:41:02 GMT  
		Size: 1.6 MB (1645733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7e0fbf5a6ba06b2946518176ccde8e8bfa4d8f3998395c24e85a509ff93d51`  
		Last Modified: Fri, 07 Nov 2025 00:41:02 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e700e618881ad7249f5101e5f3f96679dc8c8ccea61438b60c5ff28fdf2ea2`  
		Last Modified: Fri, 07 Nov 2025 00:41:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823e8bc575b69e21fe3e4b2e515ee4aa0e61c4ed8e49e77ebfb6685928763c67`  
		Last Modified: Fri, 07 Nov 2025 00:41:02 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829a38bb861f7aec5b184c92d35acf64df48bcae8f477ed7d80920c6d4f8999`  
		Last Modified: Fri, 07 Nov 2025 00:41:02 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c7e6fec61dd272f7be5b666fa8669074fb4af4ebeb2670b7d354cb650ccde9`  
		Last Modified: Fri, 07 Nov 2025 00:41:05 GMT  
		Size: 20.6 MB (20641291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:877a8d7380a1fabc571e7cdc49130cc01a73c2cde488d923bfbf60fec168452d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0012987664cb973f0f24b9b700ce9ed3b63a2de2105c529c12f045963ae660b9`

```dockerfile
```

-	Layers:
	-	`sha256:e5e40c83c2c179a1349f6cb841dd310529303bdf8a3f935b5f7e0a81a2b287c8`  
		Last Modified: Fri, 07 Nov 2025 02:57:22 GMT  
		Size: 7.0 MB (7033950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0cde8497c535b705c8792591847a770ebbb5a1405f600e1f23df6792c54b743`  
		Last Modified: Fri, 07 Nov 2025 02:57:22 GMT  
		Size: 44.0 KB (44020 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:98ccabc7cd14a29195aef96bfabefafe3b868d7c9a0d996ca8bab861da389155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207579529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a24f7e167713c476b3952217bfbecc131aab31b5279bf0ca844afc5e20290`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 02:33:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:34:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:34:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 02:34:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 02:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:42:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 03:25:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 03:25:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:29:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 03:29:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:29:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 03:29:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 03:29:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 03:29:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 03:29:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:29:22 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 03:29:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 03:29:22 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 16:07:00 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 16:07:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 16:07:02 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 04 Nov 2025 16:07:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 16:07:04 GMT
ENV DRUPAL_VERSION=11.2.7
# Tue, 04 Nov 2025 16:07:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 04 Nov 2025 16:07:04 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:53:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:53:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423ff8a5d9e5803ce51c4bee23a305ce775f33ac0e1498c84052d0e8fbeb72c`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d4bf9d38282d902e4e65ff38ac946e13144e841061113ca97aee44f4413c20`  
		Last Modified: Tue, 04 Nov 2025 02:40:57 GMT  
		Size: 103.3 MB (103328858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b331438757ee31483215b6dd106186ef28c3d99b0849f835e85e4cba07a27b`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4f0a77689b5b972d24113ea299100c1a0d18a46a41dd0688dbeec9193dd5c1`  
		Last Modified: Tue, 04 Nov 2025 02:49:44 GMT  
		Size: 21.3 MB (21317849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b992e275af09d1f3142c007faa97121b28d014f4fd52e3fb4d61ab4618c85e2`  
		Last Modified: Tue, 04 Nov 2025 02:49:42 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273cced39343969a12d6439d8b0d6f90309922a8572726a8a55c0f4675362179`  
		Last Modified: Tue, 04 Nov 2025 02:49:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf2e3b17a792d54cbca3daf187d187680f503efdad9da57f1e79a53a097e09c`  
		Last Modified: Tue, 04 Nov 2025 03:30:00 GMT  
		Size: 13.8 MB (13772759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ae12babf1c9d4e33534789f7c95c31829bc1700fe884cc7b8f37e22b6b2c38`  
		Last Modified: Tue, 04 Nov 2025 03:29:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058eab590dd3f9beddc4c7414db4ee45cad37a37b554f7909cc0ef1e3707ec7e`  
		Last Modified: Tue, 04 Nov 2025 03:30:03 GMT  
		Size: 13.9 MB (13914896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b8654ebe7f3db5f754dd4089f0200c6a3a258908ec61e5631ae8bd57ab573a`  
		Last Modified: Tue, 04 Nov 2025 03:29:59 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05b21d2d86043ac7d66ee5522007f8bc8caea4c524675ed0ec7fd1c5cc639ca`  
		Last Modified: Tue, 04 Nov 2025 03:29:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769bccc4f98531f8d4494362e7075d2251624b29441bb42806143fefb410afd2`  
		Last Modified: Tue, 04 Nov 2025 03:29:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48053afe5de1a43425719ab43535bd9430dc0fedf945210d2ed98ca04452297`  
		Last Modified: Tue, 04 Nov 2025 03:29:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86a13cea098d43a4f9c0b22e9cbcb3be23553a36057bc109d22f1bd614f0a6`  
		Last Modified: Tue, 04 Nov 2025 16:08:20 GMT  
		Size: 1.8 MB (1775578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea969486a25dfedc4d96e3e06546e1af9a24fe687c68b60530adaa9b4f3e8cd`  
		Last Modified: Tue, 04 Nov 2025 16:08:19 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9cb849c205cd42659053d4cd965edc0bcde24708719a90bb0242fc6f40601f`  
		Last Modified: Tue, 04 Nov 2025 16:08:20 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453568a03b0afe851c0700b4a31fdf25e5c265c4d9e35733899e165a2fccf19`  
		Last Modified: Tue, 04 Nov 2025 16:08:20 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132a469ecf8287fb38d7d0a4519b4860eef769a1bc475e62b83557ba9a0f9970`  
		Last Modified: Tue, 04 Nov 2025 16:08:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b5163e3826ad3799b8d09482daa4f9d4e778fbb8a86f719f115ac15800da3c`  
		Last Modified: Fri, 07 Nov 2025 00:54:00 GMT  
		Size: 20.6 MB (20642792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f6272ab53f9865d7b1242848c0bdf69d03f1705ce613aee0820c429eeedc750b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1e1be2da5fa8a593852a3bf323733e2722df44c38f208665ffa005ac2dee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6701508cc8a56a8906e4bd03543c7339b9fbc26b0ddcda767a3f1810a8e31464`  
		Last Modified: Fri, 07 Nov 2025 02:57:29 GMT  
		Size: 7.0 MB (7031082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0e9c07392ea5279e373054fd79c899b683802e6cc9c5c93b4a0fc71139553e`  
		Last Modified: Fri, 07 Nov 2025 02:57:31 GMT  
		Size: 44.2 KB (44169 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:417c3435b4cf5cc1a9899f238aab2653b10b2c1b036391c59c153c5ea14c901d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176842381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0022a1a6d7c9048299b7fbe6e622d9a644a76d614a9d310908bbf6ccac8e04d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:30:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:35:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:59:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:02:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:02:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:02:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:02:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:02:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:02:28 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:02:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:02:29 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:02:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:02:29 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 10:05:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 10:05:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 10:05:07 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 04 Nov 2025 10:05:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Nov 2025 19:27:59 GMT
ENV DRUPAL_VERSION=11.2.7
# Thu, 06 Nov 2025 19:27:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Nov 2025 19:27:59 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:52:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:52:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de54dbb81980c9b8d3c221063f25b8474ca2be777ee639ae7b090f0b6933433`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3263ba1b0b7542bbb392f8a89ebf9d5562c8e7a8d05dd575aaae0c51490011e0`  
		Last Modified: Tue, 04 Nov 2025 00:35:33 GMT  
		Size: 80.8 MB (80826218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66245e37d456fef550ca4136b0b6f8bf79ff609208f0f6a1a952faf0bd6a42`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d886063e6a65a87446dbef8cf7d4ac5e0be955ef53742cbf993f02b0aaaa4e68`  
		Last Modified: Tue, 04 Nov 2025 00:39:58 GMT  
		Size: 19.9 MB (19910158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1e04afbcc9c41c784462e4aac422fef0d41cb802f6e761b7c0b09e2fbf9df`  
		Last Modified: Tue, 04 Nov 2025 00:39:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8df14519eea8fc933faf236a723ee6253b8948a5b7ff5b8e7560685817f5e`  
		Last Modified: Tue, 04 Nov 2025 00:39:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a42256a9db1515d1411f39572c83ecfa5b4c1920376e17dd50530bb78b075f0`  
		Last Modified: Tue, 04 Nov 2025 01:03:07 GMT  
		Size: 13.8 MB (13771687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46667e637d1f351304c024f9818827f466db615fcb747590bb7694797aa850`  
		Last Modified: Tue, 04 Nov 2025 01:03:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff3b69b62436f7c0989c785fd65ddab45d755c2f4f7c16c02e958e7cad53c1b`  
		Last Modified: Tue, 04 Nov 2025 01:03:05 GMT  
		Size: 12.6 MB (12563642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36418eaff47655a26cedfa656d7ed7317f9c3cee55717bc9d2111f7ca641732`  
		Last Modified: Tue, 04 Nov 2025 01:03:04 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5393586aa22b36898c25d8d77dc4570091d34fcc40ce4e4adbef082ed7516caa`  
		Last Modified: Tue, 04 Nov 2025 01:03:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369c1c2dac4fcc7a6e3b4863b08e55e97f1af13ff4a0c9e4a30dee3535374c48`  
		Last Modified: Tue, 04 Nov 2025 01:03:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c61d1f3282c0569bbc655c930580865ee72f48990c360748944e4fc6bf7a5`  
		Last Modified: Tue, 04 Nov 2025 01:03:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400c072ddf0365a36d121915bfda59665c8e764aa18cc45a41600afbaaa24c22`  
		Last Modified: Tue, 04 Nov 2025 10:05:57 GMT  
		Size: 1.5 MB (1484730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7ccdf562dfe8254107d3912a253b3151fe7df4f613af8141471d41975192ba`  
		Last Modified: Tue, 04 Nov 2025 10:05:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba908bde1e1104e96174a245230a25c4cc1628c0d895566b63519c052d993b3`  
		Last Modified: Tue, 04 Nov 2025 10:05:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a53bbae0660c25cec21f74e0c81652436a512a1560ee7b781517b9b9232859`  
		Last Modified: Tue, 04 Nov 2025 10:05:57 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820baff4e85cff7aa881175087bcdc6d0f23438a2af4fa93e7c828d9df23ffac`  
		Last Modified: Thu, 06 Nov 2025 19:28:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea523d95fde3a5d906f504cc46dc1c458fd5afa1f0b133d30c1591a6c0c28e01`  
		Last Modified: Fri, 07 Nov 2025 00:52:50 GMT  
		Size: 20.6 MB (20643493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:83e0d74833bef29dee460a13ebb4804633121bc773a84ccac33ffbfb962bae4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa38c3ea144822f793704e5f312074f1836f8009e9469a4d5f755a7eccb5077`

```dockerfile
```

-	Layers:
	-	`sha256:540a59f5ac07d569f276e941f8904cbbf09192e0b1ccceb72df98df36656d4fc`  
		Last Modified: Fri, 07 Nov 2025 02:57:38 GMT  
		Size: 6.9 MB (6891424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a38042d7e866e8efc16791cbd9e16436a597602bbac89f7cf34d7f083590a8`  
		Last Modified: Fri, 07 Nov 2025 02:57:39 GMT  
		Size: 44.1 KB (44078 bytes)  
		MIME: application/vnd.in-toto+json
