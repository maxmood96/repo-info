## `drupal:rc-php8.3-apache-bullseye`

```console
$ docker pull drupal@sha256:5145061f968b93a450de7f62dd2ffb5424e7faef3760571f42f4449c2d5402ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `drupal:rc-php8.3-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:db575c039a3eab0f7cc66c2654640728ad38016950f0bbe3d759a223080a4297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188519888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed5b66645c58f92ade7a0dfa89e425557d1a8fa2dbe0fd580d57dd30522cb94`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:01:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 14:01:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 14:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:01:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 14:01:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 14:04:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 14:04:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 14:05:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 14:05:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 14:05:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 14:05:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:05:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:05:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 14:05:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:40:22 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:40:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:40:22 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:40:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:40:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0754b57b9b7d3a089ca18ba98121861a56ce2624c2875a8e7bf8b21a7957eec8`  
		Last Modified: Tue, 21 Nov 2023 16:37:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e5060f3937930b5fa3d39f56adf3c2acfea72741014d1969f3f437e5835631`  
		Last Modified: Tue, 21 Nov 2023 16:37:56 GMT  
		Size: 91.6 MB (91635313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25a6e74b7f558f50a59c2efa94a62c44a6323861b0c76e6d2144078ab6c5ed4`  
		Last Modified: Tue, 21 Nov 2023 16:37:43 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d33b602102b183f8435dd317aff8889153fbf7eb46df307891feaa427a627c`  
		Last Modified: Tue, 21 Nov 2023 16:38:15 GMT  
		Size: 19.3 MB (19259224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866c9e44fbd45ff348f92197e8339f30a9888e80f74473a4354e370b3039760f`  
		Last Modified: Tue, 21 Nov 2023 16:38:12 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2572036f7c292392aafb9fb89d2ce0215b5dcb6c8046f4e3eba4933e1f16d0`  
		Last Modified: Tue, 21 Nov 2023 16:38:12 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab1bff1bb9be42e4f64dc7c177ec927216df96fcfc7be881cab4340b067e06`  
		Last Modified: Tue, 28 Nov 2023 00:11:57 GMT  
		Size: 12.8 MB (12772922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4511ca74e80ff75450de242cdba63417c8d8aad13499b65830b1db1b4808935`  
		Last Modified: Tue, 28 Nov 2023 00:11:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71f0667d858b807d68765489ca3da414964d93f533fe580baa158fd33d3656c`  
		Last Modified: Sat, 16 Dec 2023 06:42:37 GMT  
		Size: 11.6 MB (11600053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec850b2f6b2cfdc2cd14a9c88e75fcf09d135abf12867d1e94aaf9bbd25024d9`  
		Last Modified: Sat, 16 Dec 2023 06:42:35 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35d5f47f27604158404ff4a36279ae022dace3a0856e6ee0e56031360165725`  
		Last Modified: Sat, 16 Dec 2023 06:42:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac8bac61f933c352e5f28a07ed269b918b3ae94a2f4142d4255f307f1ce312`  
		Last Modified: Sat, 16 Dec 2023 06:42:35 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d4af7f741987c6281869f37e9d6386f557ec4be5b00571289868d9e85f59c`  
		Last Modified: Sat, 16 Dec 2023 10:48:31 GMT  
		Size: 1.9 MB (1929722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a3b8bf7e7cdf8d1943389b962e047abd90cc067bda94e436555822d92aa9c8`  
		Last Modified: Sat, 16 Dec 2023 10:48:31 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeba18d7bb243d11967518274bf3499501eef37422b9435df9c29f409891915`  
		Last Modified: Sat, 16 Dec 2023 10:48:31 GMT  
		Size: 705.2 KB (705210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4d8a08a706db840be1353cf8e1d8b2308f22b68ed5e6176c2c96cc9d40087`  
		Last Modified: Sat, 16 Dec 2023 10:48:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bbac40b17de109ec19a0dd1a03fcf405897e8946af842f2dbb8eb4fa64c24`  
		Last Modified: Sat, 16 Dec 2023 10:48:32 GMT  
		Size: 19.2 MB (19193620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:87aeac169e89e511e6f5da432191780248c8656ba46c2a46a3408da63072334c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6006392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0b7fd378499ee11c23416b789e1a5133af90f291a17cac21db4504e90b4036`

```dockerfile
```

-	Layers:
	-	`sha256:b620ca594f04245680ec9cae87ed16d792f471d94053b45d16768d07fa5b1144`  
		Last Modified: Sat, 16 Dec 2023 10:48:31 GMT  
		Size: 6.0 MB (5967323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385e91dc9b5b82bc08bd0267665851e3a320f3257730ba5aedeb48950bc648d0`  
		Last Modified: Sat, 16 Dec 2023 10:48:30 GMT  
		Size: 39.1 KB (39069 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:11e2743f59213ff29f2eff058eeb00f69db06b79bc68100d9716d6dae4973621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157943480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b9d72148e74e84bf75e191f2b614aeb73f6fb5fd7ae7a256bd42f8e3edcc9f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:04 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Tue, 21 Nov 2023 03:58:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:37:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 08:37:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 08:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:37:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 08:37:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 08:40:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 08:40:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 08:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 08:40:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 08:40:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 08:40:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 08:40:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 08:40:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 08:40:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:23:07 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:23:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:23:07 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:23:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00118114a1839c710dff505972914cfb60bfc81927081b4315a18f6c424531f`  
		Last Modified: Tue, 21 Nov 2023 10:52:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbdada88591659c80fda241d952db57844abfa1bddf9bd59aed59eb4e756389`  
		Last Modified: Tue, 21 Nov 2023 10:52:37 GMT  
		Size: 69.3 MB (69322894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f115413ab5c0481075f5e637d041f9c76020e040854004fd7188869d6cf2d`  
		Last Modified: Tue, 21 Nov 2023 10:52:25 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bccac24513cce414ff6f596621792454590cfcfebd2d8f3db79651bbd72050`  
		Last Modified: Tue, 21 Nov 2023 10:52:57 GMT  
		Size: 18.0 MB (18017813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c712ec22d9e608ec098ccfd3d6f03dc49ad78131e6f220bb9d8c9b0412998b1a`  
		Last Modified: Tue, 21 Nov 2023 10:52:53 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35499e190aed7216d431797b167104750ed92b22ab148e52b96bca41bb1c4784`  
		Last Modified: Tue, 21 Nov 2023 10:52:53 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2828c99b75a037812e044033108289d338098db62ffeae9c7505238117d7c238`  
		Last Modified: Mon, 27 Nov 2023 23:49:27 GMT  
		Size: 12.8 MB (12771418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e202b10a6479fa717269fac76b7cc11ed3b06941c98ea17561189977aa9f1e`  
		Last Modified: Mon, 27 Nov 2023 23:49:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407e6cafd58544e506329a941389944ced3f99c9edf90103d54c5c18649237c`  
		Last Modified: Sat, 16 Dec 2023 06:13:30 GMT  
		Size: 10.0 MB (10036473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66b4b56c76bb8011a4bae79b2aeb82c0eb271061438f2377ff0455b6e338e9`  
		Last Modified: Sat, 16 Dec 2023 06:13:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073fc04704ab9b5b5f24606e69f93cfa5a54a114657c655286ce009c24bac20`  
		Last Modified: Sat, 16 Dec 2023 06:13:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb16f10842e164e4e2514915a30d22761127d65f5b5b7ec4f337369a21a75e1`  
		Last Modified: Sat, 16 Dec 2023 06:13:26 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34222c1893d710963a1c30edadf938644c75f50f08ba6b11b30d8ae461b64a73`  
		Last Modified: Sat, 16 Dec 2023 11:53:37 GMT  
		Size: 1.3 MB (1310869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcdfd0c59d2778a5d207c44e37207b41bd0088926d1f2e4e7edeb6e6c8c8254`  
		Last Modified: Sat, 16 Dec 2023 11:53:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92c1d0802662e71e1f64caa3d786898e7720b1e003546c8d9bf43c6c317dd66`  
		Last Modified: Sat, 16 Dec 2023 11:53:37 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be183e66f83d652467b3edf7a617e77d0300ee1aea0b1058123783b42a30d6`  
		Last Modified: Sat, 16 Dec 2023 11:53:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913137921762e0e904aa13b2012f289933c0b39a9ecc01bf980187be24ad9aea`  
		Last Modified: Sat, 16 Dec 2023 11:53:39 GMT  
		Size: 19.2 MB (19193770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:69ffba5b3d525074b5e894ace63c4cb5c0764e2521a68bef8a645d683340e43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5838683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c4d1650ef574667dbaf26c07ea9505c359697f4d465bdb2690229dc3785644`

```dockerfile
```

-	Layers:
	-	`sha256:71d394a4dd5d8ed49cbc2d12aaa4d2a55177addf5229f299e5d58e7a5a9fc37b`  
		Last Modified: Sat, 16 Dec 2023 11:53:36 GMT  
		Size: 5.8 MB (5801783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e59b5d8e27f5e1b9d540ba271bf996d132d77349dc0b17dfb9ccfc2e86d7286`  
		Last Modified: Sat, 16 Dec 2023 11:53:36 GMT  
		Size: 36.9 KB (36900 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:9aebf99b93418434407e262fc1839df1002b3e625c9e15c57252f305d99d6eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182713623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b4e6f7eab1d4028b982a3c45a7e6283bd1513ecd7f1fb4a622c372c04a779`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:15:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 14:15:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 14:15:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 14:15:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 14:19:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 14:19:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 14:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 14:19:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 14:19:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 14:19:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:19:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 14:19:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 14:19:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:09:18 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:09:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:09:18 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:09:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962dd5329fe78a5b7771f5e8185e57fa02ab85dd0e29d06209fd0c765e4fcfe`  
		Last Modified: Tue, 21 Nov 2023 16:36:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343833a8d9a793ce2a45a7c002adfa6a3bb5a7979770e9179de28b8e5adf8ca7`  
		Last Modified: Tue, 21 Nov 2023 16:36:48 GMT  
		Size: 86.9 MB (86933577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2591c5ed67a6732c68cab0f741ba7fc77bb24bab13c72c0c116435b6a4009c6`  
		Last Modified: Tue, 21 Nov 2023 16:36:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83b5f940f44725d68bd99daece80d68f31be2e8556e630a054c3f25c95caea7`  
		Last Modified: Tue, 21 Nov 2023 16:37:06 GMT  
		Size: 19.2 MB (19177585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe40c918833f655210f1f82dacfd83abd2298a6dbef516604dae8e314a41368e`  
		Last Modified: Tue, 21 Nov 2023 16:37:04 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ad5a90509716966c24807c6e5995b82c37154367e22c79ea4d3802cf30ef65`  
		Last Modified: Tue, 21 Nov 2023 16:37:03 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7e43f4bf99511677d503916b79440e0ad0c55c4f2509b57fcddd5bd28d06b6`  
		Last Modified: Mon, 27 Nov 2023 23:37:41 GMT  
		Size: 12.8 MB (12772175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41a0ca0859cdaa71c7626a595b6a1d66fa69c6452fdaec8f9a5ccd3a4f0b`  
		Last Modified: Mon, 27 Nov 2023 23:37:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4637028659d08329edfc3d966dbb42f146a6635fab178bbf72d8567aedf08`  
		Last Modified: Sat, 16 Dec 2023 06:00:34 GMT  
		Size: 11.7 MB (11668015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df741a9c2a1a3b5c5b6f66976fb4d93a5d0196eade062e1d43579bb4aef9ab3`  
		Last Modified: Sat, 16 Dec 2023 06:00:32 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea1cd237bc5d9a0a0f8c01901b9c9fd84c4ae08d73929f8034a215168743c5c`  
		Last Modified: Sat, 16 Dec 2023 06:00:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deeffc611d9ff65ba4bfb7ddbef902a5d7c9a8f84175c041088c9239f08c015`  
		Last Modified: Sat, 16 Dec 2023 06:00:33 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00e76454abdd433873b1dd71f4040df65738907b9ddd7c53d522c11b4106de6`  
		Last Modified: Sat, 16 Dec 2023 19:30:10 GMT  
		Size: 2.2 MB (2193466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b619ee210be8d3d1643effdcc7cbe6f01f55669e2cbf3cad1ed82a72d5b8b5aa`  
		Last Modified: Sat, 16 Dec 2023 19:30:10 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd94ce448cb568caf7e3d1dc90e74c30f522a34eb2aa1bbbea6917c706ae313`  
		Last Modified: Sat, 16 Dec 2023 19:30:10 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614e20a3a537de3343080690c4d61228596e5e16144066cb3b7e002c50dd201`  
		Last Modified: Sat, 16 Dec 2023 19:30:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96668c9d5f407b3537d267a0246272c4c44ca9bc11a279b76c1d37ecbb2b432`  
		Last Modified: Sat, 16 Dec 2023 19:30:12 GMT  
		Size: 19.2 MB (19193469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:67673292c9abae6391de1e8bf873255c2f519eac5da51fd6a8e780a7f43f707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6006813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d22657758e4b00ad7d2ccc1ae0b9d4f3ef2a93a97e7021c95bd0607ff6cef45`

```dockerfile
```

-	Layers:
	-	`sha256:1ffb94ffb302e4a111d2d9d37f94d54c9cc6cc8bea4fefdd9de5b2fa37cb4140`  
		Last Modified: Sat, 16 Dec 2023 19:30:09 GMT  
		Size: 6.0 MB (5970009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2df8629a90aa9559f9cbfe9c974f1005827b9cc7b734088f5d241bcd516e5df`  
		Last Modified: Sat, 16 Dec 2023 19:30:08 GMT  
		Size: 36.8 KB (36804 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:0c8a51067572d64a2f22ec6db0914db79af95213fb3e0e0617fc212f3c67a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191366439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce70a6ceaeb81f56e94024b89ccfed8e458c1078f5562280d9c6ff076585c21`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:15 GMT
ADD file:7de881b584405a880c4d02778056aaa81bb5dd5d1af65b3086d66aed9ff0ad4b in / 
# Tue, 21 Nov 2023 04:40:16 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:47:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 09:47:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 09:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:48:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 09:48:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 09:54:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 09:54:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 09:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 09:54:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 09:54:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 09:54:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 09:54:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 09:54:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 09:54:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:11:30 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:11:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:11:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:11:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:11:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:75c11612678b54e79a38118fe66e532c61b3d0798afb741007b4cd3209c0ec4e`  
		Last Modified: Tue, 21 Nov 2023 04:45:24 GMT  
		Size: 32.4 MB (32402632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d5ea5604b9d5e6c2327efcf70a55b5b343d4efb21ef7682636424a47f89122`  
		Last Modified: Tue, 21 Nov 2023 14:13:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e173b0090b614752b3bd03186bedc273001922e0a82892b5757b5574a1a4425`  
		Last Modified: Tue, 21 Nov 2023 14:14:08 GMT  
		Size: 92.7 MB (92724390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c70549cb086ee59c11e9f8d36cf19fac1d8073b169bc9127df1982ff7a4f510`  
		Last Modified: Tue, 21 Nov 2023 14:13:45 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f030b6f6639a9b3c6a1074505ddeeaa67a60444f563ecb6aae3deb95a3e9d2`  
		Last Modified: Tue, 21 Nov 2023 14:14:29 GMT  
		Size: 19.7 MB (19745363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7776c262cb5d6956a7cac217bcb580059ed29b4f47d660bf8f5e13dea14d16b`  
		Last Modified: Tue, 21 Nov 2023 14:14:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f670f3cebd80e8fa34c0c681b25a47f54eb403fd511bea894ada7deaa4f25c5`  
		Last Modified: Tue, 21 Nov 2023 14:14:24 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bb9035c8cbf5c00a04a3e52f494b5d75b84bae080159a92078a8b4d8b3dfa0`  
		Last Modified: Tue, 28 Nov 2023 01:34:04 GMT  
		Size: 12.8 MB (12772216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390905d2301e67a22ffd52d57504d8da323969d503e31e5ecca423d81b05ec01`  
		Last Modified: Tue, 28 Nov 2023 01:34:01 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21020b0130bf1d13e9f6a1d876228048133122b5a9a62809db3feff384fc6b1`  
		Last Modified: Sat, 16 Dec 2023 10:06:48 GMT  
		Size: 11.8 MB (11820353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070152697bdef21d1ba9d8d38ac9844ca0694d0018fd3b11a47d2be85ad8fae9`  
		Last Modified: Sat, 16 Dec 2023 10:06:45 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172b41f771570dbb3b82d8d6edb26d12f283aed8163cb5f01ede8da3a084d71a`  
		Last Modified: Sat, 16 Dec 2023 10:06:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c204372568929b75019c97bfac59c62abbe4eb533f7436a7934fdf5c86db239`  
		Last Modified: Sat, 16 Dec 2023 10:06:45 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560271d7717ba9f44af55f18ff9fb86e4d6f7f331bf682cfe62087d4f0cced55`  
		Last Modified: Sat, 16 Dec 2023 21:48:53 GMT  
		Size: 2.0 MB (1996555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476ca6ff98d2d9ca4adb72bf5baf85cbc186e71c3c326b763723ed495e6da50`  
		Last Modified: Sat, 16 Dec 2023 21:48:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dd8b952bfd101225fcbba56fb9b961078823b3afd1ce4321c973dddd963a23`  
		Last Modified: Sat, 16 Dec 2023 21:48:53 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aba3275bf00aa205f323e60081ca5e08505e080ec1e5e6c78c2ab867ded4dd0`  
		Last Modified: Sat, 16 Dec 2023 21:48:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401594f4846a66248f21ff5f2d1d83649bbf5f87b58c3d46453ba3fe7950a120`  
		Last Modified: Sat, 16 Dec 2023 21:48:54 GMT  
		Size: 19.2 MB (19193709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5ad037ff7217281a59d60e05b8dd5f97e5c94f1a817f8bdb0d1f526883ab5e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 KB (38822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4524e83ab46b7544fcd7674094740be08233b7b6a03e95adc02410dc07e77e`

```dockerfile
```

-	Layers:
	-	`sha256:d1e99edd8184421e1eda985bee0a3d072b2cc74d34a7c15b33aaf32ecbd02519`  
		Last Modified: Sat, 16 Dec 2023 21:48:52 GMT  
		Size: 38.8 KB (38822 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:1aea4ab41926fbcad99b960ffd16810d86ab63c699c4d8e7987cca18a17be0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40290aad1611d67bdfde309b76f9173f051bf409b5dbf042f4e6b0e6186655d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 13:16:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Nov 2023 13:16:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Nov 2023 13:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 13:17:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Nov 2023 13:17:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 21 Nov 2023 13:20:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 21 Nov 2023 13:20:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 21 Nov 2023 13:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 21 Nov 2023 13:20:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 21 Nov 2023 13:20:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 21 Nov 2023 13:20:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:20:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Nov 2023 13:20:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Nov 2023 13:20:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 21:40:04 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 21:40:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 21:40:05 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 21:40:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Nov 2023 21:40:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773c547f3c0aa5a48c6fdc0bf9f6db649f30bbe51f8daf375233167a64f10d2`  
		Last Modified: Tue, 21 Nov 2023 15:19:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac6a64a4258db247aea2855fa6bd828091c762a0e58c3124dc996c30c18ba13`  
		Last Modified: Tue, 21 Nov 2023 15:19:42 GMT  
		Size: 86.6 MB (86641900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ac2fa78b90aba05f0034a35e87616e7518f6c301fab6e4b1613890d37fe258`  
		Last Modified: Tue, 21 Nov 2023 15:19:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7fa080c9b88b1c4f5a1e2df863ee5959df92a489942604eef19cbeb84e2ea9`  
		Last Modified: Tue, 21 Nov 2023 15:20:04 GMT  
		Size: 20.5 MB (20474886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff0fab872b4e553d8e83a67b9e361becf709b9ff03f198075f966b8ed6e7bc`  
		Last Modified: Tue, 21 Nov 2023 15:20:01 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99af5918931dafd542d3792c914f9c64ee2b2b449e92023bab1dad63e3d5f18`  
		Last Modified: Tue, 21 Nov 2023 15:20:01 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7ba0735dba489b18b925e8814282505582349d292cae744021ef0f78b5cc33`  
		Last Modified: Mon, 27 Nov 2023 23:49:17 GMT  
		Size: 12.8 MB (12772847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fd564c47eb0842946c1e64357f921f85ce9003c5a69d8d4075c18db3f453bc`  
		Last Modified: Mon, 27 Nov 2023 23:49:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab7fbb3b77a17e766c0ba9d64573bcb841ab8ad82dbc511964061dfba9b294b`  
		Last Modified: Sat, 16 Dec 2023 06:07:46 GMT  
		Size: 12.1 MB (12052980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d40f3622443e9e9104c1307975c559e9ffa457d07d20da0543c7c3f802bfd0`  
		Last Modified: Sat, 16 Dec 2023 06:07:43 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7655fec61b3d89c9c3e00212b57df0e72a653cc59eb7a1c4909fc0b348330c6`  
		Last Modified: Sat, 16 Dec 2023 06:07:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f474b097cedcca804913f6e2ace4ef6b5a98d10379ae601bb0951aa5bd33a8`  
		Last Modified: Sat, 16 Dec 2023 06:07:43 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddbf8bfa2ea0eadf27e35c86d6f3b621788311014f41bd87e342210494c0644`  
		Last Modified: Sat, 16 Dec 2023 16:48:46 GMT  
		Size: 1.8 MB (1794743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9360bac46e099e415df7f8e01d2ff8db19edf948fc8d7efcbded9b435ce708`  
		Last Modified: Sat, 16 Dec 2023 16:48:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240edfbcbaa6ccc1d50fe86fae095cfdd110ab229421a848bd30d8385c4e3c1b`  
		Last Modified: Sat, 16 Dec 2023 16:48:46 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba1e7f2d78e68a0ef1d484517da202c7818dab5986abf03eadbd1bb1946444d`  
		Last Modified: Sat, 16 Dec 2023 16:48:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81389d54eafcf6d7c790757ef3cc001bb57b618f53212afe6fbd315e37f2b618`  
		Last Modified: Sat, 16 Dec 2023 16:48:48 GMT  
		Size: 19.2 MB (19193593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:03bc0ad06ca8e483a357447a1365b0a4779a391066e5918ea0055fc3968c3f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe94af133e47fa09cd0ba882e25c8deaecc4f9f32267c9e396857476ce85d90`

```dockerfile
```

-	Layers:
	-	`sha256:0644b57719e16b965edab2aebeb6977560d6d8fb20cd8ce05f881e8a37a42389`  
		Last Modified: Sat, 16 Dec 2023 16:48:44 GMT  
		Size: 5.9 MB (5939194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98a8d70392bcb0d8a4d87cf98ef5c3de8a8e8aa5613e8d6c7c986e0b241814a`  
		Last Modified: Sat, 16 Dec 2023 16:48:44 GMT  
		Size: 36.8 KB (36836 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:f592712a5fb400daa61ce770d763d11c88a099e5ea4217ec4650168641a547c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165271994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a6b20a5afbd84e245f9dd08c12f722d24d830f7305d3f9370a6b379b05e01`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 Dec 2023 00:36:09 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 05 Dec 2023 00:36:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 05 Dec 2023 00:36:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Dec 2023 00:36:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_VERSION=8.3.0
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Dec 2023 00:36:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Dec 2023 00:36:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Dec 2023 00:36:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Dec 2023 00:36:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /var/www/html
# Tue, 05 Dec 2023 00:36:09 GMT
EXPOSE 80
# Tue, 05 Dec 2023 00:36:09 GMT
CMD ["apache2-foreground"]
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV DRUPAL_VERSION=10.2.0-rc1
# Tue, 05 Dec 2023 00:36:09 GMT
WORKDIR /opt/drupal
# Tue, 05 Dec 2023 00:36:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 05 Dec 2023 00:36:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b09eb72e9d386dbf4dcb97b2cd8fb6c959008740372463872bcbb989f9b553`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd379a47c6b90f49f4156c7ff2dd2eb18fe68c359cee32fa1f2d5786d853a7e`  
		Last Modified: Tue, 19 Dec 2023 06:08:59 GMT  
		Size: 71.6 MB (71634732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8169479b1d74c4fef21b4c3c845f26c586316508cfb384643eddfd5325797a1`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce7e9939543e6a9f444169e00e0128eef4c91089741b274c4a2b114d8cc176`  
		Last Modified: Tue, 19 Dec 2023 06:09:17 GMT  
		Size: 19.1 MB (19080627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813124d6d9df2062098e9401e27319aaa883fa6976985b1c1c3ab72e9f50e6aa`  
		Last Modified: Tue, 19 Dec 2023 06:09:14 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597ef00b179cc766c8a38ac1743e18947bbd8b665e5121c147c0f344096f444e`  
		Last Modified: Tue, 19 Dec 2023 06:09:13 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16205c0c498e0595ee9d0c47ba03d1b531d1de2a02162ca5c7cb4ecfbce07c8`  
		Last Modified: Tue, 19 Dec 2023 06:11:24 GMT  
		Size: 12.8 MB (12771871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5f7d4fc4f1eb7938b731ed8c704ceafd2718233f80599982210929ea27875`  
		Last Modified: Tue, 19 Dec 2023 06:11:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e61488c3851a4a9727b6436334d43499a5d37f230118509710cda9c624253b`  
		Last Modified: Tue, 19 Dec 2023 06:11:24 GMT  
		Size: 10.7 MB (10699180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8f44308d7e53d4d8e51f1c9f10520582fd421f7eb2b47b606f61beeae38ff5`  
		Last Modified: Tue, 19 Dec 2023 06:11:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce73d6bcb685ef57a16fb3a8bb839ef8e186bd1892163c382a5f540dba8ea54c`  
		Last Modified: Tue, 19 Dec 2023 06:11:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513068d44732cfa455570c057ee33417c07c2d873a57a5e4388005d563bc99ac`  
		Last Modified: Tue, 19 Dec 2023 06:11:22 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a569a21c9a7e105c441fa2582ca254c035c17fc8af14cf0dafe019288363cfba`  
		Last Modified: Tue, 19 Dec 2023 16:01:27 GMT  
		Size: 1.5 MB (1523286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e6dfeb7b1d9569cf2be86e1a5d6bd6e49f7e3c2db6c04200bcb1eefc64d05`  
		Last Modified: Tue, 19 Dec 2023 16:01:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2989aea79e201c8fad56ebe66ec0e67b8528867bf698d23bcde39297c6271ec7`  
		Last Modified: Tue, 19 Dec 2023 16:01:28 GMT  
		Size: 705.2 KB (705213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46edfdaa28d0777f7fda1603fae0274c297fc916174423597047fddd67d03dbc`  
		Last Modified: Tue, 19 Dec 2023 16:01:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad916795c612010db41f867f8f3eaac47c616ecba6e90b1d864fad627b4a72f`  
		Last Modified: Tue, 19 Dec 2023 16:01:29 GMT  
		Size: 19.2 MB (19194068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:fa0d374f82b0ac84a582046449c5cff24745c169b2e11e30a17cbb6ff1556705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ae72b3a46138480ee7321440fd2833d27af950fa9eb61420b7c141ac3a3ac2`

```dockerfile
```

-	Layers:
	-	`sha256:3bcb14499307fc79223e887448b29dd6727cb06b2eab225e6b3ddec68bc37a18`  
		Last Modified: Tue, 19 Dec 2023 16:01:24 GMT  
		Size: 5.8 MB (5819478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002602936637aeb61e8094b5f4dbd3155d5add9c4a3e636134e9b934282cdccb`  
		Last Modified: Tue, 19 Dec 2023 16:01:24 GMT  
		Size: 36.8 KB (36796 bytes)  
		MIME: application/vnd.in-toto+json
