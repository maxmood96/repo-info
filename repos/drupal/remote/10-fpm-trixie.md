## `drupal:10-fpm-trixie`

```console
$ docker pull drupal@sha256:fcb1412008a3abd2297aeb14267d0562b3491cd19a18baddf86b725d3b844923
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

### `drupal:10-fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:efef562cd70b81635513bad23b22093cd3f408a5ebb1b0842b9da48fcb3543f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199226109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3920774d00fe61ade96661f46f2d4518000dcd8a99f092accd9707a29d3bf608`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:38:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 04:38:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 04:38:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 04:38:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 04:38:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:38:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:41:20 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:41:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 04:41:20 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 04:41:20 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 06:44:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:44:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 06:44:56 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:44:56 GMT
ENV DRUPAL_VERSION=10.5.6
# Tue, 18 Nov 2025 06:44:56 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 06:44:56 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 06:45:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 06:45:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7988844412cfdac063c91a36a7210df05e34ae43443f3e058db8424a62b44f62`  
		Last Modified: Tue, 18 Nov 2025 04:41:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8c61cdd11feb3e2c406532cc731b25a367fee2d7623fa510ad58b57766ed3`  
		Last Modified: Tue, 18 Nov 2025 04:42:05 GMT  
		Size: 117.8 MB (117837540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3525b2ddcef0c74cb8bd5e676639e076de6d9bd6c0a95d163aebb003dc2eefd6`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d570e6664a4cf136e1fca464b1bd8cef951bcab61cca20e70a69cea098dc3`  
		Last Modified: Tue, 18 Nov 2025 04:41:52 GMT  
		Size: 13.8 MB (13791599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3f2381ffbc21f30d253dc73e77f676131bbeff6f67caf0520e8a2b5b303574`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a8ef726859bc9e47098dd57fb2819a21dad873fa0fdcaf19131737bc30699`  
		Last Modified: Tue, 18 Nov 2025 04:41:53 GMT  
		Size: 13.7 MB (13660971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04461d72c9464d73f46a506ad00f47f78902047fab10b6b24ffaea87d00b64c`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce195a6c827079b359e583ccf91e0331a878877bf625c67c95ae59a273052c8`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74a52a0f3a4543c0c456056dbdae94dbcdbdf47a9eddea673db94e41cef0b5`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57aa505f5bbef6d819b22368c1e7c4e98f127ba6b89db6d73b17ad3f9c1dded`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852afea49e075e8d7c01e33f6008966ed39c34d5912a7b22405e5603b3675e9c`  
		Last Modified: Tue, 18 Nov 2025 06:45:25 GMT  
		Size: 1.6 MB (1632707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e6454272b8f4f8b466d2ca5aedb2d468b98dec4ab47171b807c5c45e4a934a`  
		Last Modified: Tue, 18 Nov 2025 06:45:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4232301170bcba1cc788d8b89721a4d1078cd32396961f02585a23c72cd7b2`  
		Last Modified: Tue, 18 Nov 2025 06:45:25 GMT  
		Size: 772.1 KB (772145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cfb903a913e2881e1482225ffad29af0eba3deb7159b70f894d6567dcc316b`  
		Last Modified: Tue, 18 Nov 2025 06:45:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9b8a41367dd32b252e88155a8dd064915ac89ccd1c94d22a618a150aeb1725`  
		Last Modified: Tue, 18 Nov 2025 06:45:28 GMT  
		Size: 21.7 MB (21741117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:490242562dbc872fea972ac6d035022f69949c168af90acfeb21a3579d2a5e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6840648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee15ceec9c1dd2d67987e269d594e310497b52b80f793c913844309bf935f95`

```dockerfile
```

-	Layers:
	-	`sha256:7ef62a115dd5e4ea56edbbf82ec36e0c7e6019c61343e10e558e862088ae746e`  
		Last Modified: Tue, 18 Nov 2025 08:55:13 GMT  
		Size: 6.8 MB (6803562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:debb33cd1ad420effe0de41fb7f62e2ec334d3ac18acc8dd1992817026417d45`  
		Last Modified: Tue, 18 Nov 2025 08:55:14 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:fbc02e226976e29507c86bc56ca9da20bc8e3b319d61b78b0d87a5d5fbce31b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161680490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9af356016cde4f333c9ce3d30dba08898b1671aac33727a65c80fc99ae383a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:40:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:40:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:40:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:43:41 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:43:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:43:41 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:43:41 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 05:35:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:35:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 05:35:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:35:26 GMT
ENV DRUPAL_VERSION=10.5.6
# Tue, 18 Nov 2025 05:35:26 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 05:35:26 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 05:35:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 05:35:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e15b2702538d58ad41d73933a9ca7ed75636e7a9193fcfd3938af3e225614`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc9c49daa937d4630adbfaea0671b63469bb895e99d2e511e0872b530c2f60`  
		Last Modified: Tue, 18 Nov 2025 02:44:15 GMT  
		Size: 86.2 MB (86246052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04dbb2611276383b057bfc6e2807539484105c24203e1c4d0a1f897e60d45d1`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031b724edc0959a77dc39a18b4309aaaae9cc31abbb6c10ae1c361dd6af8b94`  
		Last Modified: Tue, 18 Nov 2025 02:44:07 GMT  
		Size: 13.8 MB (13789453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6b083293147ca1e207c8b696f3464c3ee9a01191e2db74976ccea920d79b89`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe4e832dadf3287aefb07662280cda13534dcc237bf59e156218457ac0e059`  
		Last Modified: Tue, 18 Nov 2025 02:44:07 GMT  
		Size: 11.6 MB (11561877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7855992240f1e7a219f3dfbd8f347dff0b5263e06a3e52134026725e7f13c3`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b87d105eafbfaff24df97557e7181e93917b7ae8093733732d6c2af68ce271`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f138682af93afa35dd82c8b6bae0fe6a61df98e4b4d9c42496e4097d8b5b4`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1add8c45825d681aef55eb4d850cf454f52fbfbf3bd93dd2c02282632ffa4b`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694b6ea03f5e912caf3336caeff292467c9e619de9c389f1b031b7d206fb38ed`  
		Last Modified: Tue, 18 Nov 2025 05:35:58 GMT  
		Size: 1.3 MB (1346598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b1b6612e78e3c7f7152ff05ee597b2545488cc24f009aaddfe4963bd4afc6a`  
		Last Modified: Tue, 18 Nov 2025 05:35:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0e9647100b048868f295fdafa2491942f5a8ccd972d982ce3895c2d0fa8e5`  
		Last Modified: Tue, 18 Nov 2025 05:35:57 GMT  
		Size: 772.1 KB (772147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efe86b37d7339875f5cf67abe44a7a88cb5e2def44a9ea1423d792ad5a830eb`  
		Last Modified: Tue, 18 Nov 2025 05:35:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a466b7f9e1efcc8b0e1eed441119b6283ae2f23304c9efa8b2fcf55c605242`  
		Last Modified: Tue, 18 Nov 2025 05:35:59 GMT  
		Size: 21.7 MB (21740859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:a515dc6118250e639b410ccf4baf624a043f2efef0d195f0903d3bb665bb76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c306fbfb3b897a339a1b1dc7208b2fe4139ed52a42b528e272ca19ac380444`

```dockerfile
```

-	Layers:
	-	`sha256:42c3e6b7cd49bb8c2050443eaabc6ed2b1f017b0b55ce0e615aac1d653cc6796`  
		Last Modified: Tue, 18 Nov 2025 08:55:19 GMT  
		Size: 6.6 MB (6607427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed93d097913b1f634b193c1b37b0da6eb8d2ddd7f9a6a5f23f2809381ef52ec`  
		Last Modified: Tue, 18 Nov 2025 08:55:20 GMT  
		Size: 37.3 KB (37272 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:a2baf5fbd64edd990f8a2a4a8de89f9d12fa5ed93aed5f2e5254d989eb36361f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191536290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce66ffa6bd42d609758f0181963f4f55d27d2b46a48098e8d7ac41ed6ecbb5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:31:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:31:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:34:14 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:34:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:34:14 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:34:14 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 05:47:15 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:47:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 05:47:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:47:15 GMT
ENV DRUPAL_VERSION=10.5.6
# Tue, 18 Nov 2025 05:47:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 05:47:15 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 05:49:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 05:49:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707c1ebb57f901cb38bf6cf05ed313102f4997f868fe3cfcd5aa0c08a6cd121e`  
		Last Modified: Tue, 18 Nov 2025 02:26:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58514a97ad93e9d6f1994b026483165586a50876b5ed65353eba4fbcbc8387b7`  
		Last Modified: Tue, 18 Nov 2025 02:26:14 GMT  
		Size: 110.2 MB (110162500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70512b0537613eec104ea2b47f21deea93930ca7aac239756a3cf274a7b8fd4b`  
		Last Modified: Tue, 18 Nov 2025 02:26:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2096b1be0b634bd16905d4a216926b8e929116281bf83591a70d003833767fe`  
		Last Modified: Tue, 18 Nov 2025 02:34:35 GMT  
		Size: 13.8 MB (13791291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a35899f4485dff0ee9bd6659a0ccd068973d0b4b523d185f822b0a841b0a4`  
		Last Modified: Tue, 18 Nov 2025 02:34:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b007cf57197326ddaf4aaf98c821711216b2e45a60a3bbbb7c89cef86e558a7a`  
		Last Modified: Tue, 18 Nov 2025 02:34:34 GMT  
		Size: 13.3 MB (13328293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c28e818fdba84235a26b1468589ca017964cdaeb22d448a82845f02b48485bd`  
		Last Modified: Tue, 18 Nov 2025 02:34:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c78c2cf0204b122400b78fdcf121b5fc0c6ccc6b50829c699ca5194f5b86d`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5281a7db138889dea51bca47f4ac405ef107912b8d5408748d0dae0c9c6cf60`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625127e538e46e10a6579f32b633a51d0468f5b2ccb803a25ff680f862035056`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5437a33589ddfd5f81b2abefe087a298c882df0ef85aae38e377d8c309efb7e3`  
		Last Modified: Tue, 18 Nov 2025 05:47:48 GMT  
		Size: 1.6 MB (1590131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c9a234420da0b721db3ee3ecd50d696ed40f24ba2073a4edb2fdc2add55b4`  
		Last Modified: Tue, 18 Nov 2025 05:47:48 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc0bcaab301397f3342694bf8c8a65bfd41eb6c27860bcc7f728d3f0e29dfc7`  
		Last Modified: Tue, 18 Nov 2025 05:47:48 GMT  
		Size: 772.1 KB (772147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bf32fe7b8f6d14890ef756d752e811b899b5641a86ca4a5e0d1254bf6d5393`  
		Last Modified: Tue, 18 Nov 2025 05:47:48 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d6b7c0b3629a587f889058a0b19e9ca26a1d6dcb989d127d08532f0e6b16d`  
		Last Modified: Tue, 18 Nov 2025 05:50:05 GMT  
		Size: 21.7 MB (21739775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:6bc9778ff2170564ca549d6a7aaa4739aaf83a5547556fb60cc72586f91c0e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b029716414da934a2cdea09e2f6055287ae6ca2f326a60b0a4a9091961976cd`

```dockerfile
```

-	Layers:
	-	`sha256:078cd758cd31468d4357e797bbe231413da01cf5db9b88e183783df2e355e077`  
		Last Modified: Tue, 18 Nov 2025 08:55:25 GMT  
		Size: 6.9 MB (6900944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532636e4eff46498496ef3c12dac98674b3dd0a6e520ee4185b63d337ad602db`  
		Last Modified: Tue, 18 Nov 2025 08:55:26 GMT  
		Size: 35.0 KB (34988 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:54d718f73f35b2839be56f8342f30f8af9ae8b1c032f9cf38b89fac05b3210cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199416739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55385df12aaf38ebf0afca2bb8d1e75866069df38b23d655bc3d2dbb18b740e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:26:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:28:52 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:28:52 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:28:52 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 04:27:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:27:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 04:27:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:27:13 GMT
ENV DRUPAL_VERSION=10.5.6
# Tue, 18 Nov 2025 04:27:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 04:27:13 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 04:27:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 04:27:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9ed2cdd021787dec191a45b5dd2cc0df86560b7c37ca01983bcc3b524e1091`  
		Last Modified: Tue, 18 Nov 2025 02:25:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4432538c5a560d91f94280046a687b78b8c8276eea739476a31d69f05e9b04`  
		Last Modified: Tue, 18 Nov 2025 02:25:52 GMT  
		Size: 116.1 MB (116138468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ed3ea53aa36deec3d875de1e4f17d1d65241896416d4af8f1d7b3365ea593`  
		Last Modified: Tue, 18 Nov 2025 02:25:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efcd8f720b0f8f8259983646155f29d2ac2bbe72b57768e859ff2afb371116f`  
		Last Modified: Tue, 18 Nov 2025 02:29:10 GMT  
		Size: 13.8 MB (13790763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbfc6e61acc96c9ec7ce4b6dba0f3f4608f6a1b5f1e26bb84f7d22628502b2d`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4dfa1c11a3ae29a7109811ba49fc3f7fd94bd7cb1a986341f75d6ec08af6f`  
		Last Modified: Tue, 18 Nov 2025 02:29:10 GMT  
		Size: 14.0 MB (13957220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639992346e7fae3d13af805a0d4e39ae958e3e410659f23cf43038a1ab0b861`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91c416c37479df4b1215afdd60417af1f220196c9196a979ca9663ba3420f2`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580c0c32ca496e98ccd516b5d052c30af173008b01c2771b6f89f6d798450f9`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0a4941e2a48ee6a3c4cf7761f072ffde4250e79f09a30276621ec6293c1c6`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b59b36f31ee04f14fb6530410b628c5b24a09c4da8ded1df208452c4ee2864`  
		Last Modified: Tue, 18 Nov 2025 04:27:41 GMT  
		Size: 1.7 MB (1713238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11386e7344b4f4a31fd96b4c438f3b4d26223ef71c7c4f6c89c9d9ea98a489ab`  
		Last Modified: Tue, 18 Nov 2025 04:27:41 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a340b37ba09a993c247f6fb484f1a2934fd094155563705a997a87610fdbee`  
		Last Modified: Tue, 18 Nov 2025 04:27:41 GMT  
		Size: 772.1 KB (772140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43efb9826e15b161e3ae8afb15ae43b9c1c5f8dc7fef5aa46483a8530ab8a9`  
		Last Modified: Tue, 18 Nov 2025 04:27:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a7b5c8b9fd2fc9c49eaf90e7dbbbd3d7ce344dbfc4e40b4d911b1671c1a537`  
		Last Modified: Tue, 18 Nov 2025 04:27:43 GMT  
		Size: 21.7 MB (21738296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:6c6637cc18ae9da4b801dfa1b423405efb5e1740f6c0e306b58e75b605b813f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6814410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad11b1f5c3eceb84d9a291bb6a08daa0f02cf14cf2baf39a3c524e74f1b018f0`

```dockerfile
```

-	Layers:
	-	`sha256:ab596cb03a259f4965ae2c218b06d7f4c4d982a86f03c8781fe44a68ca838d2a`  
		Last Modified: Tue, 18 Nov 2025 08:55:31 GMT  
		Size: 6.8 MB (6777406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c375bb815e26b58bf141dec5a409a6a42ea805e10fc07d60eb18039e3352656d`  
		Last Modified: Tue, 18 Nov 2025 08:55:32 GMT  
		Size: 37.0 KB (37004 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:374c2078266afc36bd15505ea4677d582e30c838bee5d7df4e784416a9f36f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195548107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0d8e0d1cc7282c5cb01483dcec72c7e7b53ed28abd74fcd5e8a8d93601b4dc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:13:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:13:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 03:00:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 03:00:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:14:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 03:15:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 03:15:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 03:15:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 03:15:56 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 03:16:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 03:16:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 03:16:06 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 03:16:06 GMT
CMD ["php-fpm"]
# Thu, 13 Nov 2025 19:17:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
ENV DRUPAL_VERSION=10.5.6
# Thu, 13 Nov 2025 19:17:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:17:48 GMT
WORKDIR /opt/drupal
# Thu, 13 Nov 2025 22:32:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 13 Nov 2025 22:32:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656e7846c7f44be5e3b20020683ff090edb2eb912594bbc202519629107b2cf`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b9ffc03561872af5426b43902b2fa8677357153c8026953c971daa576c870`  
		Last Modified: Tue, 04 Nov 2025 02:18:50 GMT  
		Size: 109.6 MB (109597848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf1f4cde3b0ec73324641d784753c77627b0db1a0e1c39f0478fd104a862fa`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12c388008e9cc92053d381edb5b5c198b5e25df8543bbb843372a746f6b1bf`  
		Last Modified: Tue, 04 Nov 2025 03:04:52 GMT  
		Size: 13.8 MB (13799724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb83b258194d65f6411e481969d68ccb3255de83ccace29505cdcc6c9ff58b6`  
		Last Modified: Tue, 04 Nov 2025 03:04:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26ed855a2fd05714a76dcd88c2fbaa1810942625c428e0e207ee8d1a90738c`  
		Last Modified: Tue, 04 Nov 2025 08:16:42 GMT  
		Size: 14.2 MB (14205902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c770ba072f478d5b38e9d0e9758856c196e4171f63e6e4ee3f31d14d8cc7bac`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121abbf8afcbdec6a71782f4dfa1ea6b91de3be7469b62b2d0d1ca197d3ef`  
		Last Modified: Tue, 04 Nov 2025 04:00:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e6b03653c4e8ca46372cd8bb054dfda2a34cc0419f6c00041a9766056203c`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175b83927e69307d5a394ac08bf52d721d20539de81903ae622492649323e40d`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c9ed0b2adfa2f7b587df8199163b4da5588630415aeb824f65860eb30ccf4e`  
		Last Modified: Thu, 13 Nov 2025 19:18:59 GMT  
		Size: 1.8 MB (1821838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2f3118a10d28c51f0fe140ef8f6218951efa895ca42bedecdca9d402224187`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fd868b88482afd6b09438819d96800c9fddeda1c8437c357a8549c4f507e9`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 772.1 KB (772144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c0fd2e075fbd62f540278c85ae08b082c99d169b8086d51b44e7610b74858`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68ac143bb2da4d1b39ca9e5433070827ba4f846464259b3e8627eced2cd0455`  
		Last Modified: Thu, 13 Nov 2025 22:33:01 GMT  
		Size: 21.7 MB (21738464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:bb7a5f2c09e93121e6f0de6a8a3747ed31b604f3a0d2cea57f5a66bc59ab6784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6840486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e77e5c7810672548689eb05b15ee7d567ca0440b74eb8d1989e65ca17a4aa7`

```dockerfile
```

-	Layers:
	-	`sha256:7ad72c28905912ed146e9a36bb2adfd281b91a157445f3a0cbf18f458daef34f`  
		Last Modified: Thu, 13 Nov 2025 23:55:27 GMT  
		Size: 6.8 MB (6803293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d462c34a19f5a3bc6e01b6c5972ac985d4ad5ac59ed941a85636512ab8e3fa03`  
		Last Modified: Thu, 13 Nov 2025 23:55:28 GMT  
		Size: 37.2 KB (37193 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:5ad7c3a71ed433a3f7111e9445b6e241b36c426f039919181fdae2ae67288b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225858913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f752922eda1e4122a8b6e7d40f7b98d226b5ff4e4e32e7e4baecd3e2f994aea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 05:51:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 05:53:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 05:53:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 05:53:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 05:53:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 05:53:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 09:41:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 09:41:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 12:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 12:31:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 12:31:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 12:31:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 12:31:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 12:31:41 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 12:31:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 12:31:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 12:31:42 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 12:31:42 GMT
CMD ["php-fpm"]
# Thu, 06 Nov 2025 08:07:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Nov 2025 08:07:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Nov 2025 20:18:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 20:18:09 GMT
ENV DRUPAL_VERSION=10.5.6
# Thu, 13 Nov 2025 20:18:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 20:18:09 GMT
WORKDIR /opt/drupal
# Fri, 14 Nov 2025 19:49:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 14 Nov 2025 19:49:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b60b8763b9288d96a2c0a03f91b6bbda8b8e90cabe195aac6ab08bb9b7c3be`  
		Last Modified: Tue, 04 Nov 2025 06:58:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ab2470133012ddd1028070c153f252fcdd37f14c86fe8f1b3bb6c5c16701c`  
		Last Modified: Tue, 04 Nov 2025 12:32:14 GMT  
		Size: 146.6 MB (146578993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9382a8b397fe6627424fd03c69c0c2a758bc0e6965d1d6005ac796e8fda70e`  
		Last Modified: Tue, 04 Nov 2025 06:58:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f17361ee032cd66332d69b356101753fa641c0b2c743fa397abc56629f02e9`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 13.8 MB (13799575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ddc026a571f42a77d8e0bfcb9b4bc04a0aa8899be19c6268950bb80187ee52`  
		Last Modified: Tue, 04 Nov 2025 10:38:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c0b892cf252817096e4c2b21d3a1aa37b659cb5c1f962f21b5b83c2298d4e`  
		Last Modified: Tue, 04 Nov 2025 12:34:50 GMT  
		Size: 13.1 MB (13131594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27134edd8ce3c1babb30e7f9aa42f9199be4d3851e1a3e62980fb9b0d518ce1a`  
		Last Modified: Tue, 04 Nov 2025 12:34:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8de49296df32d3399124292b87c0dd38694bd961e946014cd3646f363472709`  
		Last Modified: Tue, 04 Nov 2025 12:34:49 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874cc1f1dd8de312e692989ca54736aeb96f15d66548491c20312b1c1d0d956`  
		Last Modified: Tue, 04 Nov 2025 12:34:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd25430915e44f56f0912a3ae5b02a878bb4ff088975c07cb34ab2ff7095ff9`  
		Last Modified: Tue, 04 Nov 2025 12:34:50 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad42cfe8a2886a72d0a045cdb6cdb5de547750da1babf01e11d5afa5f30ebe`  
		Last Modified: Thu, 06 Nov 2025 08:13:04 GMT  
		Size: 1.5 MB (1548533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baebf8a0939fad7f13254892bb179c694aa543ed7a7c2ece0a1ecc8dfca8b24`  
		Last Modified: Thu, 06 Nov 2025 08:13:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145ba0a3db8a840fd033cb854c4a8a76b3ec8d1821c98f60e8c601ee6b4e292`  
		Last Modified: Thu, 13 Nov 2025 20:23:49 GMT  
		Size: 772.1 KB (772146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b20882a36a1de2dd8d28db3c3192d2d9a29df3a962c1bc4faf807bb3fb252a0`  
		Last Modified: Thu, 13 Nov 2025 20:23:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a29acf9c804abc245774dc820d6ac1f3fbfd32416ac2e47d086b60e63a4cc02`  
		Last Modified: Fri, 14 Nov 2025 19:53:50 GMT  
		Size: 21.7 MB (21738727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:dd6f7f36e627cd6241261c4aa9abc259f6b57b6ea5f6986d16c3ae72ca3c854b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6912546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d53147f2cf582f6c09df49b292fff2e34639691cab3ba989eedb14e54c4b77`

```dockerfile
```

-	Layers:
	-	`sha256:a866dc982d4da8496786bcdec19d02305d4e6c997072cc87fe85fa0549350952`  
		Last Modified: Fri, 14 Nov 2025 20:53:55 GMT  
		Size: 6.9 MB (6875354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda2d3d148b33c9bb53d946c4ccc25ced2a5f261d30c98c975e130e1595e1c59`  
		Last Modified: Fri, 14 Nov 2025 20:53:56 GMT  
		Size: 37.2 KB (37192 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:c84ae78789af812fb09e5b41dce94e6b964f375d9d99e5cf8c87daed42db6304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173826098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a9ae6b6c48e5ef28f70a465eef20f3a2db39e6e278a169e2a12446cbf7c3eb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:23:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:23:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:23:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:40:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:40:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:43:32 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:43:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:43:32 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:43:32 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 06:10:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
ENV DRUPAL_VERSION=10.5.6
# Tue, 18 Nov 2025 06:10:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 06:10:14 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 06:10:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 06:10:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6112e3b80a3e216627481de123e8987e8cbfea908febedcef4d94eed43b14cf4`  
		Last Modified: Tue, 18 Nov 2025 02:26:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1cb9329bce7ae43bba9aade993af0716833c7ec3d06730bc0608966c31f5fe`  
		Last Modified: Tue, 18 Nov 2025 02:26:45 GMT  
		Size: 92.6 MB (92564354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc3e0671c639ec518dccc66d47a93c2878c73e2a26fb691b9604b4a7f6acf75`  
		Last Modified: Tue, 18 Nov 2025 02:26:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac38f4f86881882fd11f2bbee5b60d62a9695d85aa40fc15ff52ab60eb282e`  
		Last Modified: Tue, 18 Nov 2025 02:43:56 GMT  
		Size: 13.8 MB (13790209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dd9dcdf6ee5759ed497535c2fc8425c19d7a46bec9bf5fea223f411d9a744e`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee30960862e4c7f18656a3ed42e981ec23e2dd33fad13a549e7e21817a12f7d`  
		Last Modified: Tue, 18 Nov 2025 02:43:54 GMT  
		Size: 13.5 MB (13458606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdc92ec277d996082be86ee7616e0339ff7a3d395e3a89e87d9c99dde9a357b`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc17e811fac2aa081dce751b0d0bb31eec8bbc14eb4abde6965dfe35d713b2b`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4692b04cfd5343a7fbb4c2c08b295be2544629024fefdd2bdd3f48958b79f8c`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd341d193e78806161f22d02b2de702259cc3087c8528077c3e5067a6c8d52d8`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a041d0c12e16b49585519562e2c50b44bfe96de2e0bb529b4965edfe428498e`  
		Last Modified: Tue, 18 Nov 2025 06:11:09 GMT  
		Size: 1.7 MB (1651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c6a8b94cb3783f554b7ba2747055bc24b406cfd701639419d8a9efabcf75d`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bffe1b4689fe9e07c7e135b390fa061cb7e365af47636fb15bdb64bab6d932`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 772.1 KB (772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c949d2bf41ff6fbc30db5e3b171c1ec793661de7af3eac72a22bf67189dd048`  
		Last Modified: Tue, 18 Nov 2025 06:11:08 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec2b85437f54cdc6f36b9513469d2bc2c297715d0cf3e22caf8d38cda55f78`  
		Last Modified: Tue, 18 Nov 2025 06:11:10 GMT  
		Size: 21.7 MB (21741129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:d11958846f2b07df6e9d272cc5d5ff49bc126669ba47c44678adebb9339d46cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6657908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4969f4e99b6c2df4497e250d107ffccb614431697ddd8baa81fb24099360084`

```dockerfile
```

-	Layers:
	-	`sha256:665b57e26e60822a9e1635a5c2e039a79ad0566e9271d926b897387ef4da9f65`  
		Last Modified: Tue, 18 Nov 2025 08:55:48 GMT  
		Size: 6.6 MB (6620828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de5f82004aeebf6bf98006e8c3071e6af8117148afda8a07210c5fbda15ad51`  
		Last Modified: Tue, 18 Nov 2025 08:55:49 GMT  
		Size: 37.1 KB (37080 bytes)  
		MIME: application/vnd.in-toto+json
