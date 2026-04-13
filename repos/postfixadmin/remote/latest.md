## `postfixadmin:latest`

```console
$ docker pull postfixadmin@sha256:7a731d1c119d5fca72062f54f34558ec1c101590b30f7b4975bf3471def59172
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
$ docker pull postfixadmin@sha256:6c4c6c49b26dbcfc77368d9c3c5bb8b6f2b71f70c7df5005026adeba8cedaae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208367426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ce3097ee066626955261ba3aad6f6d80734604139e2b790c691f19f94d02dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:24:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:24:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:24:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:24:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:24:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:24:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:24:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:24:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 01:24:35 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 01:34:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 01:34:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 01:36:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 01:36:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:36:22 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 01:36:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 01:36:22 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:36:17 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 09 Apr 2026 23:36:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:36:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:36:35 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:36:35 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:36:35 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:36:35 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:36:35 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 09 Apr 2026 23:36:35 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 09 Apr 2026 23:36:37 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 09 Apr 2026 23:36:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:36:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:36:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 09 Apr 2026 23:36:44 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:36:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:36:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbd63ae63a08ec4a4cded5f5416ad837a15734fba61fe17c6d8cdf02185970`  
		Last Modified: Tue, 07 Apr 2026 01:27:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5af5dfa43d4c47e59ee529339aa6b8fb67e05dbe1b34fd0f95b08e30e906585`  
		Last Modified: Tue, 07 Apr 2026 01:27:42 GMT  
		Size: 117.8 MB (117843159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24121de25e617ae77d05cd8974c09a9306e3b23b0959f506a257b351284fb15`  
		Last Modified: Tue, 07 Apr 2026 01:27:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de502dcf081a303375db3ebdbc2345d59c61008ef69dd1f79b77869d15d2d0df`  
		Last Modified: Tue, 07 Apr 2026 01:27:39 GMT  
		Size: 4.2 MB (4226904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e11af4b25665980559c4b10e2c5f4be9dbccfbc305bf4800e392753b7562fe`  
		Last Modified: Tue, 07 Apr 2026 01:27:40 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90be0470639d8e068815daa3a4d5bea242aebc16fb4fba794e9806c56c388db8`  
		Last Modified: Tue, 07 Apr 2026 01:27:40 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa182c1d4581894a8b7adb4a9b3a1f5dbeb81a2416b7b965a380cb23bb3bc81`  
		Last Modified: Tue, 07 Apr 2026 01:36:33 GMT  
		Size: 12.8 MB (12774731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4443d9c71a47378f88cdd4826be3f2a90e78b199a8912e2127fcda4427dd93ce`  
		Last Modified: Tue, 07 Apr 2026 01:36:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde0c34d1f458b4c7025011702c139b91f7dc6ecb2c480c6026c142cab0cb9f`  
		Last Modified: Tue, 07 Apr 2026 01:36:33 GMT  
		Size: 11.7 MB (11714134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871c6a1a47ccee76e4e903c43e1e66aa0f1bbe6c171e74710b39cc193f9eb0a1`  
		Last Modified: Tue, 07 Apr 2026 01:36:32 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb746f747ab41ca98bb284359f3cdd0c8c2889afaa22613cc2b7a271598c0ed`  
		Last Modified: Tue, 07 Apr 2026 01:36:33 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6562f7228ec3830e05c2b44def05d89ed833fc0bb0902f71f55927957de4a95f`  
		Last Modified: Tue, 07 Apr 2026 01:36:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568912d7e28db15af3d19b2f8f09b440a9c06cedc96aed1f7eb4335b67b119c3`  
		Last Modified: Tue, 07 Apr 2026 01:36:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd074ae65af15a2f554d19df9d38d1979d442996b90e0a7721b2acb9046d0ce6`  
		Last Modified: Thu, 09 Apr 2026 23:36:50 GMT  
		Size: 1.4 MB (1352064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2633cdb7bd08421eceba9b54bf56dde82c24e310f7355ceb7a8353e220f1b577`  
		Last Modified: Thu, 09 Apr 2026 23:36:51 GMT  
		Size: 3.9 MB (3873377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef5a3816e705a0678ff3f7d40782f449707487f11286d243e4c8e846cb8ed3`  
		Last Modified: Thu, 09 Apr 2026 23:36:50 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc5dfb6e61a6e8073b0ac36e73886000023dfb06a4f2d92fb80086ae3d5d16d`  
		Last Modified: Thu, 09 Apr 2026 23:36:51 GMT  
		Size: 2.6 MB (2602186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01123fa20abca92760eea487ec9847c1feef5f09aadcbdb97af6dddf11f34b`  
		Last Modified: Thu, 09 Apr 2026 23:36:51 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f04ac0188c406c99f87caef09526bf7434df2860721c5f6d43ccb426b0486d`  
		Last Modified: Thu, 09 Apr 2026 23:36:52 GMT  
		Size: 777.5 KB (777539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793dea812093c26673aa867709d650290459cfd7b38a4a87de27df08ca562d09`  
		Last Modified: Thu, 09 Apr 2026 23:36:52 GMT  
		Size: 23.4 MB (23412819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:ce1695aa5d4c0b0937d12a03d5a384262a4b35a4c6c742026263a8f5fe3eed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378826885cbb67a2497f0546aae300d8b0c453244cc0d617d146e2bbe73244e2`

```dockerfile
```

-	Layers:
	-	`sha256:b9f29799a0cd4f41402364ab284aa1aea1e0347f3b3edebd1b6b91d05f49ace5`  
		Last Modified: Thu, 09 Apr 2026 23:36:50 GMT  
		Size: 50.0 KB (49980 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:7e487b4a77e375440a27d9aa6c92b76835293297012ba11b071cab960be6dbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170189735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e9e2fde10d77a686fc8838f923ed01d42d3add75884cf1d27b5efcf57d9a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:29:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:29:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:29:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:29:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:29:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:29:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:29:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 01:29:55 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 01:30:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 01:30:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 01:32:45 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 01:32:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:32:45 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 01:32:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 01:32:45 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 00:15:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Apr 2026 00:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 00:15:53 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:15:53 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 00:15:53 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 00:15:53 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 00:15:53 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 00:15:53 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 10 Apr 2026 00:15:53 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 10 Apr 2026 00:15:54 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Apr 2026 00:15:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:15:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:15:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 10 Apr 2026 00:16:05 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:16:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Apr 2026 00:16:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e82aedfe7821fc24f867b8a4159c354806813945badfbbdb839003260ca6d`  
		Last Modified: Tue, 07 Apr 2026 01:33:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cddce315e100c3bc96434f2ae81901ff196d97bc889fb37323716a14376f227`  
		Last Modified: Tue, 07 Apr 2026 01:33:04 GMT  
		Size: 86.2 MB (86247541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9af748ac925dd1026c35c86479e0bce984b9a969bde1333297f943394a3511`  
		Last Modified: Tue, 07 Apr 2026 01:33:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df57f188a6fe6bb841f24a231b36e4f24bbd1055649187e1ac217b7711a35af`  
		Last Modified: Tue, 07 Apr 2026 01:33:02 GMT  
		Size: 3.8 MB (3757195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab3f7b66658065d78bb037297b03bd50213deaf148757511a7c4f9d408d39e`  
		Last Modified: Tue, 07 Apr 2026 01:33:03 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851902b77cfc719e209d1ee6ba4aa735f8395e367a249003a679022bf0dc46b`  
		Last Modified: Tue, 07 Apr 2026 01:33:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa7a5c6d74678b18cca6f5a0e038889cafe75c4b8c04416f7e26dea8ac07cc1`  
		Last Modified: Tue, 07 Apr 2026 01:33:04 GMT  
		Size: 12.8 MB (12772403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f55a73a74ee1243dcf17f590263a57f4b445cf7a6700590648c442370faf6e`  
		Last Modified: Tue, 07 Apr 2026 01:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f2398516f021796f29ded92d43d5f0a39bbfd7399853970f80a3df27d926c`  
		Last Modified: Tue, 07 Apr 2026 01:33:05 GMT  
		Size: 10.1 MB (10073153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f0de1fb426876908183b1913d28e37d79ee83927d6f243ee11cf40d4af013`  
		Last Modified: Tue, 07 Apr 2026 01:33:05 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485dcbe16923f125ad68c4deb8edb58cbef0c13347c82d8d47147907498dd14`  
		Last Modified: Tue, 07 Apr 2026 01:33:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff9846b33d8cf35dae4981280c6f564b81741e40a030dc4e66f688336349028`  
		Last Modified: Tue, 07 Apr 2026 01:33:06 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d685dac73cff9140c437c6738a4813722641ff71d8f235fe1910786f2c7b1e6`  
		Last Modified: Tue, 07 Apr 2026 01:33:06 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f665bbadf914580797bd4d2b494e70aaeb26fef7940ce7100b5470e2d9f06c6`  
		Last Modified: Fri, 10 Apr 2026 00:16:12 GMT  
		Size: 1.3 MB (1289367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b050f64fc60cb871f48b2f0a0729050a763ff43a3a00029ac38745c5e6027`  
		Last Modified: Fri, 10 Apr 2026 00:16:12 GMT  
		Size: 3.0 MB (3035241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c2cf7d9976112d0beba950483afe4b52a9022041bfdbb26dd21a23dcebb2c0`  
		Last Modified: Fri, 10 Apr 2026 00:16:12 GMT  
		Size: 7.5 KB (7477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db390a9ac6cea8019739258a6c886c73f30fe93efecdcf18b18d3dc222173ee`  
		Last Modified: Fri, 10 Apr 2026 00:16:12 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282689033dca1dea6921858b4b68b626f6b1e478a0c377509cb82b356dfddbd9`  
		Last Modified: Fri, 10 Apr 2026 00:16:13 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d2552494107f68fa28499fd7aca3be6d030f369e1b9a6780d8db25397f69a`  
		Last Modified: Fri, 10 Apr 2026 00:16:13 GMT  
		Size: 777.5 KB (777543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aab72dd98a126f0d5424d683f17cac5665cb801a8793ba2c45e3d1507d5ea19`  
		Last Modified: Fri, 10 Apr 2026 00:16:14 GMT  
		Size: 23.4 MB (23410588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:31fcf48e14183115af4d5a69a75cbecee865df0960fec763e73b4858df7cfa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fb3e1b53e9bd23a5ec15504d2f3cfc73dd6c785c9f6bdcf6c9f4e25931297f`

```dockerfile
```

-	Layers:
	-	`sha256:bff0d8d50e076e17e2d72572b59e0bcbeb2ff43399069d12bf097ffa4559b09b`  
		Last Modified: Fri, 10 Apr 2026 00:16:12 GMT  
		Size: 50.2 KB (50158 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:85fa89353c5a73f0b1ec0598f99914a2f32579229ed3a5cee183098fd034a173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201405272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467a285cae806a3838e3193754d98f73fbe01988dbd4edca51f770c648d5a148`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:34:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:35:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:35:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:35:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:35:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:35:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:35:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:35:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:35:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:35:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 01:35:09 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 01:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 01:35:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:39:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 01:39:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:39:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 01:39:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 01:39:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 01:39:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 01:39:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:39:09 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 01:39:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 01:39:09 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:36:00 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 09 Apr 2026 23:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:36:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:36:22 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:36:22 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:36:22 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:36:22 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:36:22 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 09 Apr 2026 23:36:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 09 Apr 2026 23:36:23 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 09 Apr 2026 23:36:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:36:23 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:36:23 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 09 Apr 2026 23:36:32 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:36:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:36:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf14cfde2434933423961bbc24b781eb17108bca0b5f18951ac888033c300a6`  
		Last Modified: Tue, 07 Apr 2026 01:39:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a69e51ec1b0d6ee27e4c1a6ec5f2bc017550b84c69ab83d5ddde0a2b895d5`  
		Last Modified: Tue, 07 Apr 2026 01:39:33 GMT  
		Size: 110.2 MB (110165217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1989ce9da9071d48a9f10bbc248989952ddd136d18fb1056ef5d1cb6cddf21`  
		Last Modified: Tue, 07 Apr 2026 01:39:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99698ce303ac6cb24268b5dba508ae527e3316fde1b08729d7c0493c86a6befe`  
		Last Modified: Tue, 07 Apr 2026 01:39:31 GMT  
		Size: 4.3 MB (4305591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fa1b011871a92b9b54c267413c3d424b0734d97986f59744a713fe216ead07`  
		Last Modified: Tue, 07 Apr 2026 01:39:32 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cd10658fc796ebb3c09aec76c5b9d5c44ce5ec2f8b3174e61a3563395eb9ac`  
		Last Modified: Tue, 07 Apr 2026 01:39:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dafdc7d0d5f7cfbcb47a4c7f723bf1af1bfd271d050df03b09933f9750fa8c`  
		Last Modified: Tue, 07 Apr 2026 01:39:33 GMT  
		Size: 12.8 MB (12774284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db82578c40d594fafead816bd8c3f0b6aab570b50df0e32afa0c0ba0fa029e11`  
		Last Modified: Tue, 07 Apr 2026 01:39:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd608f0061386d7a11dbd38244d01ac9f636c036ed94c12e531f136f3f049ede`  
		Last Modified: Tue, 07 Apr 2026 01:39:34 GMT  
		Size: 11.7 MB (11732779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50802fcc91aee4770e10ad91bb4429eb82f5ffb85f4da37cbf7dadb7c790a7a`  
		Last Modified: Tue, 07 Apr 2026 01:39:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7998d5ba8f9a232f41749660b2cd676def886250a270939584d36bd3d28454e`  
		Last Modified: Tue, 07 Apr 2026 01:39:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a78fe65013ee0252726f193c29f2dbf155846ab981204af0aea4753b9078ed9`  
		Last Modified: Tue, 07 Apr 2026 01:39:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb44a004b09dfa09151efac73e86ff21e40c83e31003ff1591da28b07bd1d3`  
		Last Modified: Tue, 07 Apr 2026 01:39:35 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb5056b86e3d47a41c1d706f389a147656b9a1ebd353ae181643b6d0641747`  
		Last Modified: Thu, 09 Apr 2026 23:36:38 GMT  
		Size: 1.3 MB (1266030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1757ed423ed010b34988f5649d07f5e4a85781bc75bafd1d631f46e409d291`  
		Last Modified: Thu, 09 Apr 2026 23:36:38 GMT  
		Size: 4.2 MB (4215709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce055bcb005398fb742d4ebe5d7013cec58bc624777eda1e1447318a5640e7`  
		Last Modified: Thu, 09 Apr 2026 23:36:38 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0240ebf03e56a4d2fe924048e060e488d4262997a0c455fa24036d0216343bf9`  
		Last Modified: Thu, 09 Apr 2026 23:36:38 GMT  
		Size: 2.6 MB (2602188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceeb12af938e4d504c83b610249194a0a3053289f00ae31c5590bbef744fdb1`  
		Last Modified: Thu, 09 Apr 2026 23:36:39 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6de26c551bd27a537bd34f772504ffc5136db7bf2f22d53eefbb8d5181d7e`  
		Last Modified: Thu, 09 Apr 2026 23:36:39 GMT  
		Size: 777.5 KB (777544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22871a3aff0301cbb1a17646ae22e2fdeb5ba5f6493c99e526731f9fb9d2f6a`  
		Last Modified: Thu, 09 Apr 2026 23:36:40 GMT  
		Size: 23.4 MB (23412515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f5baf07858fdc22850f275d309ddc4670db11af4307278a644cecca112f26aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474605ac2b4d0ce8667b87faaf461f446ce1969fc842c1839451e384e92068c8`

```dockerfile
```

-	Layers:
	-	`sha256:fad8ef9f259cf679db80e9e413614e545b03e0be3f3fb1cb1b75c24998a5e2f2`  
		Last Modified: Thu, 09 Apr 2026 23:36:38 GMT  
		Size: 50.2 KB (50219 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; 386

```console
$ docker pull postfixadmin@sha256:684e4a7c04972fa961524f95fab528767b52dfaa366807e368aac659626e9ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208540118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac94654c88a1d939761b2611853289bb0c0b51a2f5f449f18deb10819c8bb91a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:16:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:16:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:19:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:19:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:19:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 01:19:47 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 01:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 01:30:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 01:33:05 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 01:33:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:33:05 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 01:33:05 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 01:33:05 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 04:14:39 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Apr 2026 04:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 04:15:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 04:15:04 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 04:15:04 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 04:15:04 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 04:15:04 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 04:15:04 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 10 Apr 2026 04:15:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 10 Apr 2026 04:15:05 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Apr 2026 04:15:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 04:15:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 04:15:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 10 Apr 2026 04:15:16 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 04:15:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Apr 2026 04:15:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706a53cb459d886b815f98d2376b81932690aca063f4cd96d47ac862fd2f424c`  
		Last Modified: Tue, 07 Apr 2026 01:19:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919aefacfe65a7331e03683a17b08be3b4582d0f197e6210fa167a9024dd344c`  
		Last Modified: Tue, 07 Apr 2026 01:19:34 GMT  
		Size: 116.1 MB (116144481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba635213e55b783db3788d60cf50d129847439889e4b2b35c8863c05b94067ae`  
		Last Modified: Tue, 07 Apr 2026 01:19:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96ec9d4297465367c57a27926e031aae0b9b179eade6d362efce0606d6ab94f`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 4.5 MB (4458367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700f4ddcadca492089e6ebba3bd938d31015e1ce0d80531e4d8de4e65e0b6fe1`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab19e63931082fb42f84e0566632fc21f00f760c10e95f7af25520d42d933e3`  
		Last Modified: Tue, 07 Apr 2026 01:23:11 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e36a1c192ce70ded23d7d43c0a78155ccc066af679a3b13ee59108141546ca5`  
		Last Modified: Tue, 07 Apr 2026 01:33:15 GMT  
		Size: 12.8 MB (12773488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659799f654c34a10ba4afca46233dd4447fd2fa00b75afad2f96133a4f8c3afa`  
		Last Modified: Tue, 07 Apr 2026 01:33:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea97383187367e60e64cc5b3d095a8b937af1cb0d984c10652326352bf8a11`  
		Last Modified: Tue, 07 Apr 2026 01:33:15 GMT  
		Size: 11.9 MB (11924323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7300e692ed1b471e90b81e52af5969d8e814afeaba9781b15abd264086eead`  
		Last Modified: Tue, 07 Apr 2026 01:33:15 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c709cb71a9ef196506e2f7dfced927545772a6a927c033f5766943d885038d`  
		Last Modified: Tue, 07 Apr 2026 01:33:16 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdd750ad2c5039dcab1724aa801e8161e1b8291a3e816c2913fd4c20b35ae9b`  
		Last Modified: Tue, 07 Apr 2026 01:33:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b753b014aa23fd9ece2ca330366bccc3196115e75042179e07f1deb4d0449d`  
		Last Modified: Tue, 07 Apr 2026 01:33:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8f3eab4490add585b2c73c3b36a2080def9b70dfca6d61a67839956fb4d94`  
		Last Modified: Fri, 10 Apr 2026 04:15:22 GMT  
		Size: 1.3 MB (1310962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b33d7e29f83178857e876feaed48fbb6109b6ad50cfb42cfd78a952aa6df541`  
		Last Modified: Fri, 10 Apr 2026 04:15:22 GMT  
		Size: 3.8 MB (3830650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee1e4fd39dd868adaa5a610031513db5f90ab10b802266846d2bca831e6c57`  
		Last Modified: Fri, 10 Apr 2026 04:15:22 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708161fc2e4b402c4f097850292dea6436154fc6bebbf4927b595b65b7466bd0`  
		Last Modified: Fri, 10 Apr 2026 04:15:21 GMT  
		Size: 2.6 MB (2602189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8274dc929b1c72e58066c6f3cdd7f5e8bb19ff21ade500ec15c38482a72d4f6`  
		Last Modified: Fri, 10 Apr 2026 04:15:23 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941a963a95ef6b1330a956b88764c32f5f73697d2068137ecc9ae28143f9714`  
		Last Modified: Fri, 10 Apr 2026 04:15:23 GMT  
		Size: 777.5 KB (777544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a2471950b51a8003a801565531767de5f8e6c584ba99ab62df6dcd6fa8f69`  
		Last Modified: Fri, 10 Apr 2026 04:15:24 GMT  
		Size: 23.4 MB (23411987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:36b282b3c88f9cec363fae276b46955c489b93a728701671d13a13463ca52fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 KB (49913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c8da05c61280fe5bdeecd35ff6677fc6d67d24151bb17e880aa1789ef2859f`

```dockerfile
```

-	Layers:
	-	`sha256:49aca721a4552395a66c57e33cadafe57690b24d7b561eeab6398bc97e84eef5`  
		Last Modified: Fri, 10 Apr 2026 04:15:22 GMT  
		Size: 49.9 KB (49913 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:9450f008c2f84a20f71bf993d16e7d7b109d245b9ebbf3d7c0191fc0bba33f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205235651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94b51eef1f81c7ed8f374356caf83cee3010acda93f6cfaa1087bbeb17588b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:52:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:53:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 02:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 02:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 02:15:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 03:19:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 03:19:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:24:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 03:24:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:24:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 03:24:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 03:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 03:24:03 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 03:24:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:24:03 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 03:24:03 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 03:24:03 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 01:44:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Apr 2026 01:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 01:45:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 01:45:41 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 01:45:41 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 01:45:41 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 10 Apr 2026 01:45:41 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 10 Apr 2026 01:45:41 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 10 Apr 2026 01:45:42 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 10 Apr 2026 01:45:43 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Apr 2026 01:45:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 01:45:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 01:45:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 10 Apr 2026 01:46:07 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 01:46:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Apr 2026 01:46:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9146bf73c8a452f415773cc4d7b28152e6a0132b4872c062036e93ceda4a1`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f4a0e07fb6454284581cfcdd933b1a8aeaf834a24a8768bd1bdee7fe76ac43`  
		Last Modified: Tue, 07 Apr 2026 01:58:49 GMT  
		Size: 109.6 MB (109599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e4f5187124bd689202e1c0b532dcdbfed0adfcf45354b5dcc246a80a88c8e`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2826d5bd7597d2bc055cec74a30953477482f418eb99bc191b54a5657bea0`  
		Last Modified: Tue, 07 Apr 2026 02:22:07 GMT  
		Size: 4.9 MB (4881630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4711f0a1e700d515af14d521ed74bc330dbff10a897db0c88f1da3017c82e`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea076c7d43b09b2edeb333274a93e4615a067914cc9eb5a71e39816735581b`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11cc9ff1639fb4b40ae4eb4b41e6201cb03591c897f1790d13fd1e5c2acd46`  
		Last Modified: Tue, 07 Apr 2026 03:24:26 GMT  
		Size: 12.8 MB (12782702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246d9468f3de72ff6c7ff70ee18d7f74fe9b1257a9727b0ac3b641086324a090`  
		Last Modified: Tue, 07 Apr 2026 03:24:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fbbe483a99ebf5d4536191522f970824b676f6871bb5aff8f2bafc3e06c0e`  
		Last Modified: Tue, 07 Apr 2026 03:24:26 GMT  
		Size: 12.1 MB (12121996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803782d98576d9815396b9ba4178d14339e3383e65380f99ed3b81e9cf5a14b3`  
		Last Modified: Tue, 07 Apr 2026 03:24:25 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e103ac87b3d847ced391805db9e801673454ed9d5cf010861b10316148097e33`  
		Last Modified: Tue, 07 Apr 2026 03:24:26 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e73f1f435c10f0489c9e9a25b5828a6d7d3a8819179aa10228f9601d778b6b8`  
		Last Modified: Tue, 07 Apr 2026 03:24:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41bd3aa0726e5ff4e87b80c3351bc6d8511214ab4e4399ec10f3ab3d4ea3f4`  
		Last Modified: Tue, 07 Apr 2026 03:24:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca606f965004ec258a13f708dd680d9d2061710d2640db0abe681ae51c0b9734`  
		Last Modified: Fri, 10 Apr 2026 01:46:19 GMT  
		Size: 1.3 MB (1268576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44df0c2bb1bf8103094f514f0599100e2739da14a4e357a3d3155f0f6535fac`  
		Last Modified: Fri, 10 Apr 2026 01:46:19 GMT  
		Size: 4.2 MB (4181678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d577a067dc244cea39c5bfee00db6967b143352fb6302c334f1eaaa565b20f`  
		Last Modified: Fri, 10 Apr 2026 01:46:19 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc741a4403e3eddf59a4c71c28369bfae98c96161b87e382390be30d54f6e4a`  
		Last Modified: Fri, 10 Apr 2026 01:46:19 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75ee00a94c8341da4e7a82eaed6b835ccbf8f9de53663ed170e69fee081d6ed`  
		Last Modified: Fri, 10 Apr 2026 01:46:20 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1e198d3201886e4f1115c6d2fca971a29efa49a982d415ca5a1c8c864a6a54`  
		Last Modified: Fri, 10 Apr 2026 01:46:21 GMT  
		Size: 777.5 KB (777546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46c0b439c2d517294945d16b7012f9c0b39c9f13b6a2e62cdfc0f0509ca7ca`  
		Last Modified: Fri, 10 Apr 2026 01:46:21 GMT  
		Size: 23.4 MB (23412351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:ce3d5b6b508c586bb52b2b5dc8188ade1dc18bca2eaf19a764665fe0cad3f2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eabf2038f96f94f61f4e9f64581e9e1748f7203da3f2a16f8dc3eb26771c16`

```dockerfile
```

-	Layers:
	-	`sha256:4e0f8f1cffbc0e2e4c7d31b2399ac796c8d86728d77d33e560be9c4fcca348fa`  
		Last Modified: Fri, 10 Apr 2026 01:46:19 GMT  
		Size: 50.1 KB (50067 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:326ad696261ced528939867c9a944b5cfa40d13ec74fd2f34776cc94d09a47d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234496533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ae27c4d476febfbd1e31f0120d13d0f31430675a6cc7070aeffdd6873b8b8e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 08 Apr 2026 07:41:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Apr 2026 07:41:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 08:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Apr 2026 08:31:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 08:31:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 08 Apr 2026 08:31:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Apr 2026 08:31:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Apr 2026 08:31:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 08 Apr 2026 08:31:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 08:31:12 GMT
WORKDIR /var/www/html
# Wed, 08 Apr 2026 08:31:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 08 Apr 2026 08:31:12 GMT
CMD ["apache2-foreground"]
# Mon, 13 Apr 2026 13:39:59 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 13 Apr 2026 13:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 13:44:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 13:44:08 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Mon, 13 Apr 2026 13:44:08 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Mon, 13 Apr 2026 13:44:08 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Mon, 13 Apr 2026 13:44:08 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Mon, 13 Apr 2026 13:44:08 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 13 Apr 2026 13:44:09 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 13 Apr 2026 13:44:11 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 13 Apr 2026 13:44:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Apr 2026 13:44:11 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 13 Apr 2026 13:44:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 13 Apr 2026 13:45:40 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 13:45:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 13 Apr 2026 13:45:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee52d4a171f7393d107004b83735b8f843402b3b39c74ed4d4d39352ef6a11c`  
		Last Modified: Wed, 08 Apr 2026 08:34:21 GMT  
		Size: 12.8 MB (12789097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b6c9e285f7c2e26e3a805da698ab8452e9e6ad745f2b843df736e4f37d62b9`  
		Last Modified: Wed, 08 Apr 2026 08:34:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658b9ddaabb3242ac9bfc4a8a12068a4d85327021e41226389dca11dcdd2202`  
		Last Modified: Wed, 08 Apr 2026 08:34:21 GMT  
		Size: 14.3 MB (14291378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0624e1a4566cc9b300ff135d63938aee84c1c29d9475d7ba385a922263c672f`  
		Last Modified: Wed, 08 Apr 2026 08:34:17 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc2b67fe470036e4dba0bc2c675ad5bc6344409547a2bc996f222dca871fb98`  
		Last Modified: Wed, 08 Apr 2026 08:34:19 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b3a0f0983ad7c8a2925261498fd31742bb8343ac85e280c3998035c3fc11b`  
		Last Modified: Wed, 08 Apr 2026 08:34:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37187d0a79bc22e76a9245a34b80c9d7e931593a72a25cfaafa53d094b257b4`  
		Last Modified: Wed, 08 Apr 2026 08:34:21 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6914e5296d19d1e6d11b97642cd91f9308a80c00348e1c9079d1285a7c4b135e`  
		Last Modified: Mon, 13 Apr 2026 13:46:52 GMT  
		Size: 1.3 MB (1266043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1281ceeffa1b01e1a838fd8556649dd50eec3813863ab856b108bf93f631f187`  
		Last Modified: Mon, 13 Apr 2026 13:46:52 GMT  
		Size: 456.1 KB (456149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883dba1968e2017e05661c22410955a06bcf20c2087758a842d652efd91732`  
		Last Modified: Mon, 13 Apr 2026 13:46:52 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7efb3fc1db139ca2edd3205a8e0b02950c9a67a4b32d5bbfaff45caafb56c`  
		Last Modified: Mon, 13 Apr 2026 13:46:53 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2af2b7aeab81fea4ba9fe84fc1de8472663f63a1fe1d9f7d445bc27a3c34b69`  
		Last Modified: Mon, 13 Apr 2026 13:46:53 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae66f7f451cc859045972f7456750989ed4b4bf73faf7777de8807c633b1ed10`  
		Last Modified: Mon, 13 Apr 2026 13:46:54 GMT  
		Size: 777.5 KB (777548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f1aa0f2977063a56bcf4b73fccd862e4b08684ccf0247f3c92f0e422c734c6`  
		Last Modified: Mon, 13 Apr 2026 13:46:57 GMT  
		Size: 23.4 MB (23413239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:fc6cada79964f91418a2da4d078adf28fa2ea33d08bd3b5b4e80dba0e8254f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66035d939b8ee442b1e45fedbbb9f6b074fcf8eeeb90101323c8ee252fa1d389`

```dockerfile
```

-	Layers:
	-	`sha256:ac2b27ebcbb00a09e99b657927bc4872e6e64d2165be69f3117e8659bbb1cc64`  
		Last Modified: Mon, 13 Apr 2026 13:46:51 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; s390x

```console
$ docker pull postfixadmin@sha256:65dde3d6143858aab855d6f85b3560c6968eb0283d44ee2a09f9d9d84881fa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182739426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644324492e1eb26c07db45581d77d0b71408c200bff83b32697bfc94dcf04718`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:28:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:28:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:28:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:28:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:28:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:29:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_VERSION=8.3.30
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 07 Apr 2026 01:29:01 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 07 Apr 2026 02:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 02:12:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 02:15:12 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 02:15:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:15:12 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 02:15:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 02:15:12 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:42:58 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 09 Apr 2026 23:42:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:43:20 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:43:20 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Thu, 09 Apr 2026 23:43:20 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 09 Apr 2026 23:43:20 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Thu, 09 Apr 2026 23:43:20 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 09 Apr 2026 23:43:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:43:21 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:43:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 09 Apr 2026 23:43:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 23:43:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:43:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a0ba9dd82d347df99933450adc7b4b5ebd450ecf06d8e33de4590c01baf6f2`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ecb81d69135694beb29b311f6564c601c6401fc3cfc01e848c637cd902c1`  
		Last Modified: Tue, 07 Apr 2026 01:34:29 GMT  
		Size: 92.6 MB (92573387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f4ead5e9fe90fedf7ab6cc72e260983245abfab9745bcaf8ac63573660bbe`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d86b92cceade56e257b7a0c3b83c30180afbebb18d02d9326aa539f1432b4ae`  
		Last Modified: Tue, 07 Apr 2026 01:34:27 GMT  
		Size: 4.3 MB (4329556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0deda63bdf870ce31de2d7ef225061f1607e1d17d255e6c312982dfdf0038`  
		Last Modified: Tue, 07 Apr 2026 01:34:28 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8e217a79dfaa8369a757d0d5fb236f873bf2cc136b107c4094232fad4c071`  
		Last Modified: Tue, 07 Apr 2026 01:34:28 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e699cc6b9d17816348d62ff968679f29d5a62484d6feab818455215da23254`  
		Last Modified: Tue, 07 Apr 2026 02:15:30 GMT  
		Size: 12.8 MB (12773235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe4e1f81828d8f89d77c3302b41e27a07995cac29183480b4fb02dd303b11`  
		Last Modified: Tue, 07 Apr 2026 02:15:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b704a1c90cb361df4ef30a710e64167cd254d2e8731ff282220024222ee392`  
		Last Modified: Tue, 07 Apr 2026 02:15:30 GMT  
		Size: 11.6 MB (11571686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b321e0c07b9608e595d342ac31a045bc427b0042ef47f9b72eacec60e97dce`  
		Last Modified: Tue, 07 Apr 2026 02:15:30 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ccb4ffee5b78f8b38f235976f2619079ba2d2a756cf86c1a738f2a4c8617fb`  
		Last Modified: Tue, 07 Apr 2026 02:15:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1df11acd04952e517bf0a3b467dba152d23494baac2f264cb50ccafe2f7016`  
		Last Modified: Tue, 07 Apr 2026 02:15:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad9567067d0449dc2d389884d946928a95bd7493df9b2b62a1504ca1ac52b3`  
		Last Modified: Tue, 07 Apr 2026 02:15:32 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04fcd179ecc38d619c7ecc282574fd37c1430c387ef93f2eb2beca863e468a5`  
		Last Modified: Thu, 09 Apr 2026 23:43:40 GMT  
		Size: 1.3 MB (1307436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2007fc54cbb833ad5ce1d1a732d53e28f423583da9564e554a9dd38314da18f2`  
		Last Modified: Thu, 09 Apr 2026 23:43:40 GMT  
		Size: 3.5 MB (3542962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb07f4239237a9b4fe7371458e9786b6d50df44ede0496234c7b4310a9d528`  
		Last Modified: Thu, 09 Apr 2026 23:43:40 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e298cd7d060a61d083c9fae8aa7a9dc4a6c5a17c777bbad496a41ccfe264a47`  
		Last Modified: Thu, 09 Apr 2026 23:43:40 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859fcba6b4f52333d10239221edf1eaeaacd224aae7f96f5e39534560094c6d3`  
		Last Modified: Thu, 09 Apr 2026 23:43:41 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fa115774d7b6d38371544ebdaa996e1c1f03a4a4d29be3d828b2df0a4dae6`  
		Last Modified: Thu, 09 Apr 2026 23:43:41 GMT  
		Size: 777.5 KB (777535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bec2f9368aa46c9d4e52965d745b5d41ac2d599ec252252d7e48a22bf415bfc`  
		Last Modified: Thu, 09 Apr 2026 23:43:42 GMT  
		Size: 23.4 MB (23411162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:396554d629b584b5a4dd637eb236586388eb1bf8b0270143b12ab5463ab7641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878dd1e4b36f49ddb6c8225aaf75837bf11dc4f73cd3301c5e8acc942ec9f5d9`

```dockerfile
```

-	Layers:
	-	`sha256:cbc0e807d253e7fed004732457fcb8d4f868cf9e77ee0e3ebd42a3f76836ec97`  
		Last Modified: Thu, 09 Apr 2026 23:43:40 GMT  
		Size: 50.0 KB (49972 bytes)  
		MIME: application/vnd.in-toto+json
