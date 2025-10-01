<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.32`](#backdrop132)
-	[`backdrop:1.32-apache`](#backdrop132-apache)
-	[`backdrop:1.32-fpm`](#backdrop132-fpm)
-	[`backdrop:1.32.0`](#backdrop1320)
-	[`backdrop:1.32.0-apache`](#backdrop1320-apache)
-	[`backdrop:1.32.0-fpm`](#backdrop1320-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:efcb5b67dc5cfe788a6c50de1354bb284fb9db2fe78664704d37a47dbfc93d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1c2c7981cb5ec8fa47cfe114161cc6aa1ca38d4faece871c67d02e17b73c1bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187960971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e386a2be0714c3dd79c878a6fa40976b658082c630afc1a7a8e45e0f9dc4bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c8d5d12c4f4e5b183ad210abbf8b268ed89f238ed07ab3f341f46f83e960`  
		Last Modified: Tue, 30 Sep 2025 00:03:12 GMT  
		Size: 12.7 MB (12727881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e20d94ccba4ffca89dcdb350e6b67d414553255efa8c6f6194ea5e905c94039`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91963ef564362d3dd0baaef67b7824072036d411e3a21385432900ba6e8c45ed`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 11.9 MB (11895444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec909aac6f2b58383e92aafa39883f94615675d80631e181904013224618f66`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1273b91a8c61380b86d63dfcf114e4fed1fadef7c7d529f69e0dda3beb84818d`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7d9f8cf967757bc2c3cc7d6f14d2eaf29ba8df1dee174ea6265223e34c6c72`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3843e32417c15b13619811ceda2f47119168948a8560d2fa20c61fe4da7d3`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef76cd4f7011324dadbd0b4caefc2c1a4b1c40c35f2d394f44284c71185bd36f`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6538121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160bed861402c1a5b8729a0dd6dd3321a894b4fc036b09f5fb95a428d68ff1c7`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 9.2 MB (9170799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81e45b4ce7778d8afc9f361d512817671d6b60eabf9aff93a17c068a682e96`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ced2e4a4c50281d9a0f46efeedb063b069be812c039ea8baa185d4614cad1685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7c5af65a8cbd9f0de7724afa73e54048961dde246704cd9c34707767e8985`

```dockerfile
```

-	Layers:
	-	`sha256:b888e6be8aac8868cf31c1872e016195f0bb6a891c164a2cc8029ba312fe22cb`  
		Last Modified: Wed, 01 Oct 2025 15:31:10 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a266bec1f159d1ff5fc9748bb27823721281d2af8014cb17a54cda5be7e95a4c`  
		Last Modified: Wed, 01 Oct 2025 15:31:11 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:cf47937ac855341cad4debf0962e215522c180fa1a2ee98984d390cfe32bb1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181294933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c407eed34c4a556eeaa7a171fe2570c32148c5c89cf8f5d59b0945b7ab0acb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93be2c55e921669c0adae9cb6992f46bb5149aa09ab3033b8c4cdf83f0c6aba`  
		Last Modified: Tue, 30 Sep 2025 00:04:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe29501d57f5d808605ef3ac9acc7715b7d8ab4ef10b627878b8c70b3382980`  
		Last Modified: Tue, 30 Sep 2025 00:05:17 GMT  
		Size: 110.2 MB (110163075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cf1cb205b7e33c49926d79bb4fe1ef7155bfa1b8ae0091e695d600095fd612`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2624237b1c9e5f3f9a48802db217dc53ae0d5e6ebe2ac490e020208328dc9b27`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 12.7 MB (12727363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a30b25ff21bc0b72f1f8ebb452eec1188dea0561a39451cefb70f51759d25e`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86221e20127e226b35a60d9368be1148d4476e44f007f42a507dbfb281e1341e`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 11.9 MB (11921370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156aa158931dd3d92d1e6338397acf5c8327c32428a3363014f0d45d812aef9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9d375853ccfb5763c3062a2068ca98110c7b162b135c868cf78103c586f16`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce29fb46f3a8d585a4dc80e9e34ecda6dbd1403ecacde29366e5e563e7d5b9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef90b382693472bc121fa622bd7f30c604980226b20f3e73ff2348d23101f1b`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f104a17f51f3f3363358a7e97c48b29d7c1d81efc2efd199b68a972fb998b9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 7.2 MB (7157401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d182e84dcd8c2f6b548346ff93a00f7f0136bca3615725180511aac6642a257`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 9.2 MB (9170803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515ca905ea2a22830b357e9ae5d64f937e123a85d9d7371a9afdc819e1ad53d`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:103eda938aaaeb3814238d8148bd4e1544e24af232f28e17652a49c4e34e7fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0594adf23bf31f1b561a6f8aaad4dba426075d7e44b05db24dc864ccc16268f`

```dockerfile
```

-	Layers:
	-	`sha256:8df5bd6ca23308f65bb34e43664bdbcd2c3e3a04da24f15d777e82221e68c95d`  
		Last Modified: Wed, 01 Oct 2025 21:26:32 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888250d9cc1faa5afd811d9ba6cee4b50362b7897e65f1bf8fb1af5838886130`  
		Last Modified: Wed, 01 Oct 2025 21:26:33 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-apache`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-fpm`

```console
$ docker pull backdrop@sha256:efcb5b67dc5cfe788a6c50de1354bb284fb9db2fe78664704d37a47dbfc93d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1c2c7981cb5ec8fa47cfe114161cc6aa1ca38d4faece871c67d02e17b73c1bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187960971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e386a2be0714c3dd79c878a6fa40976b658082c630afc1a7a8e45e0f9dc4bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c8d5d12c4f4e5b183ad210abbf8b268ed89f238ed07ab3f341f46f83e960`  
		Last Modified: Tue, 30 Sep 2025 00:03:12 GMT  
		Size: 12.7 MB (12727881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e20d94ccba4ffca89dcdb350e6b67d414553255efa8c6f6194ea5e905c94039`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91963ef564362d3dd0baaef67b7824072036d411e3a21385432900ba6e8c45ed`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 11.9 MB (11895444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec909aac6f2b58383e92aafa39883f94615675d80631e181904013224618f66`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1273b91a8c61380b86d63dfcf114e4fed1fadef7c7d529f69e0dda3beb84818d`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7d9f8cf967757bc2c3cc7d6f14d2eaf29ba8df1dee174ea6265223e34c6c72`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3843e32417c15b13619811ceda2f47119168948a8560d2fa20c61fe4da7d3`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef76cd4f7011324dadbd0b4caefc2c1a4b1c40c35f2d394f44284c71185bd36f`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6538121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160bed861402c1a5b8729a0dd6dd3321a894b4fc036b09f5fb95a428d68ff1c7`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 9.2 MB (9170799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81e45b4ce7778d8afc9f361d512817671d6b60eabf9aff93a17c068a682e96`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ced2e4a4c50281d9a0f46efeedb063b069be812c039ea8baa185d4614cad1685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7c5af65a8cbd9f0de7724afa73e54048961dde246704cd9c34707767e8985`

```dockerfile
```

-	Layers:
	-	`sha256:b888e6be8aac8868cf31c1872e016195f0bb6a891c164a2cc8029ba312fe22cb`  
		Last Modified: Wed, 01 Oct 2025 15:31:10 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a266bec1f159d1ff5fc9748bb27823721281d2af8014cb17a54cda5be7e95a4c`  
		Last Modified: Wed, 01 Oct 2025 15:31:11 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:cf47937ac855341cad4debf0962e215522c180fa1a2ee98984d390cfe32bb1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181294933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c407eed34c4a556eeaa7a171fe2570c32148c5c89cf8f5d59b0945b7ab0acb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93be2c55e921669c0adae9cb6992f46bb5149aa09ab3033b8c4cdf83f0c6aba`  
		Last Modified: Tue, 30 Sep 2025 00:04:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe29501d57f5d808605ef3ac9acc7715b7d8ab4ef10b627878b8c70b3382980`  
		Last Modified: Tue, 30 Sep 2025 00:05:17 GMT  
		Size: 110.2 MB (110163075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cf1cb205b7e33c49926d79bb4fe1ef7155bfa1b8ae0091e695d600095fd612`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2624237b1c9e5f3f9a48802db217dc53ae0d5e6ebe2ac490e020208328dc9b27`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 12.7 MB (12727363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a30b25ff21bc0b72f1f8ebb452eec1188dea0561a39451cefb70f51759d25e`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86221e20127e226b35a60d9368be1148d4476e44f007f42a507dbfb281e1341e`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 11.9 MB (11921370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156aa158931dd3d92d1e6338397acf5c8327c32428a3363014f0d45d812aef9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9d375853ccfb5763c3062a2068ca98110c7b162b135c868cf78103c586f16`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce29fb46f3a8d585a4dc80e9e34ecda6dbd1403ecacde29366e5e563e7d5b9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef90b382693472bc121fa622bd7f30c604980226b20f3e73ff2348d23101f1b`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f104a17f51f3f3363358a7e97c48b29d7c1d81efc2efd199b68a972fb998b9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 7.2 MB (7157401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d182e84dcd8c2f6b548346ff93a00f7f0136bca3615725180511aac6642a257`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 9.2 MB (9170803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515ca905ea2a22830b357e9ae5d64f937e123a85d9d7371a9afdc819e1ad53d`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:103eda938aaaeb3814238d8148bd4e1544e24af232f28e17652a49c4e34e7fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0594adf23bf31f1b561a6f8aaad4dba426075d7e44b05db24dc864ccc16268f`

```dockerfile
```

-	Layers:
	-	`sha256:8df5bd6ca23308f65bb34e43664bdbcd2c3e3a04da24f15d777e82221e68c95d`  
		Last Modified: Wed, 01 Oct 2025 21:26:32 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888250d9cc1faa5afd811d9ba6cee4b50362b7897e65f1bf8fb1af5838886130`  
		Last Modified: Wed, 01 Oct 2025 21:26:33 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0-apache`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0-fpm`

```console
$ docker pull backdrop@sha256:efcb5b67dc5cfe788a6c50de1354bb284fb9db2fe78664704d37a47dbfc93d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1c2c7981cb5ec8fa47cfe114161cc6aa1ca38d4faece871c67d02e17b73c1bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187960971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e386a2be0714c3dd79c878a6fa40976b658082c630afc1a7a8e45e0f9dc4bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c8d5d12c4f4e5b183ad210abbf8b268ed89f238ed07ab3f341f46f83e960`  
		Last Modified: Tue, 30 Sep 2025 00:03:12 GMT  
		Size: 12.7 MB (12727881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e20d94ccba4ffca89dcdb350e6b67d414553255efa8c6f6194ea5e905c94039`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91963ef564362d3dd0baaef67b7824072036d411e3a21385432900ba6e8c45ed`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 11.9 MB (11895444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec909aac6f2b58383e92aafa39883f94615675d80631e181904013224618f66`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1273b91a8c61380b86d63dfcf114e4fed1fadef7c7d529f69e0dda3beb84818d`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7d9f8cf967757bc2c3cc7d6f14d2eaf29ba8df1dee174ea6265223e34c6c72`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3843e32417c15b13619811ceda2f47119168948a8560d2fa20c61fe4da7d3`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef76cd4f7011324dadbd0b4caefc2c1a4b1c40c35f2d394f44284c71185bd36f`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6538121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160bed861402c1a5b8729a0dd6dd3321a894b4fc036b09f5fb95a428d68ff1c7`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 9.2 MB (9170799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81e45b4ce7778d8afc9f361d512817671d6b60eabf9aff93a17c068a682e96`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ced2e4a4c50281d9a0f46efeedb063b069be812c039ea8baa185d4614cad1685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7c5af65a8cbd9f0de7724afa73e54048961dde246704cd9c34707767e8985`

```dockerfile
```

-	Layers:
	-	`sha256:b888e6be8aac8868cf31c1872e016195f0bb6a891c164a2cc8029ba312fe22cb`  
		Last Modified: Wed, 01 Oct 2025 15:31:10 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a266bec1f159d1ff5fc9748bb27823721281d2af8014cb17a54cda5be7e95a4c`  
		Last Modified: Wed, 01 Oct 2025 15:31:11 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:cf47937ac855341cad4debf0962e215522c180fa1a2ee98984d390cfe32bb1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181294933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c407eed34c4a556eeaa7a171fe2570c32148c5c89cf8f5d59b0945b7ab0acb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93be2c55e921669c0adae9cb6992f46bb5149aa09ab3033b8c4cdf83f0c6aba`  
		Last Modified: Tue, 30 Sep 2025 00:04:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe29501d57f5d808605ef3ac9acc7715b7d8ab4ef10b627878b8c70b3382980`  
		Last Modified: Tue, 30 Sep 2025 00:05:17 GMT  
		Size: 110.2 MB (110163075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cf1cb205b7e33c49926d79bb4fe1ef7155bfa1b8ae0091e695d600095fd612`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2624237b1c9e5f3f9a48802db217dc53ae0d5e6ebe2ac490e020208328dc9b27`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 12.7 MB (12727363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a30b25ff21bc0b72f1f8ebb452eec1188dea0561a39451cefb70f51759d25e`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86221e20127e226b35a60d9368be1148d4476e44f007f42a507dbfb281e1341e`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 11.9 MB (11921370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156aa158931dd3d92d1e6338397acf5c8327c32428a3363014f0d45d812aef9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9d375853ccfb5763c3062a2068ca98110c7b162b135c868cf78103c586f16`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce29fb46f3a8d585a4dc80e9e34ecda6dbd1403ecacde29366e5e563e7d5b9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef90b382693472bc121fa622bd7f30c604980226b20f3e73ff2348d23101f1b`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f104a17f51f3f3363358a7e97c48b29d7c1d81efc2efd199b68a972fb998b9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 7.2 MB (7157401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d182e84dcd8c2f6b548346ff93a00f7f0136bca3615725180511aac6642a257`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 9.2 MB (9170803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515ca905ea2a22830b357e9ae5d64f937e123a85d9d7371a9afdc819e1ad53d`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:103eda938aaaeb3814238d8148bd4e1544e24af232f28e17652a49c4e34e7fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0594adf23bf31f1b561a6f8aaad4dba426075d7e44b05db24dc864ccc16268f`

```dockerfile
```

-	Layers:
	-	`sha256:8df5bd6ca23308f65bb34e43664bdbcd2c3e3a04da24f15d777e82221e68c95d`  
		Last Modified: Wed, 01 Oct 2025 21:26:32 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888250d9cc1faa5afd811d9ba6cee4b50362b7897e65f1bf8fb1af5838886130`  
		Last Modified: Wed, 01 Oct 2025 21:26:33 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:efcb5b67dc5cfe788a6c50de1354bb284fb9db2fe78664704d37a47dbfc93d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1c2c7981cb5ec8fa47cfe114161cc6aa1ca38d4faece871c67d02e17b73c1bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187960971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e386a2be0714c3dd79c878a6fa40976b658082c630afc1a7a8e45e0f9dc4bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c8d5d12c4f4e5b183ad210abbf8b268ed89f238ed07ab3f341f46f83e960`  
		Last Modified: Tue, 30 Sep 2025 00:03:12 GMT  
		Size: 12.7 MB (12727881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e20d94ccba4ffca89dcdb350e6b67d414553255efa8c6f6194ea5e905c94039`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91963ef564362d3dd0baaef67b7824072036d411e3a21385432900ba6e8c45ed`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 11.9 MB (11895444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec909aac6f2b58383e92aafa39883f94615675d80631e181904013224618f66`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1273b91a8c61380b86d63dfcf114e4fed1fadef7c7d529f69e0dda3beb84818d`  
		Last Modified: Tue, 30 Sep 2025 00:03:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7d9f8cf967757bc2c3cc7d6f14d2eaf29ba8df1dee174ea6265223e34c6c72`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3843e32417c15b13619811ceda2f47119168948a8560d2fa20c61fe4da7d3`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef76cd4f7011324dadbd0b4caefc2c1a4b1c40c35f2d394f44284c71185bd36f`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6538121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160bed861402c1a5b8729a0dd6dd3321a894b4fc036b09f5fb95a428d68ff1c7`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 9.2 MB (9170799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81e45b4ce7778d8afc9f361d512817671d6b60eabf9aff93a17c068a682e96`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ced2e4a4c50281d9a0f46efeedb063b069be812c039ea8baa185d4614cad1685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7c5af65a8cbd9f0de7724afa73e54048961dde246704cd9c34707767e8985`

```dockerfile
```

-	Layers:
	-	`sha256:b888e6be8aac8868cf31c1872e016195f0bb6a891c164a2cc8029ba312fe22cb`  
		Last Modified: Wed, 01 Oct 2025 15:31:10 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a266bec1f159d1ff5fc9748bb27823721281d2af8014cb17a54cda5be7e95a4c`  
		Last Modified: Wed, 01 Oct 2025 15:31:11 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:cf47937ac855341cad4debf0962e215522c180fa1a2ee98984d390cfe32bb1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181294933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c407eed34c4a556eeaa7a171fe2570c32148c5c89cf8f5d59b0945b7ab0acb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93be2c55e921669c0adae9cb6992f46bb5149aa09ab3033b8c4cdf83f0c6aba`  
		Last Modified: Tue, 30 Sep 2025 00:04:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe29501d57f5d808605ef3ac9acc7715b7d8ab4ef10b627878b8c70b3382980`  
		Last Modified: Tue, 30 Sep 2025 00:05:17 GMT  
		Size: 110.2 MB (110163075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cf1cb205b7e33c49926d79bb4fe1ef7155bfa1b8ae0091e695d600095fd612`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2624237b1c9e5f3f9a48802db217dc53ae0d5e6ebe2ac490e020208328dc9b27`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 12.7 MB (12727363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a30b25ff21bc0b72f1f8ebb452eec1188dea0561a39451cefb70f51759d25e`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86221e20127e226b35a60d9368be1148d4476e44f007f42a507dbfb281e1341e`  
		Last Modified: Tue, 30 Sep 2025 00:05:10 GMT  
		Size: 11.9 MB (11921370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156aa158931dd3d92d1e6338397acf5c8327c32428a3363014f0d45d812aef9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9d375853ccfb5763c3062a2068ca98110c7b162b135c868cf78103c586f16`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce29fb46f3a8d585a4dc80e9e34ecda6dbd1403ecacde29366e5e563e7d5b9`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef90b382693472bc121fa622bd7f30c604980226b20f3e73ff2348d23101f1b`  
		Last Modified: Tue, 30 Sep 2025 00:05:09 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f104a17f51f3f3363358a7e97c48b29d7c1d81efc2efd199b68a972fb998b9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 7.2 MB (7157401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d182e84dcd8c2f6b548346ff93a00f7f0136bca3615725180511aac6642a257`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 9.2 MB (9170803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515ca905ea2a22830b357e9ae5d64f937e123a85d9d7371a9afdc819e1ad53d`  
		Last Modified: Tue, 30 Sep 2025 01:01:24 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:103eda938aaaeb3814238d8148bd4e1544e24af232f28e17652a49c4e34e7fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0594adf23bf31f1b561a6f8aaad4dba426075d7e44b05db24dc864ccc16268f`

```dockerfile
```

-	Layers:
	-	`sha256:8df5bd6ca23308f65bb34e43664bdbcd2c3e3a04da24f15d777e82221e68c95d`  
		Last Modified: Wed, 01 Oct 2025 21:26:32 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888250d9cc1faa5afd811d9ba6cee4b50362b7897e65f1bf8fb1af5838886130`  
		Last Modified: Wed, 01 Oct 2025 21:26:33 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:661876a0a40ee920e4e45ce1e84f81f5f8107493ecd49ad150488952ef03a33f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:964863b65d3e6e2769f147be213c3f8b345b8a444759f9032635cccda3d85bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192011250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b4cbf74ebe34e1a0a72ad7db2119d509cfb7f5d2a6dbdb4718a40164d6337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5ad0f09b60528473481c46ba7354a807c85f60e1ba774062697f9d15e8d48`  
		Last Modified: Tue, 30 Sep 2025 03:18:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0b9d8e50512a02c37ef77e751711c494f71137b783dc0110c1bf5a896212e`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 6.5 MB (6537490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff901e5e78af6c02ac649aaf89e73af9f31d241450fbfa66062336fe0a1671d2`  
		Last Modified: Tue, 30 Sep 2025 03:18:05 GMT  
		Size: 9.2 MB (9170797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b7df351c5c996affd5cb4b8729e570576c0ea7b0287785a99313e6256325e`  
		Last Modified: Tue, 30 Sep 2025 03:18:04 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:125a2c8fabcd314574e0155ea4afabd4d4d96740846c848be776cd6897323656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8c4e68747619706598b7085003b2fbb4cb549e7ea0ab8cb1d349d0fee0fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e154fb7e74ebef7612dad063940658e7b02a188c16fb49a703e9e57611c273a9`  
		Last Modified: Wed, 01 Oct 2025 15:31:01 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2348b3b3dd591039bfc197e4a00e7540ffe4dd07f3a13d99f44fa8277f0c7b`  
		Last Modified: Wed, 01 Oct 2025 15:31:02 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b6472d08c0ad174fd36754c5e1a654205258a776f8e53179a21beba4c5de2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185419072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df473c0b962d85af247187a1e890fd25a4ba958891674da5bb781f5335c5069`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 18 Sep 2025 23:57:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59290f42487426698e63cc38dbe0601e098c992d4056f5b8733a574a20d5cef1`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daab96e96a2689e6ab9231931f647a5653cfa050cd761a1a97ab4a32c81865a`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 7.2 MB (7157097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07a8b9b3081c0f6e42c3006ead8902707fdac8b0479fcc8cda57b412de8633`  
		Last Modified: Tue, 30 Sep 2025 01:01:20 GMT  
		Size: 9.2 MB (9170798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77496ebfe9e06dff19d760fdb42908cbc979fd61bfddd7be21e78d66a9fb4670`  
		Last Modified: Tue, 30 Sep 2025 01:01:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:c48fa0540261407acbb5ff5673e9629bfc091549d809c2c575e53334c64d4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d455882ea8a6610a579c81cd4635891e23ad8506d4721dd92001af21e0c48c4e`

```dockerfile
```

-	Layers:
	-	`sha256:0502f8b5fc2ab6401ed25f23aa89928b5c424169d452887fce5190100bbf2a26`  
		Last Modified: Wed, 01 Oct 2025 21:26:24 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41791df8ae420ccb2d5af8ac561265a8d603e8a36acf905f43af195cad7eb6`  
		Last Modified: Wed, 01 Oct 2025 21:26:25 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
