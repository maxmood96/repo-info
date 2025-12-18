## `drupal:latest`

```console
$ docker pull drupal@sha256:4c0d004045c5825edfccd78760879f332855c8e26fb99121c60caff400c2977e
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

### `drupal:latest` - linux; amd64

```console
$ docker pull drupal@sha256:8737123c9f0da5a132ca75e3fc57c21e86e3ab537de8df8f685af46d2a89002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202933439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a935dde2aec9ae0450512f7e3436ab294b0df7c39c07e906f22ba26487f5ffe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:40:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:40:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:40:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:40:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:40:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:40:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:40:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:48:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:48:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:48:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:48:14 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:48:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:48:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:51:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:51:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:51:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:51:04 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:51:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:04 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:51:04 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:51:04 GMT
CMD ["apache2-foreground"]
# Wed, 17 Dec 2025 23:30:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:30:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:30:46 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:30:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:30:46 GMT
ENV DRUPAL_VERSION=11.3.0
# Wed, 17 Dec 2025 23:30:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:30:46 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:30:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:30:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614c05582e091fb79450c5f9c2d1f6ab2e50ca199fedece4a12a4bd279dcb7a`  
		Last Modified: Mon, 08 Dec 2025 22:44:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a87700c50c82328f1e0287dc1756da15b5765523086f3f64a9b2751b59015`  
		Last Modified: Mon, 08 Dec 2025 23:31:30 GMT  
		Size: 117.8 MB (117837165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459e9d1aeedba5e764240422ccebd54585c95f5f8b2fdbd40e46b1d8d629ca0`  
		Last Modified: Mon, 08 Dec 2025 22:44:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b0eb6ac4874d70b386e16f16887eac6b487449f479dc8fd8faccfc89e1b72f`  
		Last Modified: Mon, 08 Dec 2025 22:51:24 GMT  
		Size: 4.2 MB (4224539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8992f34a94ce734a5f436e95d62987f232f07ed74b76289b55a813f7fe23da8a`  
		Last Modified: Mon, 08 Dec 2025 22:51:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0753f47822acb1ff10cedccc2ae1392ae1b39241bc3344eb3c5035f02b629d`  
		Last Modified: Mon, 08 Dec 2025 22:51:33 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f866e2f8d6a368b246e14fb6fd7f382334787b9e5e2c3ef751e000ab6b1e2773`  
		Last Modified: Mon, 08 Dec 2025 22:51:25 GMT  
		Size: 13.8 MB (13818940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b48018c5666f01a52157ecc91733580514d77c1323c49e1f2fceac9edab5a1`  
		Last Modified: Mon, 08 Dec 2025 22:51:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0615f10c9847eec8d1a3a34223268a951fca60e86a6ca4c50612af4c33772f7`  
		Last Modified: Mon, 08 Dec 2025 22:51:25 GMT  
		Size: 13.5 MB (13533322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d17cb806608606401ee31b9c28d6085bc1eed8f78ff95f7dff915a7836006b`  
		Last Modified: Mon, 08 Dec 2025 22:51:23 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87189c1074b4d2c677216eb004ae91c562e874ce489e56b751e7b0e7957d71d`  
		Last Modified: Mon, 08 Dec 2025 22:51:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9691ad3b25c5123a70b1a33c30ea77fb44f422c39d20b31d1c66389f77d731f`  
		Last Modified: Mon, 08 Dec 2025 22:51:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0d4cb98a2e7c89047c3ea8696e5057c5f803f13c9c0718cb6b27c6de053ee`  
		Last Modified: Mon, 08 Dec 2025 22:51:24 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4513baba35803a26811d8b7e465ab3378352c5223d5cac14e5fa058d8ddda3`  
		Last Modified: Wed, 17 Dec 2025 23:31:16 GMT  
		Size: 1.7 MB (1657311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f929166503eb6686a82c19ae6e9a02c34ddd9fcf547a0837abe0cd7714d2de9`  
		Last Modified: Wed, 17 Dec 2025 23:31:16 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1a92995e5c46c13423907b0cd647a40d802dd7d58054ecc81dc573e490d252`  
		Last Modified: Wed, 17 Dec 2025 23:31:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94753501b16b35e84ab1747013cc1ba73a6b0d71fb8a1ff44b39aeeb350d63d7`  
		Last Modified: Wed, 17 Dec 2025 23:31:17 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b1587d56f23ebaa5b954a7dfa8940fc74bc727c64b57124c514ddce1d3ed0`  
		Last Modified: Wed, 17 Dec 2025 23:31:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4b5e993a1d0b2af6b281c14c2f14c1da64db421721d6976f964dd63113b5d3`  
		Last Modified: Wed, 17 Dec 2025 23:31:18 GMT  
		Size: 21.3 MB (21301249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:a2fec225b238e7f0e86aa6c41c2713296638db055c981d3787d08f9864a07232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825de23bf4ad9fb3ec2ad28785b9311811a52619856fae2c2eb1000f1c83e522`

```dockerfile
```

-	Layers:
	-	`sha256:33dc89afb1799f0ec36a461853bedbc15fcbc5808e2220e34e19b17f02fe3920`  
		Last Modified: Thu, 18 Dec 2025 00:06:13 GMT  
		Size: 7.3 MB (7341989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea33c386bf7a1eca57ca556ce66a622321281b7be6064f0d558aa7714aaca70`  
		Last Modified: Thu, 18 Dec 2025 00:06:14 GMT  
		Size: 48.8 KB (48787 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; arm variant v7

```console
$ docker pull drupal@sha256:05f4754ba8621e78da330ecde34c6e340cda279122a93a8100dabe7e7cab60ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165091035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6ce9dac5aa84bcedac6d0b2bdb5dcbadda66236ffe15d41611922896ff7ab7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:41:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:41:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:41:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:41:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 23:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 23:01:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 23:01:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 23:01:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 23:01:10 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 23:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:01:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:04:08 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:04:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:08 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:04:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:04:08 GMT
CMD ["apache2-foreground"]
# Wed, 17 Dec 2025 23:32:05 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:32:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:32:05 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:32:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:32:05 GMT
ENV DRUPAL_VERSION=11.3.0
# Wed, 17 Dec 2025 23:32:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:32:05 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:32:12 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:32:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1182b39b0a1f09d8646ce298477880a1f7e4339a0a5475a83c881a2c7cbb95ae`  
		Last Modified: Mon, 08 Dec 2025 22:44:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77487e815ec77698e3c4679f7ff5bf65e70a052363a854972b4908868f1a1f60`  
		Last Modified: Mon, 08 Dec 2025 22:44:47 GMT  
		Size: 86.2 MB (86246306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8eac7845632e051aea62aad22599f2ca8e9f717c5f20070b3925d7fc49233e`  
		Last Modified: Mon, 08 Dec 2025 22:44:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ca9a6dd82ef20348bf559367795d60d3f26a7dd39ca64bd7d14320350f596`  
		Last Modified: Mon, 08 Dec 2025 23:04:29 GMT  
		Size: 3.8 MB (3752461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8af100258a69c78442f1bb30ecb8d48d008d8dc16101eafa35d7186e76248e`  
		Last Modified: Mon, 08 Dec 2025 23:04:28 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd27f51957148a7064d31b8698fc5efe90ad5c3c38f127bde56c9cfcfb38cf85`  
		Last Modified: Mon, 08 Dec 2025 23:04:29 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58330a27118b9088468e0b27d1b0bf2168e45273693518002fc77945b767ce`  
		Last Modified: Mon, 08 Dec 2025 23:04:34 GMT  
		Size: 13.8 MB (13816566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a4da913615ffa87daf7c405f59093076b8a3efbb3f32c8121bd0356661b19`  
		Last Modified: Mon, 08 Dec 2025 23:04:28 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b549847f618d6ab8cc14f41ee1472057512247604493bb9c6aaaf32db0c01ebb`  
		Last Modified: Mon, 08 Dec 2025 23:04:30 GMT  
		Size: 11.6 MB (11609256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb003f7f82035222429389250baf771ae0a5542bfc5b4c21ddef55b392632c`  
		Last Modified: Mon, 08 Dec 2025 23:04:29 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0e61abf190d99e37d4914eab5d8dc09515a75a5d9ac9d926f2555e56822ef`  
		Last Modified: Mon, 08 Dec 2025 23:04:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce1098eb27a374818d24142060502535002402fdbced938911bc99446460b9c`  
		Last Modified: Mon, 08 Dec 2025 23:04:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f539eb8ece54501309435874113ac8a5d14ed375a6e58559d58d8d4e506275b0`  
		Last Modified: Mon, 08 Dec 2025 23:04:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76211662b4cd6210cbd97d425a216afba4600845f708ec5155bdc4884599714d`  
		Last Modified: Wed, 17 Dec 2025 23:32:36 GMT  
		Size: 1.4 MB (1370610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503829c21bd4709624fde5192fc8b1d5b9b0bc03ad780818a1aa04302b150d43`  
		Last Modified: Wed, 17 Dec 2025 23:32:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9417ef8e47f2ec41aac55715c6359f0d14d09db986b8ef59f3e0168756fc9853`  
		Last Modified: Wed, 17 Dec 2025 23:32:36 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a1295c4b1018e65f999b1de6137821f150b11fe6a27d3a4f63c9a063d9a1e0`  
		Last Modified: Wed, 17 Dec 2025 23:32:36 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c076e86400d92da76015ea4249be6e24fbea18f94c4f90f864467539190ce6d8`  
		Last Modified: Wed, 17 Dec 2025 23:32:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fefcfdf163d50d62e50af910daeed9ff0aae899ace8e61f0015e71c2eb69af`  
		Last Modified: Wed, 17 Dec 2025 23:32:38 GMT  
		Size: 21.3 MB (21301413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:501b08975ec57c3f6f2f7df6599172a3118f28899a03a10653db59089bb6e1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff688a2a98784761d6f694c4f9f4ef1eb1bcb607731e2a23ebf876986cd5d3f`

```dockerfile
```

-	Layers:
	-	`sha256:29bd1704772156493405836b798394ef2ff6613d3e8f8c2c81b108e81c00c63f`  
		Last Modified: Thu, 18 Dec 2025 00:06:21 GMT  
		Size: 7.1 MB (7145998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac02949b2a3c3cc2abe6672bc4e361179bf2b1f95131dc308477d65145355fa`  
		Last Modified: Thu, 18 Dec 2025 00:06:22 GMT  
		Size: 49.1 KB (49080 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:419319adc0d480e405f8000157b3e02f59875345e7e5fba600a2d2d1353c9214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195309791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e444242d31630f7350691c26b66ccb6692c3bb51ee2931915f3a18124bd666ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:39:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:39:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:48:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:48:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:48:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:48:06 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:48:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:48:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:51:19 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:51:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:51:19 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:51:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:51:19 GMT
CMD ["apache2-foreground"]
# Wed, 17 Dec 2025 23:30:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:30:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:30:27 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:30:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:30:27 GMT
ENV DRUPAL_VERSION=11.3.0
# Wed, 17 Dec 2025 23:30:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:30:27 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:30:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:30:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0bf3bb21220442b3346d851cb1b212d70eab67d32540fb6e475450e1f1a2a1`  
		Last Modified: Mon, 08 Dec 2025 22:43:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbf1baec87c4ef9433181d8f9d28e9d4ac6f7a28e1c252bf9396161c39dea98`  
		Last Modified: Mon, 08 Dec 2025 22:43:23 GMT  
		Size: 110.2 MB (110162590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a92183a4d6d17f00fe908f2388b23e419cdcf0096680d1507f25274a0af4b`  
		Last Modified: Mon, 08 Dec 2025 22:43:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04899eae475eb101855d777131424822509fe8d73576d3e45f64e28723e48e96`  
		Last Modified: Mon, 08 Dec 2025 22:51:38 GMT  
		Size: 4.3 MB (4302245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f4a936e9291a7eb10ca8c26e797d863e28e17ae1ce1ac90a9eba12abfcfeaa`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99305bd9c0e32498634cd5a71ad48cc48947389d6b3e89de4b0dfb285c28710`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8753da925cb62cf6cb7b9070c1159c0cc1ac545391b5c806d49c798f73ef2fda`  
		Last Modified: Mon, 08 Dec 2025 22:51:39 GMT  
		Size: 13.8 MB (13818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5fcde429752cee6b11d445bfd21681ea813001fbc30fc2abac3300c9e2364f`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a48fbe5438f45c1849bbd1f9a1a29e800fee3b81152e4b14ba79402bdcd0716`  
		Last Modified: Mon, 08 Dec 2025 22:51:39 GMT  
		Size: 13.2 MB (13187626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af1a8a68f53c9ea7c8f968e382a030e2617da7898ee626d5f953d0f0b56989`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c42e9da3e552f195653c9ceb5a972fcc0883abf34e74f731fd33af0aded4f`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa2e05d582711b4fb2e7831ffd22bebb581c141fe248d46ace41c0ad5449a6`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f067dbaeee423ae4e1edda8ee93b06c314bad7532cfcb01854cd708fb2de750`  
		Last Modified: Mon, 08 Dec 2025 22:51:37 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1d21eb2124fdf0f0aa237325703f419c312666eb9b07c5f95fe6e08acbfacf`  
		Last Modified: Wed, 17 Dec 2025 23:31:00 GMT  
		Size: 1.6 MB (1614373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5dbcbe264d501971cd1ef7e3766fdd943cb8f2485b5485d7bff0f0a76c75b6`  
		Last Modified: Wed, 17 Dec 2025 23:31:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156ea3d630107638a3acf64c9b5bf454503a2d5afd3343ea502aeeb8f1389047`  
		Last Modified: Wed, 17 Dec 2025 23:31:00 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8eea7e6e6c5b3b43d1b3f61f4b15253e8fd3d40c319de71ce4b5e09226e926`  
		Last Modified: Wed, 17 Dec 2025 23:31:02 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a22a34f1ad1e12b183e04ab9d5537f8f276d20c2fbadfebc7838fad095e1b`  
		Last Modified: Wed, 17 Dec 2025 23:31:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237715310e68e67bf40b35036dfb619723b011c23edc5aa6903351eecc1310c1`  
		Last Modified: Wed, 17 Dec 2025 23:31:01 GMT  
		Size: 21.3 MB (21301358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:25a8a74b18328f8c487b3f75cfdd5d19be965c4d2aedf03c81282933a33c61e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33b954a16582cf0d02ee7d18ac05c5431845b89df4b15338a280d0f904f9707`

```dockerfile
```

-	Layers:
	-	`sha256:5946a397dc36436ee49023c1d769d7d5d05ae84f631ccf2cd447888d7c680f62`  
		Last Modified: Thu, 18 Dec 2025 00:06:29 GMT  
		Size: 7.4 MB (7439531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45fe46c880f81c364f9ca02608d1e2cfa3031f01e4468130da9b1f7a3818881`  
		Last Modified: Thu, 18 Dec 2025 00:06:30 GMT  
		Size: 49.2 KB (49202 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; 386

```console
$ docker pull drupal@sha256:2b90344161111d72a21f120b022e6c9dcee0eedf1bfb7959ac0c94d3cb427edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203357447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a94ca6c216a4cb18b6f04b1b00896c4fe18fb555c1f4532592d0d98e0d0bf1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:36:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:36:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:36:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:36:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:36:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:36:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:36:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:36:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:36:30 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:45:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:45:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:48:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:48:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:48:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:48:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:48:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:48:58 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:48:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:48:58 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:48:58 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:48:58 GMT
CMD ["apache2-foreground"]
# Wed, 17 Dec 2025 23:31:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:31:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:31:14 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:31:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:31:14 GMT
ENV DRUPAL_VERSION=11.3.0
# Wed, 17 Dec 2025 23:31:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:31:14 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:31:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:31:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8de1d77631c6e7656c6eed8125d70b404c7b1b9cd3826a4bc02f36f87eb766`  
		Last Modified: Mon, 08 Dec 2025 22:40:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7446805ffe50e86a2e5ffbb651df582072a18ac9016e04f02f35e3720c0b3d`  
		Last Modified: Mon, 08 Dec 2025 22:40:52 GMT  
		Size: 116.1 MB (116138522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ae555e5a04ea0c558d91253b64d546bb43d2c2d1357b6f65f3e8f48c310517`  
		Last Modified: Mon, 08 Dec 2025 22:40:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed754d109f5add413612e546256eddb9cf43ed566ff9ddb963d154d225c7f2`  
		Last Modified: Mon, 08 Dec 2025 22:40:44 GMT  
		Size: 4.5 MB (4455959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27fdaecdb7234c00511bf689a7a21fcda891ceab387d0a3ad46f84d72a5f408`  
		Last Modified: Mon, 08 Dec 2025 22:40:44 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9b7565c0867d91ebf229c8a5764c3b6b9ce1f8e39f3794397d6506c6ffca86`  
		Last Modified: Mon, 08 Dec 2025 22:40:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294aef8a14ac4f32fb0dc08cac7efb6a312c141d8c3390731bfc671c8cf524a3`  
		Last Modified: Mon, 08 Dec 2025 22:49:16 GMT  
		Size: 13.8 MB (13817931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2e1f6f6bac7af86feabfac09dced1c6374633349de393fee10fb29d5429cd4`  
		Last Modified: Mon, 08 Dec 2025 22:49:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3bf375ec32a915c5b89e320592ae975703229922df265225a22884a0e0c80`  
		Last Modified: Mon, 08 Dec 2025 22:49:17 GMT  
		Size: 13.8 MB (13829421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86b5b606275db7bc8a93c77553ae76a494294334e81ac5d15f663175f043248`  
		Last Modified: Mon, 08 Dec 2025 22:49:15 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b45be779232e076d63aa56c6b223c2e97e1c92eee3290c4f9843780481c9c6c`  
		Last Modified: Mon, 08 Dec 2025 22:49:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb7f65b7d060176f85695940b739d105cbdb816191303d2b2f74942f570a72`  
		Last Modified: Mon, 08 Dec 2025 22:49:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd41a8f402b35a12103dcdf6ee9af26cb1731e622bf2ba94497c9e05864aacb7`  
		Last Modified: Mon, 08 Dec 2025 22:49:15 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644b75ad9fed8f8b7374b26a0914ae5c33cbbf38ef4ae2d5c2d8863036ce06a9`  
		Last Modified: Wed, 17 Dec 2025 23:31:51 GMT  
		Size: 1.7 MB (1736900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52b47c2e35dbfa164d4a8006543d6ebfc8333921cb10a4b6554e2773e8722`  
		Last Modified: Wed, 17 Dec 2025 23:31:50 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644655b669564f318036bf713d6c50d6705a588f1074f29f69cd4195f0ee0473`  
		Last Modified: Wed, 17 Dec 2025 23:31:50 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b58887ca09798180f1a0026faf9209f361f29384739f8b9ebc21aa3afffbb7`  
		Last Modified: Wed, 17 Dec 2025 23:31:51 GMT  
		Size: 778.0 KB (778005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5270d3b0243b35f26eb519b968f8a2a1858aef661d69d49b05826797cf423342`  
		Last Modified: Wed, 17 Dec 2025 23:31:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d938fd2edecb81f4a00e8e5b2c8df48eadb47882e6ee096d198c529a72fd97`  
		Last Modified: Wed, 17 Dec 2025 23:31:52 GMT  
		Size: 21.3 MB (21301239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:02c0e9e2bdf92020448f9281610603890c63cdf8f46e32d00fecc8c25ec4514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5a5f3c9832348c62db2774cb427fefed204938caa7479db38f03d804bc1981`

```dockerfile
```

-	Layers:
	-	`sha256:7c602a360f53de8a01eb602e4ff0c6c59f6e3fa89b45cd98264a8e6bbf49cebc`  
		Last Modified: Thu, 18 Dec 2025 00:06:37 GMT  
		Size: 7.3 MB (7315741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aafe8e7c58ec39e5d844643bad88017342eb1029bc817e37c277318831c4d72`  
		Last Modified: Thu, 18 Dec 2025 00:06:38 GMT  
		Size: 48.6 KB (48642 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; ppc64le

```console
$ docker pull drupal@sha256:da3e9910fbd91cb0d4551895d582585a20f9efe30b0b01e6d91cf74f94da9fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199756201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e6136be27373127ae1b191c9e1fa042b3c9960ad623bf0ace1fef9f27498e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:35:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 00:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 00:36:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 00:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 00:41:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_VERSION=8.4.15
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Tue, 09 Dec 2025 01:13:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 01:13:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:17:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 09 Dec 2025 01:17:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:17:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 09 Dec 2025 01:17:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 09 Dec 2025 01:17:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Dec 2025 01:17:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Dec 2025 01:17:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:17:24 GMT
WORKDIR /var/www/html
# Tue, 09 Dec 2025 01:17:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 01:17:24 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 04:34:11 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 04:34:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Dec 2025 04:34:12 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 09 Dec 2025 04:34:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 04:34:13 GMT
ENV DRUPAL_VERSION=11.3.0
# Tue, 09 Dec 2025 04:34:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 04:34:13 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:29:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:29:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e968a4c552b5d63962c849d9412a26339a7f50c4b8dee90079284c674840b8`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30124c487aeb9dddde3de1f906a208cb9bd0ae4a03d96c1622924a8622e568`  
		Last Modified: Tue, 09 Dec 2025 00:41:59 GMT  
		Size: 109.6 MB (109597911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd51466d9c6ea60e911a8b8d548a3ce159de7cc08df81891f748149917d7196`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cdd7fdbb4f498b6540140a43b62e20227e731c816b54e09c4166f8ff8637fb`  
		Last Modified: Tue, 09 Dec 2025 00:55:22 GMT  
		Size: 4.9 MB (4876044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662dc1d5e5e4a3977cad81ad0301a23d9a7c393028d08dafd0f088f67701014`  
		Last Modified: Tue, 09 Dec 2025 00:47:34 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e1761af690f425f7869d904bbd39508f379bcb057f9a915bfe9e5a5ffac93d`  
		Last Modified: Tue, 09 Dec 2025 00:47:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe51447936073ee9852fbd99f52e808d6c2fc7c68b815ca7fcbe5a759421b69`  
		Last Modified: Tue, 09 Dec 2025 01:18:00 GMT  
		Size: 13.8 MB (13818121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc3eac31f3fcee22ef6e8469e8d0c8971956256ad311b78ed7591df7a50dd8c`  
		Last Modified: Tue, 09 Dec 2025 01:17:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61c0865cedfded34411aa840faf91b35edd94f470bb6053ca801938509b18fb`  
		Last Modified: Tue, 09 Dec 2025 01:18:02 GMT  
		Size: 13.9 MB (13935257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827f8d45c8897e28ce752173f82293d2937caef326337693ab0a6bc4317872d`  
		Last Modified: Tue, 09 Dec 2025 01:17:58 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd61b30427f520d12b2f250b0c644b673ef491d630878045dac63a3696f5ae5`  
		Last Modified: Tue, 09 Dec 2025 01:17:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dacde49d626fc007a483dc52036d1f0ebcf6bc407161aa9301b64d3da39525`  
		Last Modified: Tue, 09 Dec 2025 01:17:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f16168ca8339613b810e1500ac811c9fd04f4bb630dc5dbd80f020b8d22c92`  
		Last Modified: Tue, 09 Dec 2025 01:17:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5dbfe4d325afc7bcf644e144b02be288026f01edf946968c3d033b3678942b`  
		Last Modified: Tue, 09 Dec 2025 04:35:20 GMT  
		Size: 1.8 MB (1846107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5df4fd96643b74839dce1eb6ea598b40690e153ef304fb3b9da1c3ac558c379`  
		Last Modified: Tue, 09 Dec 2025 04:35:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a948533cfe60f299db343f6632ddeffee4fa3b2738a7678a31830827b468e3e2`  
		Last Modified: Tue, 09 Dec 2025 04:35:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24981123ab964b65ad21d216ca9813954db6c7ac90319250ad1ed81c547bf20`  
		Last Modified: Tue, 09 Dec 2025 04:35:20 GMT  
		Size: 778.0 KB (778005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45f41c4307ffee2dd1427c88a910dd67603c97a594fd68f3b2f48a8d2fa989`  
		Last Modified: Tue, 09 Dec 2025 04:35:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623f46395b73b6e1816d3da99ccb23b2a60acf7f120ceb2eaa4e4e50a4e8d3fc`  
		Last Modified: Wed, 17 Dec 2025 23:30:53 GMT  
		Size: 21.3 MB (21301439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:383caa871422c5c0f56f5b89027579146fe77411d3fbefa2ffbf9a8199163483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4b0dbb3532f98457fb2f3a4c47d5cce771dc1a12ca0fbb44394a0266fffbc`

```dockerfile
```

-	Layers:
	-	`sha256:36ff501d2c24cbf63fae95bb3ce879c32db09ceefd50598f8633483a67ea9526`  
		Last Modified: Thu, 18 Dec 2025 00:06:45 GMT  
		Size: 7.3 MB (7341898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a071a867243032bcca48a6d4098b7fcc1d717fc1675a4fd3f59489efd481f9db`  
		Last Modified: Thu, 18 Dec 2025 00:06:46 GMT  
		Size: 46.8 KB (46768 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; riscv64

```console
$ docker pull drupal@sha256:bd452d528187a03a7fca7e16a822e36b1a8f2951a211c999d7a39873048999b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228705583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17b3ae968e77557ee66431e202bb39c8a45d3928f54785419711c4225d5e613`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 08:01:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 08:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 08:03:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 09:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 09:08:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 09:08:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_VERSION=8.4.15
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Tue, 09 Dec 2025 21:14:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 21:14:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 22:08:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 09 Dec 2025 22:08:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 22:08:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 09 Dec 2025 22:08:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 09 Dec 2025 22:08:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Dec 2025 22:08:58 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Dec 2025 22:08:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 22:08:59 GMT
WORKDIR /var/www/html
# Tue, 09 Dec 2025 22:08:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:08:59 GMT
CMD ["apache2-foreground"]
# Thu, 11 Dec 2025 08:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 08:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 08:59:00 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 11 Dec 2025 08:59:00 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 08:59:00 GMT
ENV DRUPAL_VERSION=11.2.10
# Thu, 11 Dec 2025 08:59:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 11 Dec 2025 08:59:00 GMT
WORKDIR /opt/drupal
# Sun, 14 Dec 2025 08:51:42 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sun, 14 Dec 2025 08:51:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53d28a615a791c3859b4a1756ba700dc2c4f69377eb59f2058ba63d00e0869a`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8434337c0c50639ecc5b6dc774986d4e9420e3476e8e2468932a6a85632eb`  
		Last Modified: Tue, 09 Dec 2025 09:07:07 GMT  
		Size: 146.6 MB (146578870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e90ba410db15c99bcf35ee3bbf15863cbe2650207953ae1e912e0e6bf7fda0b`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74b4e149c4738e4a9c37f39d8a642897edbd74a4bf14ea4f27d976938c2b0f`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 4.0 MB (4033863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f674e0bc56dc657de8b096a1cd8ed3c4b0cbb2de5d3a05d6e50989e9b86ab`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c810195650744e7970d6163d3e7b56ea79e2877073201e867cf1c229807a8924`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5be10725e8271cf53bf602be0221e7ec4258d879368ac9e1cbd6acb2051a21`  
		Last Modified: Tue, 09 Dec 2025 22:12:18 GMT  
		Size: 13.8 MB (13833098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257fb37c453608cb782a22fef41cec77c177612b2e1d9622ee257dcfc44e9f45`  
		Last Modified: Tue, 09 Dec 2025 22:12:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a78cd49e6b8d82ca4e1fc82fd84e8ef99ab86aabbb7be5c9558bd5caf52bcc`  
		Last Modified: Tue, 09 Dec 2025 22:12:18 GMT  
		Size: 13.0 MB (12966951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0817032dd9aafe7f21ffb73fde1998c37ab4bf2ab6c81c26d25ff68a6a74d89`  
		Last Modified: Tue, 09 Dec 2025 22:12:17 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f1fc6d0db570ee07431a64f9c8849731e82352ee26712ada6bbf323d2fc09`  
		Last Modified: Tue, 09 Dec 2025 22:12:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edeeb0764b8a4e262352b43bff38f934293d3e7894be3bc62f9651aa0826397`  
		Last Modified: Tue, 09 Dec 2025 22:12:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcd1ff7fa3b860da85a7b5ed435f49a8178202866f4e33327c8a104a5a66ae9`  
		Last Modified: Tue, 09 Dec 2025 22:12:17 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18745968982fc84fcef3329cb3f6fc425e81bc394712ee155a3d7d4dcbfa72ec`  
		Last Modified: Thu, 11 Dec 2025 09:04:44 GMT  
		Size: 1.6 MB (1573613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e5ca42b67cd9495760aebd551f45089009b15581803df70c5c5cb55be1b1a1`  
		Last Modified: Thu, 11 Dec 2025 09:04:44 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc9055ce5c7c412c18113e7e0f65e796917af93266793a29bd345ada4a169e6`  
		Last Modified: Thu, 11 Dec 2025 09:04:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ce2c0cfa9636bdc06902fa0eefbb0a514f5f22fc0f9fc3da7c59b6b3df75b`  
		Last Modified: Thu, 11 Dec 2025 09:04:44 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eb1c215afa7e054f111345dbd4d0006872eb595fe04bf76cc8266ddd5f8fd2`  
		Last Modified: Thu, 11 Dec 2025 09:04:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e36219012ab7959df266ff7a94788d038bbfab309cc85b4cd65392665427dba`  
		Last Modified: Sun, 14 Dec 2025 08:56:39 GMT  
		Size: 20.7 MB (20661596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:95b8eab5fbdf4911a0e909dbba7ede252427aef2cd532cf34a6352d01532ee65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef5e25ea5640a42fd5b2ce548739285edf58f8a3ec2b52d550638da4ff7f1b`

```dockerfile
```

-	Layers:
	-	`sha256:50848946b466a5ff62908d6d414d5868e1f523b26c5cedc8fd8ad4a5602704d6`  
		Last Modified: Sun, 14 Dec 2025 11:57:42 GMT  
		Size: 7.4 MB (7416053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c05391b1a1e7e14502630465c225a005c2aa29ec5e9b5cb12a2d1c9e8cbb9d`  
		Last Modified: Sun, 14 Dec 2025 11:57:43 GMT  
		Size: 49.0 KB (48980 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:latest` - linux; s390x

```console
$ docker pull drupal@sha256:9059c69f6333c0f8df2adf1de3c5486b0d5894fc620f7c4861422bebb99a8e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177600202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417a293e3d228eaff580a5d7ec6195f6426cb96ccde9e040472b803b5f5ab41a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:37:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:37:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 23:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:04:30 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:04:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:04:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:04:30 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 01:54:00 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:54:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Dec 2025 01:54:00 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 09 Dec 2025 01:54:00 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:54:00 GMT
ENV DRUPAL_VERSION=11.3.0
# Tue, 09 Dec 2025 01:54:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 01:54:00 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:28:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:28:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06325ac7d48e9543412848e1fa70a7cb9a579c86f688b2e2e9bd944346590fce`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a4b708d85d9501bc1929ab5cadbcf5d4c4bca40490257ace724e13a60fcbe4`  
		Last Modified: Mon, 08 Dec 2025 22:41:12 GMT  
		Size: 92.6 MB (92564698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d9f5a2f9a70ca9e903eb070a1168477352c4a37bbecf3ddf16c7afe71c0e`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92dc5e34b4915edbdad5123bd5ae0d2c6a40e6471d283ad84545bd68e81f92a`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 4.3 MB (4320856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ee5f503eaad0fe4d32cdc7ac6d3f69c18294139afbeddfa165cfa252fda81`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeb52f4bcf5819a6d5437fcce1e1e4325546addfcf171571a63a6d4fcf38a2d`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade497590a226b04f91f94fcec4f4767b7f16b42b2d031407e2363936c70f200`  
		Last Modified: Mon, 08 Dec 2025 23:04:56 GMT  
		Size: 13.8 MB (13817305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2b8a021123aadf774f53545df115eb5a5d6c64485c7760a47166eda1db7780`  
		Last Modified: Mon, 08 Dec 2025 23:04:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8d9c6a5afe47ba08106c02653f2a772933c717ca4b249b60ff2e06b978efc`  
		Last Modified: Mon, 08 Dec 2025 23:04:54 GMT  
		Size: 13.3 MB (13302002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871157607b2486950212e1485cb69ed1e5f64a625d6bc52f6176fdd7ad62bc8b`  
		Last Modified: Mon, 08 Dec 2025 23:04:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c5982816215ae8ea1db60995e5e0341359f8198df308bfc294b69af9061c`  
		Last Modified: Mon, 08 Dec 2025 23:04:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dfa9a936c1657d44373fbdba1b61ba45d15b3b0f0651e98ce3f3bf4856eaaa`  
		Last Modified: Mon, 08 Dec 2025 23:04:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed8388da19f6730b23ef07f87ea900452cdb1ad681a7ddbaa49dd7ffe90f0b4`  
		Last Modified: Mon, 08 Dec 2025 23:04:54 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f6f46e503dba31e7527a2605c232061791744e94ae29bd300855e5b2883cf`  
		Last Modified: Tue, 09 Dec 2025 01:54:46 GMT  
		Size: 1.7 MB (1675187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fa72054f9b40402f9ee47257e00d7dc2bb865be52a2adc10d24428c39d4d8c`  
		Last Modified: Tue, 09 Dec 2025 01:54:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaacf40f58e6ecf6c9c490a39582257a8d40e4a28c22e6a6b516f7e472b12ad8`  
		Last Modified: Tue, 09 Dec 2025 01:54:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3c0d240559ba9d042054ac053e605ac9aec57dcc8068be6e661c9264b5467b`  
		Last Modified: Tue, 09 Dec 2025 01:54:46 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f9c4cef9249dae62fdeab4f520b4150604db2d33e7e733218aa78c614a186`  
		Last Modified: Tue, 09 Dec 2025 01:54:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0754c066cb19d3eb5cd25d4faf96090df2d1c551878473743126f5290be353b`  
		Last Modified: Wed, 17 Dec 2025 23:29:28 GMT  
		Size: 21.3 MB (21301339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:latest` - unknown; unknown

```console
$ docker pull drupal@sha256:7294338724ed7eaff5243b6ee7b790eeb0ccf42508aeda4154a05007f25d0576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184170105c24486c4fef1aa41e3be3600087bb5cef2e5b336440add36f47cef3`

```dockerfile
```

-	Layers:
	-	`sha256:d34112461310581d212e3f801ae5553855cdf2f4bd95fe7ebeceffa4f3f586f8`  
		Last Modified: Thu, 18 Dec 2025 00:07:00 GMT  
		Size: 7.2 MB (7159203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0419e5240a94dade48bf1773ca8d1c7a2930b780bc2fef0797844573ca954cae`  
		Last Modified: Thu, 18 Dec 2025 00:07:01 GMT  
		Size: 46.6 KB (46581 bytes)  
		MIME: application/vnd.in-toto+json
