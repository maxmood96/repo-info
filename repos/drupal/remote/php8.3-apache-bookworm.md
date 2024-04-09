## `drupal:php8.3-apache-bookworm`

```console
$ docker pull drupal@sha256:f836e529855e120aa25e5ca9ac6fa75739f160c3ae63e3758293ab57a396990e
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

### `drupal:php8.3-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:1417fbe83568e43c0699f39e8d70770da78c498e672aca8a298310c292c40713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200180966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c2b80e62118f2336b52959dbd365e1423f479fc9bf7431033eda7e98b68a2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:57:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 02:57:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 02:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:57:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 02:57:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:01:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:01:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:01:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:01:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:06:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 00:06:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:06:02 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 00:06:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 00:06:02 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 00:06:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:06:03 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 00:06:03 GMT
EXPOSE 80
# Sat, 16 Mar 2024 00:06:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de14226e1706b621fe796af63b375db247a2490752558ed4f5ea40648234129`  
		Last Modified: Tue, 12 Mar 2024 05:25:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aaf617d1d2bc41efbec77e9f05370e6f35d8f4363fb26fa04883ec538b7d66`  
		Last Modified: Tue, 12 Mar 2024 05:25:37 GMT  
		Size: 104.4 MB (104355586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba065e262ff15c57d91609cae32d80920edac1e9b0826e0d8cf5f0f3c60107`  
		Last Modified: Tue, 12 Mar 2024 05:25:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ecae067f5d5cbf3c2a3cf42d5677472bc8cc633b8ccea33d011749bb84661`  
		Last Modified: Tue, 12 Mar 2024 05:26:03 GMT  
		Size: 20.3 MB (20303886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f1b407f7499799755557f8769bbeb98d0573d6092913d5303cf951acdace0b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1b2cfb806df514ad4cf5cffa00c66aaa6322c1ef8f3b1c597592771925569b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7214a7d8b094ac5c57e27a6253262bf227c0bd2f9e15b0a2baa340c33f2a8b67`  
		Last Modified: Sat, 16 Mar 2024 02:33:29 GMT  
		Size: 12.8 MB (12777091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e055f8d0e6b4159ee0c461adbf769594edd20f18c9452f610634d55c779222`  
		Last Modified: Sat, 16 Mar 2024 02:33:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d823b2a82ecea49c91ada6d5e2eb007cc3815199485a624224c95f8a4ca8`  
		Last Modified: Sat, 16 Mar 2024 02:33:29 GMT  
		Size: 11.6 MB (11632114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb2c18412fea4b68876e78655cf262c7ec42e56f21ed7d33c4866239d7f2eef`  
		Last Modified: Sat, 16 Mar 2024 02:33:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68596cb92282dcf2b87dfc2cc4b71ecf8d3cf0c6286578e1b206960c5d088957`  
		Last Modified: Sat, 16 Mar 2024 02:33:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37124bcfe26d6cd8cac9cc0eb3316b0568d5f2be37d63bc4e554aa4b026f2fd`  
		Last Modified: Sat, 16 Mar 2024 02:33:26 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620708cd3465fe553e2a9014a31c06930530eaaa88108653517ac6223af62f0`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 2.0 MB (1999575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fa625bda7cfb5072a17a06c1249ca1fea617a74f617e3924208430dc746923`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcef21745416a9360ccef3d7decadc3b9ae753aa60c11d50ed100172a8dc1999`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 722.2 KB (722250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee6efbbcd8dafaa44424e95a6a31509a6c80d9649b96f36336b6866e68f3f3f`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8ec8c94e27fef09c461fe0a36cf370c516c8ff2325658b89ae5cb289d89aff`  
		Last Modified: Mon, 08 Apr 2024 21:56:12 GMT  
		Size: 19.3 MB (19260283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:d4bf0cd709501fdec4b637fc0595371530c66822e8aeee0430b7373b7de3f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6820363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a766e8d7cf2124f5d8c72db0b12a8cb5220af759ce3e5c66d6be3cde8216ed73`

```dockerfile
```

-	Layers:
	-	`sha256:204e56914730ada30e89435e20428d9740e7b3322d11a3b5fa22a0cb47e4852e`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 6.8 MB (6777917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76df827b5847f2457bd2fa5b6865d8b4be5c7a491b83b9086175467ed2112be9`  
		Last Modified: Mon, 08 Apr 2024 21:56:10 GMT  
		Size: 42.4 KB (42446 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b9ea8b6227f44d95beba780141e7088f40a490ec7c9f92f8e85503d97b24d7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164079140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc66f00e443dd42c8aa4d960e9a83cf1f44325ac5da65fe4f38c7b7a34f407f3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:23:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:23:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 07:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 07:26:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 07:26:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 07:26:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 08:42:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 08:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:45:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 08:45:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:45:02 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 08:45:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 08:45:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 08:45:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:45:03 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 08:45:03 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:45:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd82a33324e79052aa5fed0978c223b7d05b5a41532eca869d5602ee24d0c7c`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57829c9789b8ee6e6ebe4a80c39f9393df7fcf20975d1d8135fc2142cad63d8`  
		Last Modified: Tue, 12 Mar 2024 09:24:42 GMT  
		Size: 76.2 MB (76169934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1e9e48950eb6ede1065099dd2b976917707ffa4953e5c351638a845668823`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98245a88fa6adc9fd93e0af245463b9d9dc7cbea417c92646663e9f7375ffa93`  
		Last Modified: Tue, 12 Mar 2024 09:25:08 GMT  
		Size: 19.0 MB (19045529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff6ef8d01cdfd6ba1026fbed3898bbc602bc4e92c1a6879b933c622d36a7a42`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b18f3b6afb527e3463e62dae0e34a48ea21bcfdf1bfb8a5bbe5c978746c3e6`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c13e4abe30135f25b1010ee9f887b3248bdce6838a576b4f0132925aa13902a`  
		Last Modified: Sat, 16 Mar 2024 10:57:32 GMT  
		Size: 12.8 MB (12774944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da4081b4f9b9bd64f5fc59aaa3f520ae67b4cdc1d79b1b7376256aa156e4a7f`  
		Last Modified: Sat, 16 Mar 2024 10:57:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959eb122c6162580d0bc5eb8434bafb0f304d706f0beebca34e1c1bc8ee3657b`  
		Last Modified: Sat, 16 Mar 2024 10:57:32 GMT  
		Size: 10.0 MB (10027602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8008aaf0e240e5003a697a7f5ddd18bf876e62724fa4ffd642b294c40356992`  
		Last Modified: Sat, 16 Mar 2024 10:57:28 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9158be1f19af49428e2595769f757c2b31aed32af1e5e354540c1e7f13764f7`  
		Last Modified: Sat, 16 Mar 2024 10:57:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab48e121beb65090f2c7d1d5621033c3cff1c31a69dd56cdc9c58d20949e10eb`  
		Last Modified: Sat, 16 Mar 2024 10:57:28 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9844048356beed2effdf44e59e1ac0ec786aba9b523211670ee57e6785a52b4`  
		Last Modified: Mon, 08 Apr 2024 21:55:44 GMT  
		Size: 1.4 MB (1355723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20edb1cf42d4e0733af726bd5b6e5e7fd4518c614a54cca0132774015952dd1f`  
		Last Modified: Mon, 08 Apr 2024 21:55:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051466b383e17fcad057ed1fa5c40314681eb05341928f4ab5c40755f65d8de7`  
		Last Modified: Mon, 08 Apr 2024 21:55:45 GMT  
		Size: 722.3 KB (722252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7526fa193f0b24786ce83c4738936ddb5a355d257bb5124a6666d8399fe6eb`  
		Last Modified: Mon, 08 Apr 2024 21:55:44 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e40fe48378053aa10f4abec455d074267dd5386f6f06c4914ae0b7295443a47`  
		Last Modified: Mon, 08 Apr 2024 21:55:46 GMT  
		Size: 19.3 MB (19260429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:e234d4068622b6c08d5c0d149584da165a823b814f6f9a664d1b80bb54611ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c26091685515377008c966cff10adc56812b0caf67c4f0baafd8ea24ef590a3`

```dockerfile
```

-	Layers:
	-	`sha256:9fd97d74b2ee06c08930640e71c58e5a7050c30e7481d719abb9113cf1272643`  
		Last Modified: Mon, 08 Apr 2024 21:55:45 GMT  
		Size: 6.6 MB (6594052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8bd593cb3d00d31814c76f8fafce85113a274367cb1d1384f1f4a4867a096c`  
		Last Modified: Mon, 08 Apr 2024 21:55:44 GMT  
		Size: 40.5 KB (40509 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:2da90a2a7d8a1af8527e644098904b4d33bbc84dc3e5d428089ae2177ef8c9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194241403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dd2b82714924d8541c8ab59b441ec132210953d5185d3651b88123e007bbd5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:38:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 04:38:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 04:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 04:39:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 04:43:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 04:43:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 04:43:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 04:43:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 04:43:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:12:19 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:12:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:12:20 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:12:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:12:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:16:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 00:16:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:16:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 00:16:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 00:16:04 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 00:16:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:16:04 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 00:16:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 00:16:04 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b17d6e35656ac020a43a3f9453f06b61a9c61212e0437b31bac9d2b974cb4d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431cb294ec999c969b368afe1f6bb5484654b2ce2932cb1a6780d9c52781090`  
		Last Modified: Tue, 12 Mar 2024 06:57:29 GMT  
		Size: 98.1 MB (98126016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735009beb2cceac6bf57add7c26d3a77c8d92fc49ea5e05d8b2452e84a09b61d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036053896963520b5ce13f9151d0ad3dd4aff6d300c0cf85402700844e48dff6`  
		Last Modified: Tue, 12 Mar 2024 06:57:52 GMT  
		Size: 20.3 MB (20305130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9751366e208c9511ed7ed698080806c444f2effdd9f321b90fa1055b14a79e9`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53fc5dec6a2ddf288e227b9388cda0cb816d4b7e952c795bb0af42afafc9c3`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbb17f699a977d67cb733affc5e0bc56692d887469e79d005d87dbc7b23e437`  
		Last Modified: Sat, 16 Mar 2024 02:14:49 GMT  
		Size: 12.8 MB (12776790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24557a80713a659f9964cd9cbde716c7d86a28814ffa1ce36710f5ecd97acc8d`  
		Last Modified: Sat, 16 Mar 2024 02:14:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb2c578ab1e96d92334e6591a250c5734f3d2c9029e067dbc81fb619042c676`  
		Last Modified: Sat, 16 Mar 2024 02:14:48 GMT  
		Size: 11.6 MB (11629617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff929ad58498e9f4eaeb2646bb7716e8de8a175f883b55dd493cbf880d5e822e`  
		Last Modified: Sat, 16 Mar 2024 02:14:47 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151fa1649ad2300b1d594c5427a94f035daa6de183fba9648371236e0f468a52`  
		Last Modified: Sat, 16 Mar 2024 02:14:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d356d2a3d19311ceddfcb5777f3638b6b0c3c4205dd1e763104133bc3d94b7`  
		Last Modified: Sat, 16 Mar 2024 02:14:47 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b798efaed29db99793c112e07b01533bf2147346fa497dcabc3f45b15a850f1`  
		Last Modified: Mon, 08 Apr 2024 21:56:04 GMT  
		Size: 2.3 MB (2258871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27cbac25406479276141d8570257fe95766ac68bac68c96fe4fd93b69cb9360`  
		Last Modified: Mon, 08 Apr 2024 21:56:04 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d68a150f483b2e2419ae139778a64950f78b6c4f48d592decfb39f8e18fde85`  
		Last Modified: Mon, 08 Apr 2024 21:56:04 GMT  
		Size: 722.2 KB (722247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9375c2749a8d4c9f82de0e62244dd16996eab6279e68c73d75ea976a08c808e4`  
		Last Modified: Mon, 08 Apr 2024 21:56:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099571ea0149444a42b0c3974ff80e8edbc6f482fe7874548fa1a65d3d30e164`  
		Last Modified: Mon, 08 Apr 2024 21:56:05 GMT  
		Size: 19.3 MB (19260304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:903928f2efa1eaedef2a424b1c0aeb3b3f31496d0699688bc1175638a9449e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af4a01f0ab73d0295b2b230430128895ac6048772ca39839bcb448079ef5412`

```dockerfile
```

-	Layers:
	-	`sha256:a14aaab4e1629f0ce29876e01db52f4a0d0a264c7db2f209ec6ef0b35e57cbe3`  
		Last Modified: Mon, 08 Apr 2024 21:56:04 GMT  
		Size: 6.8 MB (6806332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1ec7eab0ced5c09e0661f594423f90d847e01c754c6990126992b73cde3eef`  
		Last Modified: Mon, 08 Apr 2024 21:56:03 GMT  
		Size: 40.4 KB (40359 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:e64644091b899fd901d89880eb798dc9108730611b9fe998b3b1d6405d2a9d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199163023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea3a4691b67e7b7d3acd430f844900b8fef53ab931016e8b8f000b180a5fa6f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:39:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:39:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 01:46:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 01:46:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 01:46:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 01:46:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 01:16:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 01:16:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:22:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 01:22:46 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:22:46 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 01:22:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 01:22:47 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 01:22:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:22:47 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 01:22:47 GMT
EXPOSE 80
# Sat, 16 Mar 2024 01:22:47 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc8b418f2e8ebe03c4a8d60a403099d5bd9956664693b358caef9096763fabd`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f25d2333bd6d54c124fa174175081a9c95780122966ffb6532bd93757a9bd`  
		Last Modified: Tue, 12 Mar 2024 05:53:38 GMT  
		Size: 101.5 MB (101519737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6e71adc002ea9786257601b0d391da402881cf3c46d70b1bf238b5e218a47`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ac2ec3c620e7a371533497b0cfd74ea84db2b079763c0c27f094625f447cf`  
		Last Modified: Tue, 12 Mar 2024 05:54:05 GMT  
		Size: 20.8 MB (20826115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef95ebea38d5ed66df38918c6398211026347c3a649d8cc4c3d081f4e7c6290`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea05f91953dd8b5d5da845bf416fd786a74c12a214cd690ab7a3fe6bc5a5774`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1935c5d0444873785b5095449427db54198de964b4641c4e6721b621f8fd23e`  
		Last Modified: Sat, 16 Mar 2024 04:56:03 GMT  
		Size: 12.8 MB (12776106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8bb9071613093e32e9c74f9a34749c4949254b1421ee78d8b4b8b0e7c8ee7`  
		Last Modified: Sat, 16 Mar 2024 04:56:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177335a0b15c2bbc1292d9e5d0a57559c17ec71ae5dbfda96d3852bdb8447dc5`  
		Last Modified: Sat, 16 Mar 2024 04:56:03 GMT  
		Size: 11.9 MB (11857033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8943b5c5344514de7a70a6d997fa6115270d77fbc259ec420fa4beb19cfc1d18`  
		Last Modified: Sat, 16 Mar 2024 04:56:00 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251a5a8eb2ec5e304b8d713cf73d094e35ea6ed7d9cf9ce01a3fdade2c6dd847`  
		Last Modified: Sat, 16 Mar 2024 04:56:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93a390e67e187d1ba21563a65963c843bdf2d487c0bad2022fc9897537d210`  
		Last Modified: Sat, 16 Mar 2024 04:56:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b85120d38142efa7e34bf1e926d4917f53b2d8168e482089e97528f1c71386`  
		Last Modified: Mon, 08 Apr 2024 21:55:52 GMT  
		Size: 2.1 MB (2053583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7b1b7aa6b781d0331a2345b9cd03fd1d2deb9d4770beda4d9189273cc1c00`  
		Last Modified: Mon, 08 Apr 2024 21:55:52 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6134922c4bc192a6b8c79babae92642e41f85b16fc3820d1d91146d6b61bd171`  
		Last Modified: Mon, 08 Apr 2024 21:55:52 GMT  
		Size: 722.2 KB (722250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9611cdbff2993f3e9c14a8434b5bf257a341c6c50e9cc481c62de406288f8b`  
		Last Modified: Mon, 08 Apr 2024 21:55:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd3aa450ee081f32c34192753920bfbffbfae3431507e4bfa75f0838a61f808`  
		Last Modified: Mon, 08 Apr 2024 21:55:53 GMT  
		Size: 19.3 MB (19260319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:90776b55550f8117d454e468786079528ec2e8c8977bd14e2cf4adefca343b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6801006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e0b49c62f0bcf6c50b7ba694909ecec4652fe6547033f5dc7437ed2ae0e0dc`

```dockerfile
```

-	Layers:
	-	`sha256:704524bf2788cb46da5f529b8b874a69be4148d0a6082cc42ab56bb7cf39b544`  
		Last Modified: Mon, 08 Apr 2024 21:55:52 GMT  
		Size: 6.8 MB (6758635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c525e313ffeedf1f925aaad5ada45fcc8b55e77626b00e945834404a0f3389d3`  
		Last Modified: Mon, 08 Apr 2024 21:55:51 GMT  
		Size: 42.4 KB (42371 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:bd7fd8717da350fa47e7db9f957f9eb8e1534acbc62f0d5a3d61c0f3d359a51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204593481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ac926f4e97b6319ccb298f5c06f9263a8685d196e6b2a47dcbba20453b6f80`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 03:44:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 03:44:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 03:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 03:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 03:48:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:57:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:57:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:59:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:59:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:59:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 05:09:00 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 05:09:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 05:09:01 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 05:09:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 05:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:12:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 05:12:42 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:12:43 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 05:12:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 05:12:44 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 05:12:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:12:44 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 05:12:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 05:12:45 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=10.2.5
# Fri, 05 Apr 2024 21:55:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /opt/drupal
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729fb27eaa92097ad878499ec6403a23c58d8214dac659ab72a1e323819ef57a`  
		Last Modified: Tue, 12 Mar 2024 08:08:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce4a728b9ae2c7eefcd9b8c3b9dc1d62b72c1c071f16bc427f26b3053a56b1`  
		Last Modified: Tue, 12 Mar 2024 08:08:52 GMT  
		Size: 103.3 MB (103313606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40564a51615fdea74995b1c4e47872bc1cb06986eab253f3b5c5bb070cb76e`  
		Last Modified: Tue, 12 Mar 2024 08:08:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d0172ecc888b93bd448b82bc6d9f857b3d92b715a3dbf98063659ae5aeb9c4`  
		Last Modified: Tue, 12 Mar 2024 08:09:23 GMT  
		Size: 21.5 MB (21490020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3644f81176bc8772d0ef995fb85eb87ab44e5d4ec0edc420255e9c461846490`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136812f7b93f984042c6fc7d609a2cafb56b8f103e463590d92b4795c71c2dbe`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e67f5595b7de15188478931c65794ac1c7b434c36bebc6d1e255dd46e2c9706`  
		Last Modified: Sat, 16 Mar 2024 06:52:36 GMT  
		Size: 12.8 MB (12777061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8659ec72138fbabda29e6ff83e16c45108aba907ac83b102d82f356d7d45bd9c`  
		Last Modified: Sat, 16 Mar 2024 06:52:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4c2ba3af3696a999ba4b71f2f4c04c4ccf33132748b8d058d97b14270475b`  
		Last Modified: Sat, 16 Mar 2024 06:52:35 GMT  
		Size: 12.0 MB (12048286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743d671c6193baadf7308be970d71ba1d515090f6f5c9149a62a4c80d325400`  
		Last Modified: Sat, 16 Mar 2024 06:52:33 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c534d9c5372a5a386dad0dc1ce3deef9c803754a493a4fc15b7e1ea136ebf7bd`  
		Last Modified: Sat, 16 Mar 2024 06:52:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123558a8332af87c0d56d34ed021a13dc91cd767ba699441ba390bd7f0c55025`  
		Last Modified: Sat, 16 Mar 2024 06:52:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208d8daaaec1595628f301a83449e0d3873b52a6c86379aa7fc14b6b69a6a04`  
		Last Modified: Mon, 08 Apr 2024 21:56:24 GMT  
		Size: 1.9 MB (1856920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b0887c0c83cd405e43a33f4e135811eabe9012b7972bd0c15804d0990e0f4d`  
		Last Modified: Mon, 08 Apr 2024 21:56:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce719cae7dfc12c3eac072ce6e10d3934eaa4d50f4db4edb1c0d4fdef5a670a`  
		Last Modified: Mon, 08 Apr 2024 21:56:24 GMT  
		Size: 722.2 KB (722249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a61b312f427199a2b0cc496f17fd17ff4acead8eaae279287c5495f6277f8b`  
		Last Modified: Mon, 08 Apr 2024 21:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863cfae20d6a18d37e593aac2c92e8c322ca3a0334059b3adf1ed33f167e6e33`  
		Last Modified: Mon, 08 Apr 2024 21:56:25 GMT  
		Size: 19.3 MB (19260297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:e4c6e1610be42cd9d50669408c3e99887899239f18e6e56dd29aa2d66ed8c146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af8f3ec3bbb057c75ca4fe42f182aa9fa183b822d0fe91b86d06159ae338323`

```dockerfile
```

-	Layers:
	-	`sha256:d88b4ef793a3760e897259cb3ba0549cf1941f3c0fc91fd88ed1ad8f075c0438`  
		Last Modified: Mon, 08 Apr 2024 21:56:22 GMT  
		Size: 6.8 MB (6755264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41edf55b5a3c9a0880ada9f31d8718a3e6ce4bc82fa87159d37de1c517decc70`  
		Last Modified: Mon, 08 Apr 2024 21:56:22 GMT  
		Size: 40.4 KB (40432 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:ac8ea8b2ffbe914fca35ceb9f9f4cbc76729ef3bc5cb00bdf6a295b0de242253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173362049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd7d93fc508127b38675e49a9ce533ae497a7059dfd3e44858bad13f0454cf9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:04:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 08:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 08:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:05:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 08:05:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 08:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 08:09:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 08:09:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 08:09:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 11:44:56 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 11:44:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 11:44:57 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 11:45:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 11:45:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 11:48:13 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:13 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 11:48:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 11:48:14 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 11:48:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:14 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 11:48:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 11:48:14 GMT
CMD ["apache2-foreground"]
# Wed, 03 Apr 2024 09:27:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 09:27:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Apr 2024 09:27:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 09:27:54 GMT
ENV DRUPAL_VERSION=10.2.5
# Wed, 03 Apr 2024 09:27:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 03 Apr 2024 09:27:54 GMT
WORKDIR /opt/drupal
# Wed, 03 Apr 2024 09:27:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 03 Apr 2024 09:27:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d4ad3e3b59b6f54b9dcef6cff0e4615b6fa3f96f1de12d8fbeb94f7acd29b7`  
		Last Modified: Tue, 12 Mar 2024 11:15:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83835687d69ef2513b8d805100ebc4726b162f3aa9efd0cddf617127b689d25`  
		Last Modified: Tue, 12 Mar 2024 11:15:38 GMT  
		Size: 80.8 MB (80808055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e8349341cc698ac8bb86ba42ea145c47faa3f81cf9c660f105f493fc148300`  
		Last Modified: Tue, 12 Mar 2024 11:15:25 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500bb0818505be871db98ada53fff2905523f39443d3b8203de073d18275d0a`  
		Last Modified: Tue, 12 Mar 2024 11:15:58 GMT  
		Size: 20.1 MB (20083383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e602f9cc745a947e1f5e2c99c194cfdeb52cdca3fd07aa735f0135752b146e3`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f8dc84c4882804775f8abd94bf231325b2f7e4b4812cc6aba73dfb838aad26`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925e51f8f2392ba205e8269f4a629423e00632bd9d22f9567591ecf347757483`  
		Last Modified: Sat, 16 Mar 2024 14:16:22 GMT  
		Size: 12.8 MB (12775321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18d99a5ad0c94a57859e5024ab90517f7272395a3036615032a457f39d16ef0`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b6e56493ad974af511225ab349754d6f81f996d7abf2c57cc198f6c4669dde`  
		Last Modified: Sat, 16 Mar 2024 14:16:22 GMT  
		Size: 10.7 MB (10663121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda4e6e0a73f9324686dbbde89cd8a6c56058a42a154cb6b4046a9d10924ce77`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a919f1a0093dd1c6e0bc671863919b1df4fc6de94c6c389a4dd26bd796bf745`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f533efa5d87246f329e6f3ea119c6c15af4150c592ec300b42452d4b7e3a7`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd4bed03478ff1088f9c1dd19240dbbb6a4a3c1a8a87ed605c3dc7e4f96c76a`  
		Last Modified: Sun, 17 Mar 2024 09:54:08 GMT  
		Size: 1.6 MB (1555452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea0276803dd4a243688b1ea6bc734d4f3fd77d0af3acefda1c8f0a205ad34a`  
		Last Modified: Sun, 17 Mar 2024 09:54:08 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8717b4c376a40884dee56ba0fb480284c47158765be2a27abd41e268d37c7559`  
		Last Modified: Sun, 17 Mar 2024 09:54:08 GMT  
		Size: 722.2 KB (722249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8db2add9d26ba71f45d98c494aaf7b9ed29c5e0f95f56a49c6d5e37ff01244`  
		Last Modified: Sun, 17 Mar 2024 09:54:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56b21b6e7be220dcae95bc301dd2c998bc0e0b3a9b1f52ad749a56e284183a`  
		Last Modified: Wed, 03 Apr 2024 22:27:59 GMT  
		Size: 19.3 MB (19259784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:08621e63fcf7fd91b6dd8463abd963bc044883f358fc8cf741557633f1f1a93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c7ca18463c515e7266c0ad10fe139124d77e4e9c007c289a5ecf6d8d86080`

```dockerfile
```

-	Layers:
	-	`sha256:a5366189bb2767de3df7b23e40fb69ff7379d52bd722804b4e8570c406f85a0a`  
		Last Modified: Wed, 03 Apr 2024 22:27:58 GMT  
		Size: 6.6 MB (6620339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:641f951c64e805914b01b5ccec57e7258a4802f50c480e451c988c97595709b5`  
		Last Modified: Wed, 03 Apr 2024 22:27:58 GMT  
		Size: 35.7 KB (35714 bytes)  
		MIME: application/vnd.in-toto+json
