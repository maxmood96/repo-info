## `backdrop:latest`

```console
$ docker pull backdrop@sha256:8327be3edae2db56a990f10c37e316353c239a52592a79df70e2bd16bb120052
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:8705595910be640704aa22ce7b0bf4cf8b8363450161a08c208e514456134f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191751747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83745c25ff2cfc6d3dba9c87f99c55ee5888475b0fd1fb06a7f45187fe8abb1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.25
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cdc4d13cbbd81c4da28f0a5177669fb5f957466c2f904f98496f7ee0b40ef2`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdc707494c42458e3bc8fa49c7d2fb3ba9bf7e0c4167b81ebb7da71e88d578`  
		Last Modified: Mon, 08 Sep 2025 21:46:02 GMT  
		Size: 117.8 MB (117835848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7af854b6e1ae3f00efa46e227cb802e00113099fad0730bf0ea79777571937d`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27844f0bba07885733a1a891137be2bb42e3b0fd74fad355ec9aeff9fe2dce1e`  
		Last Modified: Mon, 08 Sep 2025 21:45:48 GMT  
		Size: 4.2 MB (4223985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57992caed768086a6c0e311f63782c09831610a3e32216259bdd76df6ae08363`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347ae1524e2ad360b24b4ef2387a9461da4891a4b8ef160eae8ec6ad34ca473a`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce000de9ce8887551c23d5c4567a55797742eb3a0e51305c7bc8cf1fc5ef754`  
		Last Modified: Mon, 08 Sep 2025 21:45:47 GMT  
		Size: 12.8 MB (12750151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb1c55e0d2aad7b78b024ae001e27cce8b007128502a87b156bbd9cbdbe485`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b220f5e801fbe37e7f63103f02b4e2a791105442be23ed365551ac089d56cb8`  
		Last Modified: Mon, 08 Sep 2025 21:45:46 GMT  
		Size: 11.7 MB (11705702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39fec0932f30c6ffb2c4b45aff32723c845214ce3c82df80f85e0053d04142d`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9df2d0f46cd215f60de277299b2285ecd1b6d40f305e7d230a2ffe293c65`  
		Last Modified: Mon, 08 Sep 2025 21:45:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d9c4eff296fff77f568ecb99d8c3c58ddf7f4643c37dbc869f973660fef40d`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fea5d06223ba540e4224bafb4f89d219c75cba16d48a33102d681aca5ac412`  
		Last Modified: Mon, 08 Sep 2025 21:45:45 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92d0d5dc401a63e3481c5ba9a9e0f137298b2545abffd1561467c33a2c98bea`  
		Last Modified: Mon, 08 Sep 2025 22:16:51 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79191bc69fc3de58add24433b07f1e3c70db5c01fead88d6453254e7bdf4daf`  
		Last Modified: Tue, 09 Sep 2025 00:30:31 GMT  
		Size: 6.5 MB (6537228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde697ed5f58263f89c8198e5affc53d6f13359cef2e681e73ca9e1f276c6817`  
		Last Modified: Tue, 09 Sep 2025 00:30:20 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084243a4814c0d588a94c5e1f216286fab299b7e6c0d53527f116859523ebaa1`  
		Last Modified: Mon, 08 Sep 2025 22:16:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:1b4f55a12ff35893272619c2cb6ebc17b3cd871d03db42fd35bd26529130c3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8f0e2c68b9adf4163557ef4e2021a92888c1096a6ce76c353c788c8d68d453`

```dockerfile
```

-	Layers:
	-	`sha256:ec5cdde601185decd55e8de20ff0ff3bdd685f6340138a600b9ee165826d24a4`  
		Last Modified: Tue, 09 Sep 2025 00:26:21 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd1e8717c8ee1c76b29193d12cf72a3ba293612551a3098ba5ff552f8c524c8`  
		Last Modified: Tue, 09 Sep 2025 00:26:22 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:5dd9cfb568d6b0121a9d3297f2e743baddc2630d13a6e7696164a9a028e64e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185169207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d12606f1b5a3c2eb1956ea22c2ecf190f6ba0555cf2679288bac8c45254ec88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.25
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee6d029e615fa2b873890f1011a42f1c5f78b2d100eaed3bc1df5bb73d212`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472e922e809f2164e7de33f1a04d157980da1614d66407be60d248980ca8453`  
		Last Modified: Thu, 14 Aug 2025 22:21:38 GMT  
		Size: 110.2 MB (110160334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe053e93cb40a6c44acd9d0ab0ee960880abe08bd106a21947710df1e0399e`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc43ae40cfafdbc816c6ef33e29cb3a5b1fcd866e77ed316da93e7ac7be457bc`  
		Last Modified: Thu, 14 Aug 2025 22:29:04 GMT  
		Size: 4.3 MB (4301251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0c909ee690af4ad403bf2728df6cf54495afc197ec0612503debdb1a0d47a`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5af3640212feddb52a07b6b7e3a5ba254dfe8302593969022dfcddb394f0e87`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b665425619045050bd496d421bb389bb381189ce61fbcb90a9ed9b13c064eb3`  
		Last Modified: Thu, 28 Aug 2025 19:19:37 GMT  
		Size: 12.8 MB (12762710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0198101926bb4f04c6632eff6855a5071dc515932213a0077cb2def736b51`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf76d0197768bd65adb457cbb82cb4fb482866c80dff385a217573fc902f1ab`  
		Last Modified: Thu, 28 Aug 2025 19:19:36 GMT  
		Size: 11.7 MB (11727280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c032600758105559be9ff8daa39cd4c71aa3e63c6c414f5dddd732fee71e83`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293d67932722d7e0c09907e26d6191d6705f486163975a6b7bfec649d2568a3`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf8da13eec602aa9ccdb87b3f45aa250d1f0b365527c81da6408c9af4c058cc`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a91ab10aef2ff2ebae34198ea89776200382dd48b440db97e302b70fbb4822`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0e4c38e4630c74cd7efbbd4b893ae48c419fae980c1aafcfb588324d9921f1`  
		Last Modified: Thu, 28 Aug 2025 20:56:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5733c3d87000975ff1625d7da18eaa2ff15b762caf182fd4db928df18eb015`  
		Last Modified: Thu, 28 Aug 2025 20:56:06 GMT  
		Size: 7.2 MB (7156224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e352b9072ae7eb8abc5fffbff15e738cf610b1258593d781809ce67ad5058a9`  
		Last Modified: Thu, 28 Aug 2025 20:56:07 GMT  
		Size: 8.9 MB (8918324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d5c82e992e8c79d28e8e100290be3cc11006912d2d29503ff9efc2dcf6550c`  
		Last Modified: Thu, 28 Aug 2025 20:56:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:835f6248086fd9a9894e3022b5d86d2d7b37d1c457228d46e3108a6082e1fc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84864734e3aefe8e42ce87c694985bc8d70fb404dcd8ac02dbb558623f2e66`

```dockerfile
```

-	Layers:
	-	`sha256:25cf4043ad3bb3215a5e1a388d3937604f0e7620b185a21b3d794618c289d746`  
		Last Modified: Thu, 28 Aug 2025 21:26:32 GMT  
		Size: 7.6 MB (7557736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbebf5e6a81c34a53181f386092da004390d36a6f7d6f592aba30c3844aab20a`  
		Last Modified: Thu, 28 Aug 2025 21:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
