## `drupal:11-apache-bookworm`

```console
$ docker pull drupal@sha256:67005e9bf34013edfc573e35f82c9eb111e66f5a1440b56b5503eacab917da9e
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

### `drupal:11-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:1ee45c7804bc3877bd1152962c6db737a40d0ef8ee822bf5bbae67ae4339a29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203731259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3b3531258e225054ced10b0ea96d8f8df5151eb8befa4bd177d7164f2a5f82`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:09:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:09:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:09:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:09:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:09:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:09:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:09:24 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:09:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:01 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:12:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:01 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:12:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:12:01 GMT
CMD ["apache2-foreground"]
# Fri, 06 Mar 2026 18:33:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:33:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:33:12 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:33:12 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:33:12 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:33:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:33:12 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:33:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:33:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717e6ecc3b822374852324e7d53476edab4edbccdd92bcb173c21f8fe664cc4e`  
		Last Modified: Tue, 24 Feb 2026 19:12:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea35b8744bed0613f3fdf3ce51c0e74174dc2286fb27da18cd703594c70fb4`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 104.3 MB (104335668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c1ae2468eb76e212fb8eb24a7e31f24ddef877b04d93f05a64d3eb92af08b`  
		Last Modified: Tue, 24 Feb 2026 19:12:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd06e913b963e1e3496456972e7ac21a59d8af6eff6ee65f2e19436ecece599d`  
		Last Modified: Tue, 24 Feb 2026 19:12:23 GMT  
		Size: 20.1 MB (20141702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b68d46455e369370817887061f0679f239a68f8e7d85d32b1975debce211b4b`  
		Last Modified: Tue, 24 Feb 2026 19:12:23 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b397bbfe8314ed7af77fd04578ac3da0165d86b19c81c06fe450bb2141910`  
		Last Modified: Tue, 24 Feb 2026 19:12:23 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7932a982f3035afd3ca0bc1b11d6649ba50c16bf05d5cfc23a0a6d4a931104e`  
		Last Modified: Tue, 24 Feb 2026 19:12:24 GMT  
		Size: 13.8 MB (13804275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904cab524bcf93fdbf7dfe825f671ca0637f86aad411c70c7482b8b7b8eced8`  
		Last Modified: Tue, 24 Feb 2026 19:12:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf58ff738d4d2531b5244dc6bcf02981be82f6b6e5d313abee32bf194f7a40`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 13.5 MB (13517945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde0427cd38f083a98d439e71adcf241e8b3183e8098a402abca71685b98a27`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f251f6b03668d0d365d26c3b3972a93bf88b16a6c4a55a456687f81891cdf4`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88d186a92850614a222328ec2d4ce1204a2bbece94e28f72400c14763bca3b2`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583b5e2ffb6bd07be8c444bb3b9a699435e01d4f3ec1e440367f26e2a2d0797`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7c9798bb6491efd4bdccfb67d0ba8100eadd5c69b7d5298b0976602db1e93`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 1.6 MB (1575525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c5ecca53547fa506283a272fa1f103aeb08bdc3dfdf09d7d44e9c575d32cc9`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac88ea8c3b479e5ec7a95fe965d2fb1df3a7be8c3aeeacb776fa478de0a347`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93527a260a474f757f5a55d31469fdf5efe775e001ef174f6ca5d9d262fed77d`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 777.5 KB (777549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea674ef78e910c4888e4a7edcdda9d447cbc046b5903eb334758e7f4d43f700`  
		Last Modified: Fri, 06 Mar 2026 18:33:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92909473efff404e5420346bf0b543097a33f54b2bd6ba21032be97e3b6b0ef`  
		Last Modified: Fri, 06 Mar 2026 18:33:44 GMT  
		Size: 21.3 MB (21335899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:5feb2bf1aef5f3baecd745f6c3ed6f874ff1b58e4b9ebbc543c7c98f23599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d300482e45ccfa6f0f90266762754cd932cccb2e29c0ebea05d1abcd18b411b0`

```dockerfile
```

-	Layers:
	-	`sha256:5cc7a98ca6755c44f55214ad169228b04895ce1766941ae957b00cf755a6adbb`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 7.1 MB (7052202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f62cfbbb8b478387be1d4be39bc36d7f51364bde2a1a1846fbb050e20b6e6df`  
		Last Modified: Fri, 06 Mar 2026 18:33:42 GMT  
		Size: 43.9 KB (43929 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:3462a0c660a50615200f2ccf588051c2b43f4865b4d9b0da45da298f5b9589ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167767064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2ae345fe2c6562974c17ab4feade6e4ee81f596e409387837277a3b0a99e76`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:12:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:13:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:13:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:13:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:13:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:13:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:13:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:16:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:16:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:16:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:19:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:19:20 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:19:20 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:20 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:19:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:19:20 GMT
CMD ["apache2-foreground"]
# Fri, 06 Mar 2026 18:55:39 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:55:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:55:39 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:55:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:55:39 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:55:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:55:39 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:55:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:55:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8b69c4bd2cbe58cf24eff6665ccaf037b6d40e10b40cacbf355680bce232c2`  
		Last Modified: Tue, 24 Feb 2026 19:16:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75b38b04dbbb631f5ad2e267d652506331173bcc3934c59a6faafff1552e35`  
		Last Modified: Tue, 24 Feb 2026 19:16:20 GMT  
		Size: 76.2 MB (76155118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a259c093691c6f6976eac4d9eb1f991ce095002c251ecaf2639c555b04240`  
		Last Modified: Tue, 24 Feb 2026 19:16:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e57c73dd024bebc6c2c1999859bd56525419ea76f311d5fe9b4563c4f618f56`  
		Last Modified: Tue, 24 Feb 2026 19:19:31 GMT  
		Size: 18.9 MB (18850616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa3694bf4ca53d1026102e9084058ea61ff5395bc164d8c0e9ca8f8a554cc61`  
		Last Modified: Tue, 24 Feb 2026 19:19:30 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8b4f5d0022788f47adbeee03b7615fc6970cdd60c8967a9adc3d210ebc1b2d`  
		Last Modified: Tue, 24 Feb 2026 19:19:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd36385b20d9feb933b8904cade83fc0077e82145905076dc56c78515ef36e`  
		Last Modified: Tue, 24 Feb 2026 19:19:32 GMT  
		Size: 13.8 MB (13801927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc29c2b62533bf957379487237ef31e88703a6d22608ce21eaa0ba10a7d870b7`  
		Last Modified: Tue, 24 Feb 2026 19:19:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab2e6c67650f8d9189612dda129aed801067e5f9cea14a30d6f108d9df2b5c5`  
		Last Modified: Tue, 24 Feb 2026 19:19:32 GMT  
		Size: 11.6 MB (11602659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9513a36c0b2a1832795c4bbb0e7ead8819afd013451c1873a8f2def24f13cf7`  
		Last Modified: Tue, 24 Feb 2026 19:19:33 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199ab1015754bef1256d6087f4b2027e2ba5856ab4af3dda3dd09d5ae95ab4c1`  
		Last Modified: Tue, 24 Feb 2026 19:19:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2ae7cce3e686b3b34cce61c8ef50dc74c5544e44610856c33deb5d944dbf35`  
		Last Modified: Tue, 24 Feb 2026 19:19:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08f0c1bf4027d17e90fad082549f8e5163eeaa4d4f0787d7ffbb8c0421e0560`  
		Last Modified: Tue, 24 Feb 2026 19:19:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34a24c5d631ad0270de956862a2933da4fa6bc0d194561860549d572453aa80`  
		Last Modified: Fri, 06 Mar 2026 18:56:06 GMT  
		Size: 1.3 MB (1295530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759352a9a76782cb5ae58217fad255726d6646b5b08463d2dce3b2b6fcd0470c`  
		Last Modified: Fri, 06 Mar 2026 18:56:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9401dce08f299ae5e40654a2174ede47f4ddf50af0fe8e396cd85dcbb90f415`  
		Last Modified: Fri, 06 Mar 2026 18:56:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd98c851da6035057c8a3fecee08f9caec966d369c7d4bccb3cefa80ef0366`  
		Last Modified: Fri, 06 Mar 2026 18:56:06 GMT  
		Size: 777.5 KB (777550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c09a05655ace7abf73843c59bae6143c695d14f9a99bf9de2d36d96e7979c8`  
		Last Modified: Fri, 06 Mar 2026 18:56:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce77a1875e6dc3b0794449d2cffe604affbd11299b18e3c48639e8ade45912`  
		Last Modified: Fri, 06 Mar 2026 18:56:07 GMT  
		Size: 21.3 MB (21335835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:3da26cc1aa2c76651357d7a72cd2492dbd34a972e7c1c9cf46b0b4d56a1898c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4438f71697691597a770c7edaad8c2b5b7bcce6e275afabbe4ef1b13205de3`

```dockerfile
```

-	Layers:
	-	`sha256:c5fcc3203e33907a4323ad0ff1e5187e4616bd49b385b42a07aeaf5a18648356`  
		Last Modified: Fri, 06 Mar 2026 18:56:06 GMT  
		Size: 6.9 MB (6865570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c4e046d674c27bd0249e322757fce8ed037dcf8001b0c19269bd8c2c78b603`  
		Last Modified: Fri, 06 Mar 2026 18:56:05 GMT  
		Size: 44.1 KB (44096 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c776801027db4fc2087ebe5c1561b6dde2aa847a271f87ba0dc974dfba07026f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197089889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e0c9a43cebb27fa708900d03a169f00f0b9f66a4f8e937b365196ecd2cb17`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:08:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:09:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:12:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:12:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:12:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:12:57 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:13:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:16:00 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:16:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:16:00 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:16:00 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:16:00 GMT
CMD ["apache2-foreground"]
# Fri, 06 Mar 2026 18:58:37 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:58:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:58:37 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:58:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:58:38 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:58:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:58:38 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:58:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:58:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc74000cc6326112837ed821031436a9ed7b7bba9b1bb5117aee5f910766421`  
		Last Modified: Tue, 24 Feb 2026 19:12:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a25832f7d81180bd3146629b0d09d353e125c280f19a50df8f4dd472cac1ccc`  
		Last Modified: Tue, 24 Feb 2026 19:12:44 GMT  
		Size: 98.2 MB (98168191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da26482dcf9e31346e12647c8a4785ad0d5018ce0bf8befa6b4ba862b74a3a6`  
		Last Modified: Tue, 24 Feb 2026 19:12:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71afadc217585094fe8ae32b326466729866fffd24ec7754799361fd1410e4a`  
		Last Modified: Tue, 24 Feb 2026 19:16:12 GMT  
		Size: 20.2 MB (20163712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a5f2d42a90c8287c273b9d6da33e8133794fde2574d2b1da05e82e9ad4b87b`  
		Last Modified: Tue, 24 Feb 2026 19:16:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da16b97fb09f28b6edcb57fd7799345096b434f6f62c37b89f3f0f83a31e49a`  
		Last Modified: Tue, 24 Feb 2026 19:16:12 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706a5002374ef9e66c1ffe7d5005ec8cee95c50b891ebc1119921195d0ec7c93`  
		Last Modified: Tue, 24 Feb 2026 19:16:12 GMT  
		Size: 13.8 MB (13803959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194082599e1a5b9666aa3177835f31549b9c293cc6d1e9388a249ac61f4534e1`  
		Last Modified: Tue, 24 Feb 2026 19:16:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a29e01fa7a152781c6a22378ea67075c86404075471f29775e4b6f946ff0bd9`  
		Last Modified: Tue, 24 Feb 2026 19:16:13 GMT  
		Size: 13.2 MB (13156810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a4d7e0534372b51280dca3c0afc6f230dc175acb3fd04881dfdbd6c46bfdc`  
		Last Modified: Tue, 24 Feb 2026 19:16:14 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab37d64caf5ec51fdea5824e1039fcc284bcef6dfe3b3b81ff12d85d0aae6fe`  
		Last Modified: Tue, 24 Feb 2026 19:16:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15adba1fb81d4b7c00d963e90c00e6bd9f3cf522856fc1a28f4c9dbaef45c52c`  
		Last Modified: Tue, 24 Feb 2026 19:16:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b394045b4255707894dcb8d33fee2d496c1b88d87c4cdcd066276fe71c41783`  
		Last Modified: Tue, 24 Feb 2026 19:16:14 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9600f9170df7da1a7f7c33e1aa185d1889ac7b31b0563b72edc029ee0e9e7d3`  
		Last Modified: Fri, 06 Mar 2026 18:59:02 GMT  
		Size: 1.6 MB (1563687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e611a0b60851cce040555ae52c37fdfeff7d1f7e9c3edd4d5dd7e62573275519`  
		Last Modified: Fri, 06 Mar 2026 18:59:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5129c6cb53cc631af37cb30c0cee9b33e0e43f3c515544576de0e8b2ccbbaa33`  
		Last Modified: Fri, 06 Mar 2026 18:59:02 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f14d80a8ddc86c0dfa6fae6ba3d55f225367e27a4ce172a7d56fd2ddd6461`  
		Last Modified: Fri, 06 Mar 2026 18:59:03 GMT  
		Size: 777.5 KB (777550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996e459a5c85530db3a900dd8d991db355e3772a4460f8ca4eeaa857a6512fb2`  
		Last Modified: Fri, 06 Mar 2026 18:59:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81de1d14884c5b552267401be2d902c9615a6d0f81b758999106435c591b73df`  
		Last Modified: Fri, 06 Mar 2026 18:59:04 GMT  
		Size: 21.3 MB (21333470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:5f81e3a3e56548c88b8f06b27860e542dfb43db589b29ea1dd40a75b8137e7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08394ee333ffd9813f47d33e42f4700dc969ad932b40cdce1a7049fb87ce94ee`

```dockerfile
```

-	Layers:
	-	`sha256:aa711ef2f7421996308bf9ada7236c160535215c06afa42c3164c9a0d6560d4e`  
		Last Modified: Fri, 06 Mar 2026 18:59:02 GMT  
		Size: 7.1 MB (7080663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c372a1ddb96a590c11f673b95bba0d1b4beb47fa9c1ea107659eb3c9e266a314`  
		Last Modified: Fri, 06 Mar 2026 18:59:02 GMT  
		Size: 44.1 KB (44146 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:92302bede397fcda4378cf09ccb2f434dd7090c4251afcccaff363df7fc85f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202795280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62aedf39df11252b8144aa872ea2e9beaf49a3efed76a499be89f10b552da9d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:01:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:01:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:01:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:01:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:01:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:05:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:05:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:05:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:05:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:05:03 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:05:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:07:52 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:07:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:52 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:07:52 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:07:52 GMT
CMD ["apache2-foreground"]
# Fri, 06 Mar 2026 18:34:57 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 18:34:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:34:57 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 06 Mar 2026 18:34:57 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 06 Mar 2026 18:34:57 GMT
ENV DRUPAL_VERSION=11.3.5
# Fri, 06 Mar 2026 18:34:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 06 Mar 2026 18:34:57 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:35:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:35:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659e4c38a069571d1bbca89e62c6e4301f11080cac390cb0831b20ebe9248768`  
		Last Modified: Tue, 24 Feb 2026 19:04:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0574f868dab6fbc8b0129caa5c57d08a4629090219abb3a0ab107db3af632211`  
		Last Modified: Tue, 24 Feb 2026 19:04:50 GMT  
		Size: 101.5 MB (101526564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896af6d1c4b1ecff61047f4de5fe15f3ff67a537e49b01353f1231bdd0ed3529`  
		Last Modified: Tue, 24 Feb 2026 19:04:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97ac8df4e489f46d03f257fb06e74c96e19d71a06e2f35e0507501d28c2fe31`  
		Last Modified: Tue, 24 Feb 2026 19:08:03 GMT  
		Size: 20.7 MB (20665523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777694d1c3fdfb7ee7dc0e39e6fca7fe14d6fea3d6e140d79d3ddb172d6599c4`  
		Last Modified: Tue, 24 Feb 2026 19:08:02 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d50247e1a799862a7ca04e9ff08a2b0bdb1f1a0594e8f283a841263683ee78`  
		Last Modified: Tue, 24 Feb 2026 19:08:02 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa1425a096d6cf76eee3e7402bd10f44fbb90aa571236411b76e419027031af`  
		Last Modified: Tue, 24 Feb 2026 19:08:03 GMT  
		Size: 13.8 MB (13803209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83ac6e0dcc131afc6bb19c9512feeb8b6d29bfaad29a30f0e654fb03976bd1f`  
		Last Modified: Tue, 24 Feb 2026 19:08:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc2d44811caccbac504490abe3e3d13973f535a18fc0b22c932d55ada6d297`  
		Last Modified: Tue, 24 Feb 2026 19:08:04 GMT  
		Size: 13.8 MB (13810833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391ba168a0e92d3d7978b460cd96a5bdb6b5f63a1d7f61d7f7a69bcdc1f9ca5d`  
		Last Modified: Tue, 24 Feb 2026 19:08:04 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c67e8d86ee0c00aed3a5d6a34c2777436b53f67095b1f76cd679e4b330a288`  
		Last Modified: Tue, 24 Feb 2026 19:08:05 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa662399ab061d8d7ec68d883e7debbd96cb16eeae1bac22d57b6416efa1a986`  
		Last Modified: Tue, 24 Feb 2026 19:08:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99b4d1893b540501515503558459515dca0343d004f95924d3d86272b850073`  
		Last Modified: Tue, 24 Feb 2026 19:08:06 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731a59068a13448a718b50b80531b37709a3084290aa21f9c371a1214cb9bb5`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 1.6 MB (1647699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dce71cf7ab7f7e609c648b48762c6cc526dc69d0780c51ce5807aea6b1ad9e`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80c22f2fb9fc9e91011850f1b94904fabe6b7cd3ecbde8f60b392ea2589d9f4`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fa7829bda667060adfe2992733886f847a14e7b53293bbda8fa6f66b3d5773`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 777.5 KB (777543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7e12ac9492e948964ebd6b460470a456b61954e2133bd486de2e5cebaf3aa6`  
		Last Modified: Fri, 06 Mar 2026 18:35:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a8665e48cc1347b255705f3767faf28df57e0edf2a02c9c17bfab6a1d9853`  
		Last Modified: Fri, 06 Mar 2026 18:35:23 GMT  
		Size: 21.3 MB (21335782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:90dc39b77d9af03ea9b586398d58108359f7730434a2118287d3b7afadcea0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb2ef8f1244d9b522056824726d09b99788c426951d53ef5f565a7cf4121e6`

```dockerfile
```

-	Layers:
	-	`sha256:c46d2f1eabd9bee51bc913be13bf0a8d910f7a84e890e6eac45ae58e76f3cb91`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 7.0 MB (7031930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542094da1d215c115f035e454f40d06ee481a3c179f0cc2ed5c405d7946773c0`  
		Last Modified: Fri, 06 Mar 2026 18:35:21 GMT  
		Size: 43.9 KB (43863 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:7cc312c457359c9e821513c0eaba8745ec225ca18feed86937c1c277beb23741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208367972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db1d3e259939a145cac11b727db58b0a9cd66d2b6c5d08f41d6d27ada5dc2e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:45:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:45:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:45:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:45:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:47:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:47:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:47:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 20:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:10:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:14:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 20:14:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:14:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 20:14:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 20:14:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 20:14:32 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 20:14:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:14:32 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 20:14:32 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 20:14:32 GMT
CMD ["apache2-foreground"]
# Thu, 05 Mar 2026 18:54:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 18:54:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:54:55 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:54:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:54:55 GMT
ENV DRUPAL_VERSION=11.3.5
# Thu, 05 Mar 2026 18:54:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Mar 2026 18:54:55 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 19:13:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 19:13:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8909961eea48ef1b6874fc78e0a2a67be659ef1f501c141db727def77188f`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee44b9ad8e875a3f516f25b3e3c40a3cd26acc45cc0e89783e3044adfc8d3f`  
		Last Modified: Tue, 24 Feb 2026 19:51:33 GMT  
		Size: 103.3 MB (103330209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1044ec1105edb234be52095b7e7657e4bc5695912aac59d3a42b6d4609d990`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c028bf874b5c30f73241cfb2f6871fc75b09cb312e452d430fdfa56bfcec3db`  
		Last Modified: Tue, 24 Feb 2026 19:52:49 GMT  
		Size: 21.3 MB (21332466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0702448893b5ade5883b68b8cd1235da79117ebdd7f4f6c29de6e57ca17b680e`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac90603a6aa9fb56eba677ab1d2384d71ea434e594e4b239aee8160b8cb2a68`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5762a5634619093435521e716883745f337c2fbcb4479b8702fa57f195e63d44`  
		Last Modified: Tue, 24 Feb 2026 20:14:59 GMT  
		Size: 13.8 MB (13803696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d73807471e93f83e696479eda8f8264e46b55c5299deaa96a1878698974f7f3`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df82e6767b9d35d8728f64175bcc813f264ec17ea66eeebf11574e83aef77fd`  
		Last Modified: Tue, 24 Feb 2026 20:14:59 GMT  
		Size: 13.9 MB (13925657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fd2a5a98c55b591918e5d0cfc5b2289e2817b164673b7bfdd289bcf2c16064`  
		Last Modified: Tue, 24 Feb 2026 20:14:59 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c225301b000adf6677c36971b8da08e7513a5acafbf48d8e923fccb9a05a0555`  
		Last Modified: Tue, 24 Feb 2026 20:15:00 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f50cc60671bad3dc08424c48d35001a450a2f6a2ca00cc4cb5d6dde07f756c1`  
		Last Modified: Tue, 24 Feb 2026 20:15:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6813add662d6099c845ec490a89f20272cb9cd9bb2fd4a2d0425a43dff3bf`  
		Last Modified: Tue, 24 Feb 2026 20:15:00 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d27a6db23b12fa88caca47e8f111f806024e99d795fc55a96f792b54d58c97`  
		Last Modified: Thu, 05 Mar 2026 18:55:52 GMT  
		Size: 1.8 MB (1777676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce1d78a24f9158f65fe71d817ebb2f5503e6a12428f08c17a83495ea72c1e3`  
		Last Modified: Thu, 05 Mar 2026 18:55:52 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab39fc671a26589a8128cd636552ad70544a4308313551996c3f82d397455b6c`  
		Last Modified: Thu, 05 Mar 2026 18:55:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9626df10a98c8b5982dba5c4da3c97674cc7ec0ac237e5528c89f08accd555f`  
		Last Modified: Thu, 05 Mar 2026 18:55:53 GMT  
		Size: 777.5 KB (777549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e18ddc0215112d1844648d924a9be2fe2f607cd73a44282f65033fec8fcc48b`  
		Last Modified: Thu, 05 Mar 2026 18:55:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afb9bd48b34c809b1a4651805132aee63b6d88e63b3c6910480cc1ba9fe195`  
		Last Modified: Fri, 06 Mar 2026 19:14:32 GMT  
		Size: 21.3 MB (21335926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2a08dfa7b5999961966acd40bd91840d4efbfc37e8ec848ef5ad2a286856ed17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb960c115e33ebfa7fbeb859e2bb46654e5d6a947180a17bec5abb63f3df7f3`

```dockerfile
```

-	Layers:
	-	`sha256:bd0bec214790996437c93124f2d1393ec73a98941ea0cec146d957bebd37e499`  
		Last Modified: Fri, 06 Mar 2026 19:14:31 GMT  
		Size: 7.0 MB (7029062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3db8220c50af2c957852dd624eacd480a8bc9d16cc3c84d01d172a821eaad62`  
		Last Modified: Fri, 06 Mar 2026 19:14:31 GMT  
		Size: 44.0 KB (44013 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:0e30b2529fe3f71bbf4697e8feddf34738151dffd3d1f1f37103d4175cabe0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177630503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97320cc759d9bee3f0d27f81139898d06fdc5e26d170eab461d0b7f160db3d3c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:15:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:16:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:16:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:16:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:16:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:31:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:31:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:31:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:31:22 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:31:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:31:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:36:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:36:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:36:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:36:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:36:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:55 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:36:55 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:36:55 GMT
CMD ["apache2-foreground"]
# Thu, 05 Mar 2026 18:48:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 18:48:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:48:58 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 05 Mar 2026 18:48:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:48:58 GMT
ENV DRUPAL_VERSION=11.3.5
# Thu, 05 Mar 2026 18:48:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Mar 2026 18:48:58 GMT
WORKDIR /opt/drupal
# Fri, 06 Mar 2026 18:55:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 06 Mar 2026 18:55:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888ddcf8d56ba1585c0143811b54347b2dea83987a0f877602efadae824c515e`  
		Last Modified: Tue, 24 Feb 2026 19:22:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6599039cf0d4c26d33b25e5f55305201c9c5442bd67befd50e9a7af182db7d2`  
		Last Modified: Tue, 24 Feb 2026 19:22:17 GMT  
		Size: 80.8 MB (80828334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b0b090ea9d1e02f423938fd0ed61df3e83aca17b89627a2331d38b8486ff18`  
		Last Modified: Tue, 24 Feb 2026 19:22:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65932acdea77456c931fc0f7429a25684a9ee61db34120b937c3e867f3aed9d`  
		Last Modified: Tue, 24 Feb 2026 19:37:16 GMT  
		Size: 19.9 MB (19919195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6da95b383e2ab0573d2e34efda2b584f4e5820dba28df07d5de05a6699e302a`  
		Last Modified: Tue, 24 Feb 2026 19:37:15 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70c034230c53ee0d617548b65d1d29bfb0bce9a140939436e4554eb476e3c23`  
		Last Modified: Tue, 24 Feb 2026 19:37:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff753398c9b7bdfa69f2f4d451df434e6e11d32e2662b50fe2f7d9d895a11d1`  
		Last Modified: Tue, 24 Feb 2026 19:37:16 GMT  
		Size: 13.8 MB (13802691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429c77ba51083d46b910ac53b1c31cfa7e2149d2c0f6c9f9f821d67ef66fc790`  
		Last Modified: Tue, 24 Feb 2026 19:37:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ec1f054c88e61042491cff695bcea82f9a8f32f9d86b75e12a70b192efcbdc`  
		Last Modified: Tue, 24 Feb 2026 19:37:16 GMT  
		Size: 12.6 MB (12582497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe8168abd8f6ebb06d8508e6bf6ff970ae264c40a68b66a8559b2d9a524c80`  
		Last Modified: Tue, 24 Feb 2026 19:37:17 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed90301ccdbcf540e02440f8e4f3627d02d4b9f4ec4b4df458f28788d0c76cb`  
		Last Modified: Tue, 24 Feb 2026 19:37:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206a60d28dc1cf00df5203bd480bb6ea1037bff9ea805fa8c30cbf4d50537947`  
		Last Modified: Tue, 24 Feb 2026 19:37:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24a9143536f479cc2fc6daa8c3eb574acb113fad1a3ddf2521939249b08b84`  
		Last Modified: Tue, 24 Feb 2026 19:37:18 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c455ef5b6689b20d6c8d921d0f47d9ebb8be5b00a42d9a07aa26682e6b78ae16`  
		Last Modified: Thu, 05 Mar 2026 18:49:32 GMT  
		Size: 1.5 MB (1486484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857ffa24f3e27973637d7f8ae5e7386898ab170184dc6e922f8abda8f3ce751`  
		Last Modified: Thu, 05 Mar 2026 18:49:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471aef29a4ed43ef33292f1ac0ef4a4e0520e9af01cc5f10c5cfe5e741fe01ba`  
		Last Modified: Thu, 05 Mar 2026 18:49:32 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a87602dbf1b382f648563415d73337f06b95d91d3b7cf02d7a812fdb882b56`  
		Last Modified: Thu, 05 Mar 2026 18:49:32 GMT  
		Size: 777.5 KB (777545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daef641698f270e0912bbcd6916069288ea9252e5b4b86df74f3ee89d8d544a1`  
		Last Modified: Thu, 05 Mar 2026 18:49:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591dfeab847ffc48aa85e5904caf793d0db40fc1cad7f5e903ad46dc6892fb09`  
		Last Modified: Fri, 06 Mar 2026 18:55:43 GMT  
		Size: 21.3 MB (21335791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6cded92512ae15f66de62ab9fb42f57b6250a6885790203cc3944717b41b2430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b3def3210af572e7d0fca312217de86b9993f81fba07524da6743b46f151a`

```dockerfile
```

-	Layers:
	-	`sha256:a450f7991698a5f4997454a072a7a9887d522399fb8c240bd9130e49e631e4bc`  
		Last Modified: Fri, 06 Mar 2026 18:55:42 GMT  
		Size: 6.9 MB (6889404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6029f07ff50913cd1b7332c97f49baeeeab99dd1f7f44d57da28f33f7c4f3437`  
		Last Modified: Fri, 06 Mar 2026 18:55:42 GMT  
		Size: 43.9 KB (43923 bytes)  
		MIME: application/vnd.in-toto+json
