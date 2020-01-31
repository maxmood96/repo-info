<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `yourls`

-	[`yourls:1`](#yourls1)
-	[`yourls:1.7`](#yourls17)
-	[`yourls:1.7.6`](#yourls176)
-	[`yourls:1.7.6-apache`](#yourls176-apache)
-	[`yourls:1.7.6-fpm`](#yourls176-fpm)
-	[`yourls:1.7.6-fpm-alpine`](#yourls176-fpm-alpine)
-	[`yourls:1.7-apache`](#yourls17-apache)
-	[`yourls:1.7-fpm`](#yourls17-fpm)
-	[`yourls:1.7-fpm-alpine`](#yourls17-fpm-alpine)
-	[`yourls:1-apache`](#yourls1-apache)
-	[`yourls:1-fpm`](#yourls1-fpm)
-	[`yourls:1-fpm-alpine`](#yourls1-fpm-alpine)
-	[`yourls:apache`](#yourlsapache)
-	[`yourls:fpm`](#yourlsfpm)
-	[`yourls:fpm-alpine`](#yourlsfpm-alpine)
-	[`yourls:latest`](#yourlslatest)

## `yourls:1`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1.7`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1.7` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1.7.6`

**does not exist** (yet?)

## `yourls:1.7.6-apache`

**does not exist** (yet?)

## `yourls:1.7.6-fpm`

**does not exist** (yet?)

## `yourls:1.7.6-fpm-alpine`

**does not exist** (yet?)

## `yourls:1.7-apache`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1.7-apache` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-apache` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1.7-fpm`

```console
$ docker pull yourls@sha256:b824d208a937ddd8a2c7a7956df6b64f15d7fcd908853af04da885d485a388a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1.7-fpm` - linux; amd64

```console
$ docker pull yourls@sha256:01b5c3b8614e71685df105367805677ce4c5409c93f3bc0cd6ff7ed707af8d13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147711401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70ed93dae4e69dae94eb75be121b4736186e51afb371aa803e227c6d0768d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:11:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:22:07 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:22:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:22:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:28:24 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:28:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:28:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:28:25 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:28:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 09:28:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 09:28:26 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 09:28:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:50:39 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:40 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:38 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442b1ecfb2c9a625353fea0f844074f8fe0fe6143b8d91d19ebce373d9ed1007`  
		Last Modified: Fri, 24 Jan 2020 10:46:22 GMT  
		Size: 12.6 MB (12629735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604c883860730b90a8915cb178846302377a485632f4678abbf1245bb5df6cd7`  
		Last Modified: Fri, 24 Jan 2020 10:46:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2149af9158125e9e52378bf32dd870b97bf83d41e3ee72fc17440494a32cb6cd`  
		Last Modified: Fri, 24 Jan 2020 10:46:27 GMT  
		Size: 28.5 MB (28546306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbb08b8828428d4e6e486ad6d1821d280bae55744f421fa8035d44540fab006`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1809e0c1876e3fc2c3ea53d38b99b19989dba26435b6161a7d9c072b9e424fe4`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd69a9444b9d6fe58338b42cb8e5198c82b019ca4590614d01790c770869c376`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa924e44a1f5bcdfef7eba9bf5a4f779831c0e98064ec42382e9f53dbd8d7ce`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f9324e39d14f0d2d2350bc4af8a09f727ba4ac1e189ff8a400969eb94c954b`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 291.7 KB (291679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c4c4f41bdf1a5cb5842d7d5fc99441290be8a0e6e5236ccc4ff4e57dfda8ce`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d11b8c2ff5395e48a60688f771dc13a34dc660e2c062a4af5aa620bdfc8b48a`  
		Last Modified: Thu, 30 Jan 2020 02:22:05 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ede6f75ccd4614c45f5e37928d8b8041bdfd1adab24d94a80e4bde5756db9`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6e3fb679468e6cd073b1b3fb682ac09c49a8939842dd9e369cda2479693653`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:fb994af6b4fc7458db3335fd3d16f0fdfadd47a884de51198f698fda403a416b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126187218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06387d9df9126dbd6beef0251e6fa07ce5dcf7eeff6c155d0b741a8f33ff68a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:49:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:32:24 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:32:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:32:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:36:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:36:43 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:36:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:36:45 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:36:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 21:36:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 21:36:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 21:36:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:05:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:05:36 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:05:37 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:46 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:47 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:49 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:50 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:51 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbfb91322c2c956ffb8a049056ce6ed7e8a02a509311179ea6b266b1cd45496`  
		Last Modified: Thu, 23 Jan 2020 22:09:11 GMT  
		Size: 12.6 MB (12627683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98747b31069e9460384399be99d08e3d6ba973cdc421a693dba732f9034e1858`  
		Last Modified: Thu, 23 Jan 2020 22:09:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b584443a0241f6eb684458e292d8a1364815de66d19a428c63397a77f9326425`  
		Last Modified: Thu, 23 Jan 2020 22:09:22 GMT  
		Size: 27.2 MB (27155786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62342286e070b175d5f33b0c57aaac3dcb531302615717719031379bb49bbd`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b721095f046edfcc7c96256d02cf74d7f1878b67434564c5099d4e2bc97c7`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d905d65d2a7c8b3a642c15a284c5a5eb9b5e766ce03efa7e96f1654a186a07b`  
		Last Modified: Thu, 23 Jan 2020 22:09:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f81752db9dc5105c0b0686049d8df61c37cbfc1439036c5b0507ebbf7d8be78`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b12f633c01fd0ed42e045e82f844b9dc106acf3db24b479ab4351b86a538ca5`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 275.0 KB (275005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a984a8704ce9b04866ce262c93d3f016811f963cc337f4167eecb383a4cefce2`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c76d4c578c2ea8b71fe614c34ac283ef4499baf10bb6cca8714b5cfaebed487`  
		Last Modified: Thu, 30 Jan 2020 01:49:28 GMT  
		Size: 2.5 MB (2485134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028c42b082088168c3dfd40cc3342cff201c30a1977fa6051de6a58d2df3243c`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6014ee5568d3fcaf8859e18f6a66c557acee07a3f191bc73b4e8736866f7df80`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:503fcf065f42adbc1c909c18065cfd184771b53b11cd87a0201c29ec9a9d0641
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123715481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff768dc3a6cb4787f1dbfb1cb0d807acc1368c492965340630f0b60a2cb9e1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:43:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:51:17 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:51:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:51:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:55:12 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:55:17 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:55:19 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:55:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:55:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:55:25 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:55:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:37:26 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:37:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:37:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb1758fc39381ea05e8422ad87509422182f75ed593f56bb784cc2ee8f8d0d`  
		Last Modified: Thu, 23 Jan 2020 23:49:59 GMT  
		Size: 12.6 MB (12627816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c8be070a970b9520f0c5411faaff68b310398cdfba729736a9df57fe91fbd8`  
		Last Modified: Thu, 23 Jan 2020 23:49:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf5db91a1e39f4ee33ed64b2ce1c0f67c6d6168ffd1c962f0d17942ba03bb3b`  
		Last Modified: Thu, 23 Jan 2020 23:50:04 GMT  
		Size: 26.1 MB (26139997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d1c64408f61b28105b9808140e533f282dfe098b735fa894b73fd51dde992`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b510571207603d8b273d6df417b8169f6bbf0cc1d39fb425b28f4382afc1bfe8`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0b9ba2acc5213b37b46a7a6bcee1e7e0c02c26d6bcd99f6a3721f62f3799d4`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0fabfd4ac1f5d51ab09cfd94f9e380e0640968e5a7b324629741d4b28a8602`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74821a2451c1a39fe37776ff8c2071ef99e5fafb5e90d2b2db8574b8e0e11d7`  
		Last Modified: Fri, 24 Jan 2020 06:39:24 GMT  
		Size: 247.7 KB (247734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82272351eb30b6dec796c32b9106946336efa7c2fc55683951649a8e9d74d5b3`  
		Last Modified: Fri, 24 Jan 2020 06:39:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57c1c5adc6c645d2b1fc35333027b0ed54ccb52c719addc51a9cb1f4b46a46`  
		Last Modified: Thu, 30 Jan 2020 02:03:07 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383028fb815c7fd589fdddb28f1beb3199ca8743bd814282c7a04279489cf9e5`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353080e7bb45e4c4d77e28f78bb37560ec2b0b6741febf02580932526d21819`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:102bd3f157fdced2dab193af485d83fafb6b975acbb05543720956683792e2a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139830083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e29c1d68344ae19182e342b8f893b806dcb3184feefc77f7fcf5172e0c556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:43:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 14:44:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:37:37 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:44:49 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:44:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:44:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:45:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:45:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:48:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:48:50 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:48:52 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:48:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:48:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:48:56 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:48:57 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:05:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:05:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:05:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:19 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:20 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:23 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:23 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:24 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5385e23b021c86fa2519c3af464e961ce347de02b0c3ca2926e40f888308f2b7`  
		Last Modified: Fri, 24 Jan 2020 02:46:23 GMT  
		Size: 12.6 MB (12628557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247490a29552c9c6da012dc7ea7a293a66b78f784d71e62f9b197e7a2a8c58dd`  
		Last Modified: Fri, 24 Jan 2020 02:46:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a810846e71871c7ad2826a5abb33a4e83c09b33dc949ecbf776887e6d35809`  
		Last Modified: Fri, 24 Jan 2020 02:46:27 GMT  
		Size: 28.2 MB (28231414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa180318dc8ef2bad411c5e6b92f972287e7d53ba6976c859afbe244034c003b`  
		Last Modified: Fri, 24 Jan 2020 02:46:12 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fcaa8f8a88faf16705834f29b893eb7be1e10189c54b9aa2a93987c025fd78`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d82a6edcc81dcd3aa46d2bccee534bb1498637b6a985b9d982a48e5461167`  
		Last Modified: Fri, 24 Jan 2020 02:46:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d142df4bd33c314b37742a530120372a0939a833e971b47db7a0576e7fcadda1`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089bc3d67b4e490c6544f2b280de8ff34881292944073d3b8b023de9966277a`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 284.3 KB (284288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5267d5f0e9184d651724696556d09bc2194b564641ebb28f7b0318fc33595858`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c291942bf334792ed77480fc0b42d374edd00d431ed7c4128d33655c9a97dbb`  
		Last Modified: Thu, 30 Jan 2020 01:44:10 GMT  
		Size: 2.5 MB (2485137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395b990c9dbcf4c7ef477d85aeaaa21ea24271ea4e4caa029dc2e29acbc14e9`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64629dd41bce5414d5971281d9b3e2738738b945337c4abb5a975ed4d05fa1db`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm` - linux; 386

```console
$ docker pull yourls@sha256:a3028c7ed251f3e1a738d6040840ab2924156394c2ce983578ead7fbf950658a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153487648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b961a4b045103bca431c6df18c5a0ec1a42a6c37f1c30ee66276a49a4583970e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:42:02 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:25:08 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:25:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:30:31 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:30:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:30:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:30:33 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:30:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:30:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:30:34 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:30:34 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:20:24 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:20:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:20:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:18 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:19 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e4c3884d21c912689646ef044df487d2ba5563660a7c48199494657002d8ae`  
		Last Modified: Fri, 24 Jan 2020 02:43:20 GMT  
		Size: 12.6 MB (12628971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be88344b8a867d5499c731bf7b2c4ce3da59fbc53490ca490b0fa834bf2e385`  
		Last Modified: Fri, 24 Jan 2020 02:43:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1f649f6a0fc1bc15c1b6073b282721d907c3e98c967c42ba2441e6b22b9375`  
		Last Modified: Fri, 24 Jan 2020 02:43:29 GMT  
		Size: 29.1 MB (29112034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377ba8601df6ecff1825708c6a04f421167d938a2aaab37aca18914b110dba16`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4173bd41a613e320793f323a704526922df3d3a6db5510fad85a035b7de7b03`  
		Last Modified: Fri, 24 Jan 2020 02:43:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b918685c71fa48d6e4f27fd3019c5f1a074d371ff6f9b857fffe797df5ad3631`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aaafa98d5bff0795de02c9b8a85482591bcfa3718c8a5189a93b7602f072f7`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1313cc666858c3fbf3761cde39726d40e423a307783edc8bfa0103c0df7f63e`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 300.3 KB (300334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9370e4cd5f9b6334afedbbda81083630b745a0c9b512bcb54c68503776ff22c8`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6349e0c7616f4e696b45ff9ff8d8ec35921711e48664d494e8ff7e3b85af6dc`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165a82a2a23f3878e537927ef32507188267136d047301ed0ba7348c94a090f3`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf7ad141068b6803eb4dce32190d923dec5e9508f09ebd560e95b6823cfaf30`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:444f9ae1ba7b1cb9b1c9532b7651618816069e2adca92b8328a0edab90703378
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7c418249d87b67d1fe7d9cd2a6670c24a9179dd95b594f3748787aba64b2f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:23:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 18:23:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:23:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:24:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:33:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:23:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:23:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:23:30 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:24:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:28:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:29:01 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:29:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:29:15 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:29:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:29:20 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:29:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:29:28 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:29:30 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:55:06 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:55:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:55:14 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:20:27 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:31 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:40 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:42 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:43 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569cb347cab0d4635b52aabf03a42c7b540a9cdb8a7cc3724e035548cb2479c`  
		Last Modified: Fri, 24 Jan 2020 02:44:40 GMT  
		Size: 12.6 MB (12629483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7f9344526bdabbec6ca4032f08dc34692fe191bdfd2823bf82e84d2da1bb2d`  
		Last Modified: Fri, 24 Jan 2020 02:44:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3e9e86279b094e4fcda41c96f85140f5e2c97c20ed45abf760efe04fa028e`  
		Last Modified: Fri, 24 Jan 2020 02:44:46 GMT  
		Size: 30.2 MB (30243520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b77ffab588104f2668d6b0f944389432ed4160c951de7ef7f46ba7cdf88179d`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388698cb0d1b4ac7615cffdc3fcbdf4c05c9cf65ae377df6169dd3b338792fe`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa9d46432c785ae0cd3e45eb865d048dd4adc9aef4faef88e4b8d8f9cd53b12`  
		Last Modified: Fri, 24 Jan 2020 02:44:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade4f3c53bdd51572900708e83ba2057be3d4c20cd154b218246bf56801e90c`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6ceda7ebffa5b7f688100d88c571f8759321a8a7123e29a0abe8d792eb67b`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 322.8 KB (322761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2805e3c107f737ca23ea5a8b2929fdcec068c27e8d83173bed2c15359e4041c`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40499203c6719755f97fae3ccf8f55651615f8c019dd724ff0b9d643bff06bab`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e065b02e85e387e7a86f73514572ba0f535d319124db5ac45b196f2b710450`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be02c4b3683724d4117a4d242ceded30ced3ef212a8a9b2ae13459b7d409a24`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1.7-fpm-alpine`

```console
$ docker pull yourls@sha256:0330e5b850c7d5d1745f4aeaf640f9f2dd539f8447a0ebc965cf8a50cfa62ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1.7-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:bd4ea8165751899c16a2fc66635e2c17b6bba8944e4f47ee39d00a2060313565
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34689132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa09543500501ddd080f4f4d3901c214c54ffbfb3b053105c0115f66a4067d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:18:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:18:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:18:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:18:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:18:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:23:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:57:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 10:03:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 10:03:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 10:10:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 10:10:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 10:10:40 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:10:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 10:10:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 10:10:41 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 10:10:41 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:51:20 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:51:21 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:51:22 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:51:22 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:42 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:43 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:44 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c0a1817becf025301783a94fa11de700972e7d7c117ca7e45d080db0ec1a11`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.4 MB (1354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5b3ea1fc31791c18f464b5b95dd3d9b8ff97aef4b64e0202f3da7f5550e80`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87396003bdeb76e6e367a5ae26be9642a89986dcda71b3491412c579cb6859`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17200a597429895679e6159f86a8d36b47a19e3d129b274280de24310378285`  
		Last Modified: Fri, 24 Jan 2020 10:48:27 GMT  
		Size: 12.3 MB (12327117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e0b32c554d6b99c5783aefcd5e40c676adc57c3bf841ac3e75df2f48ebe74`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27693a4cd8b214566f0beaa6ad32ae12af848d918678a3ada48120498bade0e`  
		Last Modified: Fri, 24 Jan 2020 10:48:23 GMT  
		Size: 14.7 MB (14655505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165dc5b50792307d63058296f7dffb1736fdab36ae5eec8b9171f40237f990cb`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f5ecc3407bba24c5755ee7b5f66315ad12aa11f2799fbe107091763e3d4ca`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348837019c84bd0cf419da2c04934de3d0734a43bc13ddbaaada7700bc04d392`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cad7e57c42971b072fe53a9c8b7faecfa513033f552912d0cc2d9af846ffe9`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 362.5 KB (362525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd85ae9f2f169c484ccc596b08716e51bb9cd3295cdd377354412b64fa46fe`  
		Last Modified: Fri, 24 Jan 2020 10:51:58 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c5cdd0c3abb0d2d205c8e3646b5339762e8d33929dba3833c695bdc461122`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 613.0 KB (613039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b8d1dddb9bcf0341730ebe0d5399653a9c50eaced9daf03b7c517753ff5fce`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 2.5 MB (2485235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e43e8ec3155993e63f2e3672ec709f3a77d9ce8cea734ce71b4fb783eb5060`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2768c7d2613c5cdcc79f98a52987574d9d2326b868c8d9d12acd901d44dc9c6`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:b4c1d903cb7a27f1472cbf19cb6dc1e420d7d44d97f494da9a3a8cc5f18aa197
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33429819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a80aab2471c71b9bd7291f2982cdfd2abc4c224cd37bfb8576adbc077dfb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:40:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:40:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:40:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:40:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 04:15:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:38:44 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 22:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:42:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:42:57 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:43:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:43:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:43:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:43:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:43:05 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:43:05 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:07:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:07:29 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:07:34 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 00:07:36 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:49:39 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:49:40 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:49:42 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:49:43 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:49:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:49:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c701ead53742b2a88bf4f606bd05029ec59ccaf522450bfa76be8cea0cf02`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 MB (1321088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e3d03f7d4228e33415f8592e7ec2a89fe1616e0ab6366ea68045b09d7f280`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba27e9ff828195f46a3edb0b1e28b5d10451b66ae080c20794f6d005cffbd72`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df6832a2c2a8fb5bcfeb52791d0eb421259c8488f400375b165ce8893c64d63`  
		Last Modified: Thu, 23 Jan 2020 23:04:46 GMT  
		Size: 12.3 MB (12327130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe69c0d5de12e5d470ca61ed1e8963aa3abf3e404ee8532054d9500b74e5d95`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cf033fea6edee7deec178385e5c1c4618becf2e7af7484b9f98cae076ff405`  
		Last Modified: Thu, 23 Jan 2020 23:04:44 GMT  
		Size: 13.7 MB (13654217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f07cfc243eacbc5c270aaa6b18031617fec1eea18e518d1fc7fc90126dd367`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5462852adefed60378b031e016b135ce5666f2e49d982cbc8d63313e5f594aac`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 72.5 KB (72453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c8ab379509fb13b0ebe44275f2df8ad19a00a1c59c0e7b041232653dad74c`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2bf7fa95982abc3a13216bba5f6000994d76ee18184b1431d4340460b9b136`  
		Last Modified: Fri, 24 Jan 2020 00:08:13 GMT  
		Size: 345.7 KB (345725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369e36d2ba0c4e916e43c5d9bae25c8b069ac55d8c8f7f5ce3582992d645303`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf2e49ccc1984afab3b4f9cfac61e5f66ddb07677930243ff0ba8489f062107`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 591.1 KB (591118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2197112a846c7b907958f150c5b4bd33fbe04befc6adac31f5b7e7be09e137`  
		Last Modified: Thu, 30 Jan 2020 01:49:59 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a3a30325d3d12357543b10edd0b0ed71f19d04030f304767f16b06d669e5cb`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ef3dc4164bf15c0cc31f54c7e4cd7e6a7737d669f34c6fe44e9245e6cd88cc`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:cf92b775d3826527d200012694e4120c64042d4275ed2123b93dad2169e374b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32213379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451f8ec4aaca7e7205470fc440ac1c75ead9c99b9a56edcdfcaf94e08ff4438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:22:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:22:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:22:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:22:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:27:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:27:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:27:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:28:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:56:58 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 23:20:22 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 23:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:20:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:23:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:23:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:23:44 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:23:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:23:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:23:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:38:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:38:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:38:27 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:38:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:17 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:18 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:22 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecb809efefba021b07183ae486164fd475667a42a78ab308bd01b8d7dd8c1e`  
		Last Modified: Sat, 18 Jan 2020 06:09:11 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec95513b0eab50a07131cbee828abed358fb86fd276018e1bae6f04611ed9`  
		Last Modified: Sat, 18 Jan 2020 06:09:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d1b57d2f034e68934a4116a4434479186cfce56d1235af4f1c1b9de08acbc`  
		Last Modified: Sat, 18 Jan 2020 06:09:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efaa7391df564715aff5a3ed3728a8506f4242ea7af5b78f7084cba8f1d9e16`  
		Last Modified: Thu, 23 Jan 2020 23:52:11 GMT  
		Size: 12.3 MB (12327128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27fe1a4a8c3bdc42c663754127b8d2bf1d28761de505c66874975e2cfbe7d9`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc6150d058ad54d1317f115cdf515f2ee41b09349a4e48c666108c73d32063`  
		Last Modified: Thu, 23 Jan 2020 23:52:07 GMT  
		Size: 12.8 MB (12797323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0aad572300486b8710177efe735704d9acfd6f6edd3247cd91f6890909dc55`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791fec6f4e7194daae4ecf5d0bb4ab9b292190dafa9db15fa319c4e88ccd77ae`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 72.5 KB (72451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b07590f3a1c8342e06b308e79d7399c1d880aa4d1f536df9398ebf2232c551`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1a4f15d2507503adbd0ec1d83a575a6dd28ae766d2a6b7c64bb45d1f4be0c`  
		Last Modified: Fri, 24 Jan 2020 06:39:38 GMT  
		Size: 324.0 KB (323981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de491bbe822d164a59311f8f49bbafa2f2a8cb4808d9e174a44868ae75cd86f8`  
		Last Modified: Fri, 24 Jan 2020 06:39:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c53a69cd9387ecea7966ef8581ef0c3366e1779e7867d3d1ee8a20eba7367`  
		Last Modified: Fri, 24 Jan 2020 06:39:37 GMT  
		Size: 545.1 KB (545136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b210bad5c73f765d695e9251417c4e5b64a8fffd3c6ae0aefb1d1a9aa9b4e67`  
		Last Modified: Thu, 30 Jan 2020 02:03:18 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517227e51dff120fb2e91f246a01c17ad6e1e6cefbca487438f7fcde6d292879`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b8a1fcb6aecd586240f74c7cb957bda328649b10a9447b904279962cf58c31`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:4837267b96cb405b6c1ab79f92f7e0d3dc1ca796042b9f836def0bb9aae8949b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34360507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddb13cc00e36f9277b46591ff4391250c36b5cb01d879be5d5950e5476cfd52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:29:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 02:29:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 02:29:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 02:29:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 02:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 02:36:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 02:36:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:07:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:16:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:16:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:19:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:19:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:19:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:19:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:19:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:19:45 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:19:46 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:06:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:06:27 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:06:29 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:06:30 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:31 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:32 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:35 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df684e328567a0a35db6301bcecffeb8c2ab6a69340a96db5d3e73a9fde3da`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbaaf99effdf014f4ce62ee67d7cf9f23205c645f22d554e6e925ef12ffcd70`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99838bf36837f5d2206ac07b2f399dca053921c575c4e9ea8fce917f1672383a`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce00e1e2d33cde79543bc9b4fa5d33fd33d9c5ad181c2530de4700e933322a`  
		Last Modified: Fri, 24 Jan 2020 02:48:36 GMT  
		Size: 12.3 MB (12327133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5773abc403eb88d8a6b65b76101051c21a8825f96d998431948fd5391c32012a`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7f54b41d689d5a8e23cb78d3e733b08c3bced9670b452956e90753e4d57c`  
		Last Modified: Fri, 24 Jan 2020 02:48:38 GMT  
		Size: 14.4 MB (14397481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf3229c4d684db86fe9b5be5052fb6393fd9f48e91ef859d65c2f882d5e517d`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc35742ac6688b780aa26a568715c2901344953a81392f59c56be42c21e49b`  
		Last Modified: Fri, 24 Jan 2020 02:48:34 GMT  
		Size: 72.5 KB (72452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0781411d60db178aca22f04381dce10aca4d91bfa5ac3b13146449990c27b56`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37c111e33c1155179a3884270ad7ee4b6246834506e4a36b1f3f1dd9127cf03`  
		Last Modified: Fri, 24 Jan 2020 06:07:41 GMT  
		Size: 356.9 KB (356883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0b8b4be1be2f8f92c2cdc7fd340a75fa74dd88f6f86a2684ff4dafbb514b7d`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e1aa73768ce7fa0bc7ab72ff8c0e04abf383612019b88430cdffbcd0e37e04`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 623.5 KB (623521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d92bd5108cc579bd3c931353ddc5793940e6445144797c3c6f9298d8d40b9f`  
		Last Modified: Thu, 30 Jan 2020 01:44:19 GMT  
		Size: 2.5 MB (2485260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3832f13fecf5270841416d14fc30e1b3a6a2c9881517ec51ccf82c78bb715e36`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ba2524bc062dc486296a8530bf1ffd9b04f70fc31ee7a306b8e678c46aec82`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:325615cd344fe5aa9772e751abf97604e8c4e438c52dc33540286282aa4087d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35246922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c93ad9c8973b4cca340b0c5e9fb63ffe2223d9654cff7d6b497bb0a8176e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:41:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:41:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:41:37 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:41:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:41:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 06:32:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:08:55 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:08:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:08:57 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:08:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:08:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:08:58 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:08:58 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:21:08 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:21:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:21:10 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 08:21:10 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:27 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686b8c2d7ff02237fc9b12daa86e7e7328b7031b6585a20cd6b5fd618f77486`  
		Last Modified: Sat, 18 Jan 2020 06:45:55 GMT  
		Size: 1.5 MB (1452582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564ce419d6f56887ea2bd9699c37517ecd579e747f1a2698e764ad6f74e66b4c`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ef48cddae433ef86445fc9786eb75673c1c0c6d903fd7a81b2c56fb7e1b86`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5702c4bff7a894a50017cb8d26ad237f05b3ce8373acf4a23ec5c471a226f7fd`  
		Last Modified: Fri, 24 Jan 2020 02:45:37 GMT  
		Size: 12.3 MB (12327121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6363df2f3e95a21deb5655ca3c0d5727eccec7a1a2327754438d4cfb07ecab09`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7e156b40f3210869a4fc5514a09eff0486bbaffc00a9f0074fd968dc1d2d2`  
		Last Modified: Fri, 24 Jan 2020 02:45:39 GMT  
		Size: 15.1 MB (15060955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d80df17e2006212e3bfe404d01bca2ca12fb9a8236851996a44cedb8e549d7`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b10aa160d8af5bac5b5fe05bfc28fe59c62e16b29670d4172d4b5fd654a696a`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 72.1 KB (72107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ef15b4c6b44395040e47685dc8146b8b721daaf7b1f759de9667a10aca86b`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31f939f799f9b3cead96d77256a42cdf089781c26b983e4e176e680bd63ab`  
		Last Modified: Fri, 24 Jan 2020 08:22:02 GMT  
		Size: 374.1 KB (374066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b948106b58045ef1d7d0a85be08d79c9e02c4a5345260049ee6d0f67adfecb8`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f60158d6669b6b4c2ea0052c70b8a51ecabcc5ba00181a3f6f5168a13313eb`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 653.1 KB (653110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41727753f258f4a95fee2912b0f62074ff23cccdde7bec37e8eb100b1780e046`  
		Last Modified: Thu, 30 Jan 2020 01:41:09 GMT  
		Size: 2.5 MB (2485234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f6690243e337d2d22c882d360e922dfe2a5cb0f1ef70aba83fb58de94c9d1`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec7bcd3e9beef800a28f552cfe5ecb3098a4058a9688db8914d9e1027c8c32b`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1.7-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:e9131ce7a4fa4df2d51acbfeec2067ab25fad3120250758ce3a07c7c9b2a92e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35846949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8fdb680cd660c07b3853ab66aab9f45f26a6440f7fbea93c49d15226245d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:24:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:24:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:24:20 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:24:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:29:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:59:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:14 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:16 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:07:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:07:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:07:44 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:07:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:07:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:07:53 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:07:56 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:56:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:56:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:56:33 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:56:35 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:08 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:15 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:17 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:18 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccdcd97be351ef8da754f6efea3745b7060b1fe92ab96e4b8f5ff85b6322da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.4 MB (1397881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea78a138902aeee431e9b31b236dfea5d4f95a1e155aada946ca57f6650a4da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda899b5dd7be53564e6266c17b869d98468c50bc887279c51acacfa831de39f`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe788d20bfb24ce14df58fb94bd73b55687fd6de6afe42325ab1c44ba587cd3`  
		Last Modified: Fri, 24 Jan 2020 02:48:03 GMT  
		Size: 12.3 MB (12327146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae871526dcb6454acaf782bee3e5d631535828619bcbc4123867a07ee9505e`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e1fbe9be3ef95e0870d1590a81311ea511056b80639f4c7e7fcee4f01d403c`  
		Last Modified: Fri, 24 Jan 2020 02:48:04 GMT  
		Size: 15.7 MB (15654284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a7980c3234632f6f8e701aac524333a6f1c0ad5edaca10a2706868ac22f7ae`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6daa4d8c7d908b6559e4509800bcb0a9e1f094166a268352ef36abcf2de77`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 72.8 KB (72783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d52f0dd733a2a7fc154f9816e9c5c013e2d6999a2a1ba9f8f4a769e28703270`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb531ca214ceade639ebd05f1b5f2dc085fe551a38afa2c9fb8d55c257b4f74`  
		Last Modified: Fri, 24 Jan 2020 10:58:35 GMT  
		Size: 394.2 KB (394241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ee59a808dcb66b0696e608e9714fe00b8b28efffb4818c8dcbfd74fc3b9546`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264bbe1b482b9b77c5496fb4f8070f2b495cef65fc2c22efab5f67a3c522c8a`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 678.0 KB (677963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fccad52f0230ba6f70840d2bb4aeeaab419fac2d991d223c3879a7113a97969`  
		Last Modified: Thu, 30 Jan 2020 02:22:35 GMT  
		Size: 2.5 MB (2485257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a872189e6112212034ca7fd0a912804de4b84a897c6c39788e42b91a5074e7b2`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5421523593548014784c4c9fb616a133a4f389801be8831b77ef3ea673e3d89`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1-apache`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1-apache` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-apache` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1-fpm`

```console
$ docker pull yourls@sha256:b824d208a937ddd8a2c7a7956df6b64f15d7fcd908853af04da885d485a388a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1-fpm` - linux; amd64

```console
$ docker pull yourls@sha256:01b5c3b8614e71685df105367805677ce4c5409c93f3bc0cd6ff7ed707af8d13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147711401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70ed93dae4e69dae94eb75be121b4736186e51afb371aa803e227c6d0768d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:11:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:22:07 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:22:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:22:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:28:24 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:28:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:28:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:28:25 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:28:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 09:28:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 09:28:26 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 09:28:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:50:39 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:40 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:38 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442b1ecfb2c9a625353fea0f844074f8fe0fe6143b8d91d19ebce373d9ed1007`  
		Last Modified: Fri, 24 Jan 2020 10:46:22 GMT  
		Size: 12.6 MB (12629735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604c883860730b90a8915cb178846302377a485632f4678abbf1245bb5df6cd7`  
		Last Modified: Fri, 24 Jan 2020 10:46:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2149af9158125e9e52378bf32dd870b97bf83d41e3ee72fc17440494a32cb6cd`  
		Last Modified: Fri, 24 Jan 2020 10:46:27 GMT  
		Size: 28.5 MB (28546306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbb08b8828428d4e6e486ad6d1821d280bae55744f421fa8035d44540fab006`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1809e0c1876e3fc2c3ea53d38b99b19989dba26435b6161a7d9c072b9e424fe4`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd69a9444b9d6fe58338b42cb8e5198c82b019ca4590614d01790c770869c376`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa924e44a1f5bcdfef7eba9bf5a4f779831c0e98064ec42382e9f53dbd8d7ce`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f9324e39d14f0d2d2350bc4af8a09f727ba4ac1e189ff8a400969eb94c954b`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 291.7 KB (291679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c4c4f41bdf1a5cb5842d7d5fc99441290be8a0e6e5236ccc4ff4e57dfda8ce`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d11b8c2ff5395e48a60688f771dc13a34dc660e2c062a4af5aa620bdfc8b48a`  
		Last Modified: Thu, 30 Jan 2020 02:22:05 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ede6f75ccd4614c45f5e37928d8b8041bdfd1adab24d94a80e4bde5756db9`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6e3fb679468e6cd073b1b3fb682ac09c49a8939842dd9e369cda2479693653`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:fb994af6b4fc7458db3335fd3d16f0fdfadd47a884de51198f698fda403a416b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126187218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06387d9df9126dbd6beef0251e6fa07ce5dcf7eeff6c155d0b741a8f33ff68a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:49:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:32:24 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:32:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:32:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:36:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:36:43 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:36:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:36:45 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:36:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 21:36:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 21:36:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 21:36:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:05:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:05:36 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:05:37 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:46 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:47 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:49 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:50 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:51 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbfb91322c2c956ffb8a049056ce6ed7e8a02a509311179ea6b266b1cd45496`  
		Last Modified: Thu, 23 Jan 2020 22:09:11 GMT  
		Size: 12.6 MB (12627683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98747b31069e9460384399be99d08e3d6ba973cdc421a693dba732f9034e1858`  
		Last Modified: Thu, 23 Jan 2020 22:09:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b584443a0241f6eb684458e292d8a1364815de66d19a428c63397a77f9326425`  
		Last Modified: Thu, 23 Jan 2020 22:09:22 GMT  
		Size: 27.2 MB (27155786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62342286e070b175d5f33b0c57aaac3dcb531302615717719031379bb49bbd`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b721095f046edfcc7c96256d02cf74d7f1878b67434564c5099d4e2bc97c7`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d905d65d2a7c8b3a642c15a284c5a5eb9b5e766ce03efa7e96f1654a186a07b`  
		Last Modified: Thu, 23 Jan 2020 22:09:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f81752db9dc5105c0b0686049d8df61c37cbfc1439036c5b0507ebbf7d8be78`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b12f633c01fd0ed42e045e82f844b9dc106acf3db24b479ab4351b86a538ca5`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 275.0 KB (275005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a984a8704ce9b04866ce262c93d3f016811f963cc337f4167eecb383a4cefce2`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c76d4c578c2ea8b71fe614c34ac283ef4499baf10bb6cca8714b5cfaebed487`  
		Last Modified: Thu, 30 Jan 2020 01:49:28 GMT  
		Size: 2.5 MB (2485134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028c42b082088168c3dfd40cc3342cff201c30a1977fa6051de6a58d2df3243c`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6014ee5568d3fcaf8859e18f6a66c557acee07a3f191bc73b4e8736866f7df80`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:503fcf065f42adbc1c909c18065cfd184771b53b11cd87a0201c29ec9a9d0641
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123715481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff768dc3a6cb4787f1dbfb1cb0d807acc1368c492965340630f0b60a2cb9e1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:43:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:51:17 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:51:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:51:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:55:12 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:55:17 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:55:19 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:55:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:55:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:55:25 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:55:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:37:26 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:37:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:37:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb1758fc39381ea05e8422ad87509422182f75ed593f56bb784cc2ee8f8d0d`  
		Last Modified: Thu, 23 Jan 2020 23:49:59 GMT  
		Size: 12.6 MB (12627816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c8be070a970b9520f0c5411faaff68b310398cdfba729736a9df57fe91fbd8`  
		Last Modified: Thu, 23 Jan 2020 23:49:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf5db91a1e39f4ee33ed64b2ce1c0f67c6d6168ffd1c962f0d17942ba03bb3b`  
		Last Modified: Thu, 23 Jan 2020 23:50:04 GMT  
		Size: 26.1 MB (26139997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d1c64408f61b28105b9808140e533f282dfe098b735fa894b73fd51dde992`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b510571207603d8b273d6df417b8169f6bbf0cc1d39fb425b28f4382afc1bfe8`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0b9ba2acc5213b37b46a7a6bcee1e7e0c02c26d6bcd99f6a3721f62f3799d4`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0fabfd4ac1f5d51ab09cfd94f9e380e0640968e5a7b324629741d4b28a8602`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74821a2451c1a39fe37776ff8c2071ef99e5fafb5e90d2b2db8574b8e0e11d7`  
		Last Modified: Fri, 24 Jan 2020 06:39:24 GMT  
		Size: 247.7 KB (247734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82272351eb30b6dec796c32b9106946336efa7c2fc55683951649a8e9d74d5b3`  
		Last Modified: Fri, 24 Jan 2020 06:39:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57c1c5adc6c645d2b1fc35333027b0ed54ccb52c719addc51a9cb1f4b46a46`  
		Last Modified: Thu, 30 Jan 2020 02:03:07 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383028fb815c7fd589fdddb28f1beb3199ca8743bd814282c7a04279489cf9e5`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353080e7bb45e4c4d77e28f78bb37560ec2b0b6741febf02580932526d21819`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:102bd3f157fdced2dab193af485d83fafb6b975acbb05543720956683792e2a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139830083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e29c1d68344ae19182e342b8f893b806dcb3184feefc77f7fcf5172e0c556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:43:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 14:44:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:37:37 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:44:49 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:44:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:44:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:45:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:45:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:48:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:48:50 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:48:52 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:48:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:48:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:48:56 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:48:57 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:05:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:05:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:05:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:19 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:20 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:23 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:23 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:24 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5385e23b021c86fa2519c3af464e961ce347de02b0c3ca2926e40f888308f2b7`  
		Last Modified: Fri, 24 Jan 2020 02:46:23 GMT  
		Size: 12.6 MB (12628557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247490a29552c9c6da012dc7ea7a293a66b78f784d71e62f9b197e7a2a8c58dd`  
		Last Modified: Fri, 24 Jan 2020 02:46:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a810846e71871c7ad2826a5abb33a4e83c09b33dc949ecbf776887e6d35809`  
		Last Modified: Fri, 24 Jan 2020 02:46:27 GMT  
		Size: 28.2 MB (28231414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa180318dc8ef2bad411c5e6b92f972287e7d53ba6976c859afbe244034c003b`  
		Last Modified: Fri, 24 Jan 2020 02:46:12 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fcaa8f8a88faf16705834f29b893eb7be1e10189c54b9aa2a93987c025fd78`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d82a6edcc81dcd3aa46d2bccee534bb1498637b6a985b9d982a48e5461167`  
		Last Modified: Fri, 24 Jan 2020 02:46:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d142df4bd33c314b37742a530120372a0939a833e971b47db7a0576e7fcadda1`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089bc3d67b4e490c6544f2b280de8ff34881292944073d3b8b023de9966277a`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 284.3 KB (284288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5267d5f0e9184d651724696556d09bc2194b564641ebb28f7b0318fc33595858`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c291942bf334792ed77480fc0b42d374edd00d431ed7c4128d33655c9a97dbb`  
		Last Modified: Thu, 30 Jan 2020 01:44:10 GMT  
		Size: 2.5 MB (2485137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395b990c9dbcf4c7ef477d85aeaaa21ea24271ea4e4caa029dc2e29acbc14e9`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64629dd41bce5414d5971281d9b3e2738738b945337c4abb5a975ed4d05fa1db`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; 386

```console
$ docker pull yourls@sha256:a3028c7ed251f3e1a738d6040840ab2924156394c2ce983578ead7fbf950658a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153487648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b961a4b045103bca431c6df18c5a0ec1a42a6c37f1c30ee66276a49a4583970e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:42:02 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:25:08 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:25:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:30:31 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:30:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:30:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:30:33 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:30:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:30:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:30:34 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:30:34 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:20:24 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:20:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:20:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:18 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:19 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e4c3884d21c912689646ef044df487d2ba5563660a7c48199494657002d8ae`  
		Last Modified: Fri, 24 Jan 2020 02:43:20 GMT  
		Size: 12.6 MB (12628971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be88344b8a867d5499c731bf7b2c4ce3da59fbc53490ca490b0fa834bf2e385`  
		Last Modified: Fri, 24 Jan 2020 02:43:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1f649f6a0fc1bc15c1b6073b282721d907c3e98c967c42ba2441e6b22b9375`  
		Last Modified: Fri, 24 Jan 2020 02:43:29 GMT  
		Size: 29.1 MB (29112034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377ba8601df6ecff1825708c6a04f421167d938a2aaab37aca18914b110dba16`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4173bd41a613e320793f323a704526922df3d3a6db5510fad85a035b7de7b03`  
		Last Modified: Fri, 24 Jan 2020 02:43:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b918685c71fa48d6e4f27fd3019c5f1a074d371ff6f9b857fffe797df5ad3631`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aaafa98d5bff0795de02c9b8a85482591bcfa3718c8a5189a93b7602f072f7`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1313cc666858c3fbf3761cde39726d40e423a307783edc8bfa0103c0df7f63e`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 300.3 KB (300334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9370e4cd5f9b6334afedbbda81083630b745a0c9b512bcb54c68503776ff22c8`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6349e0c7616f4e696b45ff9ff8d8ec35921711e48664d494e8ff7e3b85af6dc`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165a82a2a23f3878e537927ef32507188267136d047301ed0ba7348c94a090f3`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf7ad141068b6803eb4dce32190d923dec5e9508f09ebd560e95b6823cfaf30`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:444f9ae1ba7b1cb9b1c9532b7651618816069e2adca92b8328a0edab90703378
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7c418249d87b67d1fe7d9cd2a6670c24a9179dd95b594f3748787aba64b2f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:23:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 18:23:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:23:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:24:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:33:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:23:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:23:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:23:30 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:24:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:28:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:29:01 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:29:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:29:15 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:29:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:29:20 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:29:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:29:28 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:29:30 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:55:06 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:55:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:55:14 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:20:27 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:31 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:40 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:42 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:43 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569cb347cab0d4635b52aabf03a42c7b540a9cdb8a7cc3724e035548cb2479c`  
		Last Modified: Fri, 24 Jan 2020 02:44:40 GMT  
		Size: 12.6 MB (12629483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7f9344526bdabbec6ca4032f08dc34692fe191bdfd2823bf82e84d2da1bb2d`  
		Last Modified: Fri, 24 Jan 2020 02:44:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3e9e86279b094e4fcda41c96f85140f5e2c97c20ed45abf760efe04fa028e`  
		Last Modified: Fri, 24 Jan 2020 02:44:46 GMT  
		Size: 30.2 MB (30243520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b77ffab588104f2668d6b0f944389432ed4160c951de7ef7f46ba7cdf88179d`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388698cb0d1b4ac7615cffdc3fcbdf4c05c9cf65ae377df6169dd3b338792fe`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa9d46432c785ae0cd3e45eb865d048dd4adc9aef4faef88e4b8d8f9cd53b12`  
		Last Modified: Fri, 24 Jan 2020 02:44:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade4f3c53bdd51572900708e83ba2057be3d4c20cd154b218246bf56801e90c`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6ceda7ebffa5b7f688100d88c571f8759321a8a7123e29a0abe8d792eb67b`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 322.8 KB (322761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2805e3c107f737ca23ea5a8b2929fdcec068c27e8d83173bed2c15359e4041c`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40499203c6719755f97fae3ccf8f55651615f8c019dd724ff0b9d643bff06bab`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e065b02e85e387e7a86f73514572ba0f535d319124db5ac45b196f2b710450`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be02c4b3683724d4117a4d242ceded30ced3ef212a8a9b2ae13459b7d409a24`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:0330e5b850c7d5d1745f4aeaf640f9f2dd539f8447a0ebc965cf8a50cfa62ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:bd4ea8165751899c16a2fc66635e2c17b6bba8944e4f47ee39d00a2060313565
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34689132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa09543500501ddd080f4f4d3901c214c54ffbfb3b053105c0115f66a4067d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:18:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:18:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:18:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:18:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:18:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:23:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:57:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 10:03:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 10:03:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 10:10:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 10:10:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 10:10:40 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:10:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 10:10:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 10:10:41 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 10:10:41 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:51:20 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:51:21 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:51:22 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:51:22 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:42 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:43 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:44 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c0a1817becf025301783a94fa11de700972e7d7c117ca7e45d080db0ec1a11`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.4 MB (1354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5b3ea1fc31791c18f464b5b95dd3d9b8ff97aef4b64e0202f3da7f5550e80`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87396003bdeb76e6e367a5ae26be9642a89986dcda71b3491412c579cb6859`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17200a597429895679e6159f86a8d36b47a19e3d129b274280de24310378285`  
		Last Modified: Fri, 24 Jan 2020 10:48:27 GMT  
		Size: 12.3 MB (12327117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e0b32c554d6b99c5783aefcd5e40c676adc57c3bf841ac3e75df2f48ebe74`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27693a4cd8b214566f0beaa6ad32ae12af848d918678a3ada48120498bade0e`  
		Last Modified: Fri, 24 Jan 2020 10:48:23 GMT  
		Size: 14.7 MB (14655505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165dc5b50792307d63058296f7dffb1736fdab36ae5eec8b9171f40237f990cb`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f5ecc3407bba24c5755ee7b5f66315ad12aa11f2799fbe107091763e3d4ca`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348837019c84bd0cf419da2c04934de3d0734a43bc13ddbaaada7700bc04d392`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cad7e57c42971b072fe53a9c8b7faecfa513033f552912d0cc2d9af846ffe9`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 362.5 KB (362525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd85ae9f2f169c484ccc596b08716e51bb9cd3295cdd377354412b64fa46fe`  
		Last Modified: Fri, 24 Jan 2020 10:51:58 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c5cdd0c3abb0d2d205c8e3646b5339762e8d33929dba3833c695bdc461122`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 613.0 KB (613039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b8d1dddb9bcf0341730ebe0d5399653a9c50eaced9daf03b7c517753ff5fce`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 2.5 MB (2485235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e43e8ec3155993e63f2e3672ec709f3a77d9ce8cea734ce71b4fb783eb5060`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2768c7d2613c5cdcc79f98a52987574d9d2326b868c8d9d12acd901d44dc9c6`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:b4c1d903cb7a27f1472cbf19cb6dc1e420d7d44d97f494da9a3a8cc5f18aa197
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33429819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a80aab2471c71b9bd7291f2982cdfd2abc4c224cd37bfb8576adbc077dfb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:40:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:40:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:40:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:40:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 04:15:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:38:44 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 22:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:42:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:42:57 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:43:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:43:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:43:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:43:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:43:05 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:43:05 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:07:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:07:29 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:07:34 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 00:07:36 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:49:39 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:49:40 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:49:42 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:49:43 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:49:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:49:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c701ead53742b2a88bf4f606bd05029ec59ccaf522450bfa76be8cea0cf02`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 MB (1321088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e3d03f7d4228e33415f8592e7ec2a89fe1616e0ab6366ea68045b09d7f280`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba27e9ff828195f46a3edb0b1e28b5d10451b66ae080c20794f6d005cffbd72`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df6832a2c2a8fb5bcfeb52791d0eb421259c8488f400375b165ce8893c64d63`  
		Last Modified: Thu, 23 Jan 2020 23:04:46 GMT  
		Size: 12.3 MB (12327130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe69c0d5de12e5d470ca61ed1e8963aa3abf3e404ee8532054d9500b74e5d95`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cf033fea6edee7deec178385e5c1c4618becf2e7af7484b9f98cae076ff405`  
		Last Modified: Thu, 23 Jan 2020 23:04:44 GMT  
		Size: 13.7 MB (13654217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f07cfc243eacbc5c270aaa6b18031617fec1eea18e518d1fc7fc90126dd367`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5462852adefed60378b031e016b135ce5666f2e49d982cbc8d63313e5f594aac`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 72.5 KB (72453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c8ab379509fb13b0ebe44275f2df8ad19a00a1c59c0e7b041232653dad74c`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2bf7fa95982abc3a13216bba5f6000994d76ee18184b1431d4340460b9b136`  
		Last Modified: Fri, 24 Jan 2020 00:08:13 GMT  
		Size: 345.7 KB (345725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369e36d2ba0c4e916e43c5d9bae25c8b069ac55d8c8f7f5ce3582992d645303`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf2e49ccc1984afab3b4f9cfac61e5f66ddb07677930243ff0ba8489f062107`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 591.1 KB (591118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2197112a846c7b907958f150c5b4bd33fbe04befc6adac31f5b7e7be09e137`  
		Last Modified: Thu, 30 Jan 2020 01:49:59 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a3a30325d3d12357543b10edd0b0ed71f19d04030f304767f16b06d669e5cb`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ef3dc4164bf15c0cc31f54c7e4cd7e6a7737d669f34c6fe44e9245e6cd88cc`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:cf92b775d3826527d200012694e4120c64042d4275ed2123b93dad2169e374b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32213379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451f8ec4aaca7e7205470fc440ac1c75ead9c99b9a56edcdfcaf94e08ff4438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:22:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:22:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:22:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:22:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:27:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:27:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:27:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:28:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:56:58 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 23:20:22 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 23:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:20:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:23:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:23:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:23:44 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:23:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:23:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:23:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:38:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:38:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:38:27 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:38:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:17 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:18 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:22 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecb809efefba021b07183ae486164fd475667a42a78ab308bd01b8d7dd8c1e`  
		Last Modified: Sat, 18 Jan 2020 06:09:11 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec95513b0eab50a07131cbee828abed358fb86fd276018e1bae6f04611ed9`  
		Last Modified: Sat, 18 Jan 2020 06:09:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d1b57d2f034e68934a4116a4434479186cfce56d1235af4f1c1b9de08acbc`  
		Last Modified: Sat, 18 Jan 2020 06:09:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efaa7391df564715aff5a3ed3728a8506f4242ea7af5b78f7084cba8f1d9e16`  
		Last Modified: Thu, 23 Jan 2020 23:52:11 GMT  
		Size: 12.3 MB (12327128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27fe1a4a8c3bdc42c663754127b8d2bf1d28761de505c66874975e2cfbe7d9`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc6150d058ad54d1317f115cdf515f2ee41b09349a4e48c666108c73d32063`  
		Last Modified: Thu, 23 Jan 2020 23:52:07 GMT  
		Size: 12.8 MB (12797323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0aad572300486b8710177efe735704d9acfd6f6edd3247cd91f6890909dc55`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791fec6f4e7194daae4ecf5d0bb4ab9b292190dafa9db15fa319c4e88ccd77ae`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 72.5 KB (72451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b07590f3a1c8342e06b308e79d7399c1d880aa4d1f536df9398ebf2232c551`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1a4f15d2507503adbd0ec1d83a575a6dd28ae766d2a6b7c64bb45d1f4be0c`  
		Last Modified: Fri, 24 Jan 2020 06:39:38 GMT  
		Size: 324.0 KB (323981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de491bbe822d164a59311f8f49bbafa2f2a8cb4808d9e174a44868ae75cd86f8`  
		Last Modified: Fri, 24 Jan 2020 06:39:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c53a69cd9387ecea7966ef8581ef0c3366e1779e7867d3d1ee8a20eba7367`  
		Last Modified: Fri, 24 Jan 2020 06:39:37 GMT  
		Size: 545.1 KB (545136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b210bad5c73f765d695e9251417c4e5b64a8fffd3c6ae0aefb1d1a9aa9b4e67`  
		Last Modified: Thu, 30 Jan 2020 02:03:18 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517227e51dff120fb2e91f246a01c17ad6e1e6cefbca487438f7fcde6d292879`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b8a1fcb6aecd586240f74c7cb957bda328649b10a9447b904279962cf58c31`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:4837267b96cb405b6c1ab79f92f7e0d3dc1ca796042b9f836def0bb9aae8949b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34360507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddb13cc00e36f9277b46591ff4391250c36b5cb01d879be5d5950e5476cfd52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:29:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 02:29:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 02:29:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 02:29:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 02:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 02:36:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 02:36:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:07:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:16:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:16:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:19:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:19:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:19:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:19:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:19:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:19:45 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:19:46 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:06:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:06:27 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:06:29 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:06:30 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:31 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:32 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:35 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df684e328567a0a35db6301bcecffeb8c2ab6a69340a96db5d3e73a9fde3da`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbaaf99effdf014f4ce62ee67d7cf9f23205c645f22d554e6e925ef12ffcd70`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99838bf36837f5d2206ac07b2f399dca053921c575c4e9ea8fce917f1672383a`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce00e1e2d33cde79543bc9b4fa5d33fd33d9c5ad181c2530de4700e933322a`  
		Last Modified: Fri, 24 Jan 2020 02:48:36 GMT  
		Size: 12.3 MB (12327133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5773abc403eb88d8a6b65b76101051c21a8825f96d998431948fd5391c32012a`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7f54b41d689d5a8e23cb78d3e733b08c3bced9670b452956e90753e4d57c`  
		Last Modified: Fri, 24 Jan 2020 02:48:38 GMT  
		Size: 14.4 MB (14397481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf3229c4d684db86fe9b5be5052fb6393fd9f48e91ef859d65c2f882d5e517d`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc35742ac6688b780aa26a568715c2901344953a81392f59c56be42c21e49b`  
		Last Modified: Fri, 24 Jan 2020 02:48:34 GMT  
		Size: 72.5 KB (72452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0781411d60db178aca22f04381dce10aca4d91bfa5ac3b13146449990c27b56`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37c111e33c1155179a3884270ad7ee4b6246834506e4a36b1f3f1dd9127cf03`  
		Last Modified: Fri, 24 Jan 2020 06:07:41 GMT  
		Size: 356.9 KB (356883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0b8b4be1be2f8f92c2cdc7fd340a75fa74dd88f6f86a2684ff4dafbb514b7d`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e1aa73768ce7fa0bc7ab72ff8c0e04abf383612019b88430cdffbcd0e37e04`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 623.5 KB (623521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d92bd5108cc579bd3c931353ddc5793940e6445144797c3c6f9298d8d40b9f`  
		Last Modified: Thu, 30 Jan 2020 01:44:19 GMT  
		Size: 2.5 MB (2485260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3832f13fecf5270841416d14fc30e1b3a6a2c9881517ec51ccf82c78bb715e36`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ba2524bc062dc486296a8530bf1ffd9b04f70fc31ee7a306b8e678c46aec82`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:325615cd344fe5aa9772e751abf97604e8c4e438c52dc33540286282aa4087d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35246922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c93ad9c8973b4cca340b0c5e9fb63ffe2223d9654cff7d6b497bb0a8176e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:41:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:41:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:41:37 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:41:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:41:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 06:32:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:08:55 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:08:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:08:57 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:08:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:08:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:08:58 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:08:58 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:21:08 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:21:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:21:10 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 08:21:10 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:27 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686b8c2d7ff02237fc9b12daa86e7e7328b7031b6585a20cd6b5fd618f77486`  
		Last Modified: Sat, 18 Jan 2020 06:45:55 GMT  
		Size: 1.5 MB (1452582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564ce419d6f56887ea2bd9699c37517ecd579e747f1a2698e764ad6f74e66b4c`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ef48cddae433ef86445fc9786eb75673c1c0c6d903fd7a81b2c56fb7e1b86`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5702c4bff7a894a50017cb8d26ad237f05b3ce8373acf4a23ec5c471a226f7fd`  
		Last Modified: Fri, 24 Jan 2020 02:45:37 GMT  
		Size: 12.3 MB (12327121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6363df2f3e95a21deb5655ca3c0d5727eccec7a1a2327754438d4cfb07ecab09`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7e156b40f3210869a4fc5514a09eff0486bbaffc00a9f0074fd968dc1d2d2`  
		Last Modified: Fri, 24 Jan 2020 02:45:39 GMT  
		Size: 15.1 MB (15060955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d80df17e2006212e3bfe404d01bca2ca12fb9a8236851996a44cedb8e549d7`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b10aa160d8af5bac5b5fe05bfc28fe59c62e16b29670d4172d4b5fd654a696a`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 72.1 KB (72107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ef15b4c6b44395040e47685dc8146b8b721daaf7b1f759de9667a10aca86b`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31f939f799f9b3cead96d77256a42cdf089781c26b983e4e176e680bd63ab`  
		Last Modified: Fri, 24 Jan 2020 08:22:02 GMT  
		Size: 374.1 KB (374066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b948106b58045ef1d7d0a85be08d79c9e02c4a5345260049ee6d0f67adfecb8`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f60158d6669b6b4c2ea0052c70b8a51ecabcc5ba00181a3f6f5168a13313eb`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 653.1 KB (653110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41727753f258f4a95fee2912b0f62074ff23cccdde7bec37e8eb100b1780e046`  
		Last Modified: Thu, 30 Jan 2020 01:41:09 GMT  
		Size: 2.5 MB (2485234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f6690243e337d2d22c882d360e922dfe2a5cb0f1ef70aba83fb58de94c9d1`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec7bcd3e9beef800a28f552cfe5ecb3098a4058a9688db8914d9e1027c8c32b`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:e9131ce7a4fa4df2d51acbfeec2067ab25fad3120250758ce3a07c7c9b2a92e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35846949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8fdb680cd660c07b3853ab66aab9f45f26a6440f7fbea93c49d15226245d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:24:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:24:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:24:20 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:24:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:29:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:59:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:14 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:16 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:07:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:07:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:07:44 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:07:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:07:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:07:53 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:07:56 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:56:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:56:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:56:33 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:56:35 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:08 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:15 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:17 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:18 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccdcd97be351ef8da754f6efea3745b7060b1fe92ab96e4b8f5ff85b6322da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.4 MB (1397881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea78a138902aeee431e9b31b236dfea5d4f95a1e155aada946ca57f6650a4da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda899b5dd7be53564e6266c17b869d98468c50bc887279c51acacfa831de39f`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe788d20bfb24ce14df58fb94bd73b55687fd6de6afe42325ab1c44ba587cd3`  
		Last Modified: Fri, 24 Jan 2020 02:48:03 GMT  
		Size: 12.3 MB (12327146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae871526dcb6454acaf782bee3e5d631535828619bcbc4123867a07ee9505e`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e1fbe9be3ef95e0870d1590a81311ea511056b80639f4c7e7fcee4f01d403c`  
		Last Modified: Fri, 24 Jan 2020 02:48:04 GMT  
		Size: 15.7 MB (15654284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a7980c3234632f6f8e701aac524333a6f1c0ad5edaca10a2706868ac22f7ae`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6daa4d8c7d908b6559e4509800bcb0a9e1f094166a268352ef36abcf2de77`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 72.8 KB (72783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d52f0dd733a2a7fc154f9816e9c5c013e2d6999a2a1ba9f8f4a769e28703270`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb531ca214ceade639ebd05f1b5f2dc085fe551a38afa2c9fb8d55c257b4f74`  
		Last Modified: Fri, 24 Jan 2020 10:58:35 GMT  
		Size: 394.2 KB (394241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ee59a808dcb66b0696e608e9714fe00b8b28efffb4818c8dcbfd74fc3b9546`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264bbe1b482b9b77c5496fb4f8070f2b495cef65fc2c22efab5f67a3c522c8a`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 678.0 KB (677963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fccad52f0230ba6f70840d2bb4aeeaab419fac2d991d223c3879a7113a97969`  
		Last Modified: Thu, 30 Jan 2020 02:22:35 GMT  
		Size: 2.5 MB (2485257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a872189e6112212034ca7fd0a912804de4b84a897c6c39788e42b91a5074e7b2`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5421523593548014784c4c9fb616a133a4f389801be8831b77ef3ea673e3d89`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:apache`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:apache` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:apache` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:fpm`

```console
$ docker pull yourls@sha256:b824d208a937ddd8a2c7a7956df6b64f15d7fcd908853af04da885d485a388a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:01b5c3b8614e71685df105367805677ce4c5409c93f3bc0cd6ff7ed707af8d13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147711401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70ed93dae4e69dae94eb75be121b4736186e51afb371aa803e227c6d0768d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 20:51:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:11:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:22:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:22:07 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:22:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:22:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:28:24 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:28:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:28:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:28:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:28:25 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:28:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 09:28:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 09:28:26 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 09:28:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:50:39 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:40 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:36 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:38 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442b1ecfb2c9a625353fea0f844074f8fe0fe6143b8d91d19ebce373d9ed1007`  
		Last Modified: Fri, 24 Jan 2020 10:46:22 GMT  
		Size: 12.6 MB (12629735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604c883860730b90a8915cb178846302377a485632f4678abbf1245bb5df6cd7`  
		Last Modified: Fri, 24 Jan 2020 10:46:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2149af9158125e9e52378bf32dd870b97bf83d41e3ee72fc17440494a32cb6cd`  
		Last Modified: Fri, 24 Jan 2020 10:46:27 GMT  
		Size: 28.5 MB (28546306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbb08b8828428d4e6e486ad6d1821d280bae55744f421fa8035d44540fab006`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1809e0c1876e3fc2c3ea53d38b99b19989dba26435b6161a7d9c072b9e424fe4`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd69a9444b9d6fe58338b42cb8e5198c82b019ca4590614d01790c770869c376`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa924e44a1f5bcdfef7eba9bf5a4f779831c0e98064ec42382e9f53dbd8d7ce`  
		Last Modified: Fri, 24 Jan 2020 10:46:20 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f9324e39d14f0d2d2350bc4af8a09f727ba4ac1e189ff8a400969eb94c954b`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 291.7 KB (291679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c4c4f41bdf1a5cb5842d7d5fc99441290be8a0e6e5236ccc4ff4e57dfda8ce`  
		Last Modified: Fri, 24 Jan 2020 10:51:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d11b8c2ff5395e48a60688f771dc13a34dc660e2c062a4af5aa620bdfc8b48a`  
		Last Modified: Thu, 30 Jan 2020 02:22:05 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ede6f75ccd4614c45f5e37928d8b8041bdfd1adab24d94a80e4bde5756db9`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6e3fb679468e6cd073b1b3fb682ac09c49a8939842dd9e369cda2479693653`  
		Last Modified: Thu, 30 Jan 2020 02:22:04 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:fb994af6b4fc7458db3335fd3d16f0fdfadd47a884de51198f698fda403a416b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126187218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06387d9df9126dbd6beef0251e6fa07ce5dcf7eeff6c155d0b741a8f33ff68a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 11:56:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:56:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:49:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:32:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:32:24 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:32:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:32:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:36:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:36:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:36:43 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:36:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:36:45 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:36:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 21:36:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 21:36:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 21:36:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:05:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:05:36 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:05:37 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:46 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:47 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:49 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:50 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:51 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbfb91322c2c956ffb8a049056ce6ed7e8a02a509311179ea6b266b1cd45496`  
		Last Modified: Thu, 23 Jan 2020 22:09:11 GMT  
		Size: 12.6 MB (12627683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98747b31069e9460384399be99d08e3d6ba973cdc421a693dba732f9034e1858`  
		Last Modified: Thu, 23 Jan 2020 22:09:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b584443a0241f6eb684458e292d8a1364815de66d19a428c63397a77f9326425`  
		Last Modified: Thu, 23 Jan 2020 22:09:22 GMT  
		Size: 27.2 MB (27155786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62342286e070b175d5f33b0c57aaac3dcb531302615717719031379bb49bbd`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b721095f046edfcc7c96256d02cf74d7f1878b67434564c5099d4e2bc97c7`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d905d65d2a7c8b3a642c15a284c5a5eb9b5e766ce03efa7e96f1654a186a07b`  
		Last Modified: Thu, 23 Jan 2020 22:09:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f81752db9dc5105c0b0686049d8df61c37cbfc1439036c5b0507ebbf7d8be78`  
		Last Modified: Thu, 23 Jan 2020 22:09:08 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b12f633c01fd0ed42e045e82f844b9dc106acf3db24b479ab4351b86a538ca5`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 275.0 KB (275005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a984a8704ce9b04866ce262c93d3f016811f963cc337f4167eecb383a4cefce2`  
		Last Modified: Fri, 24 Jan 2020 00:06:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c76d4c578c2ea8b71fe614c34ac283ef4499baf10bb6cca8714b5cfaebed487`  
		Last Modified: Thu, 30 Jan 2020 01:49:28 GMT  
		Size: 2.5 MB (2485134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028c42b082088168c3dfd40cc3342cff201c30a1977fa6051de6a58d2df3243c`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6014ee5568d3fcaf8859e18f6a66c557acee07a3f191bc73b4e8736866f7df80`  
		Last Modified: Thu, 30 Jan 2020 01:49:27 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:503fcf065f42adbc1c909c18065cfd184771b53b11cd87a0201c29ec9a9d0641
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123715481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff768dc3a6cb4787f1dbfb1cb0d807acc1368c492965340630f0b60a2cb9e1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 15:51:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:43:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:51:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:51:17 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:51:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:51:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:55:12 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:55:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:55:17 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:55:19 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:55:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:55:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:55:25 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:55:27 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:37:26 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:37:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:37:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:05 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:09 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb1758fc39381ea05e8422ad87509422182f75ed593f56bb784cc2ee8f8d0d`  
		Last Modified: Thu, 23 Jan 2020 23:49:59 GMT  
		Size: 12.6 MB (12627816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c8be070a970b9520f0c5411faaff68b310398cdfba729736a9df57fe91fbd8`  
		Last Modified: Thu, 23 Jan 2020 23:49:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf5db91a1e39f4ee33ed64b2ce1c0f67c6d6168ffd1c962f0d17942ba03bb3b`  
		Last Modified: Thu, 23 Jan 2020 23:50:04 GMT  
		Size: 26.1 MB (26139997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d1c64408f61b28105b9808140e533f282dfe098b735fa894b73fd51dde992`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b510571207603d8b273d6df417b8169f6bbf0cc1d39fb425b28f4382afc1bfe8`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0b9ba2acc5213b37b46a7a6bcee1e7e0c02c26d6bcd99f6a3721f62f3799d4`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0fabfd4ac1f5d51ab09cfd94f9e380e0640968e5a7b324629741d4b28a8602`  
		Last Modified: Thu, 23 Jan 2020 23:49:56 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74821a2451c1a39fe37776ff8c2071ef99e5fafb5e90d2b2db8574b8e0e11d7`  
		Last Modified: Fri, 24 Jan 2020 06:39:24 GMT  
		Size: 247.7 KB (247734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82272351eb30b6dec796c32b9106946336efa7c2fc55683951649a8e9d74d5b3`  
		Last Modified: Fri, 24 Jan 2020 06:39:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57c1c5adc6c645d2b1fc35333027b0ed54ccb52c719addc51a9cb1f4b46a46`  
		Last Modified: Thu, 30 Jan 2020 02:03:07 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383028fb815c7fd589fdddb28f1beb3199ca8743bd814282c7a04279489cf9e5`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353080e7bb45e4c4d77e28f78bb37560ec2b0b6741febf02580932526d21819`  
		Last Modified: Thu, 30 Jan 2020 02:03:06 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:102bd3f157fdced2dab193af485d83fafb6b975acbb05543720956683792e2a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139830083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e29c1d68344ae19182e342b8f893b806dcb3184feefc77f7fcf5172e0c556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:43:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 14:44:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:44:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:37:37 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:44:49 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:44:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:44:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:45:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:45:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:48:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:48:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:48:50 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:48:52 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:48:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:48:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:48:56 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:48:57 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:05:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:05:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:05:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:19 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:20 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:23 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:23 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:24 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5385e23b021c86fa2519c3af464e961ce347de02b0c3ca2926e40f888308f2b7`  
		Last Modified: Fri, 24 Jan 2020 02:46:23 GMT  
		Size: 12.6 MB (12628557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247490a29552c9c6da012dc7ea7a293a66b78f784d71e62f9b197e7a2a8c58dd`  
		Last Modified: Fri, 24 Jan 2020 02:46:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a810846e71871c7ad2826a5abb33a4e83c09b33dc949ecbf776887e6d35809`  
		Last Modified: Fri, 24 Jan 2020 02:46:27 GMT  
		Size: 28.2 MB (28231414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa180318dc8ef2bad411c5e6b92f972287e7d53ba6976c859afbe244034c003b`  
		Last Modified: Fri, 24 Jan 2020 02:46:12 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fcaa8f8a88faf16705834f29b893eb7be1e10189c54b9aa2a93987c025fd78`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d82a6edcc81dcd3aa46d2bccee534bb1498637b6a985b9d982a48e5461167`  
		Last Modified: Fri, 24 Jan 2020 02:46:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d142df4bd33c314b37742a530120372a0939a833e971b47db7a0576e7fcadda1`  
		Last Modified: Fri, 24 Jan 2020 02:46:11 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089bc3d67b4e490c6544f2b280de8ff34881292944073d3b8b023de9966277a`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 284.3 KB (284288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5267d5f0e9184d651724696556d09bc2194b564641ebb28f7b0318fc33595858`  
		Last Modified: Fri, 24 Jan 2020 06:07:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c291942bf334792ed77480fc0b42d374edd00d431ed7c4128d33655c9a97dbb`  
		Last Modified: Thu, 30 Jan 2020 01:44:10 GMT  
		Size: 2.5 MB (2485137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395b990c9dbcf4c7ef477d85aeaaa21ea24271ea4e4caa029dc2e29acbc14e9`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64629dd41bce5414d5971281d9b3e2738738b945337c4abb5a975ed4d05fa1db`  
		Last Modified: Thu, 30 Jan 2020 01:44:09 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:a3028c7ed251f3e1a738d6040840ab2924156394c2ce983578ead7fbf950658a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153487648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b961a4b045103bca431c6df18c5a0ec1a42a6c37f1c30ee66276a49a4583970e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 17:02:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:42:02 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:25:07 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:25:08 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:25:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:30:31 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:30:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:30:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:30:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:30:33 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:30:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:30:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:30:34 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:30:34 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:20:24 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:20:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:20:25 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:18 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:19 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:21 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e4c3884d21c912689646ef044df487d2ba5563660a7c48199494657002d8ae`  
		Last Modified: Fri, 24 Jan 2020 02:43:20 GMT  
		Size: 12.6 MB (12628971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be88344b8a867d5499c731bf7b2c4ce3da59fbc53490ca490b0fa834bf2e385`  
		Last Modified: Fri, 24 Jan 2020 02:43:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1f649f6a0fc1bc15c1b6073b282721d907c3e98c967c42ba2441e6b22b9375`  
		Last Modified: Fri, 24 Jan 2020 02:43:29 GMT  
		Size: 29.1 MB (29112034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377ba8601df6ecff1825708c6a04f421167d938a2aaab37aca18914b110dba16`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4173bd41a613e320793f323a704526922df3d3a6db5510fad85a035b7de7b03`  
		Last Modified: Fri, 24 Jan 2020 02:43:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b918685c71fa48d6e4f27fd3019c5f1a074d371ff6f9b857fffe797df5ad3631`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aaafa98d5bff0795de02c9b8a85482591bcfa3718c8a5189a93b7602f072f7`  
		Last Modified: Fri, 24 Jan 2020 02:43:18 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1313cc666858c3fbf3761cde39726d40e423a307783edc8bfa0103c0df7f63e`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 300.3 KB (300334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9370e4cd5f9b6334afedbbda81083630b745a0c9b512bcb54c68503776ff22c8`  
		Last Modified: Fri, 24 Jan 2020 08:21:50 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6349e0c7616f4e696b45ff9ff8d8ec35921711e48664d494e8ff7e3b85af6dc`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165a82a2a23f3878e537927ef32507188267136d047301ed0ba7348c94a090f3`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf7ad141068b6803eb4dce32190d923dec5e9508f09ebd560e95b6823cfaf30`  
		Last Modified: Thu, 30 Jan 2020 01:41:02 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:444f9ae1ba7b1cb9b1c9532b7651618816069e2adca92b8328a0edab90703378
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7c418249d87b67d1fe7d9cd2a6670c24a9179dd95b594f3748787aba64b2f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:23:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 28 Dec 2019 18:23:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:23:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:24:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:33:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:23:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:23:26 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:23:30 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:24:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:28:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:29:01 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:29:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:29:15 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:29:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:29:20 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 01:29:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 01:29:28 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 01:29:30 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:55:06 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:55:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:55:14 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:20:27 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:31 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:40 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:42 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:43 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569cb347cab0d4635b52aabf03a42c7b540a9cdb8a7cc3724e035548cb2479c`  
		Last Modified: Fri, 24 Jan 2020 02:44:40 GMT  
		Size: 12.6 MB (12629483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7f9344526bdabbec6ca4032f08dc34692fe191bdfd2823bf82e84d2da1bb2d`  
		Last Modified: Fri, 24 Jan 2020 02:44:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3e9e86279b094e4fcda41c96f85140f5e2c97c20ed45abf760efe04fa028e`  
		Last Modified: Fri, 24 Jan 2020 02:44:46 GMT  
		Size: 30.2 MB (30243520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b77ffab588104f2668d6b0f944389432ed4160c951de7ef7f46ba7cdf88179d`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388698cb0d1b4ac7615cffdc3fcbdf4c05c9cf65ae377df6169dd3b338792fe`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa9d46432c785ae0cd3e45eb865d048dd4adc9aef4faef88e4b8d8f9cd53b12`  
		Last Modified: Fri, 24 Jan 2020 02:44:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade4f3c53bdd51572900708e83ba2057be3d4c20cd154b218246bf56801e90c`  
		Last Modified: Fri, 24 Jan 2020 02:44:24 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6ceda7ebffa5b7f688100d88c571f8759321a8a7123e29a0abe8d792eb67b`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 322.8 KB (322761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2805e3c107f737ca23ea5a8b2929fdcec068c27e8d83173bed2c15359e4041c`  
		Last Modified: Fri, 24 Jan 2020 10:58:09 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40499203c6719755f97fae3ccf8f55651615f8c019dd724ff0b9d643bff06bab`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e065b02e85e387e7a86f73514572ba0f535d319124db5ac45b196f2b710450`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be02c4b3683724d4117a4d242ceded30ced3ef212a8a9b2ae13459b7d409a24`  
		Last Modified: Thu, 30 Jan 2020 02:22:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:fpm-alpine`

```console
$ docker pull yourls@sha256:0330e5b850c7d5d1745f4aeaf640f9f2dd539f8447a0ebc965cf8a50cfa62ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:bd4ea8165751899c16a2fc66635e2c17b6bba8944e4f47ee39d00a2060313565
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34689132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa09543500501ddd080f4f4d3901c214c54ffbfb3b053105c0115f66a4067d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:18:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:18:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:18:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:18:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:18:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:23:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:57:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 10:03:51 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 10:03:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 10:03:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 10:10:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:10:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 10:10:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 10:10:40 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:10:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 10:10:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 10:10:41 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 10:10:41 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:51:20 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:51:21 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:51:22 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:51:22 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:42 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:43 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:44 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c0a1817becf025301783a94fa11de700972e7d7c117ca7e45d080db0ec1a11`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.4 MB (1354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5b3ea1fc31791c18f464b5b95dd3d9b8ff97aef4b64e0202f3da7f5550e80`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87396003bdeb76e6e367a5ae26be9642a89986dcda71b3491412c579cb6859`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17200a597429895679e6159f86a8d36b47a19e3d129b274280de24310378285`  
		Last Modified: Fri, 24 Jan 2020 10:48:27 GMT  
		Size: 12.3 MB (12327117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e0b32c554d6b99c5783aefcd5e40c676adc57c3bf841ac3e75df2f48ebe74`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27693a4cd8b214566f0beaa6ad32ae12af848d918678a3ada48120498bade0e`  
		Last Modified: Fri, 24 Jan 2020 10:48:23 GMT  
		Size: 14.7 MB (14655505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165dc5b50792307d63058296f7dffb1736fdab36ae5eec8b9171f40237f990cb`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f5ecc3407bba24c5755ee7b5f66315ad12aa11f2799fbe107091763e3d4ca`  
		Last Modified: Fri, 24 Jan 2020 10:48:19 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348837019c84bd0cf419da2c04934de3d0734a43bc13ddbaaada7700bc04d392`  
		Last Modified: Fri, 24 Jan 2020 10:48:18 GMT  
		Size: 7.8 KB (7784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cad7e57c42971b072fe53a9c8b7faecfa513033f552912d0cc2d9af846ffe9`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 362.5 KB (362525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd85ae9f2f169c484ccc596b08716e51bb9cd3295cdd377354412b64fa46fe`  
		Last Modified: Fri, 24 Jan 2020 10:51:58 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c5cdd0c3abb0d2d205c8e3646b5339762e8d33929dba3833c695bdc461122`  
		Last Modified: Fri, 24 Jan 2020 10:51:59 GMT  
		Size: 613.0 KB (613039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b8d1dddb9bcf0341730ebe0d5399653a9c50eaced9daf03b7c517753ff5fce`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 2.5 MB (2485235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e43e8ec3155993e63f2e3672ec709f3a77d9ce8cea734ce71b4fb783eb5060`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2768c7d2613c5cdcc79f98a52987574d9d2326b868c8d9d12acd901d44dc9c6`  
		Last Modified: Thu, 30 Jan 2020 02:22:10 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:b4c1d903cb7a27f1472cbf19cb6dc1e420d7d44d97f494da9a3a8cc5f18aa197
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33429819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a80aab2471c71b9bd7291f2982cdfd2abc4c224cd37bfb8576adbc077dfb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:40:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:40:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:40:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:40:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 04:15:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:38:44 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:38:45 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 22:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:42:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:42:57 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:43:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:43:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:43:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 22:43:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 22:43:05 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 22:43:05 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 00:07:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:07:29 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:07:34 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 00:07:36 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:49:39 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:49:40 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:49:42 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:49:43 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:49:44 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:49:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c701ead53742b2a88bf4f606bd05029ec59ccaf522450bfa76be8cea0cf02`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 MB (1321088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e3d03f7d4228e33415f8592e7ec2a89fe1616e0ab6366ea68045b09d7f280`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba27e9ff828195f46a3edb0b1e28b5d10451b66ae080c20794f6d005cffbd72`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df6832a2c2a8fb5bcfeb52791d0eb421259c8488f400375b165ce8893c64d63`  
		Last Modified: Thu, 23 Jan 2020 23:04:46 GMT  
		Size: 12.3 MB (12327130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe69c0d5de12e5d470ca61ed1e8963aa3abf3e404ee8532054d9500b74e5d95`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cf033fea6edee7deec178385e5c1c4618becf2e7af7484b9f98cae076ff405`  
		Last Modified: Thu, 23 Jan 2020 23:04:44 GMT  
		Size: 13.7 MB (13654217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f07cfc243eacbc5c270aaa6b18031617fec1eea18e518d1fc7fc90126dd367`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5462852adefed60378b031e016b135ce5666f2e49d982cbc8d63313e5f594aac`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 72.5 KB (72453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c8ab379509fb13b0ebe44275f2df8ad19a00a1c59c0e7b041232653dad74c`  
		Last Modified: Thu, 23 Jan 2020 23:04:28 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2bf7fa95982abc3a13216bba5f6000994d76ee18184b1431d4340460b9b136`  
		Last Modified: Fri, 24 Jan 2020 00:08:13 GMT  
		Size: 345.7 KB (345725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369e36d2ba0c4e916e43c5d9bae25c8b069ac55d8c8f7f5ce3582992d645303`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf2e49ccc1984afab3b4f9cfac61e5f66ddb07677930243ff0ba8489f062107`  
		Last Modified: Fri, 24 Jan 2020 00:08:11 GMT  
		Size: 591.1 KB (591118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2197112a846c7b907958f150c5b4bd33fbe04befc6adac31f5b7e7be09e137`  
		Last Modified: Thu, 30 Jan 2020 01:49:59 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a3a30325d3d12357543b10edd0b0ed71f19d04030f304767f16b06d669e5cb`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ef3dc4164bf15c0cc31f54c7e4cd7e6a7737d669f34c6fe44e9245e6cd88cc`  
		Last Modified: Thu, 30 Jan 2020 01:49:58 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:cf92b775d3826527d200012694e4120c64042d4275ed2123b93dad2169e374b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32213379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451f8ec4aaca7e7205470fc440ac1c75ead9c99b9a56edcdfcaf94e08ff4438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:22:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:22:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:22:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:22:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:27:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:27:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:27:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:28:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:56:58 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 23:20:22 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:20:23 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 23:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:20:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:23:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:23:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:23:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:23:44 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:23:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:23:49 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:23:50 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:38:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:38:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:38:27 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:38:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:02:17 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:02:18 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:02:20 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:02:21 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:02:22 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:02:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecb809efefba021b07183ae486164fd475667a42a78ab308bd01b8d7dd8c1e`  
		Last Modified: Sat, 18 Jan 2020 06:09:11 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec95513b0eab50a07131cbee828abed358fb86fd276018e1bae6f04611ed9`  
		Last Modified: Sat, 18 Jan 2020 06:09:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d1b57d2f034e68934a4116a4434479186cfce56d1235af4f1c1b9de08acbc`  
		Last Modified: Sat, 18 Jan 2020 06:09:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efaa7391df564715aff5a3ed3728a8506f4242ea7af5b78f7084cba8f1d9e16`  
		Last Modified: Thu, 23 Jan 2020 23:52:11 GMT  
		Size: 12.3 MB (12327128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27fe1a4a8c3bdc42c663754127b8d2bf1d28761de505c66874975e2cfbe7d9`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc6150d058ad54d1317f115cdf515f2ee41b09349a4e48c666108c73d32063`  
		Last Modified: Thu, 23 Jan 2020 23:52:07 GMT  
		Size: 12.8 MB (12797323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0aad572300486b8710177efe735704d9acfd6f6edd3247cd91f6890909dc55`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791fec6f4e7194daae4ecf5d0bb4ab9b292190dafa9db15fa319c4e88ccd77ae`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 72.5 KB (72451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b07590f3a1c8342e06b308e79d7399c1d880aa4d1f536df9398ebf2232c551`  
		Last Modified: Thu, 23 Jan 2020 23:52:01 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1a4f15d2507503adbd0ec1d83a575a6dd28ae766d2a6b7c64bb45d1f4be0c`  
		Last Modified: Fri, 24 Jan 2020 06:39:38 GMT  
		Size: 324.0 KB (323981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de491bbe822d164a59311f8f49bbafa2f2a8cb4808d9e174a44868ae75cd86f8`  
		Last Modified: Fri, 24 Jan 2020 06:39:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c53a69cd9387ecea7966ef8581ef0c3366e1779e7867d3d1ee8a20eba7367`  
		Last Modified: Fri, 24 Jan 2020 06:39:37 GMT  
		Size: 545.1 KB (545136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b210bad5c73f765d695e9251417c4e5b64a8fffd3c6ae0aefb1d1a9aa9b4e67`  
		Last Modified: Thu, 30 Jan 2020 02:03:18 GMT  
		Size: 2.5 MB (2485259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517227e51dff120fb2e91f246a01c17ad6e1e6cefbca487438f7fcde6d292879`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b8a1fcb6aecd586240f74c7cb957bda328649b10a9447b904279962cf58c31`  
		Last Modified: Thu, 30 Jan 2020 02:03:17 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:4837267b96cb405b6c1ab79f92f7e0d3dc1ca796042b9f836def0bb9aae8949b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34360507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddb13cc00e36f9277b46591ff4391250c36b5cb01d879be5d5950e5476cfd52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:29:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 02:29:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 02:29:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 02:29:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 02:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 02:36:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 02:36:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:07:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:16:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:16:12 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:16:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:19:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:19:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:19:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:19:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:19:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:19:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:19:45 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:19:46 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 06:06:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:06:27 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:06:29 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 06:06:30 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:31 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:32 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:35 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:36 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df684e328567a0a35db6301bcecffeb8c2ab6a69340a96db5d3e73a9fde3da`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbaaf99effdf014f4ce62ee67d7cf9f23205c645f22d554e6e925ef12ffcd70`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99838bf36837f5d2206ac07b2f399dca053921c575c4e9ea8fce917f1672383a`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce00e1e2d33cde79543bc9b4fa5d33fd33d9c5ad181c2530de4700e933322a`  
		Last Modified: Fri, 24 Jan 2020 02:48:36 GMT  
		Size: 12.3 MB (12327133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5773abc403eb88d8a6b65b76101051c21a8825f96d998431948fd5391c32012a`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7f54b41d689d5a8e23cb78d3e733b08c3bced9670b452956e90753e4d57c`  
		Last Modified: Fri, 24 Jan 2020 02:48:38 GMT  
		Size: 14.4 MB (14397481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf3229c4d684db86fe9b5be5052fb6393fd9f48e91ef859d65c2f882d5e517d`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc35742ac6688b780aa26a568715c2901344953a81392f59c56be42c21e49b`  
		Last Modified: Fri, 24 Jan 2020 02:48:34 GMT  
		Size: 72.5 KB (72452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0781411d60db178aca22f04381dce10aca4d91bfa5ac3b13146449990c27b56`  
		Last Modified: Fri, 24 Jan 2020 02:48:33 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37c111e33c1155179a3884270ad7ee4b6246834506e4a36b1f3f1dd9127cf03`  
		Last Modified: Fri, 24 Jan 2020 06:07:41 GMT  
		Size: 356.9 KB (356883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0b8b4be1be2f8f92c2cdc7fd340a75fa74dd88f6f86a2684ff4dafbb514b7d`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e1aa73768ce7fa0bc7ab72ff8c0e04abf383612019b88430cdffbcd0e37e04`  
		Last Modified: Fri, 24 Jan 2020 06:07:40 GMT  
		Size: 623.5 KB (623521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d92bd5108cc579bd3c931353ddc5793940e6445144797c3c6f9298d8d40b9f`  
		Last Modified: Thu, 30 Jan 2020 01:44:19 GMT  
		Size: 2.5 MB (2485260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3832f13fecf5270841416d14fc30e1b3a6a2c9881517ec51ccf82c78bb715e36`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ba2524bc062dc486296a8530bf1ffd9b04f70fc31ee7a306b8e678c46aec82`  
		Last Modified: Thu, 30 Jan 2020 01:44:18 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:325615cd344fe5aa9772e751abf97604e8c4e438c52dc33540286282aa4087d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35246922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c93ad9c8973b4cca340b0c5e9fb63ffe2223d9654cff7d6b497bb0a8176e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:41:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:41:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:41:37 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:41:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:41:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 06:32:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:04 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:08:55 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:08:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:08:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:08:57 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:08:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:08:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:08:58 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:08:58 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 08:21:08 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:21:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:21:10 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 08:21:10 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:25 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:27 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:27 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686b8c2d7ff02237fc9b12daa86e7e7328b7031b6585a20cd6b5fd618f77486`  
		Last Modified: Sat, 18 Jan 2020 06:45:55 GMT  
		Size: 1.5 MB (1452582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564ce419d6f56887ea2bd9699c37517ecd579e747f1a2698e764ad6f74e66b4c`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ef48cddae433ef86445fc9786eb75673c1c0c6d903fd7a81b2c56fb7e1b86`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5702c4bff7a894a50017cb8d26ad237f05b3ce8373acf4a23ec5c471a226f7fd`  
		Last Modified: Fri, 24 Jan 2020 02:45:37 GMT  
		Size: 12.3 MB (12327121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6363df2f3e95a21deb5655ca3c0d5727eccec7a1a2327754438d4cfb07ecab09`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7e156b40f3210869a4fc5514a09eff0486bbaffc00a9f0074fd968dc1d2d2`  
		Last Modified: Fri, 24 Jan 2020 02:45:39 GMT  
		Size: 15.1 MB (15060955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d80df17e2006212e3bfe404d01bca2ca12fb9a8236851996a44cedb8e549d7`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b10aa160d8af5bac5b5fe05bfc28fe59c62e16b29670d4172d4b5fd654a696a`  
		Last Modified: Fri, 24 Jan 2020 02:45:33 GMT  
		Size: 72.1 KB (72107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ef15b4c6b44395040e47685dc8146b8b721daaf7b1f759de9667a10aca86b`  
		Last Modified: Fri, 24 Jan 2020 02:45:34 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31f939f799f9b3cead96d77256a42cdf089781c26b983e4e176e680bd63ab`  
		Last Modified: Fri, 24 Jan 2020 08:22:02 GMT  
		Size: 374.1 KB (374066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b948106b58045ef1d7d0a85be08d79c9e02c4a5345260049ee6d0f67adfecb8`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f60158d6669b6b4c2ea0052c70b8a51ecabcc5ba00181a3f6f5168a13313eb`  
		Last Modified: Fri, 24 Jan 2020 08:22:01 GMT  
		Size: 653.1 KB (653110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41727753f258f4a95fee2912b0f62074ff23cccdde7bec37e8eb100b1780e046`  
		Last Modified: Thu, 30 Jan 2020 01:41:09 GMT  
		Size: 2.5 MB (2485234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f6690243e337d2d22c882d360e922dfe2a5cb0f1ef70aba83fb58de94c9d1`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec7bcd3e9beef800a28f552cfe5ecb3098a4058a9688db8914d9e1027c8c32b`  
		Last Modified: Thu, 30 Jan 2020 01:41:08 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:e9131ce7a4fa4df2d51acbfeec2067ab25fad3120250758ce3a07c7c9b2a92e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35846949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8fdb680cd660c07b3853ab66aab9f45f26a6440f7fbea93c49d15226245d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:24:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:24:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:24:20 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:24:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:29:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:59:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 02:03:11 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 02:03:14 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 02:03:16 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 02:03:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 02:03:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 02:07:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 02:07:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 02:07:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 02:07:44 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:07:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 02:07:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 02:07:53 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 02:07:56 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:56:22 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:56:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:56:33 GMT
RUN apk add --no-cache bash
# Fri, 24 Jan 2020 10:56:35 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:08 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:15 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:17 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:18 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccdcd97be351ef8da754f6efea3745b7060b1fe92ab96e4b8f5ff85b6322da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.4 MB (1397881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea78a138902aeee431e9b31b236dfea5d4f95a1e155aada946ca57f6650a4da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda899b5dd7be53564e6266c17b869d98468c50bc887279c51acacfa831de39f`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe788d20bfb24ce14df58fb94bd73b55687fd6de6afe42325ab1c44ba587cd3`  
		Last Modified: Fri, 24 Jan 2020 02:48:03 GMT  
		Size: 12.3 MB (12327146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae871526dcb6454acaf782bee3e5d631535828619bcbc4123867a07ee9505e`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e1fbe9be3ef95e0870d1590a81311ea511056b80639f4c7e7fcee4f01d403c`  
		Last Modified: Fri, 24 Jan 2020 02:48:04 GMT  
		Size: 15.7 MB (15654284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a7980c3234632f6f8e701aac524333a6f1c0ad5edaca10a2706868ac22f7ae`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6daa4d8c7d908b6559e4509800bcb0a9e1f094166a268352ef36abcf2de77`  
		Last Modified: Fri, 24 Jan 2020 02:47:47 GMT  
		Size: 72.8 KB (72783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d52f0dd733a2a7fc154f9816e9c5c013e2d6999a2a1ba9f8f4a769e28703270`  
		Last Modified: Fri, 24 Jan 2020 02:47:46 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb531ca214ceade639ebd05f1b5f2dc085fe551a38afa2c9fb8d55c257b4f74`  
		Last Modified: Fri, 24 Jan 2020 10:58:35 GMT  
		Size: 394.2 KB (394241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ee59a808dcb66b0696e608e9714fe00b8b28efffb4818c8dcbfd74fc3b9546`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264bbe1b482b9b77c5496fb4f8070f2b495cef65fc2c22efab5f67a3c522c8a`  
		Last Modified: Fri, 24 Jan 2020 10:58:32 GMT  
		Size: 678.0 KB (677963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fccad52f0230ba6f70840d2bb4aeeaab419fac2d991d223c3879a7113a97969`  
		Last Modified: Thu, 30 Jan 2020 02:22:35 GMT  
		Size: 2.5 MB (2485257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a872189e6112212034ca7fd0a912804de4b84a897c6c39788e42b91a5074e7b2`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5421523593548014784c4c9fb616a133a4f389801be8831b77ef3ea673e3d89`  
		Last Modified: Thu, 30 Jan 2020 02:22:34 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `yourls:latest`

```console
$ docker pull yourls@sha256:d3a7c04eea5a4735c18f80cf9efb7144282bf2fd04a6470ef2d9121be4f29102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:92fb12c683fa4a62a68c5f2902caad4c5eee9cfa1f0b8cb4d2ee29b73fe3424b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eac9b8188887b8587138417329ad10a460f1a163768787892104e13fae832f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 20:39:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 20:39:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 20:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 20:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 20:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 20:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 20:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 20:46:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 20:46:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 20:46:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 20:46:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 22:06:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 09:18:35 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 09:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 09:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 09:21:50 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 09:21:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 09:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 09:21:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 09:21:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:21:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 09:21:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 09:21:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:50:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:50:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:50:03 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:50:03 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:21:29 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:21:31 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:21:31 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:21:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf4fc8647872d4db40c6957c1a7cfefd3bcb785281f88762706926c307c56c`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970dadf4ccb644b7e193c317c67e6002c9b1386a99e062c2d67dd089625c64ec`  
		Last Modified: Sat, 28 Dec 2019 22:53:59 GMT  
		Size: 76.7 MB (76651636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04561117a4645551bc4379b1eebdc32e178a61d11c5db8d79f2658178f6639`  
		Last Modified: Sat, 28 Dec 2019 22:53:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7434b63a246cff24e7a3d2310de1b31f04f89af889acda1a1aabb53c299c5`  
		Last Modified: Sat, 28 Dec 2019 22:54:19 GMT  
		Size: 18.7 MB (18675679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d8859e9744116aa6e790b787a05a0ec71230f107ecd511b7fd2f299ca91e55`  
		Last Modified: Sat, 28 Dec 2019 22:54:15 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3d824d0ad5a0258fd7214a6e3faef915791d37af27b7afe0e59ba28c86f884`  
		Last Modified: Sat, 28 Dec 2019 22:54:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf151d73a83027f8fb21515f810bb56f9cd310b4c693090f26e887638b3f8c8`  
		Last Modified: Fri, 24 Jan 2020 10:46:08 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1780495b139a3125f0a8525eff5bd9fd2678db666976ae4fc0db7da9282ec`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8acdee7575085d4185a179cc2bec5d7d81c6f0a39f2af3a94cdd3a1c429ec2`  
		Last Modified: Fri, 24 Jan 2020 10:46:14 GMT  
		Size: 13.8 MB (13841458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f795e28ee2aeaeaaa3bfebc960821c4e705dae019e300345aaab229778907`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4ecc29fc811c88c40bc121192a1934756d552580bae5f4fdad52be64fcd64`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc78403636b9b5b84ae82af9092efef2e94cd0f66fd802a8b3567da76a026f`  
		Last Modified: Fri, 24 Jan 2020 10:46:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6181179a3e436f30ebe83fb2ea7e696ed1870038c5acb9b88ba9f49c5ec6423a`  
		Last Modified: Fri, 24 Jan 2020 10:46:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491de560be070c91e122db618cf46f6a6b0f6376fb8cda957d9ce5344969acd9`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 291.7 KB (291689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e1c583071b32e1598c2170d81afdb4e04c1bb4f85e8db46148f5484663f78`  
		Last Modified: Fri, 24 Jan 2020 10:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6292925df4bd3808bc92277d9f71e49dbab9ca268030daeae11b07902472ec`  
		Last Modified: Fri, 24 Jan 2020 10:51:40 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca02b0449d081538188718e57f8f1347d4fe34c033c74e4723241239de93ffd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 2.5 MB (2485109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5251e8983263ef95c7c3590f758880e692ede180f055cfef925108bffb2ec2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df6c9d7424ec7c71a45c2f28c571440ee84350f19ef1d9bed85155f34309dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:54 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4242247f29bce3f1a330e99db74626eb7f8d1e540736c45c31cc1c0ab6768f2`  
		Last Modified: Thu, 30 Jan 2020 02:21:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9352d644921c1b6a77b90a2f1528e4e9e471a2f10a3b5f2673405138e9de3cc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129982858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed566f0e144e56ffd1056a0d45287f619cb5c47c5211108a2596610abd94c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:49:50 GMT
ADD file:5d34c769f80c3fdbb04048f4336cf212164934607a642144ef557faef5896192 in / 
# Sat, 28 Dec 2019 04:49:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 11:46:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 11:46:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 11:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 11:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 11:46:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 11:51:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 11:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 11:52:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 11:52:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 11:52:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 11:52:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 11:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 12:45:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 21:28:17 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 21:28:18 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 21:28:19 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 21:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 21:28:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 21:31:55 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:31:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 21:31:59 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 21:31:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 21:32:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 21:32:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 21:32:02 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 21:32:02 GMT
EXPOSE 80
# Thu, 23 Jan 2020 21:32:03 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 00:04:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 00:04:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 00:04:30 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 00:04:31 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:48:32 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:48:33 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:48:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:48:37 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:48:38 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:48:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:153ccec980772b5fc4c786af0b26bba09f0a2d95d9755400febf9a79aa4220c8`  
		Last Modified: Sat, 28 Dec 2019 04:56:28 GMT  
		Size: 24.8 MB (24829618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb31ffad3b14d29eb4441c87b0f3a709311362013f6cb7af3b9a08356e3f54b`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c480440b3d2ffec23c2715bc1a23b63727a2cd4ec16dba2a4b8092960d29408`  
		Last Modified: Sat, 28 Dec 2019 13:15:33 GMT  
		Size: 58.8 MB (58799289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b6d7351fa8842e4f35ee4f387772cef51f2b0371e8426fc5fda008f66f6c1`  
		Last Modified: Sat, 28 Dec 2019 13:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da5e5fa374e831ba6fecd4fd0f4cb996d6f225cfdb539ca67b782016c3d6e97`  
		Last Modified: Sat, 28 Dec 2019 13:16:06 GMT  
		Size: 18.0 MB (18024381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82722248cd3cc009d44e401aae5b794d5f29a6dd09448f81b669b2177f10eb52`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb194a191156ae4e4b8f5be5ffd2b156ccea22cec6c79ead9b26d6a78ce698f`  
		Last Modified: Sat, 28 Dec 2019 13:16:00 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2617be9432165f4ff50def4500ca5fcf541952391f0a5d4df67701bc394d2`  
		Last Modified: Thu, 23 Jan 2020 22:08:58 GMT  
		Size: 12.6 MB (12643254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8551c3f5356bf3cfa0a66e3855a0efe8066fe7e70afa47dff31910b97c986848`  
		Last Modified: Thu, 23 Jan 2020 22:08:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729b7434145feec1c3d5e04f80e1c1e86d9e3e52bf329654c9e522b77de3e3b`  
		Last Modified: Thu, 23 Jan 2020 22:08:55 GMT  
		Size: 12.9 MB (12916666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b334636761919b50da4d1829bfaa0354494d1b74a4685041f786014c80cbf5`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3b4973e24f949da38cb81cd021c43453b3836f4745a762576934f89f0eedf4`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07b9ab9698f568ba92711f2374a519a4b890fd3eada0b0094b4d69ab1e53891`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b083b324bc21fe14166b4df6df5698a848059740fab4c17079e43447727cc`  
		Last Modified: Thu, 23 Jan 2020 22:08:45 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b921cc7e3cc1e45ecc50931195cb692b152a5aa42c7fae509c5ba4756b66544e`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 275.0 KB (275007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87351119a267bd8ad5976c1a471b75d6f975494cd395ddd307cb23cab228e24d`  
		Last Modified: Fri, 24 Jan 2020 00:06:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f993c64cc7053fba7d5c10deed461485f164a1feb75a20cf9a88d5a965369c`  
		Last Modified: Fri, 24 Jan 2020 00:06:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e8326e889f7ca6f32c8e24014192a50f953c9c61404cdb37539af39570acd0`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074e0f9d0de89ec914c1a033fcfcf7463fe573244c898d6eaf6dc014e460ba0a`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c9b57632175f661e60c4ae504b5a10654e6f13575ded276879b6ac4d19205`  
		Last Modified: Thu, 30 Jan 2020 01:49:09 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90555763aaf5f3c8c3dd04ef915bd4ae3792b189566b0bea483d66642b5d463`  
		Last Modified: Thu, 30 Jan 2020 01:49:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:d4455e9b7d82bebb4b70d4a13d5d91c0ef405d512f4d43d80b316c9588e472bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127254262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9409fb783243e5db5a390ba6ab10ac486970c78f54411d1a624749ae038b490c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:41:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 15:41:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 15:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 15:42:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 15:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 15:46:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 15:46:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 15:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 15:47:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 15:47:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 15:47:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 15:47:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 15:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 16:39:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Jan 2020 22:47:29 GMT
ENV PHP_VERSION=7.2.27
# Thu, 23 Jan 2020 22:47:30 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 22:47:31 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Thu, 23 Jan 2020 22:47:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jan 2020 22:47:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 22:50:46 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 22:50:51 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Jan 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 22:50:53 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jan 2020 22:50:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jan 2020 22:50:56 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 22:50:57 GMT
EXPOSE 80
# Thu, 23 Jan 2020 22:50:58 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:36:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:36:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:36:27 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:36:28 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:01:49 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:01:50 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:01:53 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:01:54 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:01:55 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:01:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b9b291ff1c8a76bfb2a542028eab868cdfeb8f7ce1b2816a2dd685bead53a7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aadbe9ebf4298c5a6e9a9970ebfda7d6fcee35b1a30de8ee56d0a5ba5d12306`  
		Last Modified: Sat, 28 Dec 2019 17:10:35 GMT  
		Size: 59.5 MB (59500969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f0f0a98e4a0343fb0ce2b3ee95aef4a695335ed00d7585878a052385fdac7`  
		Last Modified: Sat, 28 Dec 2019 17:10:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9280131d10e0a4bccd45d145fee5637ab0e0765ab559dd1e2b5dc7af27750c0`  
		Last Modified: Sat, 28 Dec 2019 17:11:09 GMT  
		Size: 17.5 MB (17482411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1816edc9dd5b62a2a48c193080b5268ad8c008bbe3ddca391d0b04f76205f7`  
		Last Modified: Sat, 28 Dec 2019 17:11:04 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfad187f0b662b320dd69ffc0f6f8dfd3f3802162529030831c885da10cfde8`  
		Last Modified: Sat, 28 Dec 2019 17:11:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26805bc203948aadeda056d2e497902da6f7228ca9e003b74e3bb86f95203b5f`  
		Last Modified: Thu, 23 Jan 2020 23:49:43 GMT  
		Size: 12.6 MB (12643304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba73644e5534d433ffb0dd19ca67d76d1fb18a3d80c2459736d7a7b27d65e340`  
		Last Modified: Thu, 23 Jan 2020 23:49:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef73dd928f58380ae9e7d2092eb19addd41c6c8619fb387e7e67e7ea588c9b0`  
		Last Modified: Thu, 23 Jan 2020 23:49:46 GMT  
		Size: 12.2 MB (12186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d7e8782f8b61fe94c322abf2f7b727c171321fa9ca9c1e9c7d063920ea717c`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97c1c88db50814d265515a25406e833647256a6da41bd415359764756f7b02`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92122c7c67a28259ca66bc51a4fc3ac5fc33167c8fc6ce3e2c8d39f7e59f9ed`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87303932048be5e3a37d4be810a5fdf3890d2448457e93fae62d729a07668b81`  
		Last Modified: Thu, 23 Jan 2020 23:49:40 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3a86c0e07a3fee46310c84a68d24e0ee180a75c0b102b8ccfdae88554a46d6`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 247.7 KB (247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb5f52dcb5320a4f6cea422c7fbc09ef040df69ff7ff81dfc0f22226b52067`  
		Last Modified: Fri, 24 Jan 2020 06:39:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eee0be3a1a1a72af057c1366f2fbceb6cdf7b96a275bccc5fa7396689113c9`  
		Last Modified: Fri, 24 Jan 2020 06:39:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbd6f37db1211f539bda88ad43ed582d5f18a92d3a2c9bacd945bfd9ca7d047`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ea7b6cbbaba1d1212ce3e80f2996a772870ef2debf6067cc531175d0e9544`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fb5d3c67da5ef1715d798d0b931a9aba62d00a49ea6786d8d1048c0b9b2844`  
		Last Modified: Thu, 30 Jan 2020 02:02:45 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3dfa51662546945b3572d02dd8df72aebc3c2013bbe7f06a62205f0b7b1d3`  
		Last Modified: Thu, 30 Jan 2020 02:02:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:c4595a794befe747464753b9f259ca01bea6da7268695250ab590b108d30defd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143723211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ad64d69ae061110d85f11f512e046ac6976065c38899a11d55ce2c89f45a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:34:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 14:34:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 14:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:35:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 14:35:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 14:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 14:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 14:40:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 14:40:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 14:40:20 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 14:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 14:40:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 15:33:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:40:45 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:40:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:40:48 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:41:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:44:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:44:29 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:44:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:44:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:44:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:44:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:44:32 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:44:33 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 06:04:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 06:04:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 06:04:26 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 06:04:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:43:05 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:43:06 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:43:10 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:43:10 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:43:11 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:43:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122173c172bc43784f104fb71aa1776a8615c131c729e70f550881523035d01`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77da451916b9bf0e21115b77fe13d76cc5ba92ffb452241f98f1f6da974c366`  
		Last Modified: Sat, 28 Dec 2019 16:07:56 GMT  
		Size: 70.3 MB (70335271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b031d86c7e7fc5c4c1f9be702b575c168ca6c602d89158e2a8bade9abe3c594c`  
		Last Modified: Sat, 28 Dec 2019 16:07:36 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ff20e5dfef45f1afca83759a318399f8a81e1aaba22b5307be488d2e1fbe81`  
		Last Modified: Sat, 28 Dec 2019 16:08:27 GMT  
		Size: 18.6 MB (18577647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e3077408b6e8030226b0ce72eea3a01b0bc0f1f4ebe1a2154e42f9ce2a84a`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090a390778cfa9720209069fb2b3ed504f255d2111e8ffdd7f986fa5fc96f2c`  
		Last Modified: Sat, 28 Dec 2019 16:08:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7fc8c1fada43905a4585b80be6a7f59869e0ac0c9cb19c6eac0ea64e5b6ac`  
		Last Modified: Fri, 24 Jan 2020 02:46:00 GMT  
		Size: 12.6 MB (12643956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe29be43e659f1f638ce2c0483d3b46a0c0b583f249332d771c31de1ce08398d`  
		Last Modified: Fri, 24 Jan 2020 02:45:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11b5e345703533b6aa87455cd5a451296df2c2f89d39ac226b9c04c648a523`  
		Last Modified: Fri, 24 Jan 2020 02:45:59 GMT  
		Size: 13.5 MB (13536725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec7bb197a5baf1d68c4d209daf5481a9da3c07d1b2d002c3b7579b27db6c8c`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf686e3c7140108f25fd643a0fef4a051ca43e68996f2e5f9846300656c72dbe`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e965c71c71193919e403147dde3b8ecef249fb12c1013c9d566068bd42036417`  
		Last Modified: Fri, 24 Jan 2020 02:45:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1787b9e736d36586a1d51fe2f516f1c04a5862c67aad27e65eaf8d8a0994cb`  
		Last Modified: Fri, 24 Jan 2020 02:45:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91413f393e85dfa0979ee6360a5ce5d5f674499f68eb713e4af5cfe7b70323`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 284.3 KB (284281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a610336db445ccc5fe5e6587190c6b98a803af22662c24774321531f8e2ea6b`  
		Last Modified: Fri, 24 Jan 2020 06:07:03 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7627c5405d4e1996ffb7ff795037d08730195f256f4d94e68a0d78c19f30d`  
		Last Modified: Fri, 24 Jan 2020 06:07:01 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94bd8f9ae3374cddf057dd455dfa7a7a0658fe7e523cbc2ab33b48c4d7c6b0`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 2.5 MB (2485140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43b9bc475aa06e3a62a460e8e2c844219e356107a14a66755c5a800c0afe53`  
		Last Modified: Thu, 30 Jan 2020 01:43:51 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9272987213dd62084dd3516ab220944697633ce5ae10319c320e73f8779245`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd06b51008c4480615fe9168395d288bb4a63788f4a3ac43904d0b532c1b99a`  
		Last Modified: Thu, 30 Jan 2020 01:43:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:00ca3bf4e5f47f499fc7e0052d1a1d5494d0be04a089ba5c00437583a9bc36e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157666949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b065b9aac57a8cbb9ceb2538d6f87f4dcdaa29ec163a55876884726898595cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 16:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 16:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 16:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 16:47:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 16:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 16:56:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 16:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 16:56:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 16:56:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 16:56:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 18:36:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:21:22 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:21:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:24:51 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:24:52 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:24:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:24:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:24:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:24:53 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:24:53 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:24:53 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 08:19:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 08:19:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 08:19:49 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 08:19:49 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 01:40:11 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 01:40:12 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 01:40:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 01:40:14 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 01:40:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7834f8ef235a445001f7975675aa8af1b872e0c7104ce978c07e59dc443dbec`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81a6f724259f2ff6a49a67e0c30d55830e1534058351fab438c06d13a8170f`  
		Last Modified: Sat, 28 Dec 2019 19:32:45 GMT  
		Size: 81.2 MB (81199517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75064f0106e77c164ad954ecae2c728eb2076867d32fb11b447d14dfa02dd3e5`  
		Last Modified: Sat, 28 Dec 2019 19:32:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40761e8229cc73d8ea7d9fa0d451565c5ff38066ac2546dea71211509b36dd4a`  
		Last Modified: Sat, 28 Dec 2019 19:33:12 GMT  
		Size: 19.1 MB (19111841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cebfb9b041b1fae88162028743c04818963a522ea14ea6b174dbad195c9a41`  
		Last Modified: Sat, 28 Dec 2019 19:33:06 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ce68c003e5a9a03fd4b11879aeb24cfb5559217d3ed022d06647f6b95e306`  
		Last Modified: Sat, 28 Dec 2019 19:33:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a9dec9dd465490f7f776a70b6d7fcc0c9ed93f140fc83b5c250d25b904ffa`  
		Last Modified: Fri, 24 Jan 2020 02:43:09 GMT  
		Size: 12.6 MB (12644533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe7ed6407f9b24b8a8bd7a12731077682c3d7ffee99ff882d73b8770ca5ee8`  
		Last Modified: Fri, 24 Jan 2020 02:43:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b6c401772c47c170a9440f58cba6e4406358f512dcb232cdb08b678a5f7ce`  
		Last Modified: Fri, 24 Jan 2020 02:43:11 GMT  
		Size: 14.2 MB (14169213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d922f9bf8ab41f0c5e6af77b6aad6a7ce282bbcf687fdbfd1ab510fc2cb07`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259b0b395d5aeae0ff321de169aa51d94be1414b1e4754d352da2753e619ef8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a89431fcf33a2d103d3373ec3822ccf6baed58f301cbaa72e70ac9110caff8`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f0051d00d58f456c22927f124b8724b600be621cd34abcd4ac547aa80d7a33`  
		Last Modified: Fri, 24 Jan 2020 02:42:59 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808dbc43ca157aeb6d01216843e1a5d746c536709baca3373b00731b5db8d88a`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 300.3 KB (300338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbcd4cf4a1d2e1bc7838454ba20e3072704895c1e50c5548356d208729afda6`  
		Last Modified: Fri, 24 Jan 2020 08:21:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc60daaaa48c73f4aa662e6e4bcd71eb6440137db1892fbbd74c1c4c0dfa0ab`  
		Last Modified: Fri, 24 Jan 2020 08:21:33 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a47a36b3457f73ab5dee95cab12e71da9504db23c4bb2b8dcf1a1885de069`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 2.5 MB (2485108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d695e338b033df85d44dfaaf0b8ac68aa417bc17dd96041aa20b83ca2e2085f5`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee85b2db945ead73c036e5153043986bc57e2958c011403a1e4bc82fa72c3f0`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa638c21112027d30e36ebafaedafc3e52f79727561d32b7e8ee9c4a0b66ae`  
		Last Modified: Thu, 30 Jan 2020 01:40:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:8fd384737ee60d8753316647cd5a9b62170542e3e6272f3fa401fa4381afb5f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162933681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1752ab53d28bdd97b198c94cccf755be3205f84e3e8f483cb769b1d773cebd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 10:53:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 24 Jan 2020 10:54:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:54:07 GMT
RUN a2enmod rewrite expires
# Fri, 24 Jan 2020 10:54:08 GMT
VOLUME [/var/www/html]
# Thu, 30 Jan 2020 02:19:57 GMT
ENV YOURLS_VERSION=1.7.5
# Thu, 30 Jan 2020 02:20:00 GMT
ENV YOURLS_SHA256=e8251bc99def425f647577b066d3489725a3cefde7a72f83ceab0b68e9910e9c
# Thu, 30 Jan 2020 02:20:09 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 30 Jan 2020 02:20:11 GMT
COPY file:dae29f9c1e1fe04a79abdb2b0965f1a821bebbe26ab1e1e13cae7fe5fbaf788d in /usr/local/bin/ 
# Thu, 30 Jan 2020 02:20:12 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 30 Jan 2020 02:20:13 GMT
COPY file:5b7ff05d0c98ad759c4bec0ef8a7ce74cae42e95b42564b55f43b341c2c3e3f5 in /usr/src/yourls/ 
# Thu, 30 Jan 2020 02:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jan 2020 02:20:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ba1b75a2ffe35d3e561f94ad704ffe2bd6d9bfeddb8e972a9374ccdf908d1e`  
		Last Modified: Fri, 24 Jan 2020 10:57:32 GMT  
		Size: 322.8 KB (322759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d3b5d6e8c128dc31442fbc4b66958445033fb0be542a39d4e4cc105352dfd`  
		Last Modified: Fri, 24 Jan 2020 10:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3a5c10d55d18307d517df54588a5ea705739de22cb3db62178faf8cd14b6c`  
		Last Modified: Fri, 24 Jan 2020 10:57:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb83c59c3442b408d0ec458435f58032b19f4c7c7fbae7d06f992e61807299e4`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 2.5 MB (2485135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf7e24a28c21b24c127ad0f951902414c7e8f47943ec34105683b8720973dd`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d78205fbcfecf64c9d116cfcef47ffb4113705424417440cfba1c4a27423c`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cfecbe86fb33211add4d29a6042124150112922bd7183355034f9fad7c502`  
		Last Modified: Thu, 30 Jan 2020 02:21:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
