## `drupal:php8.3`

```console
$ docker pull drupal@sha256:47ff6ce991b86f979e0eb6c3122b281bf8a141b0bed5f8fb8b6c69c22dac1eeb
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

### `drupal:php8.3` - linux; amd64

```console
$ docker pull drupal@sha256:354993283a8c7d229af8b5dbe275cdaa9292340c9916d065012ba1da9f7ab85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199594719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653564b62f70692f18b60bf1bea05fc4c55e29497ddfa2ca495c582c64743731`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 07 Jan 2025 21:30:09 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 07 Jan 2025 22:40:54 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d208fc26c5bebc10a4454c9c705658bf055bb4722c051d05d5f1f181e883e820`  
		Last Modified: Tue, 07 Jan 2025 05:15:05 GMT  
		Size: 2.0 MB (1999763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67175f05ae6b5ae864f779a08e411e70caba731873b4bf2a684b7d60602b536`  
		Last Modified: Tue, 07 Jan 2025 05:15:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3d4f6c8dedebe4f569e172383eadf62d22cf0fca46808e4596e44d3b824685`  
		Last Modified: Tue, 07 Jan 2025 05:15:04 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46326b06aa9a789584eff4ca80085951e352615d065dca5798a2957661999096`  
		Last Modified: Tue, 07 Jan 2025 05:14:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcabe4b0eb02b7e7f84c700183ad5d373e8046a96dfde7a0174f6187bdfb2007`  
		Last Modified: Tue, 07 Jan 2025 05:15:06 GMT  
		Size: 20.0 MB (20035035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:d70080aecc218e0dd074bd31ab65000677f7c7796e432a248870f1cd1244a795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6901882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50323122979255140803205f37868e8273fcb47fe6ca5012b3dce5a7350bf0f`

```dockerfile
```

-	Layers:
	-	`sha256:49a289954e2983f1ede123ad7c33c081b346b9b767d3fb617aa57d75ffe01d84`  
		Size: 6.9 MB (6858989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d725ea1787ee27f7c94f3f3359d3327a8344f90d7bc621d7870c0ec46fc3b3f3`  
		Last Modified: Tue, 07 Jan 2025 05:15:04 GMT  
		Size: 42.9 KB (42893 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d163d2f557047ef409216d7314f4877b66aab5827573417456a4a67732a6bf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163589825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035b115d9df4beedca07b55582b803c6adb48fce4fe6b5234262ce4bc309d45e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371487cffce8356bcfafa73641fa9f2323f8772bee294bab86eafd60098c3fa`  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4642677cc143257aa73de7964d6b5cc5b6060d2a6edb9a5ddd3be8f1945443b`  
		Size: 76.0 MB (75969024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc80a55774350869ee992b98dcd86030b72390bb6be124ca4de61219527683e`  
		Last Modified: Tue, 24 Dec 2024 22:46:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a47f58182addfc006a08b0f176b99027cafa95cbb11bd8c2a67cea998652ef`  
		Last Modified: Tue, 24 Dec 2024 22:51:10 GMT  
		Size: 18.9 MB (18857375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489299adde02364094cf7b587949e62efb94af380c86790375890e5970e48964`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f182d84621ff8030b0063e0c13b0e085d2c01da0e1058aaf33a38c64516b003`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af623922dc14d16cf50e56974bb1e3cb3b67c906b20fb6615703191f59f1891`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 12.7 MB (12651212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fa5845cf9b2e054d723ce873b43b0df1a1b73ac935ab518a09bfcb89227e62`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33116d28723c3b7ecd43e386fab9ad2ec37059cb09b985ae39a4372c3428fa8e`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 10.0 MB (10040894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e623219990fd2786a56b9432297efd7e3f2a33fe5c3dd899fd95e7782bc03c2`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7f050c053f206f521698efc9960af2c00935517287c5e1f1953b5b3b338093`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0d64d0ef6d25c998562031fe27ca1661e4b4fba40993ffdb05affa19d857e`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd416511799a21e50b9dd0281a60dfa383b3511409120ff1ff5d65dfed3c07d`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 1.4 MB (1355033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d546ef738e2ece6110ffabc3eca773c0b5fd7c4bb3d7733565305db3cc6f34`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df356092af2185fa7894c7b2e676ef55035ccba9b4e151e0d74e37429f200aef`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 742.2 KB (742242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04bc9a16c854dec0b59db1b9585f553ef30cd62945ca4ed99063264b1687fa6`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7183c88e96f70ad279d5d538211b88ceee72338198ca76e35e603440c2133bb9`  
		Last Modified: Wed, 25 Dec 2024 13:05:26 GMT  
		Size: 20.0 MB (20034635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:29ccf8b6d83f5ee556e3dcd5b9d5ed4d34d7767acc6c71a8a72254e96e0af2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f7cfccc176d96b51163a6e34ac657851c5b3a223460f125530d32ea776d5f7`

```dockerfile
```

-	Layers:
	-	`sha256:2111fe9b4a9192acad8adf17413b1db93601e1d2856fb74d997d7bbe63d73f19`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 6.7 MB (6674119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84a9a56196b3a4500d6c5ce18284b1234bd5e95c2b57a4068fb8ec9d6953d4a`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 43.2 KB (43172 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5263dcc9211893261b8979f5e0c197620488a6183a0aa9bdfdd880749e35e207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193456113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd533551c0666ac0696d14576885ca9c34ebc22de17208244bce9ee34975832`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e78c77837824251aace1541825d6601923f21e2ee313ee9a52a38ae0a505c2`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 12.7 MB (12652941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c5b3307a6d2076daabb4f5c018ebae4ef009e3efcbcee963cb714557e50c6`  
		Last Modified: Tue, 24 Dec 2024 23:39:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8326c89bd989feeeeb960c54e281d47c971efa9bf65b6fa1de6e571f0c5a9b57`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 11.6 MB (11645033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de671d24a51145bc481e0dc81541df0b172584690dd3d56daf9966853393abba`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ef53cc750aad9f3f053519758a892eefe7f61ae19ffd2b2f1add65b9e8df32`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe0df954404086f024b3660bc6719b221414982771d88556a71f01c0756342`  
		Last Modified: Tue, 24 Dec 2024 23:39:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8128cd195cdc58ffcead38e9b5b3410f49bcbce892fe763e62722cad0984a5`  
		Last Modified: Wed, 25 Dec 2024 08:15:58 GMT  
		Size: 2.3 MB (2259217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972d55a8c3f1fceee50979eb71256714900d10e5859bfa20ddc428e0adfd3c9f`  
		Last Modified: Wed, 25 Dec 2024 08:15:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8399ffc8b3ed8f5e4217a257995bda009615760ee078c23c39abd0817744`  
		Last Modified: Wed, 25 Dec 2024 08:15:58 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce290691dc269052ef5c043788e4fd914dbfe4d9f23be9e006128c00f791a9d5`  
		Last Modified: Wed, 25 Dec 2024 08:15:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b2ca4e488344a522f949e5c63dde2d5f189da008c9e6db7690c1f9080ef452`  
		Last Modified: Wed, 25 Dec 2024 08:15:59 GMT  
		Size: 20.0 MB (20034923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:7a807d30a78d8f3a22b673cf6f1d0e08529441f293fa8bb0b4c42451ffad8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4020a579b56f66165766caa11a6c7c53c444c552f0a6dffb1ba10e8a51617bb1`

```dockerfile
```

-	Layers:
	-	`sha256:55173f8d4a7761b13afd66c54d8214afae70fe38e9ef9d7a4f54fb9aa1eadb51`  
		Last Modified: Tue, 07 Jan 2025 18:46:44 GMT  
		Size: 6.9 MB (6887641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a449b7e0a95ca0085aa26938cefda7e23e089f8d24dedea6d1db350ea5da7d2e`  
		Last Modified: Tue, 07 Jan 2025 18:46:44 GMT  
		Size: 43.3 KB (43288 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3` - linux; 386

```console
$ docker pull drupal@sha256:e688e3680ab01c85fd4c7b8bf8541f08afa00c4e3a3de4ca0d15c17467e031d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6603a93b557b17c9e83c98ac44985b7c559caaafbab93959b213757e9aa62f6b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91aca5ecd07a667860fbacfbc18bc013c64a15031e39a35cc4cb1be2a881488b`  
		Last Modified: Tue, 24 Dec 2024 22:23:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598c524770fdbee7aac6a45782cf12c270bb2c79c9c583c0f9ce7940557bf6dd`  
		Last Modified: Tue, 24 Dec 2024 22:23:23 GMT  
		Size: 101.3 MB (101319423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500420220e69d0ce5fcddf0b89b9e9c068b9132a7aefd4c53fe08fbb500c223f`  
		Last Modified: Tue, 24 Dec 2024 22:23:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a111359f392b10e17a4a2ccc293f907788326216c4fda8d4d85474a04556d09c`  
		Last Modified: Tue, 24 Dec 2024 22:23:21 GMT  
		Size: 20.6 MB (20638435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd8b0134d908b75468f099acb1f65d2dd11f9d251b548e8debf6a1282719198`  
		Last Modified: Tue, 24 Dec 2024 22:23:21 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823edf4d918697c1fb88391c3c31efb3b0c49d8faa37506eebf732430d08a0f`  
		Last Modified: Tue, 24 Dec 2024 22:23:21 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbdd4d4abbf474c9e6cd7a8ef4c90ead2fb5b6a3cca7c0331d26ce347caa7b6`  
		Last Modified: Tue, 24 Dec 2024 22:23:22 GMT  
		Size: 12.7 MB (12652243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f973562f23584839772bf988d36089217de744fcf4000d5fb26af70d532167`  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f99b8408905d384cdf5baca48fab8b5edd53dda41f3f1dba53d541266ac1ac`  
		Last Modified: Tue, 24 Dec 2024 22:23:22 GMT  
		Size: 11.9 MB (11868877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbe62a2f17cd92723115e406650557e0f3a9d4d50c50b55e4df9ac28410dfdc`  
		Last Modified: Tue, 24 Dec 2024 22:23:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ac6e72dee56076a541ff4d37041863dc960bb43d9307a18c6fdf79d307743`  
		Last Modified: Tue, 24 Dec 2024 22:23:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646735f5dad6e105b3116dd08beefe691bdaf3ba3e5529cf32511d9de80a3ccf`  
		Last Modified: Tue, 24 Dec 2024 22:23:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fb18a42744de49a310c36c4f0708b40f768460abe24a1f5aefd5a49f85f61a`  
		Last Modified: Tue, 07 Jan 2025 05:14:56 GMT  
		Size: 2.1 MB (2052411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad1382bae1ae5d815de05cff63429765ea1922e80828c01aa685e96a2bc9a7`  
		Last Modified: Tue, 07 Jan 2025 05:14:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f304402e1c74e38b56558c3cf256b39d57ac73824b0c3fcfa8aa82dae236e936`  
		Size: 742.2 KB (742242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4244d457ae45f42698c2383356a9c087f33798d4559bbf0d7112c9d551c7345a`  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d1b080ef45ee98f2cf95c377be01bf7f7575810b2f942b13332027591f6de9`  
		Last Modified: Tue, 07 Jan 2025 05:14:57 GMT  
		Size: 20.0 MB (20034453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:7f67897a961755ea76eba966028f54fbd2954b850245d286cd6c534e205aa326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6881911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9f9aeb4d5f6afc812a520f4af5f0c682aa9dfe0f498234140f5c0f30b0fd21`

```dockerfile
```

-	Layers:
	-	`sha256:30e31b12c9a3fa24218e52f1bade231e01bc6a884ccd96e29312107bf4d46eba`  
		Last Modified: Tue, 07 Jan 2025 05:14:56 GMT  
		Size: 6.8 MB (6839160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28da846431d151b4dd7780d021ca8223da33f6e90867fd07d620214cd5e2c6b`  
		Last Modified: Tue, 07 Jan 2025 05:14:56 GMT  
		Size: 42.8 KB (42751 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3` - linux; ppc64le

```console
$ docker pull drupal@sha256:56b8ce08913699b5fe6719412c8c8dfdb8c2a7c9e356c7b5b0b6b5407d1026f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203858231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1025f254090c82098df0352841e49c967a74bf627c96aea787dffc2cf1daf4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d132df684634db62d3c01ce1613d6eb2566301af85c63410ac30f024166112ae`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd875cb56d0accafa903279e20e2f4504ccbb9a52d3356e35159318d6e6cac86`  
		Last Modified: Wed, 25 Dec 2024 04:36:04 GMT  
		Size: 103.1 MB (103128544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c503622cfce9dd90835f8eb52e082345bb8d299e64a5d12507cacb0203fab6`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc535b192e7a86a518e6f79725942e51c09ecbfe2b3a18e1ac7ba323d04859`  
		Last Modified: Wed, 25 Dec 2024 04:40:54 GMT  
		Size: 21.3 MB (21308315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144b282eeec3a288e4659f298308f4f6703eec9b9e924a1bc18380740166116`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c966348685f6c718513b59fe339b4bee7adf696c1a64b706b268a42add51d3`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29d50b4f1e285c244e4324c36587ef40c6303dace73509d894b84ea80bf9fcf`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 12.7 MB (12652618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22adf2d96b60ab542db7a096a3bb2c3195157a601383fad623fc6367053c47a3`  
		Last Modified: Wed, 25 Dec 2024 04:56:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37f1b1d57f37110f81d4a078f8175054eada4816fd5fc09315c50a6e3b1eef`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 12.1 MB (12066812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa57954973561f716294764feeb9d66eec42853a91c104738ed2bef1a9b1a89`  
		Last Modified: Wed, 25 Dec 2024 04:56:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c8375eb0a20f6d4a36273848105cade616c208a30abbbb68569c6be0ff36`  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2087b80ff4dd0882aca3215f601fd961c2ab1d6afbd56b38847577668b07be9`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2ccede99bc11a157ddc7c8c61379d22d3d68be08847419567fbbd0bac015a`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 1.9 MB (1855974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f9edf99c58d90c4a2d2bf2a8f12d854add7386600806456e06a6c68925dd4`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290eca3313b4114059e49a88f6abba71b3b3d0aaf745977c8c38ff61073179f5`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084dd00d6aa34e0f1c07405cbed0df9ff7e1a8eafad46e884fea656f6b705f62`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce568da5a1d2c5dd2fdd59d0841601bcc727a86b566ad37cc1ab2a5bfc904b7d`  
		Last Modified: Wed, 25 Dec 2024 09:48:06 GMT  
		Size: 20.0 MB (20034575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:8eecaa5a2f989c47cc96c12ee0cf18d8e2922cdf92f4e8c91853c3587731fde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6879195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ab2ef2d226bc79913b4df44753038f663844500d38368387383d7cd668217`

```dockerfile
```

-	Layers:
	-	`sha256:187573b6e59a354497168884ab53eb8f412eb75c4d8987f237694e673d4e7e6d`  
		Last Modified: Tue, 07 Jan 2025 12:01:34 GMT  
		Size: 6.8 MB (6836123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469763918f43686eefc50d06876f46eb54697c2a45e6faccef96ccf3814f6959`  
		Last Modified: Tue, 07 Jan 2025 12:01:33 GMT  
		Size: 43.1 KB (43072 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3` - linux; s390x

```console
$ docker pull drupal@sha256:cbbbd834abb37ebaa9c56bb8bf690e9fb77897a5cf9a72ac02b768e5cc0e5bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173257630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c164c5dc7290a81a9ef5b932cb9d15fd361b616257ad408fe9c4775f957bee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Dec 2024 22:27:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Dec 2024 22:27:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["apache2-foreground"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00cbfa93c448a5709b2ab89b4eecafcf312bab962f82f649a898256b58523f5`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457328e6b14be13d9f88b508b5952998504e5014f0290e6e1be39897bab54ba4`  
		Last Modified: Tue, 07 Jan 2025 21:30:30 GMT  
		Size: 80.6 MB (80624323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9339c0eb88e9961929bd0005c1c4f86104f98d5884f539ed8d91ef9f169fd7`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47fb800ea78c724c59025d5ac46e9c60dea88853ca2b4ae21855f62533c1a76`  
		Last Modified: Tue, 24 Dec 2024 22:54:21 GMT  
		Size: 19.9 MB (19895315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd195bf1bc34d371e309aeabf0a6d8810a778544fb754738ceebbed7152b26`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc4a7840b6ec52c065ff2d8ad71af54e6267fa1bbca2329da95e751d55ef9cc`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400d26f2f55018b7e7b0bbffdd3462b86f62449aec1bc9013517df4f60215c96`  
		Last Modified: Tue, 24 Dec 2024 23:09:45 GMT  
		Size: 12.7 MB (12651596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb15368ec111af0f656249c9045540822eb93e74689511313971471f8871cee`  
		Last Modified: Tue, 24 Dec 2024 23:09:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27911a224835a99e6f020384734fc6bcd8794b421d63b7af081a51de72ccbf`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 10.9 MB (10871221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62abd26f3d7b459ed85116be0fc8678c6dd16a65f900f22c87570fd1129001`  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe609398dcdb76ffb760305a258f951c538099c6f6e28f10c76461cd3431e31e`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50956637c0d421cb78660bfff0559b28f257bde9283040f193d89dd6f1bbf82`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317ff096b48d6e6bd7f00537eee8017248f3e194f6177d6b4413c73962e4ce0`  
		Size: 1.6 MB (1553579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf83222a8dad654d474eeecad0abe92b8d495e58113b491db8fd429bd250b`  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eeefaf6bae6d8de5b542cd19c5d00859041b215a2ddea7cee47a9f33334718`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 742.2 KB (742242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6616f16b7bfdf84109d2e79a74eb71e2e47b6cad1a3ca3aff4291808c0c863`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e46b72e17556a957e36af5e3b9e2f73ecd58417f90854e083575a7666731e`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 20.0 MB (20034545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3` - unknown; unknown

```console
$ docker pull drupal@sha256:65ada104406350ddbc56f9e0b207150d5388068348d805907fb469ecd65cebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6743299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7364e9a5b05f31b108197be6dd98453f04469d5ce02cb967bad0fe4abcd816a`

```dockerfile
```

-	Layers:
	-	`sha256:43f83782d11a57dfd7cf0848e95d10c521d676d4fa55222b44942c68013d546a`  
		Last Modified: Tue, 07 Jan 2025 19:25:28 GMT  
		Size: 6.7 MB (6700413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d26859d16af66618bb4b6223259bb5aade4dfbf7bcd08c4231b006c05f8bbee`  
		Last Modified: Tue, 07 Jan 2025 19:25:28 GMT  
		Size: 42.9 KB (42886 bytes)  
		MIME: application/vnd.in-toto+json
