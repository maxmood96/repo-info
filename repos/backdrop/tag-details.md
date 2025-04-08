<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.30`](#backdrop130)
-	[`backdrop:1.30-apache`](#backdrop130-apache)
-	[`backdrop:1.30-fpm`](#backdrop130-fpm)
-	[`backdrop:1.30.2`](#backdrop1302)
-	[`backdrop:1.30.2-apache`](#backdrop1302-apache)
-	[`backdrop:1.30.2-fpm`](#backdrop1302-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:7612fb9c372b1ac2f0834c592d18271e9133f3e2839e85fb87e4d80e3f625a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a47f1aef17fb05ce6652d43293fca29c48a7acbca33252076c4db9ee7fb31c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8826377b9e683879263fa8461b9cb4d0dd799a402b788d981cf1743423215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ba0353b9912233a6ec69548ef5d22c2604d7e67c80ee0240d737f93d41e7`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb655f07e940dedc6c127e5c53d8c30763f3d39f67d3f5c196e1983a12f6a78`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 104.3 MB (104329213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965cf6e9b9616efb93914a32de85e04e787c02234bfa9535582300d9f94f738c`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7099584bcb450f8c6fc51d5644e7354eb39ad0f9a93131dd52ef5f9df1d1ec1a`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 12.7 MB (12670862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c23e02268aaa9c921eb61cbcb87df85365b43269f7ddf0796ab1de35a07349`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9b9dd2b59336d9fcc84e4ce341176e3cee6c150d2344180ae277931429254`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 27.8 MB (27828274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c03754d36989af2a8bdb9403759ee07ce17d663bf3493f815b61c0a24f165d`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb33c4a409a76ef067246515f46fbcdd4e2089a7d7869cb223959000618739e`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251e456d3bb1d3bea126ebf504053d9021b9da6dc22d9a7b190a21f6c48f3d8`  
		Last Modified: Tue, 08 Apr 2025 01:21:02 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f7469118cba26e55588b3ff2508eed8e472755a8784449981373b5bc286d5d`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 5.6 MB (5587992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645a6a0fd251f7d0c74da9981a862a10cc1b049e55d06c9f3a1e43dfae2fb75`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:dd5bec20b18467df6d85a0dbf3451cab2ac7efa7fb856a4ce4702fbe8a8133c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f011b57048c0a60cdd0351c3bcf813fec18ed20e94257e417573a6306cf60b16`

```dockerfile
```

-	Layers:
	-	`sha256:9f89d3f2f0742263b9caf188aa2e3444ac68860fae2a2b62ef1796809b2f1334`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 6.4 MB (6431164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0c8a9343494437a458a8ed786e3fe31b06be294ba0332b9826c1c49aed5fa4`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:8ed90b0015167052d23b526e6a79de1dd02a3cd3c822a96b8d4aba612c5b0e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181031903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161bf3149f3c812095008e4bef638910f12319d924a4f8bedbb32ae73cd065a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0f31d0940181312546889ac406a77aa63d69dff3fbe07543d690638f92820`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 12.7 MB (12670709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f52d3ce973245446154b947b3edfc813f1ea5bf654f88c4f9024c9985dddc`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ad4523f46bff59a8ab976d648f14795886de63dbe8a77fc8ad482eb9b0dbf`  
		Last Modified: Tue, 18 Mar 2025 05:46:30 GMT  
		Size: 27.8 MB (27772398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b8820240558e2522e0ff52f891c181bf57aa20b8956454b0c28269e96c4b5`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4849a450312198e386779e8c0ee9f6d3d22e3a2a03b484b1bc0c330b90d1e`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3eea464f5bbee7f18d5565cc7c996ec4e913c72b2feac3e64ecdc11f59d5f8`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9f35b930ada38f2b293ef9ad5c559e4d947cf76051928aa5a1caeee272e43`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 5.6 MB (5603033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a89b6d15debaa4600cc083f42bee54005bf06ce244d2fc20128f9997245cc`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd579fc55f5a543e0521db571b906c9c7b06c7ebbb246ee5f14dab697ddb67c`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:d62724dbd6c9b17b1a970461a73e254d0d21dceab2d44cb124369ab05a1f1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac825001bef7c07653bccae853dd0fec58d20f4c4f4472697c24406f7827016`

```dockerfile
```

