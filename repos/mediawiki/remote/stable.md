## `mediawiki:stable`

```console
$ docker pull mediawiki@sha256:efef9c630d7b27afce6f208290c1f9e20e0321c2d0522a087121c0df7c921a4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mediawiki:stable` - linux; amd64

```console
$ docker pull mediawiki@sha256:9ae9a3b812783fbdec6aaf860625984d878dd87b72a2c6d1d89a728667b4fffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329883496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3823ed7e2a842de323664ed4914ec7ce3fc7191e086ed0e1743581fa0691921a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:23:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:23:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:23:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:23:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:23:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:23:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:23:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:27:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:27:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:27:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:27:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:27:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:29:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:29:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:29:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:29:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:29:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:29:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:29:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:29:54 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:29:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:29:54 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 20:34:21 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:35:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:35:29 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Fri, 08 May 2026 20:35:29 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Fri, 08 May 2026 20:35:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:35:29 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 08 May 2026 20:35:47 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Fri, 08 May 2026 20:35:47 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Fri, 08 May 2026 20:35:47 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:35:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c83a3a383680230e9fea033b69c5d9f72dbe1ec990c01340a9e24c804eadc4`  
		Last Modified: Fri, 08 May 2026 19:26:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218ef6f07cc82b6756f78b73613caf8e8d76ffc0ba94916d9cc87d9b6724a78c`  
		Last Modified: Fri, 08 May 2026 19:26:50 GMT  
		Size: 117.8 MB (117843017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c445e431149c32e999b77cb275ff826e31107d446449bb8f86e95f98650839f`  
		Last Modified: Fri, 08 May 2026 19:26:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44505f1315cff9836388c3b1e713f1841e2bffd85e8092f7f5efd44f869fd439`  
		Last Modified: Fri, 08 May 2026 19:30:05 GMT  
		Size: 4.2 MB (4228086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b8ca23768a1ad71e0e3df6517ab8b97d798b324af15c95700945c6f622d599`  
		Last Modified: Fri, 08 May 2026 19:30:05 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61b9621690d97db32e130338f1f3517290a28cf66d37c296ab4bfef34fc227a`  
		Last Modified: Fri, 08 May 2026 19:30:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5f325922e0b6e408006480178a2cd1cba49c82f8d02daf89760829cba51dd9`  
		Last Modified: Fri, 08 May 2026 19:30:06 GMT  
		Size: 12.8 MB (12769969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331aed9a0eed06b05cbaeac3236d7136321f39ee6bd6923749aab3f167b640fc`  
		Last Modified: Fri, 08 May 2026 19:30:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5a7f2359a5c667fbce4fe58597a6f863d336c0c07fc7d1c2a92e7925501f05`  
		Last Modified: Fri, 08 May 2026 19:30:07 GMT  
		Size: 11.7 MB (11715235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f09c012430d2ee9c9a806e3d3c3f05d366f65b4f1e0b81dbf725f1df09dfd96`  
		Last Modified: Fri, 08 May 2026 19:30:07 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4127ce68fda19c4ddf5717bfd8ef1ea2cffe2c3950e257a5ae8e7d8c998e1d`  
		Last Modified: Fri, 08 May 2026 19:30:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dccb04f243a57a3eaa17e37b375acc4f38f86bbe7b77fb2b1b08746e96e5a63`  
		Last Modified: Fri, 08 May 2026 19:30:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d38cf195bef8219457c88c4902d77c7ac019babf19deab06c7d16ca75ea3c`  
		Last Modified: Fri, 08 May 2026 19:30:08 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f5d19d32eba57b6337a1cf800ef61bfa0c0847a480881b7c5d51e9f8f21de`  
		Last Modified: Fri, 08 May 2026 20:36:05 GMT  
		Size: 52.9 MB (52931644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49f886bbc020064818b8cac39b696f9a9fdb92c28201bb7d6063fd6d7e8edf`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 17.8 MB (17810854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4cd962c780a13d6d150fd49179a7347903b0ead66320a053006b2b36dc5631`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e712b2d16fba99cb6e2db10c7e29244ad83a564376e0c8a9e1df63a531135`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baac0d410ecc63c8f3dcead9977fe7d9dae9f505a16b0bb5fbabc3fbd145a33e`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b313a2ee37f5578c68b34bc77553ea8d01f5ac0632092cd8ce1fa4de8dcac6`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4ead1a26c51561653a78198f06f72d216fed3f9a6fcc3f5cd66f3005b3fec5`  
		Last Modified: Fri, 08 May 2026 20:36:08 GMT  
		Size: 82.8 MB (82796798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:de2b17bea594a15339083d2041e93bc2dc772b8e9cdae3b616789b7644f4a666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be1fa6bbe11c9132dc992907fe1f6f259274453ab6e95a8a75e4e4f33edfc2e`

```dockerfile
```

-	Layers:
	-	`sha256:d94c77b5caa6818d1c81439a501468f821ee56b245cb4d5625ba923366a090ac`  
		Last Modified: Fri, 08 May 2026 20:36:02 GMT  
		Size: 49.1 KB (49056 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm variant v5

```console
$ docker pull mediawiki@sha256:96dfbd8c267538714b68b08a5a9fc9aafe9483eb8200b8ad7c26deb84872569e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300601099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20c0a2a6ca32e6aea1763123d6127355a354f195b1beb7ede9aa4addcc83c22`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:26:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:34:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:34:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:34:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:34:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 20:34:52 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 20:35:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 20:35:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:38:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 20:38:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:38:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:38:05 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 20:38:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:38:06 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:38:06 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:38:06 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 22:01:25 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:02:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:02:43 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Fri, 08 May 2026 22:02:43 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Fri, 08 May 2026 22:02:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 22:02:43 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 08 May 2026 22:03:05 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Fri, 08 May 2026 22:03:05 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Fri, 08 May 2026 22:03:05 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:03:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511af6baa2f48bf33f9c4bd0427a099fbf81e5d701075fd97b994061983a18e4`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7ef76a330b432d5971e4c9740e5711104085d0afaa75d9a5290e53c0656fc9`  
		Last Modified: Fri, 08 May 2026 20:31:03 GMT  
		Size: 94.9 MB (94885690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602019c031a62f9408c6238e8aeb210d54b3d18a4616365625bf4fc3519469b6`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b984c2bdf0fa9c0deafd5575a40acba95a03385b3a4bbccd25ea235981296984`  
		Last Modified: Fri, 08 May 2026 20:38:16 GMT  
		Size: 4.1 MB (4090186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c2e7ec4f9bb84657ce706f20ab548407b37345f35a7f4af75f60c7112d4f54`  
		Last Modified: Fri, 08 May 2026 20:38:16 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e4cf5ccb91b59bb8db35dfcdf53aa68cebce5ad0d4d9825882fc5c1ff8b49a`  
		Last Modified: Fri, 08 May 2026 20:38:16 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2146ce39df987db4cd517b48b858ec62043d5ff32eeee1f160f118409a4fd`  
		Last Modified: Fri, 08 May 2026 20:38:17 GMT  
		Size: 12.8 MB (12767541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23584c80a19f63d1797d4549946df8c4fe92ed4eb4f5bee47e359ddc30a0036`  
		Last Modified: Fri, 08 May 2026 20:38:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bef09a0c495a54b65a7bdbe873d983074ad35c75934392d0b0b5d4ada5b3c3`  
		Last Modified: Fri, 08 May 2026 20:38:17 GMT  
		Size: 10.6 MB (10602980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af14cb0ee8ab7788ee1b93cd7d50e8dfc1bd4efdc2fa8bb8a8cf88354ef59b5c`  
		Last Modified: Fri, 08 May 2026 20:38:18 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24643c31cc71120cb0e69e4570351289592f9acd3f5059d06d2c13cacffe6d03`  
		Last Modified: Fri, 08 May 2026 20:38:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867ae6a9b9b99c203ffeb300253f1829a2eedea4d717144e33a5f7ef3eb65db4`  
		Last Modified: Fri, 08 May 2026 20:38:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f4992f0aff884e17b7a17621dacdc4979bb2715c6299edfa67d3e8870a1cc`  
		Last Modified: Fri, 08 May 2026 20:38:19 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565ce4674d502ba0ab6a1d520cee5ec43a3d3f72b6b25a62448313a030ec5023`  
		Last Modified: Fri, 08 May 2026 22:03:23 GMT  
		Size: 50.5 MB (50455644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7136bf1468f9939916b37a1c30486e520f42ece0f83977343e1cfb7b0dcaa2`  
		Last Modified: Fri, 08 May 2026 22:03:22 GMT  
		Size: 17.0 MB (17048388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a84b7da7dcbf6f41459c70d766b481e3ad4c5e5f87f8679daf04467adf5e8a1`  
		Last Modified: Fri, 08 May 2026 22:03:22 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33203c8b4213f85c212d59f875d5dad8175397a560b0ad673690c39b962d6ae`  
		Last Modified: Fri, 08 May 2026 22:03:22 GMT  
		Size: 903.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916ff3c58a113ed48fac7299688858ed247917936536194beb82aa913730d96`  
		Last Modified: Fri, 08 May 2026 22:03:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff74aa10518be37653ec3732bec369423c761bd40781d45bacbae02dcb679b08`  
		Last Modified: Fri, 08 May 2026 22:03:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400ac510f9a50a5a1e3fd1373e1235f04df3be93bfde9c8cc1a3d6854e2987be`  
		Last Modified: Fri, 08 May 2026 22:03:26 GMT  
		Size: 82.8 MB (82794800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:b40ad3e6511f49c825b38bf9b6c9674385694ff59c54971b64612d7b6249f57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76db3844a95f9f8224cc168a7c825c7c30fcaaf9f04d0ac5119f8e04c4a8b867`

```dockerfile
```

-	Layers:
	-	`sha256:b9ade15a12469b0e4f573eab78d1e166be2809ea0a5aa9f84e7b937bd9e13e1b`  
		Last Modified: Fri, 08 May 2026 22:03:21 GMT  
		Size: 49.2 KB (49206 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:ee057825f1c958ce1ae36944d72831718cfab88e84671fb8d0fb902698169a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285290061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e06cbc60519c5f62fa44de0f59ae345d47882a0bbd5195320d43c4be91d2fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:16:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:16:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:16:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:16:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:16:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:16:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:16:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:23:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:23:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:26:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:26:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:26:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:26:10 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:26:10 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:10 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:26:10 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:26:10 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 21:43:10 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:44:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:44:23 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Fri, 08 May 2026 21:44:23 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Fri, 08 May 2026 21:44:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 21:44:23 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 08 May 2026 21:44:43 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Fri, 08 May 2026 21:44:43 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Fri, 08 May 2026 21:44:43 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:44:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26f7004e87c4de58dc3edd5e2df9724991ee3e9915a880d58d3583cf4d5bf0`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6393f0d48cd3aa2289517409694b46277da19241c5ceba80096538096ce6f10`  
		Last Modified: Fri, 08 May 2026 19:20:13 GMT  
		Size: 86.3 MB (86250382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0211bdd2a17cc65649476067f7e1008c707a83b1882863d0647ecc5e5f1c94ab`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d9507ddb21ff84107c00222304cd79e0ef4c6770844aa8c324194eb02a51f7`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 3.8 MB (3756682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929a3d6f065048ce8114679154a8c1c1f68513b0b4651e66859f987a0ed1af6`  
		Last Modified: Fri, 08 May 2026 19:20:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840bd62807310f94d12b359008c3f4dcda31455d8822566333ce250370911957`  
		Last Modified: Fri, 08 May 2026 19:20:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356ec5f7f0164488574e4369b52039f3acc5d71430b1aed80c219ec72cb2117e`  
		Last Modified: Fri, 08 May 2026 19:26:21 GMT  
		Size: 12.8 MB (12767689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0deb517da22a62fc73531d4b624f02725b2a9ff20eddfddb37b18323b5e835`  
		Last Modified: Fri, 08 May 2026 19:26:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a4cbc82839900cd837ac6cebb1a4c4651e02e634f7ff90aae8285caf716bd9`  
		Last Modified: Fri, 08 May 2026 19:26:21 GMT  
		Size: 10.1 MB (10073936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b4328401551748c4425a638f6cef6fd3ee25ede30cf34e000ec49fc71dcaf`  
		Last Modified: Fri, 08 May 2026 19:26:20 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811924bf2d53ebb370b1e0caae010fdab9cf957ec4b55cb45817b32c557e6341`  
		Last Modified: Fri, 08 May 2026 19:26:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a060e4033f7359e8a141d331f2d50cb55943c7b8f4fa27dec476629f19bae5`  
		Last Modified: Fri, 08 May 2026 19:26:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81546f35592f41d04e62a9fc9fc1adfddd4ade98571728b067cad35158f635`  
		Last Modified: Fri, 08 May 2026 19:26:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e019d644d35b3bc7b70ab663b2fb43df381a2e08d777806d58bc3ed5ac3b1737`  
		Last Modified: Fri, 08 May 2026 21:45:01 GMT  
		Size: 46.6 MB (46631625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189c8d1e8533c5bfde661583e032b436e99504a5b55dc9a5483253b41988cfc`  
		Last Modified: Fri, 08 May 2026 21:45:00 GMT  
		Size: 16.8 MB (16792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644eb69529535e482baeaeeabb4bb20c1d8c573197982f6f17765a9b7727480`  
		Last Modified: Fri, 08 May 2026 21:44:59 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0e0e3ccfe566950086552ea0b6bad3eb8674dac843d980ab9485953e02534a`  
		Last Modified: Fri, 08 May 2026 21:44:59 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b23c32db542b09e34a86da89a4c815dc8d8dc5dc782668f7226d10379c233be`  
		Last Modified: Fri, 08 May 2026 21:45:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec9b5ba1fd3af9e62f3f35fe642736348bed2da2cdf16485b694d60b4ce36d`  
		Last Modified: Fri, 08 May 2026 21:45:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f89b3a3511dfbeb4a5cc41db430f62ecff910032e75718d9503a6835b1ce0`  
		Last Modified: Fri, 08 May 2026 21:45:04 GMT  
		Size: 82.8 MB (82795042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:83baceec320d30e34f5e3903b2e6397bcac2ad995dba9e23c782cc058f8bf463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de1056e7e2e0edace1e9855929fb56745eee9a45363b8c1615e5ee60741fe0`

```dockerfile
```

-	Layers:
	-	`sha256:31eb15b1bd75ddc10590e38c0e823c0cae2f4ac531821e5b901486d385b2567d`  
		Last Modified: Fri, 08 May 2026 21:44:59 GMT  
		Size: 49.2 KB (49206 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:f71ca4fd1defc9850c73e3d7691af1e8fa8bcbf11c29bab14a2940674b718656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321435974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37b4ec2be54197a3be4facfbe374e68497e741edc62f93e78e051c3aa0fc3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:26:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:26:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:26:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:26:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:26:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:26:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:26:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:26:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:26:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:26:54 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:27:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:30:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:30:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:30:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:30:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:30:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:30:53 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:30:53 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 20:40:38 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:42:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:42:28 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Fri, 08 May 2026 20:42:28 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Fri, 08 May 2026 20:42:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:42:28 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 08 May 2026 20:42:45 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Fri, 08 May 2026 20:42:45 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Fri, 08 May 2026 20:42:45 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:42:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66a0c09325adfb2e5f99917ff9ea6547763d52cdbe0a14ad382aeefbaa8b63`  
		Last Modified: Fri, 08 May 2026 19:31:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b275c4bae9bea4f8fc67a4ac7cfcdfe9b7df6b040b497a0147a883d7be62b76`  
		Last Modified: Fri, 08 May 2026 19:31:16 GMT  
		Size: 110.2 MB (110165420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf9ff069c957413177efe9c5642760f4ee25ad78652ad8415217bdf7955adf`  
		Last Modified: Fri, 08 May 2026 19:31:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48faa27af940ee3b00074ad639e228f7fa79cc3d0757d843ba5a4848d74a402c`  
		Last Modified: Fri, 08 May 2026 19:31:14 GMT  
		Size: 4.3 MB (4307784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfbcd4482a30ddef92869c5f6b59521a14ecd41cd16a1208bec4dda64125c09`  
		Last Modified: Fri, 08 May 2026 19:31:15 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6523c31c0372dc1ae1aa3358c4b22ae5c26a5b6b8db098fadd5cfdb58cfb6eb`  
		Last Modified: Fri, 08 May 2026 19:31:15 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef997bf60291c767a25c7e9a6cec0835f3b77a863a4b2d24cfeb6eae009e8`  
		Last Modified: Fri, 08 May 2026 19:31:16 GMT  
		Size: 12.8 MB (12769660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c70e616917379bd36f0f40d71dd0e4d5a3376e2461da9e9b2a5bc013940a58`  
		Last Modified: Fri, 08 May 2026 19:31:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa4828eff48793f3cfca51244a6e68cd3f145c04b7d83b11675361e020a07d4`  
		Last Modified: Fri, 08 May 2026 19:31:17 GMT  
		Size: 11.7 MB (11734686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d81318aee4ff2c46d9871c742d77407c1fb8ec65f610685b37bc45783e7ce8`  
		Last Modified: Fri, 08 May 2026 19:31:18 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43afaf3d1fb977b36675e36248e7c207017822a176e45d1d069fe392d5501d`  
		Last Modified: Fri, 08 May 2026 19:31:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15dc0f2c241f75f22b4a2186d4512e7f798560c9721d5bf14ad0391ccb5557c`  
		Last Modified: Fri, 08 May 2026 19:31:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5868b6a78a866bb5083ecfde130d60cca1620ace768dbfc3cc46bc289268c82`  
		Last Modified: Fri, 08 May 2026 19:31:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eadd8aaac72289b673d0dd4fbc2aeeb6afdbdaea7534580ab45dcb52d23ef0`  
		Last Modified: Fri, 08 May 2026 20:43:03 GMT  
		Size: 51.5 MB (51490524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583874caeaec22580e95cd95b1a89721e9c485dfff9c785ee28a98ee9a98e717`  
		Last Modified: Fri, 08 May 2026 20:43:03 GMT  
		Size: 18.0 MB (18018314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db5dac5bbf403ca7bdb23db8447d6fe0e31595fdf5ed89fb2b47ba51245a4`  
		Last Modified: Fri, 08 May 2026 20:43:01 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c068c8873697a165a84c56c1bbc8a45ed6d72c8cc661116cfe2fc11e24d5bec`  
		Last Modified: Fri, 08 May 2026 20:43:01 GMT  
		Size: 904.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385e508aff5f923c5fcd06f35fc310e38987231cd037fc24c38c5d99c8eb9a6`  
		Last Modified: Fri, 08 May 2026 20:43:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c3572e889956b5cd88e5141a75def33d882b0e4a75e6f5306ca49148ba66e1`  
		Last Modified: Fri, 08 May 2026 20:43:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5df5b93c960aeb9d3b368ce24c91b4a94553c39482cf9a63085de4d731276d`  
		Last Modified: Fri, 08 May 2026 20:43:07 GMT  
		Size: 82.8 MB (82798278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:5132f4f78a5fce0b18d96ba7f89aa46cfbbc03b60bdd9faa7deee8de7eca2337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 KB (49250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4762a91c84ecc9ca39ea486b5a4fa2fc4954d7955c903d1d1e6162d9fdb55a1`

```dockerfile
```

-	Layers:
	-	`sha256:6c3b1877453ebe6877591fe2f1834480156a877272b7966edd73b06b6a3d2bfb`  
		Last Modified: Fri, 08 May 2026 20:43:01 GMT  
		Size: 49.2 KB (49250 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; 386

```console
$ docker pull mediawiki@sha256:235d6162f6ab35467813f1953155a94e9f43e99ae3ccf67db2f6c831066af033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.7 MB (332681888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47235d8e91fc526a280ab5a080f0fe1e956905966075cc4e45f23a2316c71245`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:25:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:25:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:25:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:25:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:25:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:25:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:25:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:25:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:25:10 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:25:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:28:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:28:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:28:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:28:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:28:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:16 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:28:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:28:16 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 23:12:33 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:13:49 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Fri, 08 May 2026 23:13:49 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Fri, 08 May 2026 23:13:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 23:13:49 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 08 May 2026 23:14:09 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Fri, 08 May 2026 23:14:09 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Fri, 08 May 2026 23:14:09 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:14:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6dfe20d62541f8363e367da85c4679889a82ae173cb57fdfdef954cd7ee8a`  
		Last Modified: Fri, 08 May 2026 19:28:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95542e8d627b3e8652ce316fcbd2d9078e91c19cdaf21fbcb23e6da2d53259a6`  
		Last Modified: Fri, 08 May 2026 19:28:40 GMT  
		Size: 116.1 MB (116144133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a04a8325e221d617ea29c79491bf357589df31fc32b7e532e0d7aa283cfaa4`  
		Last Modified: Fri, 08 May 2026 19:28:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c232a4269d2fdde64563bda0bb7cbccb2af4aad168db95188c389d7977789ec3`  
		Last Modified: Fri, 08 May 2026 19:28:38 GMT  
		Size: 4.5 MB (4459142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5dabb5c854f4f5d4c60619f3f403d406a443777b4c5758ed566055a199384f`  
		Last Modified: Fri, 08 May 2026 19:28:38 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7386c3b83a36557946cd774eae8d1c5281bfc73812091c60771be638ddf7f0d`  
		Last Modified: Fri, 08 May 2026 19:28:39 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33bca36c83ffb7c595986402e7e5e5b3787ee6354965369cf68876ad35d042e`  
		Last Modified: Fri, 08 May 2026 19:28:40 GMT  
		Size: 12.8 MB (12769079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a904f8221e33292e6697e0d1dcd6fa9e6899e9172e6ad84159d828ed243119`  
		Last Modified: Fri, 08 May 2026 19:28:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663e3d5ac345b965d10e1d679344d4a53281467de82abb1d542eb23a99cd3eb`  
		Last Modified: Fri, 08 May 2026 19:28:40 GMT  
		Size: 11.9 MB (11928835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c5cced57ed1eeb93c98aafdfebec2f21fde5af74340d79ef7819024b63c47d`  
		Last Modified: Fri, 08 May 2026 19:28:41 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f7ce0e2a9d16bd8c533ca8ef14180f974f67700dd3edd74907e45879534a87`  
		Last Modified: Fri, 08 May 2026 19:28:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c3ff15223150f579d8fedc62661a75645f8e013daeff262feb1811c0b64a13`  
		Last Modified: Fri, 08 May 2026 19:28:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b4e4ab94be41de2dd8934b5ad9d51deaa413fefbdbb6c7e727237af9f3d8d2`  
		Last Modified: Fri, 08 May 2026 19:28:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73492eb411875d576e8fda9cf36217400f2eb704b68a831660af67d94b5d91`  
		Last Modified: Fri, 08 May 2026 23:14:27 GMT  
		Size: 55.3 MB (55257451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32542c2653e5fd7eee2fa84ce9e7d1afc71978447b06b053e7f82ad7a2bec090`  
		Last Modified: Fri, 08 May 2026 23:14:27 GMT  
		Size: 18.0 MB (18022396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6146eab3edf94c7faa343683dccbbefb975d342c9aec03c04c01b230a2959f`  
		Last Modified: Fri, 08 May 2026 23:14:25 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c5f1567a9ea673b2c1902b2bad1feadad82b69279bcb160517e488e0447fdf`  
		Last Modified: Fri, 08 May 2026 23:14:25 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c2f1335d24b3f01da6918e3edd62b914064fd5741a1a4a2e50c5b45d3b036`  
		Last Modified: Fri, 08 May 2026 23:14:27 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31222a9c0e673d972f6efcd0d90fcb43664e98abb09a5c0bba571e0054726a02`  
		Last Modified: Fri, 08 May 2026 23:14:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be143c6cf2bcd9359534f21d667b6ea835c8d84ee75932ed093ee8a8069bd33d`  
		Last Modified: Fri, 08 May 2026 23:14:30 GMT  
		Size: 82.8 MB (82796797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:a300deed3a87c494f5cdf8e6aac66fc259feee355af1b775fdd2f3ca24912764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (49012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd955ae2c3295954b0597fc99448bf0fe38349ad55cedad9165430784317c7`

```dockerfile
```

-	Layers:
	-	`sha256:ee4a8dc1d5bd81cd5bb290bfb2362778cd0b053ff54da90af1f89a1ef6a074c8`  
		Last Modified: Fri, 08 May 2026 23:14:25 GMT  
		Size: 49.0 KB (49012 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:02972d4c1936659be5ff6a9156f6b07975a3571048791ef148b53663b5fa1af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331914717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7916b08b0731ecd46d0ac1e51af6168e3df6627a859129b519a7b58f323566a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:49:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:50:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:52:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:52:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:52:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:52:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 21:31:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 21:31:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:35:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 21:35:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:35:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 21:35:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 21:35:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 21:35:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 21:35:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:35:53 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 21:35:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 21:35:53 GMT
CMD ["apache2-foreground"]
# Sat, 09 May 2026 04:39:02 GMT
RUN set -eux; 		apt-get update; 	apt-get install -y --no-install-recommends 		git 		librsvg2-bin 		imagemagick 		python3 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 04:40:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libicu-dev 		libonig-dev 		liblua5.1-0-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 04:40:47 GMT
RUN set -eux; 	a2enmod rewrite; 	{ 		echo "<Directory /var/www/html>"; 		echo "  RewriteEngine On"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-f"; 		echo "  RewriteCond %{REQUEST_FILENAME} !-d"; 		echo "  RewriteRule ^ %{DOCUMENT_ROOT}/index.php [L]"; 		echo "</Directory>"; 	} > "$APACHE_CONFDIR/conf-available/short-url.conf"; 	a2enconf short-url # buildkit
# Sat, 09 May 2026 04:40:47 GMT
RUN sed -i "s/<\/VirtualHost>/\tAllowEncodedSlashes NoDecode\n<\/VirtualHost>/" "$APACHE_CONFDIR/sites-available/000-default.conf" # buildkit
# Sat, 09 May 2026 04:40:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 09 May 2026 04:40:48 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Sat, 09 May 2026 04:41:14 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Sat, 09 May 2026 04:41:14 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Sat, 09 May 2026 04:41:14 GMT
RUN set -eux; 	fetchDeps=" 		gnupg 		dirmngr 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 04:41:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec2632ee8119dd2f20ca1558eea30c9050dbe76cdeddfc47a82d2a99e3e922`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7eeddeb286b4ad82e04422070cc9d0ea14c8385e61c160fdc6de15d44b838`  
		Last Modified: Fri, 08 May 2026 20:55:24 GMT  
		Size: 109.6 MB (109599289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9201651affe69dbeea0b40dd0a01797ab879ad276cbce7b1035fd2abbe6f32`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e51c8a80d6a8bef8f0b2054c11688b31c933849cfa8969dad4e6902019fd92d`  
		Last Modified: Fri, 08 May 2026 20:57:14 GMT  
		Size: 4.9 MB (4883332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0f49e69dc9fe4788a52a9279ee2ccb8d494fe3d8ff41454f9fb3a16f8054d7`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482f0abd8de4c23e09415b0ec42b86203a86547f87a68869616944382298375`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce98efe507e5d7797d64e3d4202ca220e9d291ab2d679bbe40223086fb48170`  
		Last Modified: Fri, 08 May 2026 21:36:17 GMT  
		Size: 12.8 MB (12776650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d860dc35f69319960a406728b89c39e38482f8f98e0ab8f5d181953571c917`  
		Last Modified: Fri, 08 May 2026 21:36:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b111733ec4ac07bfdbbdf5a1eb2af7f667c05cb9dcb92f33d06fe5f61f6ad3c2`  
		Last Modified: Fri, 08 May 2026 21:36:17 GMT  
		Size: 12.1 MB (12125077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2a51855b80d5932e9dc1f9c09f41d2aa5c0ce71b8c5cf0d4a5aa83b940d92b`  
		Last Modified: Fri, 08 May 2026 21:36:17 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb56d8087a19877de60b3c6c223547938de1f43b2fd303b6c264cc225ec89f7`  
		Last Modified: Fri, 08 May 2026 21:36:18 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c337ea8a6cc51c46921a034b1590e322bc7fe0b00e902f4af31a880491ce10a5`  
		Last Modified: Fri, 08 May 2026 21:36:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a25223ffe85e6ae622ac3e7c0139317c2170bb8072fa6f88724d946586bbb`  
		Last Modified: Fri, 08 May 2026 21:36:19 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e80f168c543055464bdbe136fb0c0fd1c84e671b022ca4f32e2b953bb170fa`  
		Last Modified: Sat, 09 May 2026 04:41:47 GMT  
		Size: 58.2 MB (58204879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a6ae4e34b27619c7badfb3a2ee9517d035b5ef677e9c7e431ce427251056d`  
		Last Modified: Sat, 09 May 2026 04:41:46 GMT  
		Size: 17.9 MB (17921865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4161c2a72d90135265c79755c960f02640429699262ed4eac13e3edcd11a4c`  
		Last Modified: Sat, 09 May 2026 04:41:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811adf0ca85a339d0413961a967fe2ad8a73a20bf20d9107efce6a62595a65ad`  
		Last Modified: Sat, 09 May 2026 04:41:45 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f6588b5dba1024c12274ffc2e045bc2759559304bf912022828c79330fe241`  
		Last Modified: Sat, 09 May 2026 04:41:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5894356316974255b8457159d306c9cd66feb1d9b2715202fbd9fd5f9aed553f`  
		Last Modified: Sat, 09 May 2026 04:41:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d690901d241c98fa8430ba2426ce7b7757df26ad04a6d19880eddb489e8e7ce2`  
		Last Modified: Sat, 09 May 2026 04:41:49 GMT  
		Size: 82.8 MB (82797863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable` - unknown; unknown

```console
$ docker pull mediawiki@sha256:b5040c639b69be5f3ab53c9705f4ccb9af9bfcd5443a47bc2b0e0bbe0537a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 KB (49111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf49fc828bc0f3f73be6cf7adb3481af84633e720e960af25da0e04f1543e6d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c332056e5c5be8ce01b2916d6cc3cad9cd81427e287ef66628d40dd3970d0f`  
		Last Modified: Sat, 09 May 2026 04:41:45 GMT  
		Size: 49.1 KB (49111 bytes)  
		MIME: application/vnd.in-toto+json
