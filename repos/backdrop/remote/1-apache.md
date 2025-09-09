## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:880534fd465faf6046ee4812b8d8e765311d1022c15060642ad6ef4482f774bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

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

### `backdrop:1-apache` - unknown; unknown

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

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:54ac50d580172857acc6f2b48c7ba603ef2d371fd23e24bf4b255beca71f619b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185159908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6625a8c69350e135a2f1bfe854d879b1733af9ae9311aace45eee1c1ca12f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d62e0cfec9e84e4c3af62f0e2e2f35c0d2b43776e0f833da3bb1be361cef4b`  
		Last Modified: Mon, 08 Sep 2025 22:14:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01edce4cbf0eb2422cf320a499e3b79c2b8237c137a53b113d579a5079ca90d`  
		Last Modified: Mon, 08 Sep 2025 23:09:38 GMT  
		Size: 110.2 MB (110161594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3045fc49f81a1dc00369aac03359529eeceb6141a4335e5cf67a2a71d0c9046`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f798154dd6fce77d2fda99f17287d5cbcac140ce8d069be9a3ad9e4b4a8e2c`  
		Last Modified: Mon, 08 Sep 2025 23:09:33 GMT  
		Size: 4.3 MB (4302084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814c501dc5d5abd4e8a7fff4679a23804a4383866bffc576977ba3017b57c1cf`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9756904f2d1aee01dad39ac804538f982c188a36ad0e860f15f719123765b`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7ae7be6e677d55eef1a130c06e0667ee9370dee36be98d1989329d3d43c22`  
		Last Modified: Mon, 08 Sep 2025 23:09:35 GMT  
		Size: 12.7 MB (12749794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81dcdc4b950a19ba0fda7e25ec63befefb818fea05e64d6883fb99f7c5c734`  
		Last Modified: Mon, 08 Sep 2025 22:14:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ac0322045582a5bb10d59cf3096964f451c306080af8906ed6b69ea5b6640`  
		Last Modified: Mon, 08 Sep 2025 23:09:37 GMT  
		Size: 11.7 MB (11727427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25ab495860ad5fb7e2197a0b251a9f46d6a1bde9f3ac630482717c15e49cf6`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf1b55fb275dd6dc7c3058024831c1d0b53f9f81a300e2990c881dbd34fa9e5`  
		Last Modified: Mon, 08 Sep 2025 22:14:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d379843f75a8a85f56c33ddd4e93b94fe7f8096fcab3b1d668282330fac61b3`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7365f6418e40a65d1389c06c279bd3d578b92c67936775d8cabf7198d9ac3da`  
		Last Modified: Mon, 08 Sep 2025 22:14:30 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b30c863f4689b097b1d4ec9ba2f591c319ab39d4233a936e8a1551c462da3d`  
		Last Modified: Tue, 09 Sep 2025 02:05:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6465b4b511ab35931592da919d40a991ad511fa349aefeaa36a22cd8bdc53fab`  
		Last Modified: Tue, 09 Sep 2025 03:43:04 GMT  
		Size: 7.2 MB (7157031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9f758cde0fb35a8ee84b77521c4e5aa3400ff11e68170fe596b74deba9fd38`  
		Last Modified: Tue, 09 Sep 2025 03:43:07 GMT  
		Size: 8.9 MB (8918336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7f58a8632dc9cf1ba38b1ec51ed6f061958dee4be68e6ebbece517691d3189`  
		Last Modified: Tue, 09 Sep 2025 02:04:58 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:acd9f1dc63b0e3298728853cfdcf98602ec252bdf7fa13ea543ed422b6a4b15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2ff5acd3facb0689822af2123cf96343af16241cbf65bd501e84e7c548be50`

```dockerfile
```

-	Layers:
	-	`sha256:71b8249333a8a49eacfab973c43166f066356c3038d3586124ec67438ea9ced5`  
		Last Modified: Tue, 09 Sep 2025 03:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3b4489affc521619540532e379d0b46376848b49d84d6c26ec1d6d3722a70a`  
		Last Modified: Tue, 09 Sep 2025 03:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
