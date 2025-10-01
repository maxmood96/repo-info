## `backdrop:latest`

```console
$ docker pull backdrop@sha256:8992a3441235fbcb4c62d84e47c29a76b0bc9acd6fa6d7bbc9dd33b1e8a0bd44
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
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
