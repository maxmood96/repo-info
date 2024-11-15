## `drupal:11-apache-bookworm`

```console
$ docker pull drupal@sha256:0674ee8ff861a2966f1da64e71f2649b923b41945fb87825ec18f1a05ea345d5
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
$ docker pull drupal@sha256:8e6f47359c2eb5221ebbe615034d40435f9ef6121419108faaa331aed6557fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199874403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543965ad8775a5d41a5ad7e088e57aee6732651cddd1370a6aff5a24e6f48eb5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV DRUPAL_VERSION=11.0.7
# Tue, 12 Nov 2024 16:58:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:58:06 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711ad809e8ed1f2b6c0bf03b079947a0f57091689ef9a2e0335fc41215d21dc9`  
		Last Modified: Tue, 12 Nov 2024 02:08:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83176653a5705526d7f352ac7f87e03c8c4062b576492ebd3bc14e6e339105fe`  
		Last Modified: Tue, 12 Nov 2024 02:09:00 GMT  
		Size: 104.3 MB (104345621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c677d150c8a75ca1e028fa5466e810a3aad956aa45c19dd3223563e09fcdd06`  
		Last Modified: Tue, 12 Nov 2024 02:08:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9509fa8cf448638606ab723fe1e397f2b6118cef4b67c3f72ccb433a330472af`  
		Last Modified: Tue, 12 Nov 2024 02:09:00 GMT  
		Size: 20.1 MB (20123792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e90a89baf9b694acc777cd4ead537011fed37ac981c2ebc72f2759e39832bf`  
		Last Modified: Tue, 12 Nov 2024 02:09:00 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408661b85398eb731c110f5f578af624f40ee416bd69d42d01f476199ae54e5`  
		Last Modified: Tue, 12 Nov 2024 02:09:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2211b9d553295d8b8da01aa39c3ae17a95752cb7725463a28ccb10a2689e25`  
		Last Modified: Tue, 12 Nov 2024 02:09:01 GMT  
		Size: 12.6 MB (12612410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01f07e1a4287e3a5294234de23df527f57397108a7d53051f73d87ade1bdb45`  
		Last Modified: Tue, 12 Nov 2024 02:09:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839712f9ec25ee8be8aba4498bd0410bdea8a63af9b2c79d0d54477a530cbb0a`  
		Last Modified: Tue, 12 Nov 2024 02:09:01 GMT  
		Size: 11.6 MB (11644434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807c1fa8f78ade676a1d21b4299ff93182fcdf4f5b440a60f6192840cc9f1d29`  
		Last Modified: Tue, 12 Nov 2024 02:09:01 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaabd7df090bd64666d80538766408fafbc7cadfd220a38dd1e0ec065e04eb4`  
		Last Modified: Tue, 12 Nov 2024 02:08:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2eaa326f61742854942f681b233ff4fab94c2499cbe94f7319e007f72444a7a`  
		Last Modified: Tue, 12 Nov 2024 02:09:02 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f90a86886386b1b870d0e49a4fd8142463143669e54aca3deee1fa67fe1bd`  
		Last Modified: Thu, 14 Nov 2024 17:49:00 GMT  
		Size: 2.0 MB (1999936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512bf90b685da2ef69cb15d98162bf8cfa0e9951b40c71996b8a092d003d60b2`  
		Last Modified: Thu, 14 Nov 2024 17:49:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92923451c4f19ec7b69214437ce7262a7bc412561a88e0eb2e820ee3da0630`  
		Last Modified: Thu, 14 Nov 2024 17:49:01 GMT  
		Size: 739.0 KB (738954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e2d84920c6c68dc6ddfd1e7a97f36ee4750ae5383a31dc167e309a0159481f`  
		Last Modified: Thu, 14 Nov 2024 17:48:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ffec6910eec67be89a417aecbb7c1b6cbb6482381ee7fc6ef4e1152d338ad2`  
		Last Modified: Thu, 14 Nov 2024 17:49:01 GMT  
		Size: 19.3 MB (19275362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:8fcd74b4da11144457476c18fb8e67dcf8e09857e01f88d58e750121f737230d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6907004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abfe093ed02bbafd6f79e3b7da57237fac548577c7b28f2a0e4fb1c8f30de33`

```dockerfile
```

-	Layers:
	-	`sha256:f6f2dba6fab3f1c9b3d7984a72b1e6551002d20f3a0a801d34f90e8a26826633`  
		Last Modified: Thu, 14 Nov 2024 17:49:01 GMT  
		Size: 6.9 MB (6864110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4ed406d4dd1d85c4378a27f775572a950e86eb371145d1978958c0e2c7f6af`  
		Last Modified: Thu, 14 Nov 2024 17:49:00 GMT  
		Size: 42.9 KB (42894 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1d3ee5046d96fa2be955ebe6ac9aa3c91e4a9dddd0c421cec6d1e2b0cb8b4867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163758666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797c1cc87ed27d3a1003bf931a4a8ba4144b18c226a24471ff43c1ad25d39c27`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV DRUPAL_VERSION=11.0.7
# Tue, 12 Nov 2024 16:58:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:58:06 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4297c5ae3c7e8e8915409622802213bf4512c2b4a0bf9a86ed680878ddc18a70`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b50adcb7cdffa12052ba1589718b3c06d474e40507177a93fc914de46e895`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 76.2 MB (76162385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681174cd466f54c52977f6c159c33d12bdd6aa108d2d06470ff258ce5d3fac19`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3956adc6ba757482684b1a409597f790541c714f71ba631eee7d291574e817e`  
		Last Modified: Tue, 12 Nov 2024 03:15:54 GMT  
		Size: 18.9 MB (18857501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e647e764fe2dcfbd101cd5fcaaec1c944c7cd89cd40a65dcd2442b62733654`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429807ca1f9d7d3c489deadada060b40a6d8bd76e76a48f0a9298d511be0304c`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273028c2ba2fe41057f7a76cf4bdb6849859751926e7ad1ba2a11a8251245117`  
		Last Modified: Tue, 12 Nov 2024 05:31:29 GMT  
		Size: 12.6 MB (12610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7ea3ccfcb57ff264134d68fd8be3d4faf5f1fd72c4ceb4362859eeb6d011a`  
		Last Modified: Tue, 12 Nov 2024 05:31:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d6fe9094281c86ac33071b384c87ff8e5d7b224f73ad49662cad969a41b0a`  
		Last Modified: Tue, 12 Nov 2024 05:31:29 GMT  
		Size: 10.0 MB (10034156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe223ceb4a3059a8fb66f6063f43f829e28500175bd21d2e06b66b1b0d1a53`  
		Last Modified: Tue, 12 Nov 2024 05:31:28 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ea627ee8fa8c1d9b7339324f38653fd535ffe35efaf443dbd66107dbf63f77`  
		Last Modified: Tue, 12 Nov 2024 05:31:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adda9dd555db41037e9ff40da588da50569233b567468cdeace662dab6e757dd`  
		Last Modified: Tue, 12 Nov 2024 05:31:29 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f0194ab52c919b738eaeeb50536d8a65fb85e6a3898e049692cdc12c0f7ef`  
		Last Modified: Thu, 14 Nov 2024 17:48:37 GMT  
		Size: 1.4 MB (1355004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e675b948477165b4fffd6d84cd318a5695742d8efc83f4877a2b9b25b3bf16ad`  
		Last Modified: Thu, 14 Nov 2024 17:48:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482292f5916baae2c77629954316c03e30485612c849ff3f17bb6e5b2bf99b1`  
		Last Modified: Thu, 14 Nov 2024 17:48:37 GMT  
		Size: 739.0 KB (738953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e684be11900449a1b3f3a77ec81b95da0783630a1d5e12a07f233bbfbc5d09d`  
		Last Modified: Thu, 14 Nov 2024 17:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb218d417ed250fa3a97b0a99b252949fc9e82c0650ac88e8933c447753e17b`  
		Last Modified: Thu, 14 Nov 2024 17:48:39 GMT  
		Size: 19.3 MB (19275284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:477c063aa9f277d823ca6ba2970778be3ec6468574d62e1c19681d8eef4a6087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6722162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126a6bc71cb39fd91d9d31b887061e90dcd9febb4437f3549851d5870651e971`

```dockerfile
```

-	Layers:
	-	`sha256:1ed5592f36c5ef1f74bc5b8a128ca5e9e0d0e6388a505a933924c80adbadea5c`  
		Last Modified: Thu, 14 Nov 2024 17:48:37 GMT  
		Size: 6.7 MB (6678990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f98dae519de9e4b80d7f861d16e467f3aa52b49aabf1a3aa00b3bd0a2032701`  
		Last Modified: Thu, 14 Nov 2024 17:48:36 GMT  
		Size: 43.2 KB (43172 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:f454eef33bf6433002e8d9778f102a7899dce8d6afd9242fb6e4c91a045570a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193932217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613d9d1f1cb0891f3439bf3f91ff7d7f3ae2e34cfd063baa05782b6453e81153`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV DRUPAL_VERSION=11.0.7
# Tue, 12 Nov 2024 16:58:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:58:06 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff5ae4bc5e2e430d9b14ecd116fc553182d0a9c05c51edee0aa1e3b8765ea6`  
		Last Modified: Tue, 12 Nov 2024 05:27:21 GMT  
		Size: 12.6 MB (12612176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259914b8a04b14f7552de32bd8adbf78e62264cfae8384e0f1f8abab84a6cee0`  
		Last Modified: Tue, 12 Nov 2024 05:27:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38213c147a8bc23aff73e663636958c2329bf5b7a046439fdbe8bf2acb27a8e0`  
		Last Modified: Tue, 12 Nov 2024 05:27:21 GMT  
		Size: 11.6 MB (11632934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae588f96c68f0b598b59ac350fecf154b2944d1b82818034b6a3aca72effc96`  
		Last Modified: Tue, 12 Nov 2024 05:27:20 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5ebac94080fe45864dca377ddd239e83af897a7d23bb24db41164df450a707`  
		Last Modified: Tue, 12 Nov 2024 05:27:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f489a216032816dc4daa64713753937775f896b2696b2f4cfb745a0db1dc58d`  
		Last Modified: Tue, 12 Nov 2024 05:27:21 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509bdac03fb30f6dbcf4e73756c6fc86fb57309e16a9fe2e640050125cd395d1`  
		Last Modified: Thu, 14 Nov 2024 17:49:09 GMT  
		Size: 2.3 MB (2257930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfa900f3af49f9f98875676a71d529f5ae246eef876d1cc3fa0702021d68734`  
		Last Modified: Thu, 14 Nov 2024 17:49:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e01369c600388125945c53594836b77d31287659f7653533e3d0a899c23c1c`  
		Last Modified: Thu, 14 Nov 2024 17:49:09 GMT  
		Size: 739.0 KB (738955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a4a355cc8f14717adf24b20e4d26d0526f1916ee6ad2bcbf26417089277ed`  
		Last Modified: Thu, 14 Nov 2024 17:48:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9387f408f411ef8bca2531b3faae4f781621f1e83c91753c6c41c2df6736239`  
		Last Modified: Thu, 14 Nov 2024 17:49:10 GMT  
		Size: 19.3 MB (19275334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9ca4178ced29fc19eb7e4b437c351d6c6126e95a45d36c19a5af70e447d4de43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6936083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6b40e85fab47e88a7dc6c0fac89f1af20aeda5314f78c02bf46e23c95c10c8`

```dockerfile
```

-	Layers:
	-	`sha256:7d53fa5e6782c5927111ba8d3e151b35efd58a119af53fb58237d0820fa4fb89`  
		Last Modified: Thu, 14 Nov 2024 17:49:09 GMT  
		Size: 6.9 MB (6892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db98adf32a3da603f43b2aa7d68cd5a8b1691977810a48efa4b0044686a5eff`  
		Last Modified: Thu, 14 Nov 2024 17:49:08 GMT  
		Size: 43.3 KB (43289 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:b31ea712cbc79bae7fbdbc8cb7da416e9863bcc435e3939a733a5a065c43ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198845207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11171d77ee0f7a3916797fc08c2cb67b1a68efebf0568c239679ab5287caad30`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 10:54:37 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 10:54:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 Nov 2024 10:54:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 10:54:37 GMT
ENV DRUPAL_VERSION=11.0.6
# Thu, 07 Nov 2024 10:54:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 07 Nov 2024 10:54:37 GMT
WORKDIR /opt/drupal
# Thu, 07 Nov 2024 10:54:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 07 Nov 2024 10:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329eb31a4f93e9d41ddca528693079d4cac38e0e0cd7acbbf24dbaad04c807e9`  
		Last Modified: Mon, 28 Oct 2024 22:05:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00991a5c316faa9083955727f89b3e04028027ea095f4ebc8fe11c24701a97a5`  
		Last Modified: Mon, 28 Oct 2024 22:06:29 GMT  
		Size: 101.5 MB (101516947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479896864efa784a35768f05f72ff5585dc52a8377de29499449cbfb93d21b3`  
		Last Modified: Mon, 28 Oct 2024 22:06:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2640e1a07ee466e0bec0bd6b84574579a011598fea39c2b18beb22edef0bbf`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 20.6 MB (20638451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53c118cbbb1b6e4c239e0ea5db3ae393013c5d5e24367a20635acd0b7056ae`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0e769040ccb1546ac0d4ed3ad58ed10b689426fbff5aee2e0dd81cf1be3d27`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239b6469dc8348d269f3caefba6ac2834c0bf5e9e3e1dd1409d160af8979d0b`  
		Last Modified: Mon, 28 Oct 2024 22:06:27 GMT  
		Size: 12.6 MB (12611408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49c86746ac71d54d5b69263b64615f0f52f3f5a92a9518a6d9cf39118f2a04`  
		Last Modified: Mon, 28 Oct 2024 22:06:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd46df7b7a27b3a684a3fa865fd47872c6cb79ae483e1e3403eaa666b2c624d`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 11.9 MB (11862577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8bf4f8e802f4327016a09002d598e17cb81c8dd98f8134854c2b43f9bb82ae`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac382e0107f09c9d4f4f29c19f2ec27777333386b4927599ca03b496829569`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d6b970e9e74cad9e394a1b0e7707cf00b0673458fc3da783321cdb83b4753`  
		Last Modified: Mon, 28 Oct 2024 22:06:29 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8383e6e61ecbad50ab3ae8ceb90984f91a247ef0728c7ab182a78a9af38e12a`  
		Last Modified: Thu, 07 Nov 2024 23:59:21 GMT  
		Size: 2.1 MB (2051489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e6869b6fe5543af5d9a644abcab9ffb8fd26b2c6509a2703bc7ccb9af7b037`  
		Last Modified: Thu, 07 Nov 2024 23:59:21 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9562bd5939b0efc449c648b10dd5ec94d6d777af9df666917a64b5324bdeb0`  
		Last Modified: Thu, 07 Nov 2024 23:59:21 GMT  
		Size: 739.0 KB (738952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe487d5c9d2cdeeb7b864081f1ef9cc8b3f0b08b6db79d3c477870d4ca24a9`  
		Last Modified: Thu, 07 Nov 2024 23:59:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8361d24ab4ce8b6a6d74709a389d4f5986828fe70b179b1f9be93551738699d`  
		Last Modified: Thu, 07 Nov 2024 23:59:22 GMT  
		Size: 19.3 MB (19275220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:554358380f2bce15e545f6b44de96ebe3e36a4de80645b5fd99e630de5124ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6886950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ec8e21fe55edc21b658e24eff2e91e171d14e104b3b0d8c91f08d2f1fbba72`

```dockerfile
```

-	Layers:
	-	`sha256:ad38dcd6ded584caf1901b3ecd2bbdcea7712293eeeabb53657f71ce1cede8cc`  
		Last Modified: Thu, 07 Nov 2024 23:59:21 GMT  
		Size: 6.8 MB (6844198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e041ce38bffb19966b880b2c352e758dd2f3ddff22b6cfd036541df834ded66c`  
		Last Modified: Thu, 07 Nov 2024 23:59:20 GMT  
		Size: 42.8 KB (42752 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:843d6339fd508d06f5bd3999205221b70f820a73aa11094bc9fcc8e7e0293c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204306173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfbcae3e64b8feb955bd230fe0b1206f759eaade6d621d3486b699a1a010e13`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV DRUPAL_VERSION=11.0.7
# Tue, 12 Nov 2024 16:58:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:58:06 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02cceb11c5f92ea5660ac6e0610c26c972c38dae66eeb9d41e3387390540062`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1d6ec9f7f7d2e7f8318e16194758fc58116d42583559cad4394fb117b2d735`  
		Last Modified: Tue, 12 Nov 2024 03:22:56 GMT  
		Size: 103.3 MB (103323960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e883340f45c1d0e36d2a728cca20410ca3254d93c803c062646dc430b8e41e7b`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2155f33ef158a9585945d382ada5e33cc0a6cb3faf942e6f840e0af8c0ef4e`  
		Last Modified: Tue, 12 Nov 2024 03:27:38 GMT  
		Size: 21.3 MB (21308382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7c3966720dc0d3b2f38f69d3927be83fe5fbd6d2d6ee5d45e6635cd22825b`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b76c10e03d21d789b97d145b294ce14e9afc78a7624eddb9a1e308056c07b3`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddcfacddb89f55766916850200396dc44ce579c5ea090a49d0b1acd99d3890`  
		Last Modified: Tue, 12 Nov 2024 04:40:54 GMT  
		Size: 12.6 MB (12611820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a00b55b091fde962ef8cdc1cc9b21a20306e2eead440a6b56ee44fae9db147d`  
		Last Modified: Tue, 12 Nov 2024 04:40:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d007d75827cdcc7f0d28b1c32e47dd6957a398c8fca1372db3892992035e3534`  
		Last Modified: Tue, 12 Nov 2024 04:40:54 GMT  
		Size: 12.1 MB (12061087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e93cfd14cd6f4aed9ca62474a46fed5ef0f369caacadcddb9416bd48534566`  
		Last Modified: Tue, 12 Nov 2024 04:40:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6432cf6d07a479651cc05a22e9a4e487c5346e9d30f5db4b90dfefb889ecd17a`  
		Last Modified: Tue, 12 Nov 2024 04:40:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c80f90e024218aa343bb78e02698765409ee56368c0ff4fa66af1e842fa03`  
		Last Modified: Tue, 12 Nov 2024 04:40:54 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ba7fe9aa966e308a7687dae5b23c0c9a5caecc034d666fe93893e27678dd4`  
		Last Modified: Thu, 14 Nov 2024 17:49:26 GMT  
		Size: 1.9 MB (1855887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd77664c2ecab6a1638f9081a9009687fdccb27f03f2939d8baa6c7c05a1baf`  
		Last Modified: Thu, 14 Nov 2024 17:49:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92cb79c56bb4f6ed26e11f42bd9b72ad61fcaa52bf92e7a0a0e45d13857464`  
		Last Modified: Thu, 14 Nov 2024 17:49:26 GMT  
		Size: 739.0 KB (738953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bfebd4df0f885fbe74ec0a543db6f021a29a40e03f99592f08da19533e9a01`  
		Last Modified: Thu, 14 Nov 2024 17:49:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807063700e8657970891046e281a1aaf65cc2ff39bdc29440de1a4ae1a72a931`  
		Last Modified: Thu, 14 Nov 2024 17:49:28 GMT  
		Size: 19.3 MB (19274818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:571f36c9b196783ed67dcacb9461b0d2497cba3435fa1cff49dcd84e2d331e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6884247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b2ef054c18dc20a8afc128fcdaa6a5310a42e6a4f6c6a499464ac47d3cd23d`

```dockerfile
```

-	Layers:
	-	`sha256:eed7afe051fc7e5fdee807e6f7564bd9fe6eba1eb66e480e5636b4ddbe36bf22`  
		Last Modified: Thu, 14 Nov 2024 17:49:26 GMT  
		Size: 6.8 MB (6841174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e87c4a00e66684dcb1fc36f50e6cddbaa3b085e98e9ee86d667d87151db389b`  
		Last Modified: Thu, 14 Nov 2024 17:49:25 GMT  
		Size: 43.1 KB (43073 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:f083b032bd5b32bddb557024118e1a1d8623167599f102ee733ac2d0239ba500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173249203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fab795a69a50b9e78ba933c01f88238005b9961fda305f2b0a19e70d68ba2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV DRUPAL_VERSION=11.0.7
# Tue, 12 Nov 2024 16:58:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:58:06 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ec8c9288f91e0e914bc88a84e7f99c5caf8f6d9840288a739773c38a7c07a`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26af4e0d7a3fb552ad3968a1cee38ccd36f353e2162832fca3623342e7ab8a`  
		Last Modified: Tue, 12 Nov 2024 03:15:07 GMT  
		Size: 80.8 MB (80817024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36392fa6e835e08d294727ebd2c1c3a2bb6f80d6dc6273a5056d2f6ed2c1ffed`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e67acbced0cb69e2dc640f712d45dcfa623c348b09bd75ae63c1818f0129f`  
		Last Modified: Tue, 12 Nov 2024 03:20:14 GMT  
		Size: 19.9 MB (19895214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5427c8084a617f516431588d36205b585b6e003a7c6f3326454cc9e4e520946`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd0bc1eddda7a2174cecf32a39f30306b749d6521c2b41823a1b05b41eef6f9`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bbae546fdcd48ef02256a06eed4c9da0737d418969e287533710ef251abf0`  
		Last Modified: Tue, 12 Nov 2024 04:56:28 GMT  
		Size: 12.6 MB (12610904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cc6214ac2dc3f24efe1e45dba8ef4b53907ae92a419473078164fac5793d5e`  
		Last Modified: Tue, 12 Nov 2024 04:56:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ce96026977a8015244f0e44aa8e7c00b633d201b54ad572f5e1b8f352fcfa`  
		Last Modified: Tue, 12 Nov 2024 04:56:27 GMT  
		Size: 10.9 MB (10860861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484f9f699b682955377ef8c468dcf6a2f840f09416cc8d7f85e452553de6881`  
		Last Modified: Tue, 12 Nov 2024 04:56:27 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5677d11da5533112aabd9ccbf292431eec686d66557cbeffe31cf0742d9ccb2d`  
		Last Modified: Tue, 12 Nov 2024 04:56:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd90b117a4c5ce7e9f6e2d5f154f43d90c1d5671c89f9a351a624becf0d5eb2`  
		Last Modified: Tue, 12 Nov 2024 04:56:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada1260a307812a098e26f7351af7a8d2e5839f3e3cb7cf3c834327782429648`  
		Last Modified: Thu, 14 Nov 2024 17:48:23 GMT  
		Size: 1.6 MB (1553508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d6e54545f5518b5726ab1c97885e9b7e8c2036d0ad53dbc3998428422127c`  
		Last Modified: Thu, 14 Nov 2024 17:48:23 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043430bbc34329824c1e935e79d4548928404f9ef34e9242d6f4639a3a4926cf`  
		Last Modified: Thu, 14 Nov 2024 17:48:23 GMT  
		Size: 739.0 KB (738954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012fa66a06e23f84f3123bd27a334a7e8fe8355f17809a5e7ca418fb925c0a0`  
		Last Modified: Thu, 14 Nov 2024 17:48:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305438461632add56fd5eb9e022a7614c0299e5aa21f2ff97468dd0ab3c8acde`  
		Last Modified: Thu, 14 Nov 2024 17:48:24 GMT  
		Size: 19.3 MB (19275193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4649714369274a0f0162e7cb65eaa57a856a2d41779ccaf2d1825063bb52cc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6748213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201caf594ec1f5872568be141859c05d0f052764be0a459d91c54368f1dd07ac`

```dockerfile
```

-	Layers:
	-	`sha256:dc74fbd3ec9b4bfad9cea746fa57d53c5ffd64ee9d1286cf4a7ebdce2a309ce1`  
		Last Modified: Thu, 14 Nov 2024 17:48:23 GMT  
		Size: 6.7 MB (6705324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c622bde95798b41be723399f7383a90c69e113f26862677feda9a1169fd92923`  
		Last Modified: Thu, 14 Nov 2024 17:48:22 GMT  
		Size: 42.9 KB (42889 bytes)  
		MIME: application/vnd.in-toto+json
