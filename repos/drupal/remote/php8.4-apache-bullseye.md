## `drupal:php8.4-apache-bullseye`

```console
$ docker pull drupal@sha256:f7fb2340c958919e68d15a7b4603f1d18e92168ac1b9cc48b7d4a5dc44068d71
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

### `drupal:php8.4-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:a00dd067c5be7ef1c1eb6c4014ef1860badf3b7f56551f080eed8aa0b7bf75d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198349662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e7ed2c367ad46cb39892790138f0cd4e12aacc7df78200d0056f4dd9f704a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 23:47:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV DRUPAL_VERSION=11.1.8
# Fri, 06 Jun 2025 03:57:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:57:18 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d425376ca8328988e808d5c5a27bcd419b7deb0508a184e290239842133fac3`  
		Last Modified: Fri, 06 Jun 2025 17:42:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ace0e2f7760ac531c63ca55ad4e365aaa249a401b3f40f1ab48c6771ef0f6`  
		Last Modified: Fri, 06 Jun 2025 18:04:45 GMT  
		Size: 96.6 MB (96588014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0902086b4300e5f9e9515135def7b69cd46c3a616a8ef2ebb9b1314e7e2b20fe`  
		Last Modified: Fri, 06 Jun 2025 18:04:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4195836dded4d93afc032db1a1dc8885ea9b56dc1b61c0c595906d068e7db4`  
		Last Modified: Fri, 06 Jun 2025 18:04:37 GMT  
		Size: 19.1 MB (19064051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e70f0759cdf5f936252e61ca7e3d543040b9c502a8796b3332840586d4a718`  
		Last Modified: Fri, 06 Jun 2025 18:04:36 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c66588ae2bdf58c771703a47b952dc0b2fbdc4747990912c7377e1d2f00ca2`  
		Last Modified: Fri, 06 Jun 2025 18:04:35 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9fee506da95d3fe47f26dd48e8529dcd4257a2bf30e1f6b1351ba7df9ff3e2`  
		Last Modified: Fri, 06 Jun 2025 18:04:37 GMT  
		Size: 13.7 MB (13744956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b0b536c4d8a3aae87c29618311bf6db1d2b6e8b52533fea9fcf400092ccafe`  
		Last Modified: Fri, 06 Jun 2025 18:04:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a007fba3a60589936ec3f09a047f0d3a7ba7298f2d80d4cc8b3ca2c9e89dc1`  
		Last Modified: Fri, 06 Jun 2025 18:04:35 GMT  
		Size: 15.8 MB (15795671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83501e18659658e367da69e769fcbe2574913f1d3cdd5fef221288f5e5e10061`  
		Last Modified: Fri, 06 Jun 2025 18:04:33 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111b0994d4161de55b7164e3a56633e7483c5443017679fbfba8033f33f62d0f`  
		Last Modified: Fri, 06 Jun 2025 18:04:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a003b0854be0cd33c62174c1a89a6c52af56fae9db37f7f1b10793b98d5c8356`  
		Last Modified: Fri, 06 Jun 2025 18:04:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde0d4c73ef418490b30e4db452526b5dd1c377eee87b79f2f25dcb496f83a66`  
		Last Modified: Fri, 06 Jun 2025 18:10:46 GMT  
		Size: 2.1 MB (2064501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0edcb99ec4967ba2196a25effd2324421779bb9b986e1c606abc264a857fbe`  
		Last Modified: Fri, 06 Jun 2025 18:10:50 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1fb7859191edc5d994517351f7d52061cb48d92b862a59b1abf96b28782c6b`  
		Last Modified: Fri, 06 Jun 2025 18:10:53 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c72b62ddace0444b967d14fa67dff39e20420b0dbc32c6fabfc5c6d556c1a`  
		Last Modified: Fri, 06 Jun 2025 18:10:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56a97f437d0eb4f755ed10c571fa3ac64c3bf932d426f07af1f75aeedf2843`  
		Last Modified: Fri, 06 Jun 2025 18:11:04 GMT  
		Size: 20.1 MB (20077868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e1b1ddede0a4769c0a81b39b60b91003d59258d09bb49faf630a165762e36d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48492ccc09bf8d47d0c52d7ca3fef38444057569d88303dc0de504c945f16c4a`

```dockerfile
```

-	Layers:
	-	`sha256:dcfde868a3ceb8ddb760f6d5886f305d6509b44bd9ba9716c75b06c210241464`  
		Last Modified: Fri, 06 Jun 2025 23:15:58 GMT  
		Size: 7.1 MB (7078084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c23238b16aa4c4b2770248cfd405c1c42c0f1eb90850924a8e25301d086e2bb`  
		Last Modified: Fri, 06 Jun 2025 23:15:59 GMT  
		Size: 36.7 KB (36683 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:878311dcef0c4275b02596e16d503a772361770531ef914e2f76db48b1fbdc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162167463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b44ece3a74e3cca7973adfa4d2bfb9fc251eabaf5c088c00fdb3f1f260faa31`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 23:47:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV DRUPAL_VERSION=11.1.8
# Fri, 06 Jun 2025 03:57:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:57:18 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d9c98f5407c517a6c82e3d633185a6d76d2f1a1b173f8c84e8d09194a0047`  
		Last Modified: Fri, 06 Jun 2025 18:08:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174dd4c330a5cb2b275c9367f976035c4e9a7870c5bd8dfa239ede951528cdd9`  
		Last Modified: Sat, 07 Jun 2025 11:44:11 GMT  
		Size: 69.3 MB (69326451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b71238feba8c542154b4c87407bfbfba4330ed0b0c64c3f18e02484c87476`  
		Last Modified: Fri, 06 Jun 2025 18:08:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b2866468df76c8f23b86c6f9ea4b2b38f94eb9343d0d7f352d4382d36bd757`  
		Last Modified: Sat, 07 Jun 2025 12:05:42 GMT  
		Size: 17.8 MB (17817550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273e51f04d91ef2cd8e161ebf289529ebde809b416532c18fc9b20d76b96784`  
		Last Modified: Fri, 06 Jun 2025 20:50:01 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d81b85a4c7605624890a6f4d58d2353c920c335651987605b5cf718d5ab013`  
		Last Modified: Fri, 06 Jun 2025 20:50:05 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a66a8f9c229936e0b2a45159ea4861ff4692abf2fbc60db59dc9d0c633c8ec`  
		Last Modified: Fri, 06 Jun 2025 18:08:34 GMT  
		Size: 13.7 MB (13743416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b547d6522e4488ba0cab8b96f90db81562333ab3e6e76dff42b87db922ac1329`  
		Last Modified: Fri, 06 Jun 2025 18:08:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1edfc7ae64d2aea2a2fe3cf5423af425a360745b7950da2b254e5c8c5ed9b01`  
		Last Modified: Fri, 06 Jun 2025 18:08:45 GMT  
		Size: 13.6 MB (13579724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e940d9bc92f0474d4d6f323f4cc401177457c44e3f90917d51b5eac04e963a`  
		Last Modified: Fri, 06 Jun 2025 18:08:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db5c154dd779d88030d793805742b4e44dea2ffc64dc9b657ba0484f67dbef5`  
		Last Modified: Fri, 06 Jun 2025 18:08:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6801b0ff99bace8aae6b4ba7a7e96da6b101528b684b7009c41592a5ae50e4ef`  
		Last Modified: Fri, 06 Jun 2025 18:08:33 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2228e80ee2a21746bd3b8a854643e275984da8db70a3ba7f388cebe6708b38`  
		Last Modified: Fri, 06 Jun 2025 20:34:57 GMT  
		Size: 1.3 MB (1320100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d2eb34510068db3aa677738e9607164b0ed72aa723b6da9c139faeda41a8f4`  
		Last Modified: Fri, 06 Jun 2025 20:34:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35429844c1ccebf69a3c36e430ed8c77420a8892a08e24e8e6e5761a768537a5`  
		Last Modified: Fri, 06 Jun 2025 20:34:59 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa394935b760241d971d45c1b26f90de20a33db9fbd619169de12424ddda4a`  
		Last Modified: Fri, 06 Jun 2025 20:34:59 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2764da861c9254b76c1af6715f6535cde117530d04a7eb7b0712d23fd7fb36`  
		Last Modified: Fri, 06 Jun 2025 20:48:54 GMT  
		Size: 20.1 MB (20077642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:07086a1db98b0883c1ef19bd9b602a3239e64b1cfa4c72507584b0c79d75e83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6922981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b6e3998270d5c2259c54a11336602f8dda393c97a52a0b9e565aaa85f29c44`

```dockerfile
```

-	Layers:
	-	`sha256:32a84ddb6ad10b69978c9f0cb63c367e02c2a852773cb75183b1bbb7a530e332`  
		Last Modified: Fri, 06 Jun 2025 23:16:05 GMT  
		Size: 6.9 MB (6886175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:422f752584965d563389d89b72581f114d657b571b5f49fa485cdcd92c9cfe24`  
		Last Modified: Fri, 06 Jun 2025 23:16:05 GMT  
		Size: 36.8 KB (36806 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:97a60b48b811df6ea74ca60fd0436e0bc0e1119e0cffff0d561c47c333027463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190716841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699067d8641d16c7d5fc01e0c5d8113e725217c7b648fc0a89b4b474c1f2c7cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 23:47:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV DRUPAL_VERSION=11.1.8
# Fri, 06 Jun 2025 03:57:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:57:18 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172ab386f3db13cd04f5ecb5a0ba3663a0da50f1f5f0f595a69b8407b39bd73`  
		Last Modified: Fri, 06 Jun 2025 17:57:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58f900c2f78730779b376264aab0a750a2b59069fedc8057d2bd990c5bd534b`  
		Last Modified: Fri, 06 Jun 2025 17:57:38 GMT  
		Size: 91.1 MB (91096803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eae96444bf9d20f4dfcb4f600754dc44a40935ef5c9bcfbb19f7e4d3e9241f3`  
		Last Modified: Fri, 06 Jun 2025 17:57:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c33ae52242bcfe0579c357f4a60c82043aca3008332f4d7427e07a52267206`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 19.0 MB (18981738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f87cbc9a1d9252b24d3d7da6d375f912d058439e6aaa1779c1f49c679dfb2d2`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d448e17840e5dd362808de65c14a7e839d2477e2aae43ee1ec46755fd1760e3e`  
		Last Modified: Fri, 06 Jun 2025 18:00:37 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcb95dc977cff356d8723cf0459478f91cdb2c36085a7a3abc98ad15a166628`  
		Last Modified: Fri, 06 Jun 2025 18:00:39 GMT  
		Size: 13.7 MB (13744301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7dd8305271b3a6164f0927e715894fa8605ec69db62b41bb71d4ecb2e869d`  
		Last Modified: Fri, 06 Jun 2025 18:00:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0729c8b406aa8108dc81b8eec8453cfb7d0bdffee291499118217dcf4c92cc78`  
		Last Modified: Fri, 06 Jun 2025 18:00:40 GMT  
		Size: 15.3 MB (15347981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e5be021c334993afb14d16c492afd1e62370cb7f0440e8b3ffa59a6c27db5`  
		Last Modified: Fri, 06 Jun 2025 18:00:40 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940feeaf8a187ee4326a61222f7a7701754d9b2f2f953e42b3f50cdfd284b813`  
		Last Modified: Fri, 06 Jun 2025 18:00:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d904416526612e7016b4bc6323b20bfa755baf6e00a1ff68bb56bd450e5df92`  
		Last Modified: Fri, 06 Jun 2025 18:00:41 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf57ef1817a0dc0ae2266e619ce954822fa99e6a46a2d539ade9a64f9b6302d`  
		Last Modified: Fri, 06 Jun 2025 21:09:38 GMT  
		Size: 2.0 MB (1962708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76604bda89367e5e8916493e5aeebe33b9cb148e5c876db27dc34bd2520f0be4`  
		Last Modified: Fri, 06 Jun 2025 21:09:37 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6071a5d5bf128ce86814473f076e56f5511d2a27e4bac11d52e23be547c9f545`  
		Last Modified: Fri, 06 Jun 2025 21:09:38 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d95dfaf5aa09f4c78e092ded0e581843cf9fab90af88beaf6e807a06367c8c`  
		Last Modified: Fri, 06 Jun 2025 21:09:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54bffd9e4769cc3251813d8c8c4f49494f8280802fd3be5845dcfa143f08c89`  
		Last Modified: Sat, 07 Jun 2025 12:07:55 GMT  
		Size: 20.1 MB (20078382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:25c78429672a01644f4682f05c252c937dc63b288226f9e8ba804b9de2985fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7117433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12816409203d71fc294b2b821f89c9416fb448e198f33c77bdb6385c3a256b3f`

```dockerfile
```

-	Layers:
	-	`sha256:bd69238fb3b6845298e8d1828451943e6bbbcbc4883a310c1bb414bfb4eb4339`  
		Last Modified: Fri, 06 Jun 2025 23:16:11 GMT  
		Size: 7.1 MB (7080590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7155c5651980d84adc2a69d19b11ac7dba8165f82fedc8401d9f7320399233`  
		Last Modified: Fri, 06 Jun 2025 23:16:12 GMT  
		Size: 36.8 KB (36843 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:a037969f10ef56e197115f3e3e55909e14c2698ae0301fcc881c5eddaa127baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200825008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7aa118729aff4ce692edbc4142ec2fc7fd6a075a863717359c221db74691fd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 05 Jun 2025 23:47:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Jun 2025 23:47:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV DRUPAL_VERSION=11.1.8
# Fri, 06 Jun 2025 03:57:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Jun 2025 03:57:18 GMT
WORKDIR /opt/drupal
# Fri, 06 Jun 2025 03:57:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Jun 2025 03:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af661afe6c76e16e31da3e2720e037bdcde864849f6c66c8e848da488c341e51`  
		Last Modified: Fri, 06 Jun 2025 17:39:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9f1cfba119423746d2594007e3e41a4e03729cab8128641970387ae645a766`  
		Last Modified: Fri, 06 Jun 2025 17:39:59 GMT  
		Size: 97.2 MB (97242667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f703019f225628d672701fe19cb769b375fef172d5b9c67a96852f1db1e0f`  
		Last Modified: Fri, 06 Jun 2025 18:08:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc398dcf1f9df4e6b25941284e3b76c3e35ae602081aae9fbe154626d37af6a1`  
		Last Modified: Fri, 06 Jun 2025 17:39:55 GMT  
		Size: 19.6 MB (19553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efc2d37257b0d85b04d2e7acf9c3d86b26078d919d265f7d7836f7ea55ea1`  
		Last Modified: Fri, 06 Jun 2025 17:39:49 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097ac89bd9c15759abfd8eb17ee59f55872aa36162a03510214abf288793ab54`  
		Last Modified: Fri, 06 Jun 2025 17:39:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd3f8277082fffb637711fc03b785e4ba9fe799c8275adf8916db431b922f04`  
		Last Modified: Fri, 06 Jun 2025 17:39:53 GMT  
		Size: 13.7 MB (13744341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b70fdc3258e91a952a8c915af6024dc5feed0fa48c55f824004d66702a8c571`  
		Last Modified: Fri, 06 Jun 2025 17:39:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250d470d1b6ade20bfccf884a36d9a898a302495001e56d6f8015a15c0de207`  
		Last Modified: Fri, 06 Jun 2025 17:39:54 GMT  
		Size: 16.1 MB (16091687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb0b90e542ce1b8f1c00301dcb7ce8ac634c027428b234545f07a586287ad48`  
		Last Modified: Fri, 06 Jun 2025 17:39:51 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3a6cf9d2419eba8b430155123832a0b41e31e843987f5530112f6f188e4e8e`  
		Last Modified: Fri, 06 Jun 2025 17:39:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8615f127506d89c873509c2dc97bc93bce523b49cf9eca6466e7834bd0da44`  
		Last Modified: Fri, 06 Jun 2025 17:39:51 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196068f4e9c4af5facf68cfd3933462123ef18cae3b6d9ffe175426bd456c819`  
		Last Modified: Fri, 06 Jun 2025 18:11:37 GMT  
		Size: 2.2 MB (2167496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e8f30f400c8487f0507ed9239ddd83f1b3d94a524945bb41a7f701e8ffe4e`  
		Last Modified: Fri, 06 Jun 2025 18:11:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4280a3fb518c4dadbcee04795db3e3419efedd49d9c00ff0637301e034097b8`  
		Last Modified: Fri, 06 Jun 2025 18:11:32 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb8474a16261d935b03d74fb9f7cac7e145325cf712af05b40f3d308537b84`  
		Last Modified: Fri, 06 Jun 2025 18:11:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafed69f9d3c08c73a48ccd6a2b6db6e74946434defcdbc9caa097c99e5134d8`  
		Last Modified: Fri, 06 Jun 2025 18:11:35 GMT  
		Size: 20.1 MB (20077957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:94fcccf4c01f4228af200b1d641f47cf2bd5bf33a3cf0848820b61ae9e1043a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7104849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6ebb6a6c73a41777c954ad253e81281b8ede0836fb9e76c0b2a97ccda8ac26`

```dockerfile
```

-	Layers:
	-	`sha256:aebe507ae8d141083d5896f8f38a900aa9c6692c7108b41e2747cabff1734bec`  
		Last Modified: Fri, 06 Jun 2025 23:16:18 GMT  
		Size: 7.1 MB (7068209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b32c26c29734dfec45f6cd7f2956a69a4a870dfeea93a5ed142ea70c36cf5829`  
		Last Modified: Fri, 06 Jun 2025 23:16:19 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json
