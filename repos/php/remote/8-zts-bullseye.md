## `php:8-zts-bullseye`

```console
$ docker pull php@sha256:a0706dfb2ea9736a5e707f9b4b6275ac23ad1cb0cd117021d56284e8f2595309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `php:8-zts-bullseye` - linux; amd64

```console
$ docker pull php@sha256:5c2517b6cd06a7f228de73e2bcd0e77ec6b858dd35e9b7fde5d1ee55f0a830c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171475474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c276e42793c884526c3fbc94a90abeb8e2f2b92c71a3042f874e2c1558d7c8d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:51:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 12:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 12:52:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:52:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 12:52:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 12:52:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 12:52:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 12:52:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 12:52:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 27 Dec 2023 22:45:13 GMT
ENV PHP_VERSION=8.3.1
# Wed, 27 Dec 2023 22:45:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Wed, 27 Dec 2023 22:45:13 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Wed, 27 Dec 2023 22:45:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 22:45:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:59:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:59:11 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:59:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:59:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:59:11 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f2067ef4c9b0c9e0c12ec42bb9725681767c82c63ce30b3d61bdec9dee6734`  
		Last Modified: Tue, 19 Dec 2023 15:39:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba558f2d9945b53d1a0bf19e7bfcfc5df93c00e49e866827238eb35af55634`  
		Last Modified: Tue, 19 Dec 2023 15:39:43 GMT  
		Size: 91.6 MB (91635005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae92ca9efff667bdfbb8a1c07acb96f3c61dd7206fd8bf6c0c4a4a9a142042`  
		Last Modified: Tue, 19 Dec 2023 15:39:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627a5e13c0cf773df97fe54c67f4e9f09d5a814fa810601e231ed41e8e25223b`  
		Last Modified: Thu, 28 Dec 2023 01:15:14 GMT  
		Size: 12.8 MB (12764752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c00d17f7906e3bc8f87d6eb533f3deacf7453e118025c9ab0b8544dccf38a0`  
		Last Modified: Thu, 28 Dec 2023 01:15:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1b97ff77bb9d467ebdd4a53522a9491a43c3f5f954b3f2a500e278ce43c51d`  
		Last Modified: Thu, 28 Dec 2023 01:16:21 GMT  
		Size: 35.7 MB (35654157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95317e4f0f2c351d0c0e854c0ac6afc4b73239da4495149b30aaf65bd27588f3`  
		Last Modified: Thu, 28 Dec 2023 01:16:16 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474aecc821f81031183feffc197aac6c65b37975dcf4844a41eb16cdc593cfc7`  
		Last Modified: Thu, 28 Dec 2023 01:16:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:7626ce14a0f82febd314b26aeaa4a72e26ed4f9dc0de86cd7b3eb00f811ad74a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149174991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341e384cde277af44e9dc984f0f5ce9d2458e515db107a206e4b672f0e633faf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:38 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
# Tue, 19 Dec 2023 01:55:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:30:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 02:30:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 02:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:31:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 02:31:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 02:31:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:31:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:31:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 02:31:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 27 Dec 2023 22:17:56 GMT
ENV PHP_VERSION=8.3.1
# Wed, 27 Dec 2023 22:17:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Wed, 27 Dec 2023 22:17:56 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Wed, 27 Dec 2023 22:18:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 22:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:47:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:47:24 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:47:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:47:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:47:26 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd80286abf1a0349dff22a025ce1f8995896cb884c38443684834f7ee53d78a6`  
		Last Modified: Tue, 19 Dec 2023 04:49:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4296ee68f6a6d3e5e8b3c49e82b4a6bf047ba2db6746e308f27269d9d012355`  
		Last Modified: Tue, 19 Dec 2023 04:49:41 GMT  
		Size: 73.7 MB (73690328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb68e9d9dc7d1d29014115dacfe87ac57b0e03a99c1d0022ecab600b6b3c0a4`  
		Last Modified: Tue, 19 Dec 2023 04:49:27 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aeb8112f1fe70d951ad825921ce9a9195ff96c3b98e8fce14776f3222548cd`  
		Last Modified: Thu, 28 Dec 2023 00:33:22 GMT  
		Size: 12.8 MB (12763305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba40452ce7a30251d6cd323c684d11eaffea235b5f30d20aedb56b757f5253a`  
		Last Modified: Thu, 28 Dec 2023 00:33:20 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429045bbb8ad7b4d0455363ea75e30daeddb4bed66da435f465da361a8a3622e`  
		Last Modified: Thu, 28 Dec 2023 00:34:39 GMT  
		Size: 33.8 MB (33796379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa13718f7a174219a4924097fe99faf94388b498091bb6eb833475dd9d0f9c1`  
		Last Modified: Thu, 28 Dec 2023 00:34:31 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc1b23b1b9da132e435e246c776b81996dae751cedea51580ae73ab8701ee3a`  
		Last Modified: Thu, 28 Dec 2023 00:34:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:c5e4c5623d6218e8a019a32587074bb5be7ee8b76dc282b103f08d331dfe373a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140541378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07939a7c97aaed0bce10c29dd6e8e02d34c524d1b815db7e376fe0320e0f767b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 02:08:09 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
# Tue, 19 Dec 2023 02:08:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:22:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 05:22:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 05:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:23:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 05:23:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 05:23:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 05:23:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 05:23:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 05:23:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Dec 2023 05:45:26 GMT
ENV PHP_VERSION=8.3.0
# Tue, 19 Dec 2023 05:45:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Tue, 19 Dec 2023 05:45:26 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Tue, 19 Dec 2023 05:45:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 19 Dec 2023 05:45:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 19 Dec 2023 22:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 19 Dec 2023 22:46:43 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 19 Dec 2023 22:46:44 GMT
RUN docker-php-ext-enable sodium
# Tue, 19 Dec 2023 22:46:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Dec 2023 22:46:45 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57920847d8697c7964a31692261085bf2f2378ae3ecf002e2863475c95222e27`  
		Last Modified: Tue, 19 Dec 2023 07:36:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e488984c5928075b5b9dea91064862fa20be8786e9a15c6279b23d7ff93f05`  
		Last Modified: Tue, 19 Dec 2023 07:37:08 GMT  
		Size: 69.3 MB (69322836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1214fb5d2abafbea1a25bb8db0d422022382b1f6a5ca494d124e9a2a8e596`  
		Last Modified: Tue, 19 Dec 2023 07:36:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75b9fb9c6b2ac0ac5b977d12b2fcfe6f73fb83cdee2e684c505530e967fc979`  
		Last Modified: Tue, 19 Dec 2023 07:40:12 GMT  
		Size: 12.7 MB (12748904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f431696edaf32d195cdbd2408a2fefd40506500b94bd0503dd290f9fc82aecd`  
		Last Modified: Tue, 19 Dec 2023 07:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9319cf4dba58b9de4a47ec2c5e53e6658e2af2d1726b11a4bfbc42c6b0abfa`  
		Last Modified: Tue, 19 Dec 2023 23:56:26 GMT  
		Size: 31.9 MB (31886971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ba27879f547386287c75180ff0b6ecbd430d80b2cc1b38761d4c273a9c3f06`  
		Last Modified: Tue, 19 Dec 2023 23:56:20 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e33b1cc29c71fc3862fb80e391a6f6d3e966e166a353bc96e885b0fbe81a9fe`  
		Last Modified: Tue, 19 Dec 2023 23:56:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:390ba97b4fe72e6c25fc832c9312604f643bf19648f1bb3390786f22da8498a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165405413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2759465bf09a63e9ffca82dd49f7ab44d9890f76eece2efb2c198477e344d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:41:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 03:41:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 03:41:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:42:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 03:42:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 03:42:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 03:42:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 03:42:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 03:42:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 27 Dec 2023 22:05:56 GMT
ENV PHP_VERSION=8.3.1
# Wed, 27 Dec 2023 22:05:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Wed, 27 Dec 2023 22:05:56 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Wed, 27 Dec 2023 22:06:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 22:06:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:18:55 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:18:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:18:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:18:56 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a076a6ccd85e73e29012b8a84aad006e60b307f5df5cca21e9d9bbae5baf5974`  
		Last Modified: Tue, 19 Dec 2023 06:10:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cc9400cacbe2c77cc31c637154af3be3dcbbf65677d2acd986af40a925f0e`  
		Last Modified: Tue, 19 Dec 2023 06:10:55 GMT  
		Size: 86.9 MB (86934717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279670fefda12a2bab1c29068b63a86160147c69217f64bfe89a84aac931d572`  
		Last Modified: Tue, 19 Dec 2023 06:10:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656ca013741237633238ab72255dd3f5437ab823afa95fb4c513990c545db37`  
		Last Modified: Thu, 28 Dec 2023 00:31:35 GMT  
		Size: 12.8 MB (12764041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b8f5f3fef7ea72eb29be75527339efc6d9b419885b47477e0c2a45d3cf6bf`  
		Last Modified: Thu, 28 Dec 2023 00:31:34 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc865b41f8cbb015801e4a25383792c9003412467f2f57a0a07ad1c01960d7f1`  
		Last Modified: Thu, 28 Dec 2023 00:32:38 GMT  
		Size: 35.6 MB (35638916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d6c383f39d683a01362f8e49a013a93a9f58ab76b3e13a106b531b51a1c4a6`  
		Last Modified: Thu, 28 Dec 2023 00:32:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609751628c8f1b95543b06af3f345f7a4ed90a96bea89567f4e50d5207d0e55b`  
		Last Modified: Thu, 28 Dec 2023 00:32:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; 386

```console
$ docker pull php@sha256:abe6ccaf893f0413e0a66b7750c591876eb06c567285d4404a54390fa2781d15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173720876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfc3940d4da44e0ce7c1e0d64b11acc68d8e9d68ac0c329e7181b78a7d09b6c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:30 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Tue, 19 Dec 2023 01:39:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 17:20:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 17:20:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 17:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 17:20:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 17:20:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 17:20:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 17:20:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 17:20:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 17:20:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Dec 2023 18:11:30 GMT
ENV PHP_VERSION=8.3.0
# Tue, 19 Dec 2023 18:11:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Tue, 19 Dec 2023 18:11:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Tue, 19 Dec 2023 18:11:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 19 Dec 2023 18:11:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Dec 2023 06:56:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Dec 2023 06:56:20 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 20 Dec 2023 06:56:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Dec 2023 06:56:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Dec 2023 06:56:20 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39110ba11c8965e66c90db4a166891c890c44c96a8abdf4adc6bc9671fbf63fc`  
		Last Modified: Tue, 19 Dec 2023 21:56:06 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2f8959b86ffec4d26d14f8bcac8c102242de953477eb7372d2ddad03599bb8`  
		Last Modified: Tue, 19 Dec 2023 21:56:27 GMT  
		Size: 92.7 MB (92725759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69416bc6552a7f0a0abdb9113b6b81fa1f0a60b66d43ddfe1af6cf621af62ab4`  
		Last Modified: Tue, 19 Dec 2023 21:56:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e501f50b05c025894a108a4002aec23217a23dcd723f4f2efc63b27624b99`  
		Last Modified: Tue, 19 Dec 2023 21:59:49 GMT  
		Size: 12.7 MB (12749805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661864e96a5cc4d606904ad21539f02f4220a193df43dc3c44e7e383928289a0`  
		Last Modified: Tue, 19 Dec 2023 21:59:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7fc20a84abbfb671120caba663b27e3c8a0bc029c912f15cbafed67fe640aa`  
		Last Modified: Wed, 20 Dec 2023 09:02:13 GMT  
		Size: 35.8 MB (35838928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0625c6cce69fc4fb2212c8360f42aed762eaadf554cf5c94ffa87952563308c`  
		Last Modified: Wed, 20 Dec 2023 09:02:05 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f84ab25a9180e5bc6dfcbe253734d011110e222a155a575ebc16746f9c0df0`  
		Last Modified: Wed, 20 Dec 2023 09:02:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:2d4c1a007e748be424c78c3bf8787bd92d087fb6ef818a86e542ca664f82fedc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147758049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cafee3c644e2340c679c5e244ffc5f4f1d1302c56048f57ef351a17ac8c96b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:50 GMT
ADD file:dcc77071aa6c677714230fd845d154c00ba6ba34a78f8f1073c224e90f17f543 in / 
# Tue, 19 Dec 2023 02:14:54 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 20:39:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 20:40:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 20:41:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:41:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 20:41:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 20:41:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 20:42:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 20:42:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 20:42:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Dec 2023 22:48:00 GMT
ENV PHP_VERSION=8.3.0
# Tue, 19 Dec 2023 22:48:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Tue, 19 Dec 2023 22:48:08 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Tue, 19 Dec 2023 22:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 19 Dec 2023 22:49:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Dec 2023 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Dec 2023 23:14:57 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 20 Dec 2023 23:15:03 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Dec 2023 23:15:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Dec 2023 23:15:10 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f9454980ac665cb2d7641130c738c2054ef7a7516386fc6742b46b5b60dd93ad`  
		Last Modified: Tue, 19 Dec 2023 02:26:03 GMT  
		Size: 29.6 MB (29635982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45840e3413dae74e526f55ddcdf1db42b53ccbb27b4fb21e419a5582ca09dd18`  
		Last Modified: Wed, 20 Dec 2023 07:59:21 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95c6a802f4dd492ceb4c3eb8e35309d5c95d19cfdb86049d0c9d4882e9b422`  
		Last Modified: Wed, 20 Dec 2023 08:00:12 GMT  
		Size: 71.8 MB (71814805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbc65667ba3423adf4d9419c0ac5e16231796095992eeb158a0bd7eeb0f9100`  
		Last Modified: Wed, 20 Dec 2023 07:59:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a67b42beb474de6ad992adcc131ca8b2986204caa0d212f919742a841f357`  
		Last Modified: Wed, 20 Dec 2023 08:05:02 GMT  
		Size: 12.5 MB (12532346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a261d9df04692f228c9de8679dfe6a6321807aa6a8ed5621b4e59829207de50`  
		Last Modified: Wed, 20 Dec 2023 08:04:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3072e536992568faf7be6a7c41b4b352f45842f8445b133f13ca59cfa2a9a29`  
		Last Modified: Thu, 21 Dec 2023 01:17:15 GMT  
		Size: 33.8 MB (33771273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcddb311af4396253ddd0fb39e52c0b1882f28037213ed1300b2cdc81187fde`  
		Last Modified: Thu, 21 Dec 2023 01:16:53 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffa352f43ba7c410af1736d95592bb731f8835ebc58c3d1b0a4a6173c40a80`  
		Last Modified: Thu, 21 Dec 2023 01:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:c8914a623e2faf5b391583aff0326c98315afe92fc0e1075a25bb23eb4b7d1ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172310654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37acf295883eb752fe53eb08c70ef6212d8e50813988f56a93354c9b94e0f90`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:27:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 06:27:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 06:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:28:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 06:28:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 06:28:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 06:28:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 06:28:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 06:28:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 27 Dec 2023 22:41:55 GMT
ENV PHP_VERSION=8.3.1
# Wed, 27 Dec 2023 22:41:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Wed, 27 Dec 2023 22:41:57 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Wed, 27 Dec 2023 22:42:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 22:42:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:56:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:56:27 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:56:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:56:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:56:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cf519da704a54ecd293555ffdb5378583eb2868a1e6446dc247a6886dc999`  
		Last Modified: Tue, 19 Dec 2023 10:14:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc74cb39269dd60ed201199e7c64cdcbb45ec85b53ac6c23f0e2e855b7ef3f7`  
		Last Modified: Tue, 19 Dec 2023 10:14:34 GMT  
		Size: 86.6 MB (86643602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc627fce51a8d94e83865a3eb6e70a4ce8ac2181ec3fc10971f18a787e5ce54`  
		Last Modified: Tue, 19 Dec 2023 10:14:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107632fea8a39cfb71ccfb43a71df07a0eed106c56aeb6a05ae4d44953371dfe`  
		Last Modified: Thu, 28 Dec 2023 00:58:31 GMT  
		Size: 12.8 MB (12764661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac665f71c69335875a93af247836c780e9de2ea2e356a7a29e7125b30e9c4f9d`  
		Last Modified: Thu, 28 Dec 2023 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b1cbc77ff7bdef72d2b7feeea61aa1d1306add4424fd89003aeef4d61ab497`  
		Last Modified: Thu, 28 Dec 2023 00:59:45 GMT  
		Size: 37.6 MB (37604889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d20d0a15021367f4b3cf98d972bd26c39b85b82f1c88f4e20c7a12504720c`  
		Last Modified: Thu, 28 Dec 2023 00:59:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc84de783abfc28b18e613d84d4443af7676943933fa7fab4016bcbb06c7665`  
		Last Modified: Thu, 28 Dec 2023 00:59:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-zts-bullseye` - linux; s390x

```console
$ docker pull php@sha256:582ed424c902145afe2b1f8ed72d6ba7bd9ae398086eb2d6c2a5464d7346585c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148308663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee0a2ba32868987b3e85a0e5b913eaf287a0ea30198bb7a497e8d9ea61f0fd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:00:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 04:00:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 04:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:00:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 04:00:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 04:00:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 04:00:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 04:00:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 04:00:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 27 Dec 2023 21:53:57 GMT
ENV PHP_VERSION=8.3.1
# Wed, 27 Dec 2023 21:53:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Wed, 27 Dec 2023 21:53:57 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Wed, 27 Dec 2023 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 21:54:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:03:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:03:42 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:03:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:03:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:03:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b09eb72e9d386dbf4dcb97b2cd8fb6c959008740372463872bcbb989f9b553`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd379a47c6b90f49f4156c7ff2dd2eb18fe68c359cee32fa1f2d5786d853a7e`  
		Last Modified: Tue, 19 Dec 2023 06:08:59 GMT  
		Size: 71.6 MB (71634732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8169479b1d74c4fef21b4c3c845f26c586316508cfb384643eddfd5325797a1`  
		Last Modified: Tue, 19 Dec 2023 06:08:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c270c34106e4574205f1e4e250bbceed124531e7f49f5267fca812146d0604`  
		Last Modified: Wed, 27 Dec 2023 23:40:32 GMT  
		Size: 12.8 MB (12763714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0010292192f5950a212e200b07d434e9caebbbef1271dac84fc2121924240`  
		Last Modified: Wed, 27 Dec 2023 23:40:31 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae822fc950f086efb023ec76bef759e82f31d2e93a26c5adbecaaffa5b3f05`  
		Last Modified: Wed, 27 Dec 2023 23:41:16 GMT  
		Size: 34.2 MB (34249522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c6656cfc0735862b9fcaa7ecfd08943cbc5dc62410c59fdd38d2e85e36cf1a`  
		Last Modified: Wed, 27 Dec 2023 23:41:11 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a21e4dd7f31c8dbc323589f90e961738b619e90d71fd110554176210b4ef6c9`  
		Last Modified: Wed, 27 Dec 2023 23:41:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