-	Layers:
	-	`sha256:a9e14c6a62fd20611b7e714bfd6bf9b1db53c53d804d80998c54cbfe179b47ac`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 6.5 MB (6458220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4266588fb8ce5b6aba2f7d9ae98c40a5a42f4a0df42950ae5510e67c4b0fbc7e`  
		Last Modified: Fri, 21 Mar 2025 17:21:41 GMT  
		Size: 21.7 KB (21697 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30-apache`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30-fpm`

```console
$ docker pull backdrop@sha256:7612fb9c372b1ac2f0834c592d18271e9133f3e2839e85fb87e4d80e3f625a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a47f1aef17fb05ce6652d43293fca29c48a7acbca33252076c4db9ee7fb31c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8826377b9e683879263fa8461b9cb4d0dd799a402b788d981cf1743423215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ba0353b9912233a6ec69548ef5d22c2604d7e67c80ee0240d737f93d41e7`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb655f07e940dedc6c127e5c53d8c30763f3d39f67d3f5c196e1983a12f6a78`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 104.3 MB (104329213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965cf6e9b9616efb93914a32de85e04e787c02234bfa9535582300d9f94f738c`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7099584bcb450f8c6fc51d5644e7354eb39ad0f9a93131dd52ef5f9df1d1ec1a`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 12.7 MB (12670862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c23e02268aaa9c921eb61cbcb87df85365b43269f7ddf0796ab1de35a07349`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9b9dd2b59336d9fcc84e4ce341176e3cee6c150d2344180ae277931429254`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 27.8 MB (27828274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c03754d36989af2a8bdb9403759ee07ce17d663bf3493f815b61c0a24f165d`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb33c4a409a76ef067246515f46fbcdd4e2089a7d7869cb223959000618739e`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251e456d3bb1d3bea126ebf504053d9021b9da6dc22d9a7b190a21f6c48f3d8`  
		Last Modified: Tue, 08 Apr 2025 01:21:02 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f7469118cba26e55588b3ff2508eed8e472755a8784449981373b5bc286d5d`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 5.6 MB (5587992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645a6a0fd251f7d0c74da9981a862a10cc1b049e55d06c9f3a1e43dfae2fb75`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:dd5bec20b18467df6d85a0dbf3451cab2ac7efa7fb856a4ce4702fbe8a8133c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f011b57048c0a60cdd0351c3bcf813fec18ed20e94257e417573a6306cf60b16`

```dockerfile
```

-	Layers:
	-	`sha256:9f89d3f2f0742263b9caf188aa2e3444ac68860fae2a2b62ef1796809b2f1334`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 6.4 MB (6431164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0c8a9343494437a458a8ed786e3fe31b06be294ba0332b9826c1c49aed5fa4`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:8ed90b0015167052d23b526e6a79de1dd02a3cd3c822a96b8d4aba612c5b0e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181031903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161bf3149f3c812095008e4bef638910f12319d924a4f8bedbb32ae73cd065a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0f31d0940181312546889ac406a77aa63d69dff3fbe07543d690638f92820`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 12.7 MB (12670709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f52d3ce973245446154b947b3edfc813f1ea5bf654f88c4f9024c9985dddc`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ad4523f46bff59a8ab976d648f14795886de63dbe8a77fc8ad482eb9b0dbf`  
		Last Modified: Tue, 18 Mar 2025 05:46:30 GMT  
		Size: 27.8 MB (27772398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b8820240558e2522e0ff52f891c181bf57aa20b8956454b0c28269e96c4b5`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4849a450312198e386779e8c0ee9f6d3d22e3a2a03b484b1bc0c330b90d1e`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3eea464f5bbee7f18d5565cc7c996ec4e913c72b2feac3e64ecdc11f59d5f8`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9f35b930ada38f2b293ef9ad5c559e4d947cf76051928aa5a1caeee272e43`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 5.6 MB (5603033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a89b6d15debaa4600cc083f42bee54005bf06ce244d2fc20128f9997245cc`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd579fc55f5a543e0521db571b906c9c7b06c7ebbb246ee5f14dab697ddb67c`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:d62724dbd6c9b17b1a970461a73e254d0d21dceab2d44cb124369ab05a1f1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac825001bef7c07653bccae853dd0fec58d20f4c4f4472697c24406f7827016`

```dockerfile
```

-	Layers:
	-	`sha256:a9e14c6a62fd20611b7e714bfd6bf9b1db53c53d804d80998c54cbfe179b47ac`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 6.5 MB (6458220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4266588fb8ce5b6aba2f7d9ae98c40a5a42f4a0df42950ae5510e67c4b0fbc7e`  
		Last Modified: Fri, 21 Mar 2025 17:21:41 GMT  
		Size: 21.7 KB (21697 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.2`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.2` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.2` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.2-apache`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.2-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.2-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.2-fpm`

```console
$ docker pull backdrop@sha256:7612fb9c372b1ac2f0834c592d18271e9133f3e2839e85fb87e4d80e3f625a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.2-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a47f1aef17fb05ce6652d43293fca29c48a7acbca33252076c4db9ee7fb31c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8826377b9e683879263fa8461b9cb4d0dd799a402b788d981cf1743423215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ba0353b9912233a6ec69548ef5d22c2604d7e67c80ee0240d737f93d41e7`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb655f07e940dedc6c127e5c53d8c30763f3d39f67d3f5c196e1983a12f6a78`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 104.3 MB (104329213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965cf6e9b9616efb93914a32de85e04e787c02234bfa9535582300d9f94f738c`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7099584bcb450f8c6fc51d5644e7354eb39ad0f9a93131dd52ef5f9df1d1ec1a`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 12.7 MB (12670862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c23e02268aaa9c921eb61cbcb87df85365b43269f7ddf0796ab1de35a07349`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9b9dd2b59336d9fcc84e4ce341176e3cee6c150d2344180ae277931429254`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 27.8 MB (27828274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c03754d36989af2a8bdb9403759ee07ce17d663bf3493f815b61c0a24f165d`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb33c4a409a76ef067246515f46fbcdd4e2089a7d7869cb223959000618739e`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251e456d3bb1d3bea126ebf504053d9021b9da6dc22d9a7b190a21f6c48f3d8`  
		Last Modified: Tue, 08 Apr 2025 01:21:02 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f7469118cba26e55588b3ff2508eed8e472755a8784449981373b5bc286d5d`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 5.6 MB (5587992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645a6a0fd251f7d0c74da9981a862a10cc1b049e55d06c9f3a1e43dfae2fb75`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:dd5bec20b18467df6d85a0dbf3451cab2ac7efa7fb856a4ce4702fbe8a8133c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f011b57048c0a60cdd0351c3bcf813fec18ed20e94257e417573a6306cf60b16`

```dockerfile
```

-	Layers:
	-	`sha256:9f89d3f2f0742263b9caf188aa2e3444ac68860fae2a2b62ef1796809b2f1334`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 6.4 MB (6431164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0c8a9343494437a458a8ed786e3fe31b06be294ba0332b9826c1c49aed5fa4`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.2-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:8ed90b0015167052d23b526e6a79de1dd02a3cd3c822a96b8d4aba612c5b0e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181031903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161bf3149f3c812095008e4bef638910f12319d924a4f8bedbb32ae73cd065a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0f31d0940181312546889ac406a77aa63d69dff3fbe07543d690638f92820`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 12.7 MB (12670709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f52d3ce973245446154b947b3edfc813f1ea5bf654f88c4f9024c9985dddc`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ad4523f46bff59a8ab976d648f14795886de63dbe8a77fc8ad482eb9b0dbf`  
		Last Modified: Tue, 18 Mar 2025 05:46:30 GMT  
		Size: 27.8 MB (27772398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b8820240558e2522e0ff52f891c181bf57aa20b8956454b0c28269e96c4b5`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4849a450312198e386779e8c0ee9f6d3d22e3a2a03b484b1bc0c330b90d1e`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3eea464f5bbee7f18d5565cc7c996ec4e913c72b2feac3e64ecdc11f59d5f8`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9f35b930ada38f2b293ef9ad5c559e4d947cf76051928aa5a1caeee272e43`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 5.6 MB (5603033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a89b6d15debaa4600cc083f42bee54005bf06ce244d2fc20128f9997245cc`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd579fc55f5a543e0521db571b906c9c7b06c7ebbb246ee5f14dab697ddb67c`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.2-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:d62724dbd6c9b17b1a970461a73e254d0d21dceab2d44cb124369ab05a1f1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac825001bef7c07653bccae853dd0fec58d20f4c4f4472697c24406f7827016`

```dockerfile
```

-	Layers:
	-	`sha256:a9e14c6a62fd20611b7e714bfd6bf9b1db53c53d804d80998c54cbfe179b47ac`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 6.5 MB (6458220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4266588fb8ce5b6aba2f7d9ae98c40a5a42f4a0df42950ae5510e67c4b0fbc7e`  
		Last Modified: Fri, 21 Mar 2025 17:21:41 GMT  
		Size: 21.7 KB (21697 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:7612fb9c372b1ac2f0834c592d18271e9133f3e2839e85fb87e4d80e3f625a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a47f1aef17fb05ce6652d43293fca29c48a7acbca33252076c4db9ee7fb31c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187455189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8826377b9e683879263fa8461b9cb4d0dd799a402b788d981cf1743423215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ba0353b9912233a6ec69548ef5d22c2604d7e67c80ee0240d737f93d41e7`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb655f07e940dedc6c127e5c53d8c30763f3d39f67d3f5c196e1983a12f6a78`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 104.3 MB (104329213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965cf6e9b9616efb93914a32de85e04e787c02234bfa9535582300d9f94f738c`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7099584bcb450f8c6fc51d5644e7354eb39ad0f9a93131dd52ef5f9df1d1ec1a`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 12.7 MB (12670862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c23e02268aaa9c921eb61cbcb87df85365b43269f7ddf0796ab1de35a07349`  
		Last Modified: Tue, 08 Apr 2025 01:21:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9b9dd2b59336d9fcc84e4ce341176e3cee6c150d2344180ae277931429254`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 27.8 MB (27828274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c03754d36989af2a8bdb9403759ee07ce17d663bf3493f815b61c0a24f165d`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb33c4a409a76ef067246515f46fbcdd4e2089a7d7869cb223959000618739e`  
		Last Modified: Tue, 08 Apr 2025 01:21:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251e456d3bb1d3bea126ebf504053d9021b9da6dc22d9a7b190a21f6c48f3d8`  
		Last Modified: Tue, 08 Apr 2025 01:21:02 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f7469118cba26e55588b3ff2508eed8e472755a8784449981373b5bc286d5d`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 5.6 MB (5587992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645a6a0fd251f7d0c74da9981a862a10cc1b049e55d06c9f3a1e43dfae2fb75`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:dd5bec20b18467df6d85a0dbf3451cab2ac7efa7fb856a4ce4702fbe8a8133c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f011b57048c0a60cdd0351c3bcf813fec18ed20e94257e417573a6306cf60b16`

```dockerfile
```

-	Layers:
	-	`sha256:9f89d3f2f0742263b9caf188aa2e3444ac68860fae2a2b62ef1796809b2f1334`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 6.4 MB (6431164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0c8a9343494437a458a8ed786e3fe31b06be294ba0332b9826c1c49aed5fa4`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:8ed90b0015167052d23b526e6a79de1dd02a3cd3c822a96b8d4aba612c5b0e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181031903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161bf3149f3c812095008e4bef638910f12319d924a4f8bedbb32ae73cd065a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0f31d0940181312546889ac406a77aa63d69dff3fbe07543d690638f92820`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 12.7 MB (12670709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f52d3ce973245446154b947b3edfc813f1ea5bf654f88c4f9024c9985dddc`  
		Last Modified: Tue, 18 Mar 2025 05:41:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ad4523f46bff59a8ab976d648f14795886de63dbe8a77fc8ad482eb9b0dbf`  
		Last Modified: Tue, 18 Mar 2025 05:46:30 GMT  
		Size: 27.8 MB (27772398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b8820240558e2522e0ff52f891c181bf57aa20b8956454b0c28269e96c4b5`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4849a450312198e386779e8c0ee9f6d3d22e3a2a03b484b1bc0c330b90d1e`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3eea464f5bbee7f18d5565cc7c996ec4e913c72b2feac3e64ecdc11f59d5f8`  
		Last Modified: Tue, 18 Mar 2025 05:46:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9f35b930ada38f2b293ef9ad5c559e4d947cf76051928aa5a1caeee272e43`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 5.6 MB (5603033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a89b6d15debaa4600cc083f42bee54005bf06ce244d2fc20128f9997245cc`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd579fc55f5a543e0521db571b906c9c7b06c7ebbb246ee5f14dab697ddb67c`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:d62724dbd6c9b17b1a970461a73e254d0d21dceab2d44cb124369ab05a1f1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac825001bef7c07653bccae853dd0fec58d20f4c4f4472697c24406f7827016`

```dockerfile
```

-	Layers:
	-	`sha256:a9e14c6a62fd20611b7e714bfd6bf9b1db53c53d804d80998c54cbfe179b47ac`  
		Last Modified: Fri, 21 Mar 2025 17:21:42 GMT  
		Size: 6.5 MB (6458220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4266588fb8ce5b6aba2f7d9ae98c40a5a42f4a0df42950ae5510e67c4b0fbc7e`  
		Last Modified: Fri, 21 Mar 2025 17:21:41 GMT  
		Size: 21.7 KB (21697 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:ed7431a72eac482af8cbbfbb4fc280b2aa5e43fa3fcda534a4dcc97281ed45eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:495884f4b6169f563188c6575b01169fe2835f8b496a814f31ec64c2827dce06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191412015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54391ebab96d004f6e4b457b6930ab08b79ace5caa4e7e93ef802fd2c573081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63984f81d63619f7e1864524eff7805afd639a941fda5e676abe0a4ee8792676`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b365be746f855b17c984bcd53b7c6b11c6dd68ec117b5aabaaed2bd372f8005`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 5.6 MB (5581420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9767a0574a25f315949b148339fde16e6a48920b174f1ec540f5de203f12a4c2`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 8.8 MB (8797760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59f54329e7d4ec26f2fa829bccb6fe4fdc922c716b913a7638a46e51618fdf`  
		Last Modified: Tue, 08 Apr 2025 02:14:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:a1d76053b8d6d4f98d75b9d219d64226e7c12e360919f29ecd3191a8d4bc6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575c508e89a9a02ca2f20217681363e226db36c54dac1d0a505b4ee127fd13cf`

```dockerfile
```

-	Layers:
	-	`sha256:45049e62b2f88ebe3e17886d502307b80aceaca1a26ff4832ca71cdb5e2f088e`  
		Last Modified: Tue, 08 Apr 2025 02:14:38 GMT  
		Size: 6.9 MB (6941653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90207e876b22ec1d588174d8ca342c7cf39f99411de26d6e443787803fed5f6`  
		Last Modified: Tue, 08 Apr 2025 02:14:37 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:79fe36bb85a4c3493cca928444275eccb794a29a8e20fc58cb0a76cf683c1f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93346386da869b41ab31edd31a861e0316ba5af75adc3b7b86dba1e2b88be9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 15:35:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
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
# Fri, 21 Mar 2025 15:18:44 GMT
RUN a2enmod rewrite # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d0840fadaaed2570111bec7e9cd7957da00fddf8c6772035397c18d45f338`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 20.1 MB (20120935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804945c1dd829c960308fcc8a6cb0979652c0fe0fe19c5662f212e0c9064ef4`  
		Last Modified: Tue, 18 Mar 2025 05:51:29 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164548c32da3693854a9be5671bb93ee4599ec7efebb2f8e87fa5bcc5f8feaca`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c842d9079c652ad205e5f84d555238ae4d174b500dc2e9242df2e6db82be2f`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 12.7 MB (12689497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910cb198edab273534b75ce0a70122c4116a930c47d4c938ae2e8e56a1ab694`  
		Last Modified: Tue, 18 Mar 2025 05:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d222d1c50472e6ec7c9609f26f5f83485145240a8b95e92a62daffae4a75`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 11.7 MB (11654038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b900d6aa092769559fd7854ae7a2ebdea1e04059f45ded342dd9b3d8d2bcd3`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e2f81f5d8ccde0a76b65cad8d54b14850ee3b40de7e71b77758954109e8ff`  
		Last Modified: Tue, 18 Mar 2025 05:51:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bc6529e15e849663b751183dc2fe077218c45a0bc735522e2cfac99af59ea`  
		Last Modified: Tue, 18 Mar 2025 05:51:32 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4307057eefc2657c00bd7ba593215b36a17b8b3d7d57b992018c3d8f64f581`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6aacf63629fbd3e17c5eeb8f1e027e3f4c051d99532f406acf5bbba632dcc`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 5.6 MB (5598571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155df7a5ab268b5e7c6b4bbc21794c6c898e53ddf1b766289a946aa2c2a73f1`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 8.8 MB (8797764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb9000788c75e157fcfa6f081b0836e776d484c4211d7586dc3042b0aa981e`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:1bd14bddda702e4a69e9803f1e69b2f19e2c950e287444b4d7431bcd4a5c2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeefd17aad8a413346e0a8a2d49954a64c3b2ad91ca2a2c4a0cc71ade114e3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd3f6c39c146c605e3e1484c653a18ca6bca025fd2d95f597ee1aa78b2a19260`  
		Last Modified: Fri, 21 Mar 2025 17:20:14 GMT  
		Size: 7.0 MB (6968769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5653e26cea4f5a54ef2c6ede76c38669a2538fb625a3ffa5e2e05083dec5bf69`  
		Last Modified: Fri, 21 Mar 2025 17:20:13 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json
