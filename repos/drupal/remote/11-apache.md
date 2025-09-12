## `drupal:11-apache`

```console
$ docker pull drupal@sha256:ab2352ddb2ede62f9e8af5b961074b13726f2837f6bf5af4a4e344d38e38e8b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:11-apache` - linux; amd64

```console
$ docker pull drupal@sha256:2a16159dde6543e3789d925d7733dc920cf94a25b4f62435f7470d6cb78e9621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202798874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c51647f47cf7032f53bd49ea2c69cd2e5a24f589878172f0ced05f7f7764c9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35f4ad0b9dd77ac67f8390fc8591d027627e7009241c5d7d053de865d3237a1`  
		Last Modified: Mon, 08 Sep 2025 21:45:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9a47e0f0aa5291ae11f3ba7dfe4b31c89d950b58e7b8903509d0ae4553aacd`  
		Last Modified: Mon, 08 Sep 2025 21:46:00 GMT  
		Size: 117.8 MB (117835910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71717529431a195ed00eaa9764de91c36a9ce1dff1df22da72f61fe5012deb47`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861da3588da491ff502802921dddc2134a7d54f4eccb9f4d5564bab2d48669d`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 4.2 MB (4224080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0b33aa5bdb16abb9b1353d80dd3131f150f318a4e445bbe2a3b2e045a0a9b7`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c32d2c29006598982a80fae508389f4d2505d9a40aea2cc26e88db7cadd5fda`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0476ed41acd134fbf208db114645eadb830084420c4cc0237ab28663794d28`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 13.8 MB (13802712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528d7cab555c06b6a3ce20b7ecec8b579a0455bd97801174bd8cbc2ba49cae7b`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf044a4089516b24f696774456cbe307e7c1517faf216385fcef0b178384d4`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 14.2 MB (14213624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54b8dc4cf728a9651ce152e69ade3084dcedbfcfcfbfb214b9c10c3277aadf4`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dc8b9fbab9e8f3dfb5be173c5611df6d797b5b0cef33ed3919fef637dd0d2f`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b4ff87f3a5a30db82791d4288ade8e01d472ead7d51818f1cc007a1a6ae33a`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e25f44ad6429cec4965521b6aea42070caea3cb77d6b1e87199f80365a0a3a1`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce0591cb68c34cfb36063f7fbb0d39e900421c3e00e2a4595a543606c2cd48`  
		Last Modified: Mon, 08 Sep 2025 22:34:20 GMT  
		Size: 1.7 MB (1656208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cddeb4b03abde228c55cbe7d468cbfa2ff7b4467dbe8ebfde619a39c65d4d06`  
		Last Modified: Mon, 08 Sep 2025 22:34:26 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8f3c7f91516cef87ec810be5ab207ddcfdd5b883388c354e0059b473848ae`  
		Last Modified: Mon, 08 Sep 2025 22:34:29 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042caf2b8891f94ba9fc27bd29a189798e2ef479ba36a0c18a73d572416d561`  
		Last Modified: Mon, 08 Sep 2025 22:34:32 GMT  
		Size: 751.2 KB (751221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f46203fd350d1583fd70da11e31c6ded4dbea6fc02875e81e86ff89c94cc26f`  
		Last Modified: Mon, 08 Sep 2025 22:34:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661a34b04f8fecd40871176cadeb3b401c6bc6199d1c978dfaee026365106cb`  
		Last Modified: Mon, 08 Sep 2025 23:10:38 GMT  
		Size: 20.5 MB (20535218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8bbba8580898cc66339330532ef818eac5d277291555b53b7d5b0e4a7aa896e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a826a99a5ed60bc9a89d5458b4ca7c8f63441de3f2edf36e98b7c3a93c5357f7`

```dockerfile
```

-	Layers:
	-	`sha256:99784fc768071f71c862186e14f5d6b807065f8261ca82fb939dad7ea97f58c7`  
		Last Modified: Mon, 08 Sep 2025 23:02:18 GMT  
		Size: 7.3 MB (7343971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:131acc7a8d58758b6888a9b577ccd56916102fddf75b83f1146141c1317b8807`  
		Last Modified: Mon, 08 Sep 2025 23:02:20 GMT  
		Size: 49.0 KB (48986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:c4bab5a3a8f3dc10963273f67236da80fc0e03070e60febf0d391ac834acb706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164953891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d645e7f6f766494fab61ac1137765ec1afd773f2156f1b048f15b494349f4c6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265835c6b0c6f546efdfa654161b9e25681e872a1640c780e2d4ada1f0e0b6bb`  
		Last Modified: Mon, 08 Sep 2025 22:15:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f639826548f2d17c437e56cae04907d144132bcbb7726112da73b31bd2561ca`  
		Last Modified: Mon, 08 Sep 2025 23:25:30 GMT  
		Size: 86.2 MB (86244526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1070c22314e8ef77db96b0bc805e71dce9fb19ee317b7688a2169b81f87ac247`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253dfd2c4de60ad18a3ec650762f7ef86b4decde6c283072dc6aadcaad41a3ae`  
		Last Modified: Mon, 08 Sep 2025 22:15:52 GMT  
		Size: 3.8 MB (3751971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d3a459a98594ddf704f25da5fe47023ce119d7d1381b225a1bdfea601f27db`  
		Last Modified: Mon, 08 Sep 2025 22:15:50 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6b6475da858e0355e449d738880986efb6ec8351a9d01c1783f213d6d702bf`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b1837ddc5b5a4a228429fff6ea28601622a0ec1b889cead410d971a8056b2`  
		Last Modified: Tue, 09 Sep 2025 00:02:10 GMT  
		Size: 13.8 MB (13800251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3936df574e6c7db8736b764b8b82c2f144c03d85c6171f621e00fcb4ff7d7bb9`  
		Last Modified: Mon, 08 Sep 2025 22:15:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1119a90885d69c5e93e7a63eb35b6f57b3e54bc1cd22f771efbdaa22454c7e`  
		Last Modified: Tue, 09 Sep 2025 00:02:14 GMT  
		Size: 12.3 MB (12286437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddcb354beabb6951f9e826654519e634f8bad09c5500460cc0646aa35b2434`  
		Last Modified: Mon, 08 Sep 2025 22:15:54 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1483818509e0b83235821413a52c03884044989f4498847c364cee8d4e9547ed`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76ca7d4109bb641ba473f60e4d2f8214fefabea80abf1c4963451e0cf1f3af`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f73c8025d8b324d78a2b45ce48f97932840b786a30cdf58724ec8c5882bbbc`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c557af04d697974c368110bcc813091225b09966d3afa4b695db599e0951bd`  
		Last Modified: Tue, 09 Sep 2025 04:06:16 GMT  
		Size: 1.4 MB (1370173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef0ab8299021cddeb45a12d23f5e8e60e4bfc171bdfe7577cc899c93dff4ff1`  
		Last Modified: Tue, 09 Sep 2025 04:06:16 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258bef453526d89df7e783dde7dc9056b8a7d1b623cd04e56241a1ccb11eb0f`  
		Last Modified: Tue, 09 Sep 2025 04:06:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ee4e9720327d570102ca065c2ebd8f99d47911021e88a914c710bd80ee2811`  
		Last Modified: Tue, 09 Sep 2025 04:06:16 GMT  
		Size: 751.2 KB (751224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb78a4c5ba44193c67e21801d276eff2d91fd412cbbf695167013c022bfb8b73`  
		Last Modified: Tue, 09 Sep 2025 04:06:16 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c168fdc98ecc615cbf1e337664ce65aeae639360cb28c59e6df0a15e09a75`  
		Last Modified: Tue, 09 Sep 2025 08:04:34 GMT  
		Size: 20.5 MB (20535052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a12d797e6fcb1bad1a01e84fb3ff265598311f8dc5a4271caf19c6bd2e669f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf6244c1770000a64e9ddc506eb0d22c128768cd4263739976f9bbd1a50866`

```dockerfile
```

-	Layers:
	-	`sha256:d2a05dad6d25d996c866aef40d1a9d22defa384385f4dcd1c7430a3d3b2d310e`  
		Last Modified: Tue, 09 Sep 2025 05:02:13 GMT  
		Size: 7.1 MB (7147980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228d409c1b62fdf000347906de4f9c6f9d67d98f49ad731da85c4f2e49823ad1`  
		Last Modified: Tue, 09 Sep 2025 05:02:14 GMT  
		Size: 49.3 KB (49280 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:e39049087cbeb2d092e4c161bc3b4e24b192718a4e4e3426944dd5effec2cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195171533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41451bc31e1fbca1b1a5cdc66bca8a68b33033dee73328d7a1d8fd7020903d86`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8322ead2329e20fea95c9b42cc630b2e296fdc1be7c0a945dd9756761b30fcb9`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f21d70fc47f1001c4dab1263e0b702249cd83981798a7dfbf38db44cc05e01`  
		Last Modified: Mon, 08 Sep 2025 23:01:14 GMT  
		Size: 110.2 MB (110161609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb5da4c68249ce4e0539da7c30fe5e83a2e2904a8b015920bb751a66aaf16d7`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1999a48a51e9470f04f5e9cad054491a8e90cb0673e1bf4bafd53334af69fd`  
		Last Modified: Mon, 08 Sep 2025 23:01:09 GMT  
		Size: 4.3 MB (4302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca931ef4357a40a78bad7f82b0013a75824fc00305b085f770c5e0d7f7c011`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5f1f76fc870ba3910e31663668f7bc64926c8d7af46411b75a372185df4fd2`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8efda0126892b1b23a5662df785c53bb1064953e5851cdcd230848cc5d692a`  
		Last Modified: Mon, 08 Sep 2025 23:01:11 GMT  
		Size: 13.8 MB (13802365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742943ea7d3b64ffa767451eaae477c13e35b2c4215376e1807c8c6484c29f1`  
		Last Modified: Mon, 08 Sep 2025 22:07:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff912bf53cf9b95e13bdb347bced80f097275e80f5a1a2c87d92d62c25e883`  
		Last Modified: Mon, 08 Sep 2025 23:01:12 GMT  
		Size: 13.9 MB (13862886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485dda12ac66fe87846978ad4d9c689d64f2ff5e7eb5bda315d1a3028084d69b`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decbc90f8ed388aeda9c323a48d2d55a870bfa53ab7a1c2ecc4c257784abb2f2`  
		Last Modified: Mon, 08 Sep 2025 22:07:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde986434e48a12519f3d0be5ddb4cd2671fe2a2bf61d3ea390e904a5ff299e4`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5794f93a3680d8c26e36cd7542e84237805c268d3599fe6e09002e1d05c8b60`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a372f494023635a65ef43ca450356d4382073f66c7efad8338e3703d115330`  
		Last Modified: Tue, 09 Sep 2025 02:04:59 GMT  
		Size: 1.6 MB (1613330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9e1ed8e4b46c4f75c62013c733cfed22e3e24db19d97373ca214b15f40708`  
		Last Modified: Tue, 09 Sep 2025 02:04:59 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bf582d329acaf67a184af99ae16bda35fcd5a7824c660e991a182003122e11`  
		Last Modified: Tue, 09 Sep 2025 02:04:59 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec5871dddf89eb1039bc774329a0e4ebf76f37558cfee534290b688f74c8ba2`  
		Last Modified: Tue, 09 Sep 2025 02:04:59 GMT  
		Size: 751.2 KB (751224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424d93bc7cc92f52b4f4cec239b9da8af38beae0bab99eb04d522a86885deb44`  
		Last Modified: Tue, 09 Sep 2025 02:04:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f4b27eb7add1a3d8aac877a07288d25661ddc7e8d611e1b535bfa1e7739448`  
		Last Modified: Tue, 09 Sep 2025 05:02:10 GMT  
		Size: 20.5 MB (20535003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c8ff9e9ab50f9ec311336a4cf478fb4ec695178a68f98a60a8047b19f343a81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f46d63fe0d6aab90004ae5a4f587e77bb2747a9a54a8f8f70d0de442f50f4ce`

```dockerfile
```

-	Layers:
	-	`sha256:58295001e2c56518e5c75115a61bfa2db8c85685a89be55218ea55fee20de1b1`  
		Last Modified: Tue, 09 Sep 2025 05:02:20 GMT  
		Size: 7.4 MB (7441513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7589c05bdb9049a09ca0c0380bfd14ee051f633b7a14a83ec03f360bcf7c34`  
		Last Modified: Tue, 09 Sep 2025 05:02:21 GMT  
		Size: 49.4 KB (49401 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; 386

```console
$ docker pull drupal@sha256:a54f9113acf887de4f6017bfef14f016845d7c292a11050a5dfda5ac6db94393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203218497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4d62d2e1a3b5260dd8c04284fe46a8806fae37bd93bbed0cc02b026224a532`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4225137003d1bcacb0e653f0978721d379b8731a3c5635b2b839cf922222800`  
		Last Modified: Mon, 08 Sep 2025 21:45:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a44ba101a3f1f659bbe7b9d11cf92ecf51ab36fc3be31114936b0b450b00b0d`  
		Last Modified: Mon, 08 Sep 2025 21:45:40 GMT  
		Size: 116.1 MB (116136657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d50f4ec40c0d4ea14cb49429c05958b79f69e569d0ce4c05b89836e1f451841`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c27d3890a30b4d7f169831ee39d0571236a91743d034a5118f3cbe0d356ce1`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 4.5 MB (4455424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfa7cfe6c2d6a15b83917061a55bfb482e70f1acb3d15e82ec983e8ac298805`  
		Last Modified: Mon, 08 Sep 2025 21:45:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e100ac99b229f76451db30665c91d7a3e9527e1cf5592f04a8580db9ce05687`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b1547189d1095f1b0aa681e5da1999d70df7da2c0f6b42c756dba1a424f20`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 13.8 MB (13801579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a0ce0b68ed8955d09112e02fd97154d1909961f877adf103581f33a81bddd8`  
		Last Modified: Mon, 08 Sep 2025 21:45:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f1f95fbb387c821fb78fccbc90e6ee3cdb046510b1864c168d8db2a2331a10`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 14.5 MB (14506296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441607364f140044b9b0604067562c150dd938a2ea8e7ba90217b4e51d6f7376`  
		Last Modified: Mon, 08 Sep 2025 21:45:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e08a54e2c185f5797f5601e639ebf31948002c05a6b7522b6d3d1de78302230`  
		Last Modified: Mon, 08 Sep 2025 21:45:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6b71ba005ffb7f5a455d6978e6bd283760be19b83af3e643e2108f82ba1baa`  
		Last Modified: Mon, 08 Sep 2025 21:45:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f04abbd5a5d34fe24d91121ec4b5f1fde14d822a265e9b2f3000df55585b79`  
		Last Modified: Mon, 08 Sep 2025 21:45:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76db42997691f5b4e1ebca1133d40ef18fe1d95206b0aa6ac776d32506ee4cd3`  
		Last Modified: Mon, 08 Sep 2025 22:49:00 GMT  
		Size: 1.7 MB (1736061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e196f2995dfda96a7820ee88f5f9acef4b3fa52b586532e41097325913b1cda4`  
		Last Modified: Mon, 08 Sep 2025 22:48:58 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6cc7cabf59706b42c3053b13a183afce096639a624b93015f05197774a5df2`  
		Last Modified: Mon, 08 Sep 2025 22:48:57 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a9dd174556c138b4f108c9250253d02f8741a8559f753ce2a0d2197872c7e2`  
		Last Modified: Mon, 08 Sep 2025 22:48:59 GMT  
		Size: 751.2 KB (751223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b9149f40bde95e6379b78ebeb223a37700e01a40f90dc0aa7823da7315515`  
		Last Modified: Mon, 08 Sep 2025 22:48:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6875717e277771ea47ed28be05354c7a185e7467d4cf77ad986080e50c1084`  
		Last Modified: Tue, 09 Sep 2025 08:37:03 GMT  
		Size: 20.5 MB (20535065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:eb2f44e3956c5e1bf504a6062b2d9fdd20a0ad2abf06d40448e423273521b269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8027a275e0be0122a859acc96a4bd935a07d6914f2da04cc77d86dbafb8d3b2`

```dockerfile
```

-	Layers:
	-	`sha256:d638c9b1e0f3fa6af943f4f777f683e25d8b7d5da837bf51246f927e0fcaf024`  
		Last Modified: Mon, 08 Sep 2025 23:02:36 GMT  
		Size: 7.3 MB (7317723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820d608dc8133e24f9aae2e2855005af2781ca18e7498899043a43c0f8b1b224`  
		Last Modified: Mon, 08 Sep 2025 23:02:37 GMT  
		Size: 48.8 KB (48841 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:d7e14113301f852906da4aff8e6347af34d2dba0cb93208074f4a0c1c44b5805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199621962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df923521d5136e1e858eaeda0f3ef71ef7e29fe8b8e19ea6e13a852b573bf75`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb5a7c2ec964eef33815fc315209dc7259500f176c00afeea12dce7c2622677`  
		Last Modified: Mon, 08 Sep 2025 23:13:09 GMT  
		Size: 4.9 MB (4875556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133daf04d0a4d1719a190dde5b767dcf5cb67060f9891ee35f0f786a618e0699`  
		Last Modified: Mon, 08 Sep 2025 22:47:21 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8262f8dc896e13cd1eb8cc0b98965b00768f23f0b8b2ca4eb70fd73e0c4d3`  
		Last Modified: Mon, 08 Sep 2025 22:47:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf25697fb6bfdbd5424548fbeca4744847a8d58ac636a4d28775fee6407c289`  
		Last Modified: Tue, 09 Sep 2025 00:31:11 GMT  
		Size: 13.8 MB (13801785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b5e19757db5602bc483a4d04e1c32c659ef248ea767716a0a80de66b240e57`  
		Last Modified: Mon, 08 Sep 2025 23:13:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6c2e690bcfdaeef6bd218a2788874d89ed1ebc55349aa2466b83ee0c866477`  
		Last Modified: Tue, 09 Sep 2025 00:31:04 GMT  
		Size: 14.6 MB (14615098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec3d7f05c4b3c2e8bb2c1a862c51497d3f0bf801576d6ba136cd4a21173140`  
		Last Modified: Mon, 08 Sep 2025 23:13:04 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc50f55aba3d2763ffe6c07333f0d405a4c5d43887bc9fe9b98901460ef397`  
		Last Modified: Mon, 08 Sep 2025 23:13:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386245b07b2e744d4a37ddd66185f8acf818288f71a0991f060ac78b44861059`  
		Last Modified: Mon, 08 Sep 2025 23:13:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351954998dc0d91ea9da2e41d4f4a232e1c6e3518d28ffb3d600e67a2cdb16cf`  
		Last Modified: Mon, 08 Sep 2025 23:13:16 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d61a31070d0ea83176c0b3bfbd0cf7495973e07a5f031671624dc47c21e743`  
		Last Modified: Tue, 09 Sep 2025 15:33:37 GMT  
		Size: 1.8 MB (1845486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda8fda9d8cf3bdb40f7ac1b6f1f1b5d5018b1f3a844c59f5fa7c8694c554d7d`  
		Last Modified: Tue, 09 Sep 2025 15:33:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7ab77e7d04ea7607d4740b8d1cbffc2b79efd429c016c289d7e54c3b08fd3`  
		Last Modified: Tue, 09 Sep 2025 15:33:37 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f35f8b6aab12c7799ad9be67a62f68a36a2f5c041285b22e316aecbddf4b79`  
		Last Modified: Tue, 09 Sep 2025 15:33:37 GMT  
		Size: 751.2 KB (751230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c30abe689bc4c9742110dfb5044712bd43538159f317b8a66c49b32a950cd64`  
		Last Modified: Tue, 09 Sep 2025 15:33:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baef71e4c6b1e925db0793c9c9e50d14122bdf979ba78f068066dc70f3e7099`  
		Last Modified: Tue, 09 Sep 2025 15:33:46 GMT  
		Size: 20.5 MB (20535359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:0561d50fb7ccbb4baf20cfaedef277596c026af7db5230792d521ee12519d5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4d87b8ee9b249d68f9cde2010926a42148e182cad24e60d36438b7f67dd517`

```dockerfile
```

-	Layers:
	-	`sha256:987910670a7b787487c9f440dc81373eac9e38df7c77fd8393add23077df768a`  
		Last Modified: Tue, 09 Sep 2025 16:58:19 GMT  
		Size: 7.3 MB (7343916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50bfc99d365755808df1a1c90c9fd2f1fdc3732228b953f0976a43f287e8da7`  
		Last Modified: Tue, 09 Sep 2025 16:58:20 GMT  
		Size: 49.2 KB (49166 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:ee840e5127531cbaed0d9300a887b823357e68df4b1be56ee519b20f9114ef25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebddc2f9f3da8cc605196279dc4162e4d57586dcbb87ddd770fa2d2d146f29d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae3e77da310b8f6abd1c47c2c908b688364ff453788dffc1ea3755bda9a618`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25a2ea3673eda57f8891f3fdc7a2b5bd7baa28ce076ff3427218ba02258d5f`  
		Last Modified: Tue, 09 Sep 2025 20:58:30 GMT  
		Size: 146.6 MB (146579169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd9eb164bef808ab9cc8b8afd7d2a60572baa81f3ff4c56c34d90a36945fb1`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1d685c22b2a71e0ac90af447b986ccd452c8bf3b3279addf81fabe668d6190`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 4.0 MB (4026102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3b33f48477a8d3d6159781343071903515e9a5e4e3a498f12132dc4e16087`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31a861095607a227987a9645651b2b7a18d0f30647655179a2cb5c863f10929`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe095892ed2a96e9c482cc864543bd6bf675307856a60937682551bc7dec452`  
		Last Modified: Wed, 10 Sep 2025 00:03:43 GMT  
		Size: 13.8 MB (13807860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6231221c79cdadf107836cfbca51538af63e5bf13e4cde6a9a3729af656078`  
		Last Modified: Wed, 10 Sep 2025 00:03:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd15111580379d08fb851e9731ad2e5ac774a9205a3b2298d634ea9282d536b`  
		Last Modified: Wed, 10 Sep 2025 00:03:44 GMT  
		Size: 13.7 MB (13653038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33589a4a6c2211faefa734772f12a79c9e507e94516cc7d568880a32bb1c2bbb`  
		Last Modified: Wed, 10 Sep 2025 00:03:42 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b19ca26e3315855cc8396cc11d8b84e85603c8c051cc74cb534b12416f1a8b`  
		Last Modified: Wed, 10 Sep 2025 00:03:42 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0dbc57a0754529885604d698cd7430c231ac1520608828b9490f21d79f6c0`  
		Last Modified: Wed, 10 Sep 2025 00:03:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e32ac90ddf0b03aaf941e2baccd12cdd88075cc182110251cd9435435ff9ab`  
		Last Modified: Wed, 10 Sep 2025 00:03:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ed6858547acf2ab6193148aedfaeb8fab52cfdbaee5750dbe7fedc99720772`  
		Last Modified: Fri, 12 Sep 2025 02:41:57 GMT  
		Size: 1.6 MB (1572507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756df016a27d184b6aba888cdc1ee25aa73704f264db57565938726b44ba8596`  
		Last Modified: Fri, 12 Sep 2025 02:41:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b9626d663b9512e312191c0e5b4add6c11b2a342b73b4912e2df604bd321e`  
		Last Modified: Fri, 12 Sep 2025 02:41:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bad73c2e619faedfac91d639a9f27c1fe613029802d2a173ee2016f9fa39ba`  
		Last Modified: Fri, 12 Sep 2025 02:41:56 GMT  
		Size: 751.2 KB (751230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abee26d4ceea7217aca183435892f8bd6431ab4be29830c9375c265042c67fa`  
		Last Modified: Fri, 12 Sep 2025 02:41:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd0b172c857a290e8ecc9bb46eda430605cf6b0871c755af60cdbb40c19fd4`  
		Last Modified: Fri, 12 Sep 2025 02:41:57 GMT  
		Size: 20.5 MB (20535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:42274885ec44b438cba10d79217f5bb6499f36fc9a064f105a4d44e5035fe036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa542259fbd98c98f2bd4ab20ace49fa2e1586ca26011f89f7e5182c32dc8d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8a6cd7e039e4a4e5846fb448ce19a80d06d550ec25a433181e7f6e565fab50`  
		Last Modified: Fri, 12 Sep 2025 04:58:27 GMT  
		Size: 7.4 MB (7415913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dca7f552b29981f8cb5ed1d640b080648e04dfa11e9191db8b5d3b410888e9`  
		Last Modified: Fri, 12 Sep 2025 04:58:27 GMT  
		Size: 49.2 KB (49166 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; s390x

```console
$ docker pull drupal@sha256:5e3902610015b4e06ab173bef6963954058f618780e13a433e21a623a928fb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177771299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214b848d525dfb92a5ee521ebe26db65e6f8274113f39086328106fb003f2763`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 12:46:41 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 12:46:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 12:46:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_VERSION=8.4.12
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Thu, 28 Aug 2025 12:46:41 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 12:46:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 12:46:41 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 12:46:41 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 12:46:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 12:46:41 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f633efb1bb21ecc579e196bca25f5ab7d52d7c2db3ee2a067ee60f0f9c012`  
		Last Modified: Tue, 09 Sep 2025 00:03:06 GMT  
		Size: 4.3 MB (4320437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c2cf9f6a014fa655f3eb4189a487c63fa210b55a95d802554be23b3bcfe1cf`  
		Last Modified: Mon, 08 Sep 2025 21:55:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bab93bff6df540c8c28fd0c65b5629bb7a3784cb5470795e60ecbef3aa18f1`  
		Last Modified: Mon, 08 Sep 2025 21:55:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a32247c136962f87d4bb9cfc6d04d5391f1d7b5c679e697ccb55cfbada5e6e6`  
		Last Modified: Tue, 09 Sep 2025 00:03:16 GMT  
		Size: 13.8 MB (13801047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40cbeaf453969a938342b917a017452beadcddf4173c452a34c2e5d6dda7802`  
		Last Modified: Mon, 08 Sep 2025 23:09:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277a59dc383a6180065b14cc9a55f80b4edc944b51511ea6f58b8371d0b5d240`  
		Last Modified: Tue, 09 Sep 2025 00:03:21 GMT  
		Size: 14.3 MB (14286851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed92dd1e39f892639a717d3d802a91053ead63afca8d75ec862d79cf43ebb835`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f2cfdc08a5ef1bf2757ac62c4d2142c8a05e248501c92f7dad8683aa5e505`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585529ba1d3832b70b49a4c94e6ac3808fcd0c23546e3acd489648ad581402d`  
		Last Modified: Mon, 08 Sep 2025 23:09:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072a5bc23f318f9cbfe78907ddb70bcee13cd75f536ae5b97d6ad9831ca655e7`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adb70cefc91c1bc39a21e7d03aa6fd2525f28f38cf679b8ecc05bdcd008e61e`  
		Last Modified: Tue, 09 Sep 2025 11:48:36 GMT  
		Size: 1.7 MB (1674815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c9aaf77661fef33262e824a4a5892a210c1674e8f80d236d728fa19326cc96`  
		Last Modified: Tue, 09 Sep 2025 11:48:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a14997757fca798991206d528dd1f0c95e195da050c2bbd81d2abe0f580c8d`  
		Last Modified: Tue, 09 Sep 2025 11:48:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0881d68d46baa058a72aae4ddcc70cb11c19a4860726ee016be1db982576cc89`  
		Last Modified: Tue, 09 Sep 2025 11:48:37 GMT  
		Size: 751.2 KB (751222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f5ba5427dbe83d6c0f226cf81d1b0eb85774d2fe3f1a707a57280922458f5a`  
		Last Modified: Tue, 09 Sep 2025 11:48:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f48545e26deed3a8c475dfbd4342a3f8dd2621d2a8e2c55191da2f90b5bdaf`  
		Last Modified: Tue, 09 Sep 2025 11:48:40 GMT  
		Size: 20.5 MB (20535103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:ef5a9ce31f40beddb1b57454a24584bf0833f701b1c92cf97b9b67650f783704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea216ec2999cbe612029afff5ecd0249ccb497c0ac6e5b4de5ec919c4497c609`

```dockerfile
```

-	Layers:
	-	`sha256:c6647b0e5412d22ab04087a75c80ef7dd5933b1b548f8fb813e0e2eb17d8a00c`  
		Last Modified: Tue, 09 Sep 2025 14:01:30 GMT  
		Size: 7.2 MB (7161221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86bbd5a8f99fc6037c0124b390351c88bdbf2980c4323d26c7fb282bf4319982`  
		Last Modified: Tue, 09 Sep 2025 14:01:31 GMT  
		Size: 49.0 KB (48979 bytes)  
		MIME: application/vnd.in-toto+json
