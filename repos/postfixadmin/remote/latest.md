## `postfixadmin:latest`

```console
$ docker pull postfixadmin@sha256:0d88eb723ae6ce84d3e9ee3ad20cf73341dc73656da255b01a1689b0c7791313
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

### `postfixadmin:latest` - linux; amd64

```console
$ docker pull postfixadmin@sha256:3b6c8d267cb6da76b7003302f3c6a5feef3377933681a722c5d101ffc0086785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204942988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4aaf94366596f47de08645f640b673001732525ea2434825d3cbecadb10c9b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:39:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:53:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:53:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:53:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:56:17 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:56:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:56:17 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:56:17 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:20:42 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 00:20:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:21:01 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:21:01 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:21:01 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:21:01 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:21:01 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 00:21:01 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 00:21:02 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 00:21:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:21:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:21:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 00:21:11 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:21:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60df91c45d0a86e1db8d1d912fb5cf26d490f2284dac0daa5f35109768e26545`  
		Last Modified: Mon, 08 Dec 2025 22:42:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8710b0f16836f0a18a496d19ba862ec3b1cea366c4521ef644d9b073f1524`  
		Last Modified: Mon, 08 Dec 2025 22:42:56 GMT  
		Size: 117.8 MB (117838586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4542c4381529b61bface7c43a625307bba7d14bf252ab1b57a2f24cfb5b332`  
		Last Modified: Mon, 08 Dec 2025 22:42:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7470ee1455546c25b2680a49cdb78d0d7c65d1e4170192fbad3e729813792`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 4.2 MB (4224526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cb708df8f05272a256d8e92d2096f7eab3290fb84bb6c7a502b916bf3ddcdf`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d0d313218aba7dc3fc5855e6b355961ad12f0e396a34bae518c80238534dd3`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e61c85737cca7294530dcd669d76a12cee0dbd9d1f4d2c7c0237c1634273b`  
		Last Modified: Mon, 08 Dec 2025 22:56:37 GMT  
		Size: 12.8 MB (12770195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543828ab9fd42599e7a1c381e754d023c357c3bec8b88ff7ecc1adac437aaf64`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab8f1d104c541ba44266eee56e79b97f9c2c3c097e01dbbef481430d678b2cb`  
		Last Modified: Mon, 08 Dec 2025 22:56:37 GMT  
		Size: 11.7 MB (11713288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ce6266145199e14d29ffe22bb0795d38978130f9e08f29165d401acf30f89f`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16d68226cddedf8a1b4b217a45e36897d229d6b283ebf47b16e2b24836ad0bc`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c5c71ad84360684503dc8ceae651b6a1721ac66e4c236b410139ac78dbdc25`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da081f25a1b30f03de3aa9ac768679d36bdec758603631177fe2dc4ac6195edb`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0653a93e10dd7fbc2959f2c1385d72eb502d24e5f52d0ee6fcecdebfe83e3c94`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 1.4 MB (1351938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb064f808c1e069e22e3ee54a6973ea36a049024c3812589ce98ca1be4686cd`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 466.3 KB (466296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d731efd370d9da49ddbbfdd76442ff3575b3fd424c2ea79ff95fc310fee6558`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 7.5 KB (7476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d75d99b878e38418507fd961f55d86d635a0527685a6fb4542eb8972339b1b7`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c829f73eabdeb797311fb6652d37682bbd34b079e624e4d200b5f0614080620`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c56f7f11d3368527268a7c06d2dc5c4193b08f4433e050d49b58a6a3db4743`  
		Last Modified: Tue, 09 Dec 2025 00:21:26 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e366bc76e691213127941f9e843c9d4fba242c7ddcf2f9731427bb8c464fb`  
		Last Modified: Tue, 09 Dec 2025 00:21:28 GMT  
		Size: 23.4 MB (23406613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:cabfba2da6f5831e52b8eef64f4374e6b06495d105eb3dbd1cb961b31ca5eed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb5445cb8c30158ddf904969e4d91d1d3138d94d2729e752debcb694fda826d`

```dockerfile
```

-	Layers:
	-	`sha256:f308f8f23a61168df1abac45245e9e8c228c50d543fdf973e4e207ca2e11778e`  
		Last Modified: Tue, 09 Dec 2025 03:10:51 GMT  
		Size: 50.0 KB (49975 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:5fb466ddeb25cc406f2bc353b49153c5d5bca6adcb8ca03ee544d56493029bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167556262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414b70ebf14226ac75bfb2e35cef548bcbe7918ff50f1e044ba8ab1ffdd8f788`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 23:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 23:12:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 23:12:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 23:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 23:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 23:12:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:12:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:15:28 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:15:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:15:28 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:15:28 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 01:47:16 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 01:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:47:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:41 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 01:47:41 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 01:47:41 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 01:47:41 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 01:47:41 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 01:47:41 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 01:47:42 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 01:47:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:47:42 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:47:42 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 01:47:52 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 01:47:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b777f680ea5ed6244de9922459aca5e8f721dd50afe3ad69bd160d32b03fed74`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892beb557407f1ac713d96f814f3d44dc1f4b7577c30e3232053ccc0ecc1acfe`  
		Last Modified: Mon, 08 Dec 2025 23:16:01 GMT  
		Size: 86.2 MB (86246508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e34241676ecd248c3c604ff9ff8e3c42a09b306a317700fe1b02c144f79a28`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae3fb9ca4fa496585289c07a64816f09c57ae2629a92f8925148a56e408597e`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 3.8 MB (3752414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bc52f4c6d03d2de94f2aa9db372c265d3d80df3430c29c3f82bbb6e08d0939`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5521d93ca8953e3b2971412de188672c166ca9d93e56b2cbac405a9d351769`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e236f7bb7fb4d00df90682ec06f4b237ae2adefcdced42a1a5a7fda8753c7b3d`  
		Last Modified: Mon, 08 Dec 2025 23:15:57 GMT  
		Size: 12.8 MB (12767793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6eeabbbde0f4cf8be66d73f09608ebcac2a8e41ed202124bc8a0cd22e95a8`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548c2ee49539f86c5f116cd4f0f50c3b9eaac2a5f6bb1ecd8a3596a47ecec3e`  
		Last Modified: Mon, 08 Dec 2025 23:15:57 GMT  
		Size: 10.1 MB (10069913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3263787bde47d23cc53f47de8f560681087a55e9e28284702e77a64f055ec0dc`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da6e3a92cd906f34cb8f02d0fb40bff471e0d825cfad4e9e8cdc6dfa3eab37`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a9b8ff0f7c25a1c5e9a9bd32de2d1f381f35bd7ff0b60537a0410d5c7bfc0`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfa2ad1dd9fe7b67dcb31090ea75ddefb49570e62891cd44b295650829bb12`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fcafd2877eb15792bfa0dff49e181c68aedd44d1bc482a511a05fb9f92ff9d`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 1.3 MB (1289171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c27fe739b8c022d0a0f640b0bece5970481411b276aef4cd278921a5920c1d`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 420.9 KB (420949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8737112dfb52ea7e21d516b82e51b12ba3e0fafcdb3e6911ecd29ff63f943a88`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc7099ee836b2a496efe94520150f18c1ca66ba6b9692afba52ab4b2dbec99`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0e3bf324be44f12ec23694cebf647fd15a8bd77b80b8d4675d461770a366b9`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f80e333c85068796f821b2a7a990193edfbf6714b3876246531a7887a76856`  
		Last Modified: Tue, 09 Dec 2025 01:48:06 GMT  
		Size: 778.0 KB (778005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e25ffbbb782811dd70dbda7c2efb0fb264f958fa30964dea63af529b7b3936`  
		Last Modified: Tue, 09 Dec 2025 01:48:10 GMT  
		Size: 23.4 MB (23404447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:73747f9949ed36af72fa308e7a99cfa3b19c42fe8082eb056682aacbd0b43f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921fd798a3093521da870f797d91173a9462864180b06f590ac968473d16e886`

```dockerfile
```

-	Layers:
	-	`sha256:955afa3433d93f012b0accfdfcb18021b335e817fb9e5445410680e6e1a34488`  
		Last Modified: Tue, 09 Dec 2025 03:10:55 GMT  
		Size: 50.2 KB (50152 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:1601ac8c1e67be74486a1cc9c263a311f41ed1860c1b88b7ee8e9045d3698d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197632170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41071ef50e4191a76b9afc08ec5cbc715534f2b8dec50a3e469b749405a4389a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:39:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:39:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:39:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:55:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:55:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:58:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:58:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:58:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:58:55 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:27:29 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 00:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:27:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:27:50 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:27:50 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:27:50 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:27:50 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:27:50 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 00:27:50 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 00:27:51 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 00:27:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:27:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:27:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 00:27:58 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:27:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:27:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db55d306a36fab75ed7d777aa9d49e7ff8f8d56b31b5ab58baec1feb7cd8ed6`  
		Last Modified: Mon, 08 Dec 2025 22:43:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f917fdde723bb9eeffdac3800d7c39abcd722fc080e2db6cd3a9bf35764fd07`  
		Last Modified: Mon, 08 Dec 2025 22:43:19 GMT  
		Size: 110.2 MB (110162673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d87be9b989aa856a793b7ddc0d880ba4ee5b7217f0d5ff25b541d7084ee566`  
		Last Modified: Mon, 08 Dec 2025 22:43:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e9469eb184f28f35ced71fc9f3eebb692ac5c738982e61a304e2437aa67c75`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 4.3 MB (4302241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a25a5c5337ccd28d55e0797d93bcfff4539dc555079083a227332c312cab9e`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d0c8a8ae6e76d72b08c7db07500e8804384f40605d5a0eca0f37e82ea46be4`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08d1d3fb794d1a56c1a01ebf8500672da1f55c427e6924c85159d4c04946f6`  
		Last Modified: Mon, 08 Dec 2025 22:59:15 GMT  
		Size: 12.8 MB (12769808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf3154bb243ec992fe49167ecab6bba6488c6a14ba3eb2d4eea1827aed254f`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f0f2fa87c8d325b8946a90b3284c4f0651dd20374d9c7752bfb8944c754bd`  
		Last Modified: Mon, 08 Dec 2025 22:59:17 GMT  
		Size: 11.7 MB (11729803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3de5a445d66564dd814bf63b4b3a350602ffec3fb2ef12f9a90ce59a31338`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1bf44af048c36422962fbb5c0145c9d816af3edc1c624723f3d899896d0e82`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96ec1e97ee77dc168b947a2d0c87605cf360bdee0e30a11be1fdd26d28b15b`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17722d9f32ff2de17cb65701c07e026e726f4a178298df205a25a148376db94a`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f8b73e26306e7a2bac940258c6faf9f644ca50c814616b3bc9233ba7777388`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 1.3 MB (1265875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf3b6685549f8bde63459b91681fe313fe42fe9a7afd9f3ba657788a8c12e5`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 461.8 KB (461790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9095ac20012527cd05abfd8ffcbcdda283874cb91eb10626dfc9d3b1aed6eff6`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a6c2d8e3c36c461657f18288ce6034b0168e9f0002e9ff576cee243a58f800`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 2.6 MB (2602188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713f51c0125929f336a62ec53611e3a08528ebf4461a27ab1afeab75bb1ff71`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eb8c711aed598bc70962396d5e021d452bc669fc94489607ac0f0d42026d57`  
		Last Modified: Tue, 09 Dec 2025 00:28:13 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6199cd896df866a12216fe2e0e187b6880a34f80327a7c8705b2f45fbf94b6b`  
		Last Modified: Tue, 09 Dec 2025 00:28:18 GMT  
		Size: 23.4 MB (23406301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:2a90e6192cc09210461e6e7671c2faf8928129559e3c48d478b82c72b07a106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc1801b84a6ed8f94f666d5ab6dbd1c0a9a9accffdff9b0c6576f95e327cc49`

```dockerfile
```

-	Layers:
	-	`sha256:cbeacd9f96fdd3d3aaaf4d516659d6772feb832cedf1c26b1fd87676f3c791f3`  
		Last Modified: Tue, 09 Dec 2025 03:10:58 GMT  
		Size: 50.2 KB (50212 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; 386

```console
$ docker pull postfixadmin@sha256:6f4f083c2b22fb9e0ef4f38f8199520649776aa3f0fb48ca03440af894133d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205170233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdd507b3a23c77e0127832eafaa415b1140db7edfbe415c714b69c32489727e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:36:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:36:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:51:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:51:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:51:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:51:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:51:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:51:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:54:32 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:54:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:54:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:54:32 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:16:08 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 00:16:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:16:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:29 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:16:29 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:16:29 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 00:16:29 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 00:16:29 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 00:16:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 00:16:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 00:16:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:16:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:16:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 00:16:38 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:16:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154524b7be3749cfa72d3bbb2e8d095db97110da5060ceb7e4f1473e9e61790d`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd631d2861c5c3a023b3ea0aaa64fa40fa6346b13d7b39ed45652f7e9987632`  
		Last Modified: Mon, 08 Dec 2025 22:40:08 GMT  
		Size: 116.1 MB (116138575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bac1aca55e1ea704979c288343f39f70510215a9cf6b945e40b6feec2ce06`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acc81ce731ef4a4d465cb8a583291202dee016a0120a19261fb3a5845b4e4c`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 4.5 MB (4455999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548db23afcf0fb44a20278337a2d0ae10b3d88e365e609bc2359f06447deb7df`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e74b5b7c6ce77596201b5299e77e44b14037ada823b0b47879fd5669475b9d1`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d02c5939f502ede48e83231474b4a29f515d4a4973c4e8f006febf34142717`  
		Last Modified: Mon, 08 Dec 2025 22:54:52 GMT  
		Size: 12.8 MB (12769206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd529f9cf71080d89aab96bd9d156dc40abd62fbd99947e2bb1de01e2be85d6`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46361a7b7e61932b252074c133ca58c96a16c4035dc5bf14ccb8cb67484e2a0`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 11.9 MB (11919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d249c3ac14675eab656e934c20be7760d64b4ccf05edfa4b96eac2d35abd04c4`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccefa0e3b73973b55bbd0cd753631ba859cebe2c5577770522e47f8ed047b95`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0016a305cac02834a5b6c83a6bdcff0f6efb48b78c56de27fdc2edae81bb309`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5d52512d83589b07bc92be254b256a860514a73c3a62881cba7284e6591c04`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14f6da400bcea7c6c9abbbe9c166242e6e406b75cf07f4f5e4a6c62c713b990`  
		Last Modified: Tue, 09 Dec 2025 00:16:52 GMT  
		Size: 1.3 MB (1310825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ee59f1df05bb4a2e15685e4baf4463f5e8755180bfd1c2134cb12032bd2c67`  
		Last Modified: Tue, 09 Dec 2025 00:16:51 GMT  
		Size: 482.2 KB (482195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312e34c481cdd2e2a52f3ef7442aeb9dd98b26f8e5c830889e1ff153a9369c7`  
		Last Modified: Tue, 09 Dec 2025 00:16:52 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b460f08c911ae05706492db33a8a9f7c8f14ebe7debd0603c9a9845e0b5bbf`  
		Last Modified: Tue, 09 Dec 2025 00:16:52 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508e958bcb0ca7bf7a51d33507dbbf433210be75a3710676701317ece8b6e247`  
		Last Modified: Tue, 09 Dec 2025 00:16:52 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352f2899bcec90062fb7e7104843961f4eaa784189bb73d78772f2626fd01ed0`  
		Last Modified: Tue, 09 Dec 2025 00:16:52 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc60e43aed91f300ee0ed7fbfb95e4cbbbbd46b9d9cf3d7a5e5b4bd572edcae`  
		Last Modified: Tue, 09 Dec 2025 00:16:54 GMT  
		Size: 23.4 MB (23405911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:2dadade162bb976423369ac262968d370af878af1aab629fc1ccad4ac44e4d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 KB (49908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca092507599e8919e07cd4f7a30d121dbe1526bea9a4c76a68ba9f0c9c0f7340`

```dockerfile
```

-	Layers:
	-	`sha256:a2c4fb6afea7f1ba0c4aeeb344ad23d243f26e373cd939b5ab3dee45aaf3b31c`  
		Last Modified: Tue, 09 Dec 2025 03:11:01 GMT  
		Size: 49.9 KB (49908 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:78fbbc8083f579e09f7f88371b0c223f662641ea446f4ee0a6dce79ad2ffdc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201529494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13cd2bcfcb5568734a87a0571eade0e6e5f5ac9ff5127bb194880e938b7d5806`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_VERSION=8.3.28
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Tue, 09 Dec 2025 01:33:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 01:33:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 09 Dec 2025 01:37:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 09 Dec 2025 01:37:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 09 Dec 2025 01:37:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Dec 2025 01:37:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Dec 2025 01:37:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:57 GMT
WORKDIR /var/www/html
# Tue, 09 Dec 2025 01:37:57 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 01:37:57 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 07:59:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 07:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 08:00:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:00:13 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 08:00:13 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 08:00:13 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 08:00:13 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 08:00:13 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 08:00:14 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 08:00:15 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 08:00:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 08:00:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 08:00:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 08:00:34 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:00:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 08:00:34 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:df386b317f873f24c954490897003afc0cd48be0e216913d2700314a12cf667d`  
		Last Modified: Tue, 09 Dec 2025 01:38:32 GMT  
		Size: 12.8 MB (12769347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafe4867fe44992b5e9da2f31f9f093454e8333307cc103ad864f491e636990`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6641e9f23a6e17563d111f9c04952240793978906b18abbb29c3bc0320dc0b`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 12.1 MB (12119745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3fb9d439a4c14195727e33767c51d42645f95622ee76b4f4beeac52113766c`  
		Last Modified: Tue, 09 Dec 2025 01:38:31 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138a4d96d15997e661c28682350dfb784f9048e5d641a2cc94d921759c95881e`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885efa4b912c17f55261ee92c49f5db0bfc72d1e54b25223a1e04b17b6a54a80`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1e3f3d801f7432dd31097d645a3fc6b24c89639455efcf4cc2c9b4e7e6aad0`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7c31c1894da95cea0d9d495adf83795275381e3b2d6b0255bbb1220180ae3`  
		Last Modified: Tue, 09 Dec 2025 08:00:57 GMT  
		Size: 1.3 MB (1268371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5d9a10999ff876cea3d9ee8b6a99f9eaee3e09d1cdf9dbe36c37f013549313`  
		Last Modified: Tue, 09 Dec 2025 08:00:59 GMT  
		Size: 499.9 KB (499920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65900ea5f89b767c22fb06cdf20b0a57e95fd083fbb09b6ff9e6468994bb06f1`  
		Last Modified: Tue, 09 Dec 2025 08:00:57 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e9992be8d69cc7391a81deca498c3118453c3a6cf230d77340b2519b09f3e7`  
		Last Modified: Tue, 09 Dec 2025 08:00:57 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e070aca7c88db9684d964bfe4b677b626a1f4e3cc218196e5cc7b924ae0ccd`  
		Last Modified: Tue, 09 Dec 2025 08:00:57 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f637bb78be91ec85deafd4b29e7d9f2aca9dbc66ce189e08c6417243863c5e`  
		Last Modified: Tue, 09 Dec 2025 08:00:57 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e035007327fbe208ee95d5ef004548e067feaad003fbd0d0a9d3daad183923e1`  
		Last Modified: Tue, 09 Dec 2025 08:00:59 GMT  
		Size: 23.4 MB (23406204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:425e70c6799997f982fc22152fcd8ef1547cd25cd055cbecb6b11830c99270d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fbbe9d7d3cc2f871c20553f812c1e9e255c8d7f677fc9931543544af3dea5a`

```dockerfile
```

-	Layers:
	-	`sha256:d0fe919b5c9848f87bb177a71f7ef4325f425d24940ebf6aca368d60f0b46858`  
		Last Modified: Tue, 09 Dec 2025 09:10:35 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:0fe941441ca24977778daca989e7940f9a7e4a3a70b43981a80060764817013e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231447468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e11bb94bab1a1adf30c41a9e5aef18d2d7a737f44caa0237104361acd576ac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:15:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 15:17:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 15:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 15:17:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 15:18:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 15:18:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 15:18:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 16:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 16:25:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 16:25:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 16:25:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_VERSION=8.3.28
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Tue, 18 Nov 2025 16:25:15 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Sat, 22 Nov 2025 12:58:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 22 Nov 2025 12:58:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 13:47:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 22 Nov 2025 13:47:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 13:47:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 22 Nov 2025 13:47:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 22 Nov 2025 13:47:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 22 Nov 2025 13:47:46 GMT
STOPSIGNAL SIGWINCH
# Sat, 22 Nov 2025 13:47:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 13:47:46 GMT
WORKDIR /var/www/html
# Sat, 22 Nov 2025 13:47:46 GMT
EXPOSE map[80/tcp:{}]
# Sat, 22 Nov 2025 13:47:46 GMT
CMD ["apache2-foreground"]
# Wed, 26 Nov 2025 05:55:00 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Wed, 26 Nov 2025 05:55:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Nov 2025 05:59:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 26 Nov 2025 05:59:05 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Wed, 26 Nov 2025 05:59:05 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Wed, 26 Nov 2025 05:59:05 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Wed, 26 Nov 2025 05:59:05 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Wed, 26 Nov 2025 05:59:05 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Wed, 26 Nov 2025 05:59:05 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 05 Dec 2025 11:35:39 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 05 Dec 2025 11:35:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 11:35:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 11:35:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Dec 2025 11:36:57 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 05 Dec 2025 11:36:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 05 Dec 2025 11:36:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8158ca8e7142e2a2e752aa54f9f38b113c4da18a1203f8a016c20021e2c7f958`  
		Last Modified: Tue, 18 Nov 2025 16:23:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff319280e8296116d4860bcff3a58b87a62fddefafde0f28fe3ef23903b406`  
		Last Modified: Tue, 18 Nov 2025 23:23:16 GMT  
		Size: 146.6 MB (146579223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b4e03a4bf5c5637137f3accd87df858f6838f0f9d69f831ab3812abd3ce599`  
		Last Modified: Tue, 18 Nov 2025 16:23:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abeed7e11593572f205773941d3d6e6929e6593298b11b456f1482e5acacc97`  
		Last Modified: Tue, 18 Nov 2025 17:27:12 GMT  
		Size: 4.0 MB (4026540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb1d7c292ba75a577d4ddf8cd2aafbdabaff80a2abcf13b22c0e52dd03d2511`  
		Last Modified: Tue, 18 Nov 2025 17:27:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bf5bf65dd0ebdeb094f44e303ff78a21f87eb1122d6c027af7286f17e6dce6`  
		Last Modified: Tue, 18 Nov 2025 17:27:11 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1745afe5af530398e2fe8685a1d8894fece1f5185de9feb1fef5bc5e663dca9e`  
		Last Modified: Sat, 22 Nov 2025 13:51:03 GMT  
		Size: 12.8 MB (12784329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8632e6dd30ac0faa7800d7fb3a0c446dd2ac6c192cf275b28d60c4281577d2`  
		Last Modified: Sat, 22 Nov 2025 13:51:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426bd759d93cade63486c0dbbbb4e453cf39b62340eac370dece1c55351583ee`  
		Last Modified: Sat, 22 Nov 2025 13:51:01 GMT  
		Size: 11.2 MB (11247355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271ad7c1c01568cd0b9b7758b932d69b9d1beed17c53d14cba4187f79239bcac`  
		Last Modified: Sat, 22 Nov 2025 13:51:00 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed68df8651ff6f6feded51a48ee793cc4f57afbd91d9225fe4522e862514351`  
		Last Modified: Sat, 22 Nov 2025 13:51:00 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e17055deafe15cbeb820d261577fad51ab1bcb2e479825046192477f1ff31d`  
		Last Modified: Sat, 22 Nov 2025 13:51:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f54dec0d5b01f5a63867da5248f65d16fbeed0a7cd558c353775b6b0783fe`  
		Last Modified: Sat, 22 Nov 2025 13:51:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827f0a4675737ae7490b6b44741187a6a8ad85e2e61ebf25d4ef6bd7559cabf4`  
		Last Modified: Wed, 26 Nov 2025 06:01:47 GMT  
		Size: 1.3 MB (1265510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a304bf17f99c6e89654eb78c718238ddefaea4dce47fa41378525f7ea5b683e6`  
		Last Modified: Wed, 26 Nov 2025 06:01:47 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf777c60df2f31a28289991181b475a2a074b298a6c62f39f14fb466d7d4fcc7`  
		Last Modified: Wed, 26 Nov 2025 06:01:47 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527138511b384e5c2914bec59e9d8afdfbe0469b563557c23118ec12b862375`  
		Last Modified: Fri, 05 Dec 2025 11:38:23 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb694844c0c32e04018f9e8b86c93f254040e045725932764ab97f96ab8dbb`  
		Last Modified: Fri, 05 Dec 2025 11:38:22 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fd4bc2d8f44f5d9bf1d9c7719d7de47a3c8e32582f88213605e7fa1f66b432`  
		Last Modified: Fri, 05 Dec 2025 11:38:25 GMT  
		Size: 778.0 KB (778006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf54fe0482af11d08dc8d1e10e3da908f13b713cecc78b7ad12480138ba2a23`  
		Last Modified: Fri, 05 Dec 2025 11:38:26 GMT  
		Size: 23.4 MB (23421317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:fbe7355db89498a429df7e1549d66d92c73eaa19540bb5639b867fc2618814f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977f64b9f989bb394e0309aacb78f6efd6bf94cd6fe693c70e7d8c918f8a7cfe`

```dockerfile
```

-	Layers:
	-	`sha256:6e58d62feb3b36921857f2702f2423b493deeb280923a5fdd9c4802af8e2332c`  
		Last Modified: Fri, 05 Dec 2025 12:10:29 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; s390x

```console
$ docker pull postfixadmin@sha256:64a4ace64817b8b60f7319a94f54f62cb496478031ca85aae18bdc2e3f2eac07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179635875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dfa8fc5bb63f783339b5cbfbc61a374302ebbbbfdf9318eb67a4b04ff67196`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 23:17:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:17:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:19:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:19:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:39 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:19:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:19:39 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 02:30:48 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 09 Dec 2025 02:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:31:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:31:13 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 02:31:13 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 02:31:13 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Tue, 09 Dec 2025 02:31:13 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Tue, 09 Dec 2025 02:31:13 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Tue, 09 Dec 2025 02:31:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Tue, 09 Dec 2025 02:31:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 09 Dec 2025 02:31:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:31:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:31:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 02:31:23 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:31:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:31:23 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:6d54cd27f2dbadc5d04ec0756d2663d5a3d1526eb890efb948b0c4773a98966a`  
		Last Modified: Mon, 08 Dec 2025 23:20:03 GMT  
		Size: 12.8 MB (12768507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ce765fa4dfde18b09096c237dbbb6ba8b05a96ad5fc13d2cf6e63ca73a574a`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8ce7ddf74a104be45192626f720a78a38b4b07f38aa9feb4c9e023b7d66031`  
		Last Modified: Mon, 08 Dec 2025 23:20:02 GMT  
		Size: 11.6 MB (11566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb12c8a0f4ced6cc8e82ec3127a06e92266977dcc4f852ba8ba155b2d8998a0`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12de441af61860b987b76efd830daffcaabca7645deaa9211f7fe37d4cb932c`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da7b15f48264e2611f86bcff3a935289958cdc605d1dd53a4f31472dd0612b`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b327abbc493408dabfa8841e0cf290ebda99298ef44a05d738985362cd2c97`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e349eb627ac0256a9f85233262e7e65844d35f6909ba55c482e4e46029705dba`  
		Last Modified: Tue, 09 Dec 2025 02:31:41 GMT  
		Size: 1.3 MB (1307210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da33e373a9a4be5a7d5ffb8a7a3dddf064f6392d25af9feaa422bedad13bebe`  
		Last Modified: Tue, 09 Dec 2025 02:31:41 GMT  
		Size: 473.8 KB (473776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc29b8acf01357c965cbf0974e0093d9bc9f03eeaa1c2d02b9f2c32105b83360`  
		Last Modified: Tue, 09 Dec 2025 02:31:42 GMT  
		Size: 7.5 KB (7482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f44ebfb177538089bb21a178cc5da6505c8613ef5f955149e60f08f57bb12`  
		Last Modified: Tue, 09 Dec 2025 02:31:42 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bac14e44a7fa30ad42ab75997961659e058d4574ee2fcd91523aed6d063fe8c`  
		Last Modified: Tue, 09 Dec 2025 02:31:41 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3abbd0ab8269766dcea3a3dd044e1da432cd544f9b835653f26b808d8843007`  
		Last Modified: Tue, 09 Dec 2025 02:31:42 GMT  
		Size: 778.0 KB (778005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8556f4f65f93e47b624e4d0266c766474a3e8b20b55b70abfd6bfe7fb013fe02`  
		Last Modified: Tue, 09 Dec 2025 02:31:43 GMT  
		Size: 23.4 MB (23404923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:0cb60f0d65302df9e738defe07fbc37a319096ae43f43675f24581d245ee428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04614e07072777c1f5fcf4d7c58d987634e93dd7647df6e3ecc3e4bf05362f66`

```dockerfile
```

-	Layers:
	-	`sha256:bb880f700238ce28d58613000e3287066a637cd44998b252c32fd9124549d4b7`  
		Last Modified: Tue, 09 Dec 2025 06:10:43 GMT  
		Size: 50.0 KB (49967 bytes)  
		MIME: application/vnd.in-toto+json
