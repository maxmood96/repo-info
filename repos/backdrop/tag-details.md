<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.25`](#backdrop125)
-	[`backdrop:1.25-apache`](#backdrop125-apache)
-	[`backdrop:1.25-fpm`](#backdrop125-fpm)
-	[`backdrop:1.25.1`](#backdrop1251)
-	[`backdrop:1.25.1-apache`](#backdrop1251-apache)
-	[`backdrop:1.25.1-fpm`](#backdrop1251-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:5f20befd411991f5c9dcc7126237a7f2910cb9a11624f2c5ca282513a9aaa782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0478cf3d2c9aa3a7c57f73bfae12c609cd01fa2d57f66f491746e320d2e4b5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174512768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b4d130d7ab8d4ec15847515e3e355d52270de8e46dc6912351e8deb3ec50f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:03:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:59:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 00:59:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:09:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:09:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:09:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:09:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:09:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:09:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 04:01:25 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:01:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:01:28 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:01:28 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:01:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94fcedaefe080e3ed1e2e8ff76be549d4d7be1b0596bc0e335b9d33d90bcd4e`  
		Last Modified: Fri, 09 Jun 2023 02:48:42 GMT  
		Size: 12.1 MB (12111656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb3c7d20542ec78b2e2b74f29914cc2963e57a22ddf3d4a5ac0843812ce2d5d`  
		Last Modified: Fri, 09 Jun 2023 02:48:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc87360a828e1367c389850baf810f08991cac8a0aae7cefee87920d2a56120`  
		Last Modified: Fri, 09 Jun 2023 02:49:28 GMT  
		Size: 28.2 MB (28159707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9636b80dd5c47b9a90ebf426e2584205d3f5f8640f4ed18ed88822fafc7dd1cd`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556a07c48dd9765dbd516a557012b8da81b71cfa97649840e3e8bd394b6092f`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e0f4ff9411d92b72cb7193867ab206d7adbaa91c85fc463535d1faf54cd77`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ad6265ffb81f0acc292ce8905ee10a19647bc9f0fdb99976ffe16e656a534`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 2.4 MB (2422856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35525a5c29bbd7a3d75b931913cbb20c3ea55bfb396d9ab51e0b44cd1c175eab`  
		Last Modified: Fri, 09 Jun 2023 04:02:15 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc5ed8d332ebd499de1cc5ca6d17678dcc6379a3f621d4bf2422abf6c1b9594`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:34417d7868f201e40d518cebd2fbf8cd8249e0a3ae675094a765ce9127a6fb56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166556146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51af6351a70a4162931d5d520945770da696cf754054f393a09e19b1052f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:18:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:27:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:27:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 13 Jun 2023 09:27:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jun 2023 09:27:05 GMT
EXPOSE 9000
# Tue, 13 Jun 2023 09:27:05 GMT
CMD ["php-fpm"]
# Tue, 13 Jun 2023 19:09:30 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:09:30 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:09:33 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:09:33 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:09:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:09:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057240c114d62c093225ecb2f25e1fb120d14d85d1ae5ffebcbf3235a060f639`  
		Last Modified: Tue, 13 Jun 2023 10:07:22 GMT  
		Size: 12.1 MB (12110892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261cdaf3dea02295e9b652f0a6e24217fa30b46c56137b29556d72355ccf37bb`  
		Last Modified: Tue, 13 Jun 2023 10:07:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9667c550c5b773eae15d1d8286dbf153b0970f8e3faaf5989e8cb8af60fa1e7e`  
		Last Modified: Tue, 13 Jun 2023 10:08:03 GMT  
		Size: 26.3 MB (26289957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bd8b43a56a5ba574db217ae164bf8d0c5b1f1807909f6d020f760389cf4da3`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8edcfd607aa0599182b1c27bb0b11ae99f227fd3c81fdf8ce3e1e42a0de84f`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389016bdc7b75157113a00b89a23ac21dfa9197d65ecb6fa81f1742ff1e27d45`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66003234794732c9b9029059a3551949ff32f8cb6c267937828ea98cc4efa76`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 2.4 MB (2384896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d523a2b4c34cd9649c633e56f3ef2ae01b39f151d302d4c5e6f82e068615ab`  
		Last Modified: Tue, 13 Jun 2023 19:10:21 GMT  
		Size: 8.8 MB (8765744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398e269f3cab8cbb1c467d7120dc7f89a45405717a22d559ec83e6c8e5a50fa`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25-apache`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25-fpm`

```console
$ docker pull backdrop@sha256:5f20befd411991f5c9dcc7126237a7f2910cb9a11624f2c5ca282513a9aaa782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0478cf3d2c9aa3a7c57f73bfae12c609cd01fa2d57f66f491746e320d2e4b5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174512768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b4d130d7ab8d4ec15847515e3e355d52270de8e46dc6912351e8deb3ec50f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:03:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:59:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 00:59:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:09:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:09:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:09:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:09:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:09:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:09:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 04:01:25 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:01:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:01:28 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:01:28 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:01:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94fcedaefe080e3ed1e2e8ff76be549d4d7be1b0596bc0e335b9d33d90bcd4e`  
		Last Modified: Fri, 09 Jun 2023 02:48:42 GMT  
		Size: 12.1 MB (12111656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb3c7d20542ec78b2e2b74f29914cc2963e57a22ddf3d4a5ac0843812ce2d5d`  
		Last Modified: Fri, 09 Jun 2023 02:48:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc87360a828e1367c389850baf810f08991cac8a0aae7cefee87920d2a56120`  
		Last Modified: Fri, 09 Jun 2023 02:49:28 GMT  
		Size: 28.2 MB (28159707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9636b80dd5c47b9a90ebf426e2584205d3f5f8640f4ed18ed88822fafc7dd1cd`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556a07c48dd9765dbd516a557012b8da81b71cfa97649840e3e8bd394b6092f`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e0f4ff9411d92b72cb7193867ab206d7adbaa91c85fc463535d1faf54cd77`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ad6265ffb81f0acc292ce8905ee10a19647bc9f0fdb99976ffe16e656a534`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 2.4 MB (2422856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35525a5c29bbd7a3d75b931913cbb20c3ea55bfb396d9ab51e0b44cd1c175eab`  
		Last Modified: Fri, 09 Jun 2023 04:02:15 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc5ed8d332ebd499de1cc5ca6d17678dcc6379a3f621d4bf2422abf6c1b9594`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:34417d7868f201e40d518cebd2fbf8cd8249e0a3ae675094a765ce9127a6fb56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166556146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51af6351a70a4162931d5d520945770da696cf754054f393a09e19b1052f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:18:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:27:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:27:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 13 Jun 2023 09:27:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jun 2023 09:27:05 GMT
EXPOSE 9000
# Tue, 13 Jun 2023 09:27:05 GMT
CMD ["php-fpm"]
# Tue, 13 Jun 2023 19:09:30 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:09:30 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:09:33 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:09:33 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:09:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:09:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057240c114d62c093225ecb2f25e1fb120d14d85d1ae5ffebcbf3235a060f639`  
		Last Modified: Tue, 13 Jun 2023 10:07:22 GMT  
		Size: 12.1 MB (12110892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261cdaf3dea02295e9b652f0a6e24217fa30b46c56137b29556d72355ccf37bb`  
		Last Modified: Tue, 13 Jun 2023 10:07:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9667c550c5b773eae15d1d8286dbf153b0970f8e3faaf5989e8cb8af60fa1e7e`  
		Last Modified: Tue, 13 Jun 2023 10:08:03 GMT  
		Size: 26.3 MB (26289957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bd8b43a56a5ba574db217ae164bf8d0c5b1f1807909f6d020f760389cf4da3`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8edcfd607aa0599182b1c27bb0b11ae99f227fd3c81fdf8ce3e1e42a0de84f`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389016bdc7b75157113a00b89a23ac21dfa9197d65ecb6fa81f1742ff1e27d45`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66003234794732c9b9029059a3551949ff32f8cb6c267937828ea98cc4efa76`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 2.4 MB (2384896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d523a2b4c34cd9649c633e56f3ef2ae01b39f151d302d4c5e6f82e068615ab`  
		Last Modified: Tue, 13 Jun 2023 19:10:21 GMT  
		Size: 8.8 MB (8765744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398e269f3cab8cbb1c467d7120dc7f89a45405717a22d559ec83e6c8e5a50fa`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25.1`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25.1` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25.1-apache`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.25.1-fpm`

```console
$ docker pull backdrop@sha256:5f20befd411991f5c9dcc7126237a7f2910cb9a11624f2c5ca282513a9aaa782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.25.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0478cf3d2c9aa3a7c57f73bfae12c609cd01fa2d57f66f491746e320d2e4b5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174512768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b4d130d7ab8d4ec15847515e3e355d52270de8e46dc6912351e8deb3ec50f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:03:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:59:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 00:59:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:09:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:09:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:09:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:09:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:09:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:09:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 04:01:25 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:01:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:01:28 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:01:28 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:01:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94fcedaefe080e3ed1e2e8ff76be549d4d7be1b0596bc0e335b9d33d90bcd4e`  
		Last Modified: Fri, 09 Jun 2023 02:48:42 GMT  
		Size: 12.1 MB (12111656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb3c7d20542ec78b2e2b74f29914cc2963e57a22ddf3d4a5ac0843812ce2d5d`  
		Last Modified: Fri, 09 Jun 2023 02:48:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc87360a828e1367c389850baf810f08991cac8a0aae7cefee87920d2a56120`  
		Last Modified: Fri, 09 Jun 2023 02:49:28 GMT  
		Size: 28.2 MB (28159707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9636b80dd5c47b9a90ebf426e2584205d3f5f8640f4ed18ed88822fafc7dd1cd`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556a07c48dd9765dbd516a557012b8da81b71cfa97649840e3e8bd394b6092f`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e0f4ff9411d92b72cb7193867ab206d7adbaa91c85fc463535d1faf54cd77`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ad6265ffb81f0acc292ce8905ee10a19647bc9f0fdb99976ffe16e656a534`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 2.4 MB (2422856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35525a5c29bbd7a3d75b931913cbb20c3ea55bfb396d9ab51e0b44cd1c175eab`  
		Last Modified: Fri, 09 Jun 2023 04:02:15 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc5ed8d332ebd499de1cc5ca6d17678dcc6379a3f621d4bf2422abf6c1b9594`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.25.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:34417d7868f201e40d518cebd2fbf8cd8249e0a3ae675094a765ce9127a6fb56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166556146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51af6351a70a4162931d5d520945770da696cf754054f393a09e19b1052f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:18:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:27:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:27:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 13 Jun 2023 09:27:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jun 2023 09:27:05 GMT
EXPOSE 9000
# Tue, 13 Jun 2023 09:27:05 GMT
CMD ["php-fpm"]
# Tue, 13 Jun 2023 19:09:30 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:09:30 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:09:33 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:09:33 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:09:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:09:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057240c114d62c093225ecb2f25e1fb120d14d85d1ae5ffebcbf3235a060f639`  
		Last Modified: Tue, 13 Jun 2023 10:07:22 GMT  
		Size: 12.1 MB (12110892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261cdaf3dea02295e9b652f0a6e24217fa30b46c56137b29556d72355ccf37bb`  
		Last Modified: Tue, 13 Jun 2023 10:07:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9667c550c5b773eae15d1d8286dbf153b0970f8e3faaf5989e8cb8af60fa1e7e`  
		Last Modified: Tue, 13 Jun 2023 10:08:03 GMT  
		Size: 26.3 MB (26289957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bd8b43a56a5ba574db217ae164bf8d0c5b1f1807909f6d020f760389cf4da3`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8edcfd607aa0599182b1c27bb0b11ae99f227fd3c81fdf8ce3e1e42a0de84f`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389016bdc7b75157113a00b89a23ac21dfa9197d65ecb6fa81f1742ff1e27d45`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66003234794732c9b9029059a3551949ff32f8cb6c267937828ea98cc4efa76`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 2.4 MB (2384896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d523a2b4c34cd9649c633e56f3ef2ae01b39f151d302d4c5e6f82e068615ab`  
		Last Modified: Tue, 13 Jun 2023 19:10:21 GMT  
		Size: 8.8 MB (8765744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398e269f3cab8cbb1c467d7120dc7f89a45405717a22d559ec83e6c8e5a50fa`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:5f20befd411991f5c9dcc7126237a7f2910cb9a11624f2c5ca282513a9aaa782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0478cf3d2c9aa3a7c57f73bfae12c609cd01fa2d57f66f491746e320d2e4b5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174512768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b4d130d7ab8d4ec15847515e3e355d52270de8e46dc6912351e8deb3ec50f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:03:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:59:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 00:59:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:09:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:09:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:09:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:09:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:09:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:09:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 04:01:25 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:01:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:01:28 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:01:28 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:01:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94fcedaefe080e3ed1e2e8ff76be549d4d7be1b0596bc0e335b9d33d90bcd4e`  
		Last Modified: Fri, 09 Jun 2023 02:48:42 GMT  
		Size: 12.1 MB (12111656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb3c7d20542ec78b2e2b74f29914cc2963e57a22ddf3d4a5ac0843812ce2d5d`  
		Last Modified: Fri, 09 Jun 2023 02:48:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc87360a828e1367c389850baf810f08991cac8a0aae7cefee87920d2a56120`  
		Last Modified: Fri, 09 Jun 2023 02:49:28 GMT  
		Size: 28.2 MB (28159707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9636b80dd5c47b9a90ebf426e2584205d3f5f8640f4ed18ed88822fafc7dd1cd`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556a07c48dd9765dbd516a557012b8da81b71cfa97649840e3e8bd394b6092f`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e0f4ff9411d92b72cb7193867ab206d7adbaa91c85fc463535d1faf54cd77`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ad6265ffb81f0acc292ce8905ee10a19647bc9f0fdb99976ffe16e656a534`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 2.4 MB (2422856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35525a5c29bbd7a3d75b931913cbb20c3ea55bfb396d9ab51e0b44cd1c175eab`  
		Last Modified: Fri, 09 Jun 2023 04:02:15 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc5ed8d332ebd499de1cc5ca6d17678dcc6379a3f621d4bf2422abf6c1b9594`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:34417d7868f201e40d518cebd2fbf8cd8249e0a3ae675094a765ce9127a6fb56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166556146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51af6351a70a4162931d5d520945770da696cf754054f393a09e19b1052f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:18:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:27:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:27:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 13 Jun 2023 09:27:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jun 2023 09:27:05 GMT
EXPOSE 9000
# Tue, 13 Jun 2023 09:27:05 GMT
CMD ["php-fpm"]
# Tue, 13 Jun 2023 19:09:30 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:09:30 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:09:33 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:09:33 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:09:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:09:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057240c114d62c093225ecb2f25e1fb120d14d85d1ae5ffebcbf3235a060f639`  
		Last Modified: Tue, 13 Jun 2023 10:07:22 GMT  
		Size: 12.1 MB (12110892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261cdaf3dea02295e9b652f0a6e24217fa30b46c56137b29556d72355ccf37bb`  
		Last Modified: Tue, 13 Jun 2023 10:07:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9667c550c5b773eae15d1d8286dbf153b0970f8e3faaf5989e8cb8af60fa1e7e`  
		Last Modified: Tue, 13 Jun 2023 10:08:03 GMT  
		Size: 26.3 MB (26289957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bd8b43a56a5ba574db217ae164bf8d0c5b1f1807909f6d020f760389cf4da3`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8edcfd607aa0599182b1c27bb0b11ae99f227fd3c81fdf8ce3e1e42a0de84f`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389016bdc7b75157113a00b89a23ac21dfa9197d65ecb6fa81f1742ff1e27d45`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66003234794732c9b9029059a3551949ff32f8cb6c267937828ea98cc4efa76`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 2.4 MB (2384896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d523a2b4c34cd9649c633e56f3ef2ae01b39f151d302d4c5e6f82e068615ab`  
		Last Modified: Tue, 13 Jun 2023 19:10:21 GMT  
		Size: 8.8 MB (8765744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398e269f3cab8cbb1c467d7120dc7f89a45405717a22d559ec83e6c8e5a50fa`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:780b1b1a688051ff120901f5c84bb212e223b8b5a2843137beda7659410b29ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:4c6f31b49e560c9c96b702fb55c2ee0e1dde989e4a7ba6435c33febcff44b351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178379206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0dfa005ef865b942609a61979b941221e8c6298abe144ae871b33dfdfeaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 May 2023 09:39:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 May 2023 09:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 May 2023 09:40:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 May 2023 09:40:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:06:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 01:03:06 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 01:03:07 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 01:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 01:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:06:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:06:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:06:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jun 2023 01:06:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:06:22 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:06:22 GMT
EXPOSE 80
# Fri, 09 Jun 2023 01:06:22 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jun 2023 03:59:21 GMT
RUN a2enmod rewrite
# Fri, 09 Jun 2023 04:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:00:16 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:00:16 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:00:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:00:19 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:00:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:00:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd4f3005473f269daa0db0f8a5646dcf2eb5e0a0efa07d0795c22a99954142`  
		Last Modified: Tue, 23 May 2023 10:56:43 GMT  
		Size: 19.2 MB (19248074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edd0b2ea53b7699b610b88303af4b1956ab760c21793c6678ba81643db887f3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d310c971723f0499ce1fbe04fa8027295fb1296547d61bd882c5cde2e19d3`  
		Last Modified: Tue, 23 May 2023 10:56:40 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd78d2dd96d2a9cd3c44886ce33102bb0e918d67e5511e4342c1ccd16bb5bd6`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.1 MB (12133880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467952b811182f02c758a87062be1a7ae75f68f8ea84570d6c1ad876ab3a3b41`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc4a1919bd4c1d8adba1588f29852706e3793422dbaa3f92653b60228760f5`  
		Last Modified: Fri, 09 Jun 2023 02:49:10 GMT  
		Size: 12.8 MB (12761961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b9a0b967ba26266ef9ee18b2ab95a4c68700301dfdd1d3f2e9b5f3ef2c22a`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1acc73263c9e20e553fd735ab66f5fff949cfc532422bdf240e5b187e6138`  
		Last Modified: Fri, 09 Jun 2023 02:49:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b755a02003213298b6f852b45742a415487ad97037a27adcb43c0a87145948`  
		Last Modified: Fri, 09 Jun 2023 02:49:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1744648c0777b5149ca33625b5f9ccea4e5fc9a952312b89feb69fa50a39f`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce628c412c51a0c074dc994eb9158bade6f597786437caa22742aa42cf66fe3`  
		Last Modified: Fri, 09 Jun 2023 04:01:48 GMT  
		Size: 2.4 MB (2423430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce68b30573c3dc993d355bdd6a74ac16b053f4bf24eaa27e3b8a85f202e0a9`  
		Last Modified: Fri, 09 Jun 2023 04:01:50 GMT  
		Size: 8.8 MB (8765712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b042dc9d69f4f45c4f92f1efb865da2ed8ad7b29f1bc1d55f34fe38c6bb2f4d`  
		Last Modified: Fri, 09 Jun 2023 04:01:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:43cd1e2fb177f27c4f9df10ea4e45e7f9216f3e97fbd523b2264f8366a648395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170580631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9247d8de20f4945aed94bce7275f389080e0afa8219a4f1e36dcc1033a75cdd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jun 2023 08:30:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jun 2023 08:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Jun 2023 08:31:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Jun 2023 08:31:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:31:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:21:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:21:13 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:21:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:24:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:24:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:24:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jun 2023 09:24:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:24:11 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:24:11 GMT
EXPOSE 80
# Tue, 13 Jun 2023 09:24:11 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jun 2023 19:07:47 GMT
RUN a2enmod rewrite
# Tue, 13 Jun 2023 19:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:08:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:08:37 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:08:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:08:40 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:08:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:08:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e0c83c6e9b3007b02e28e0e163362c6a1706515d8e374b7fdc05cd5b080371`  
		Last Modified: Tue, 13 Jun 2023 10:02:22 GMT  
		Size: 19.2 MB (19170313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ce0ae66b9814fa2034d345f213aaa33e9eec7bd41c6e3afd4ae2a231e49a2`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c92b54532568efaf50554dbce9ae7574d668beb76ce816e4277a6bcc5cdb4b`  
		Last Modified: Tue, 13 Jun 2023 10:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57421a0a3f6eeb09644671df7d3be316eed910b30ea8d083ba86e3899e8cdd15`  
		Last Modified: Tue, 13 Jun 2023 10:07:48 GMT  
		Size: 12.1 MB (12133235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bbb16ed37ad0fee0897b9a86483560ebdb9b1670cac9b2c88c7801db45cbc`  
		Last Modified: Tue, 13 Jun 2023 10:07:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553637437de3ceaff17e7962452849ae19c0d3e53b14f4fd347e664e0e9a12e`  
		Last Modified: Tue, 13 Jun 2023 10:07:47 GMT  
		Size: 11.1 MB (11130641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f4041b5a3be47d55754913d2168e1811709870a3cc2f3763353618ad7deb1`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71a39ed048a8559a95dbb1b1203274fd475c8d0e6353f7f953f758f87b28f9c`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25141d6978cde121a1cbbc704bae4794b451ba8ff99dcd7a145a60cb6ca43fed`  
		Last Modified: Tue, 13 Jun 2023 10:07:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77004c2e7d019830aa50e0d45b5ef6aea345cddc3ef13fabb84794a19f7c843f`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd58dbc5aadeda1ca894bf062f1dc12e74ba770031baa68a774176923d3ede5`  
		Last Modified: Tue, 13 Jun 2023 19:09:52 GMT  
		Size: 2.4 MB (2382735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667904d0c404b23f74fd3d0bc1d19cb9a413b08243d6c3195489fb8a2d1e5d6`  
		Last Modified: Tue, 13 Jun 2023 19:09:53 GMT  
		Size: 8.8 MB (8765741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e33dd20f5f78abaa34574433a7b622232c00c46b88f2623873fb0930967119e`  
		Last Modified: Tue, 13 Jun 2023 19:09:51 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
