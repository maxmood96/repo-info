## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:50a00ba47d3e89608dfe2a82553ffc4b5d68ee760c575d6f2a5bd4785dd42e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:662b51e6e5d34b3f7aec25dadccbfa33ba0ebdf4926879dd53cbb67a854b34ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155942675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492f02aa2cede1706d92af90aa85af3a70749ead6e7967a5f36abd00de916403`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:34:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 16:34:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 16:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:34:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 16:34:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:45:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 18:07:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 18:07:06 GMT
ENV PHP_VERSION=7.2.30
# Thu, 07 May 2020 00:43:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.30.tar.xz.asc
# Thu, 07 May 2020 00:43:45 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 07 May 2020 00:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 May 2020 00:43:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 May 2020 00:52:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 07 May 2020 00:52:29 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 07 May 2020 00:52:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 May 2020 00:52:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 07 May 2020 00:52:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2020 00:52:33 GMT
WORKDIR /var/www/html
# Thu, 07 May 2020 00:52:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 07 May 2020 00:52:35 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2020 00:52:35 GMT
EXPOSE 9000
# Thu, 07 May 2020 00:52:35 GMT
CMD ["php-fpm"]
# Thu, 07 May 2020 03:23:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Thu, 07 May 2020 03:23:50 GMT
WORKDIR /var/www/html
# Thu, 07 May 2020 03:23:50 GMT
ENV BACKDROP_VERSION=1.13.2
# Thu, 07 May 2020 03:23:51 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Thu, 07 May 2020 03:23:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Thu, 07 May 2020 03:23:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Thu, 07 May 2020 03:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2020 03:23:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4504446071184d4707bc1b754311b73a078008c3d1c64b7c3603e062f9e826`  
		Last Modified: Thu, 23 Apr 2020 18:46:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d55b89827dff29b49f86cebc978eddb06ffdf89e9675cc9e43e76939a1a3cd`  
		Last Modified: Thu, 23 Apr 2020 18:46:38 GMT  
		Size: 76.7 MB (76651558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf7f8bea876f55a2bbbf9e69e2190755e54d4dfc340c16418a66593e8f0cc61`  
		Last Modified: Thu, 23 Apr 2020 18:46:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec365b01c1d99a2d7a163fe5738ad211413b60bdc382e366d4606a1c2f09b0f`  
		Last Modified: Thu, 07 May 2020 02:31:43 GMT  
		Size: 12.6 MB (12605518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfea563ab774a9c8a07b541bc7a756bca038e5f8396ec424e70432542a2ce3d3`  
		Last Modified: Thu, 07 May 2020 02:31:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a5abf6fac12ad74c2dcead041fbd8330c86edcd1c8d438c93882477a48726d`  
		Last Modified: Thu, 07 May 2020 02:31:48 GMT  
		Size: 28.5 MB (28529664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d0be756e5751320a39e1d04a9d45299e66706e88908122fabd95c957fa173c`  
		Last Modified: Thu, 07 May 2020 02:31:40 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7798a6cf75696ca628ed1404e347c9efbd2e4476bc6f597ff3077e8c68111560`  
		Last Modified: Thu, 07 May 2020 02:31:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5724d804bff3a1d175edab5e599530c66a2eba662c8970be6cdf22eec311ea70`  
		Last Modified: Thu, 07 May 2020 02:31:40 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7798a68ae79fe23d13c08835dee0e50a51adf408e39e490d8ed7524be29834b8`  
		Last Modified: Thu, 07 May 2020 02:31:40 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333babea9756cb153b3ee1ba1a6a3b83bd84d749dd07db1928cfcb4c77ef5b79`  
		Last Modified: Thu, 07 May 2020 03:24:19 GMT  
		Size: 2.6 MB (2576647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ccb85de16b0764c47b76a5b6a76ea684c58e0d5e3bfcf1b8d50b2f1cbb485`  
		Last Modified: Thu, 07 May 2020 03:24:20 GMT  
		Size: 8.5 MB (8468673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5e7cb08d1eb9d03d3045a48fc467cce064d2d434a2cbdb9d06c03d5838636c`  
		Last Modified: Thu, 07 May 2020 03:24:18 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:5875172b314d67cb2cb456df0441f34539227c51dd29f189dae9afa1b82baa48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148026095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e31a084a2b0e971e035d25337699248de8fc723c2d5d5ef28f8c9f6629f5341`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:09:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 16:09:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 16:10:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:10:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 16:10:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 16:22:42 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 16:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 17:23:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 17:23:42 GMT
ENV PHP_VERSION=7.2.30
# Wed, 06 May 2020 23:30:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.30.tar.xz.asc
# Wed, 06 May 2020 23:30:39 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Wed, 06 May 2020 23:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 May 2020 23:31:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 May 2020 23:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 06 May 2020 23:34:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Wed, 06 May 2020 23:34:41 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 May 2020 23:34:43 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 06 May 2020 23:34:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 May 2020 23:34:45 GMT
WORKDIR /var/www/html
# Wed, 06 May 2020 23:34:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 06 May 2020 23:34:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 May 2020 23:34:48 GMT
EXPOSE 9000
# Wed, 06 May 2020 23:34:49 GMT
CMD ["php-fpm"]
# Thu, 07 May 2020 00:58:07 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Thu, 07 May 2020 00:58:08 GMT
WORKDIR /var/www/html
# Thu, 07 May 2020 00:58:09 GMT
ENV BACKDROP_VERSION=1.13.2
# Thu, 07 May 2020 00:58:10 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Thu, 07 May 2020 00:58:19 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Thu, 07 May 2020 00:58:22 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Thu, 07 May 2020 00:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2020 00:58:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00aeccd126509e0b42d6cba92126cce7c342206083cc40a285bd447cf1f2d46`  
		Last Modified: Thu, 23 Apr 2020 17:51:33 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103463f158e3c7f91314c099c5524db53fd97efd35b7502a2991750063630384`  
		Last Modified: Thu, 23 Apr 2020 17:51:55 GMT  
		Size: 70.3 MB (70334752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c968fd52774e9a63a8ca1cd66b708fb02df8fdc207dc98e23a8682010b0047`  
		Last Modified: Thu, 23 Apr 2020 17:51:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae5170d23f423c1c00dc7774534a2f700c2460c1ff92505d0acc5225066013`  
		Last Modified: Thu, 07 May 2020 00:29:19 GMT  
		Size: 12.6 MB (12604362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7feb8706595547fc13269c17938552c0aab5bd806b9dd932fedbd17e288420`  
		Last Modified: Thu, 07 May 2020 00:29:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111622f3c3f0d4744d94f41a3a3220793c8cb912ac9c4d25e4d5a9474878de70`  
		Last Modified: Thu, 07 May 2020 00:29:23 GMT  
		Size: 28.2 MB (28205722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa7c8b54ebdbf25279302ed4819f2f6e65febd958dec842ca931f1ff01935d`  
		Last Modified: Thu, 07 May 2020 00:29:15 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e08dba786748f0ad099545ccc8ecda5c76e28e05828beb9d248d029ca91e220`  
		Last Modified: Thu, 07 May 2020 00:29:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bba48a8bbd09d487a76c5033fc6afeaf69d30c64c4c27eb367b4aa246dd4c`  
		Last Modified: Thu, 07 May 2020 00:29:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a7128c5c810e6b9308c0b5b29cd000840a9b5e8dad0236118b3508785fca4b`  
		Last Modified: Thu, 07 May 2020 00:29:15 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792d7ada2e47ee6653d28dbdff8f008438a66512e6ba94e62af54b847d775d24`  
		Last Modified: Thu, 07 May 2020 00:59:00 GMT  
		Size: 2.5 MB (2542234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54864b2a37d08ef8d9b2b122e4b0214455be9e3876d755d674a7819410bbbda9`  
		Last Modified: Thu, 07 May 2020 00:59:02 GMT  
		Size: 8.5 MB (8468809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be848deb905457176cd24b3c3106555690852005eaf386b05127517c959ebd2f`  
		Last Modified: Thu, 07 May 2020 00:59:00 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
