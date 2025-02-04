## `php:8-apache-bullseye`

```console
$ docker pull php@sha256:0eec2a2e1e19b3172f69769680f52d547c5468ade20b440ec415bbf7e67a6b2f
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

### `php:8-apache-bullseye` - linux; amd64

```console
$ docker pull php@sha256:58a42c293b843164e373a9ab4228132ff8007f4c430e934251f3df45ac5e7ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168539328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04516124bb48393f22f262edf01e71dc83e4734b15a6ce20fb3c9c1caa1219e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ae7c3599e1506da86bf202d8880c5e348d436cdb0b0417f0480d8a1db3147f`  
		Last Modified: Fri, 17 Jan 2025 17:33:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e28ff7f1ae33e5c972ed530bf75085c0dbb9b48164d2884566c3e6170f7a76`  
		Last Modified: Fri, 17 Jan 2025 17:33:28 GMT  
		Size: 91.4 MB (91447946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a38dc4eb8d6d2a53e9347fefc1a0b308683caeba6ed8e77d6076b2db8a97da`  
		Last Modified: Fri, 17 Jan 2025 17:33:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30ccf3d3b62033bd03e2bde45bd29561b4597aa5ce8923261fb5fdad208a34`  
		Last Modified: Fri, 17 Jan 2025 17:33:27 GMT  
		Size: 19.1 MB (19064410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04d86f229d4eedeae8483dc9504d8f4d295093f76f44d126cca6f29d51bee79`  
		Last Modified: Fri, 17 Jan 2025 17:33:27 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b32967bfbe067906703992f6b30e6ca1c7bac619aae25db1d061884d36920`  
		Last Modified: Fri, 17 Jan 2025 17:33:27 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce3351cc12b66ad9a92e211033bea6671a11a6964567bc9f4e87899c310eb1`  
		Last Modified: Fri, 17 Jan 2025 17:33:28 GMT  
		Size: 13.7 MB (13695812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3a6fb8d21806b5b00c49ddf7bdd351f2a91d7056b68d33a1163a105a02eb3`  
		Last Modified: Fri, 17 Jan 2025 17:33:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f60f205be141d364763ef561968bf3dcf1b13e510724554afc8a7f46e8671`  
		Last Modified: Fri, 17 Jan 2025 17:33:29 GMT  
		Size: 14.1 MB (14073025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c77af01e59d8fe747c269c605877dc8b37996874075ab22282ac80c8ac6f42`  
		Last Modified: Fri, 17 Jan 2025 17:33:29 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ff8c43023c525366150686d6a1be8bce58f0900dbbf2d2dbeffe0ac487bb7`  
		Last Modified: Fri, 17 Jan 2025 17:33:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a59f49f9a942a921911ba5c1a7902d52ffaabf09b8dbac1b941eb805cce7f2`  
		Last Modified: Fri, 17 Jan 2025 17:33:29 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:103185265539f087e0beec7137401d57495056b180911e80ea0afc85021e1888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6978758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4139b32d6da805a7fb0d99132f3da2bb5d97034124259a28759228a1efc66ba`

```dockerfile
```

-	Layers:
	-	`sha256:96fcfc764004ec5dfbb73e22611fd43d31c47d012e5a7cdae86b46fce30e0fcc`  
		Last Modified: Fri, 17 Jan 2025 17:33:26 GMT  
		Size: 6.9 MB (6920799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b367860bdb6252c326bf8b469f88de95a450efbffd7b504778f484c9a3a6cd9`  
		Last Modified: Fri, 17 Jan 2025 17:33:26 GMT  
		Size: 58.0 KB (57959 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:260af8f9de08ab41acf8c7acdf6bcba1f199bbe62795e9e9bcf725b306c14b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138420592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90855a2be0db8718d13147fa908c16666a5585879a24183d20b5fcfd95464b4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93b737d9d37bd60c8605bf5c054750994a7d9bf9fcc44b376fd7249244abcf`  
		Last Modified: Tue, 14 Jan 2025 03:05:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69002742768de244d879a330315c30a076fb9fcc3e1b1e78748310f0f812a011`  
		Last Modified: Tue, 14 Jan 2025 03:05:18 GMT  
		Size: 69.1 MB (69119271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d38aa9fbc72534a04c8660b325338232f5eb41922619c41d2da02e32be09f`  
		Last Modified: Tue, 14 Jan 2025 03:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d381428a32e48a4dacfb792b90ceb4859009d8322b4c823148b3c11278d860`  
		Last Modified: Tue, 14 Jan 2025 03:09:07 GMT  
		Size: 17.8 MB (17816926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da83c3ff0e0a02d19d985ffeb6d447515b1a45ddb914e5f5b8db25a9475b28b7`  
		Last Modified: Tue, 14 Jan 2025 03:09:06 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406cb131443e28e5ddd0271f39bce06e38e241b3c07789009c159243754ec80`  
		Last Modified: Tue, 14 Jan 2025 03:09:06 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc5e2c26dec6bb7d9d039d18c1a275ab4e7ba08cb5ed59520ee8be0160f24c9`  
		Last Modified: Fri, 17 Jan 2025 18:03:25 GMT  
		Size: 13.7 MB (13694507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1a39612d86b3ead64251a1bf38a0055f4d82259c943467bed07255d03f8809`  
		Last Modified: Fri, 17 Jan 2025 18:03:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d17a500a8fdb9f162b071157a76b246b585555bf6a77c22d863ab7448d601`  
		Last Modified: Fri, 17 Jan 2025 18:03:25 GMT  
		Size: 12.3 MB (12250452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a94c7c7d82242f908c26f43dc0b4f109f3e301e734e6338f23a6d23d2965ffa`  
		Last Modified: Fri, 17 Jan 2025 18:03:25 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0a01eea8603d7182a2296605a3941afd6ff5152e3408529b9cc88520ecd262`  
		Last Modified: Fri, 17 Jan 2025 18:03:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d54e48a44e6c6f087a8d267bd6da5d220e51bb862b3e2d13bac28aaf4c419b`  
		Last Modified: Fri, 17 Jan 2025 18:03:26 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:94580ec2a77ac899444e65f488d912bee97ac84f9ac6407e6775482a1fb3300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29aa718a6016326b41f30ec8792b25ca7a28b74f216514783d8695ed97cb87c`

```dockerfile
```

-	Layers:
	-	`sha256:097cafb97394662fd265ee831735725852f3bca3a74fac167b0e8cb9f260766a`  
		Last Modified: Fri, 17 Jan 2025 18:03:25 GMT  
		Size: 6.7 MB (6729677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e434f31484ae813be467e5c86d2d97aaa322241a228e6247c5bbb5cb40788155`  
		Last Modified: Fri, 17 Jan 2025 18:03:24 GMT  
		Size: 58.1 KB (58139 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:75753a585502d8c2e3a886a1d5318aee9d8b52da3756ebcef07e0662e50cf568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161926550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f72e9616f5e54fe6a374a6b8f6840fb6d72f2223a48faa5289ee91a8af1fc9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f4885259ede04563f6f2c30252c470e94aaf9a95576060866ba0ca177a1b8`  
		Last Modified: Tue, 14 Jan 2025 03:28:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a0cfe9d2540e4d05e8198913405c46a9a624800b104db09fb49ea98a3d13e`  
		Last Modified: Tue, 14 Jan 2025 03:28:44 GMT  
		Size: 86.7 MB (86734429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3d3d9ba2fe6d1d3be940377c1fbbc1ab8489811531766e34900760d284128`  
		Last Modified: Tue, 14 Jan 2025 03:28:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c923b39f54480f3a20810f28af32065e592d86c00de5675982c0422bb66834`  
		Last Modified: Tue, 14 Jan 2025 03:32:03 GMT  
		Size: 19.0 MB (18981074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d134300fb349a1728b952680f10df7127ad15d99f9b83abb53bff34681c18`  
		Last Modified: Tue, 14 Jan 2025 03:32:02 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d8698a8d76fca233223fa1f9a58732bda7d6730214a75abb3876ed9b301b6c`  
		Last Modified: Tue, 14 Jan 2025 03:32:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca706ad71b14dad018e3927a9d7c03265478135486d97728c82dd4665e8c1d3`  
		Last Modified: Fri, 17 Jan 2025 17:48:01 GMT  
		Size: 13.7 MB (13695178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc627957c46b91ed8d74aab3d968b8862c4d46cdfd745bd5f04e2650beb05985`  
		Last Modified: Fri, 17 Jan 2025 17:48:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b919ca81e60980058d3c54021153fa376066108a9a32f35aca2c4ecc60dc8`  
		Last Modified: Fri, 17 Jan 2025 17:48:01 GMT  
		Size: 13.8 MB (13765473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6fe26b8b64db4fa01cd538e557c832434f24be017b8f10f6126e410d2ad4b9`  
		Last Modified: Fri, 17 Jan 2025 17:48:00 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c03560fbc3d1f967e81a84fed993074cf2dd9efb84a671f265c0b36c7f733f`  
		Last Modified: Fri, 17 Jan 2025 17:48:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6e29e08e0a88ed67e818e42aebe1f63479b35430e277e6bc0b45609b80c9b8`  
		Last Modified: Fri, 17 Jan 2025 17:48:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:d922b3c59693f96e98d86c81bde8901422e96b2541825d992ab473901e186562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8df92fec307b5f3be025b3cb52be6b0e6e311e9677f0960d8e37f4ac0b4e87d`

```dockerfile
```

-	Layers:
	-	`sha256:ffd5f3c1491a67b8aea3674248686eca1821a57191936afa139b168937afa122`  
		Last Modified: Fri, 17 Jan 2025 17:48:00 GMT  
		Size: 6.9 MB (6923589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af518aa5929a553f0e107a27186f18e1bee7ef5083b1b9f382629f677966174c`  
		Last Modified: Fri, 17 Jan 2025 17:48:00 GMT  
		Size: 58.2 KB (58183 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bullseye` - linux; 386

```console
$ docker pull php@sha256:8ce88cec7b3aa7b6afa897b4249ff63091df72a7d59577fd9a38852c6d6756ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa87a87135e31bf1e4dd6ba2f1ef785f27c7de12d3567d7c96f4c4f67b31ac9f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 17 Jan 2025 01:46:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 17 Jan 2025 01:46:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 17 Jan 2025 01:46:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a95bfd2400fb8bae27cfb223ed56cef7d19535fb6ef0a4024a0fe1516ce3d`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6e1449c3bcd29891e945c871253734a3608209e497c9de6e6a73fb4e35326a`  
		Last Modified: Tue, 04 Feb 2025 04:31:52 GMT  
		Size: 92.5 MB (92521124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f338a9878767a77c6c8ab62cc75ab8bae00740814dd4d67737f6adfc2bec99`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639d3ad3410b05f191c2da23f894c97defc25fde6c4de3bc20e0d51246841c8f`  
		Last Modified: Tue, 04 Feb 2025 04:31:51 GMT  
		Size: 19.6 MB (19552806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a05151ce484ac34ff4423740f9d7de71b657cc4484a2f1b69d05fd170129ed`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c56e93dfc888d28c619159dfe5aa5d0f63add8d8b7667c86eea7aa7eb199491`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa4266c300ca7c7db1029bd57af40d6f4870419bed9a3f80e0ba602454a26fa`  
		Last Modified: Tue, 04 Feb 2025 04:31:52 GMT  
		Size: 13.7 MB (13695197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad9bc9264caed66ff6f68445fd0984a37dbd493e12ed255710e4aab480664f3`  
		Last Modified: Tue, 04 Feb 2025 04:31:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead1f9b5f3b687bf9e7934bd2d50f46429c3a02b7c6c92b7809929b750287aed`  
		Last Modified: Tue, 04 Feb 2025 04:31:52 GMT  
		Size: 14.4 MB (14355569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11735f50401fee6dcce6ffea15bbad6ef3e1e77770c46cc7973e434c571539e1`  
		Last Modified: Tue, 04 Feb 2025 04:31:52 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ac69b15dcdb5805fa1af640e0ad137cc98ffcaf306626c079d1fb108796467`  
		Last Modified: Tue, 04 Feb 2025 04:31:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e61e64465647bf4d997737ebebc7b53589363d6bc610b489c33aa9d1fd6a7c7`  
		Last Modified: Tue, 04 Feb 2025 04:31:53 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:2b446f2257eff669958b82f2541dfae9a3796eba17bf5c1015c5b567b732c6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89815208519ef332025e0ff68f65a038bfa45edde6993969908da1d0b5e37358`

```dockerfile
```

-	Layers:
	-	`sha256:609ba340399155683a10e46b055e6ce7da4354cc65edb1f205f0fa0bd3e6ac3e`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 6.9 MB (6911419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eadb4b19c9beb105df3ccf1f64beaa921589a465a9df2a87a43433b125649ca`  
		Last Modified: Tue, 04 Feb 2025 04:31:50 GMT  
		Size: 57.9 KB (57911 bytes)  
		MIME: application/vnd.in-toto+json
