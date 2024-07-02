## `php:cli-bullseye`

```console
$ docker pull php@sha256:4290c7133aaeda986dec5d4d22bb6485383e90135207b3d34dd17cd0a72e8a85
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

### `php:cli-bullseye` - linux; amd64

```console
$ docker pull php@sha256:dfe5a466f27e916744f396d37f718c1b9e7846ce5bbfbd0feea08329a7c56139
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170833566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b9154fa1bb85f8e9f0d3fa4aa6ff6852eafadb69fb509bc7f32bf09654fa5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:25:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:25:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:25:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:25:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:54:49 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:54:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:54:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:55:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:55:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:58:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:58:05 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:58:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:58:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:58:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dbe43e30a1ec070f064e78ba481c34bcddadbad30a2204b3674f7551121b4e`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759ee6bd3706c33b42cb784d34dec8a4eabbea15cfca2530b93bb24821b7adc1`  
		Last Modified: Tue, 02 Jul 2024 04:38:06 GMT  
		Size: 91.7 MB (91650270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3df42241e90d0821c6beaae0b632772ca7c45471efc1fd020bb51049f741038`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e0b7268491e523586fa285aad151cdcd445d4552048a56f9d728b53cf69ad9`  
		Last Modified: Tue, 02 Jul 2024 04:40:47 GMT  
		Size: 12.8 MB (12799397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a128963b7a3a806f5c28fb2348377cd5ed2804bf4b910391873bf2875d723a0b`  
		Last Modified: Tue, 02 Jul 2024 04:40:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9236b19bbb0dc7b880761085a5cf05e96a0793c325619312bb45714a937d7d`  
		Last Modified: Tue, 02 Jul 2024 04:40:51 GMT  
		Size: 35.0 MB (34957974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e511f5db738b77c8de48b27f40adeef5bd24f369250d7b66a7046c7146978097`  
		Last Modified: Tue, 02 Jul 2024 04:40:45 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790362ae38299ad87b43f2151fd11325dfe406bb378158021847ce1a0263140e`  
		Last Modified: Tue, 02 Jul 2024 04:40:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:d1b22f51ef6b4dc321df8ed0f4e32621c338174c4a058efd47d2529e6123d1b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148334159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901a759a11ff544e046d412ecada0bd8a3349b5dcfa143b052555acf1310b46a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:43 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Tue, 02 Jul 2024 00:48:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:39:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:39:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:39:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:39:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:39:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:39:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:06:46 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:06:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:06:47 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:07:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:07:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:09:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:09:47 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:09:48 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:09:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:09:48 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ea1d136a0316c3c6cfab8ae6bb76454b8562314f8d7e552a5f06ba7d8d4fbe`  
		Last Modified: Tue, 02 Jul 2024 03:42:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cc766543faef6c79562d3f8d742bbb34bae433bdccfb9554ff78708c3b6637`  
		Last Modified: Tue, 02 Jul 2024 03:42:51 GMT  
		Size: 73.7 MB (73698312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1beb3b5ace36342878b3bf9adb858ec9286b901c9b292868aa0adc017dcfae2`  
		Last Modified: Tue, 02 Jul 2024 03:42:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c42637bb871b27d28e6280890178a1b0a6b8d8c7b8a7e584d0e9bd025113030`  
		Last Modified: Tue, 02 Jul 2024 03:45:41 GMT  
		Size: 12.8 MB (12797801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2bdee5477a89a1a614a30ddf9653a633923ed07aa437d6150a7f8602c603dc`  
		Last Modified: Tue, 02 Jul 2024 03:45:40 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a9398d621d673200f3b461b59a48a5da72a84a26b673ca6ea486675aa144e6`  
		Last Modified: Tue, 02 Jul 2024 03:45:46 GMT  
		Size: 32.9 MB (32909693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206e299898f8eb2f443c3517f61d248c6d1625368c4f913918be569bee8364e`  
		Last Modified: Tue, 02 Jul 2024 03:45:40 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fbbec296b5835fa6dffdcbabe9a06116ee15ced7bf8ed64de92a42b75e4559`  
		Last Modified: Tue, 02 Jul 2024 03:45:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:062cc25ce37656029dc09a25f8432fceced202400e0cc96bbf0fa024ab0e0af1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140215394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c69d176f25feeff5475e046480a134e9598568042bf0e964e05e8f7f9b94e1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:02:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:02:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:02:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:02:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:26:36 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:26:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:26:36 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:26:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:29:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:29:09 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:29:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:29:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:29:10 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169340bbc9b11466dc02ad185ab4ec5be5ae3f2d1bfadf025062aee784d7cf8`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33cc5c115210ef3a85f7c10ea07381ce083592b603b1061dc201bea60ecafbd`  
		Last Modified: Tue, 02 Jul 2024 03:58:41 GMT  
		Size: 69.3 MB (69327786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fcbcd04aaf63c6b9ff83a247cf90682f60d62cabedfca5e92463f2e670db42`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31a68c0d97ef532ea5d5e7e19984170794f425522bb4932623607e30c647e81`  
		Last Modified: Tue, 02 Jul 2024 04:01:42 GMT  
		Size: 12.8 MB (12797791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacefd86609320eb14eeb4f0a19933fb583cb2a9d648772cb5c4ec662bfa67fc`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c6eee0ae7a96ecf05179b8e09698fbc3510a46ba78e5185d788a416d2b631e`  
		Last Modified: Tue, 02 Jul 2024 04:01:47 GMT  
		Size: 31.5 MB (31503475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad65cf90ff91be2827829fee39922205bb5c11899484f5b9e8a2821b9434d7b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3e75d93513ccb035cfa292ce32aedaeb631f7ac19cc6f4f6e902ba6834a566`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:da3817a5f02fd00ab0d9f4dc2f55faee5693f21bedc02fa3f9e607d7c06309ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164662938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f474d2fe3e4ec393ca398cc2c17b31e2869d0794fe6e77e319c001086c6bd4b5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:33:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:33:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:34:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:34:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:34:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:02:39 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:02:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:02:40 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:02:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:05:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:05:48 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:05:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:05:48 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335aec71aeb153fbea1427f7ea534c8097ca1898940f18317d638023574b8ee`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bc195ca28e4f92808a4f6fd9b73331db6859db9e2ec74c189e231c415818e0`  
		Last Modified: Tue, 02 Jul 2024 03:38:01 GMT  
		Size: 86.9 MB (86939700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451e19963414458f43c8264137cea0d3aaaf9648417827bdcd7a2db62f7e0f89`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291890bd781768cc7e277eb356b291b5b28c0ba4f8bb1ec7e9ad7aa7ec2faa8`  
		Last Modified: Tue, 02 Jul 2024 03:40:42 GMT  
		Size: 12.8 MB (12798531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f010b6fe9bd0ccd1b853ec3f01d57263a545bb6e414383a1ad7372e73ad91431`  
		Last Modified: Tue, 02 Jul 2024 03:40:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a961dc1e87f21cca50c0a17069b7b6159dbf3142452aaf1aa1b069cd7c1542`  
		Last Modified: Tue, 02 Jul 2024 03:40:45 GMT  
		Size: 34.9 MB (34851450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9fbd53655da4323bf7d5b43d7f4e4979a71504c0ed735cd034ca8454c7aebc`  
		Last Modified: Tue, 02 Jul 2024 03:40:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a9694cf5001f790bbe12d0e3e1eafe6e79b88f7ba32fce745f3684fea07928`  
		Last Modified: Tue, 02 Jul 2024 03:40:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; 386

```console
$ docker pull php@sha256:f8edf6aaa5aba931aaedd9857fe3fc6ee53be810cc576e5fa9f8d3d631e6de2d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173510113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4966339e2c80ea518d9b846571a151af8e0d3b468af9247e4712cc3d9b65dafe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:08:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:08:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:08:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:08:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:08:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:08:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:55:47 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:55:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:55:47 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:55:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:55:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:01:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:01:05 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:01:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:01:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:01:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ab6efef12df0de52bf9e83bb54eeb04b25e4bddee111bb8de64345305496a`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90549434c6bff14f52cbc9958e76ddae4f172308e4aba9cdcc10c126accc3b94`  
		Last Modified: Tue, 02 Jul 2024 05:41:16 GMT  
		Size: 92.7 MB (92720434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e55f446fcc5301935ef2eed4717ce1921ca07f5b60bea264e88372cd08c54e8`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e756fd9f8da7449af37fc3fce3ed3ad88be1d6dda8e6fbb8df3337fc84926c3d`  
		Last Modified: Tue, 02 Jul 2024 05:44:15 GMT  
		Size: 12.8 MB (12798516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4748a97f132bfdb1a5604e3cda65987013095c815673d0f284420ffbf306bef9`  
		Last Modified: Tue, 02 Jul 2024 05:44:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7075fc6bf97ee4279850a14c628c28f771fc7dc014f14070f5f8b220139fc1d7`  
		Last Modified: Tue, 02 Jul 2024 05:44:22 GMT  
		Size: 35.6 MB (35579076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75c2bf8ca2bdc208a46efba5aaa2b8b1b5ff93e5a6dbca5abe8433cb7b3ce2d`  
		Last Modified: Tue, 02 Jul 2024 05:44:14 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90006a61d03cec528430d34ad6f4fb2faa6a42c940b86f326181eb838b3663b5`  
		Last Modified: Tue, 02 Jul 2024 05:44:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:114c966c83169c68000049e8ccd723882c5fb811ad3bba75653161b9a2af4fbd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147741007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1bb551cc2565ec007dc2fcd34a3c5a9cf57e8bd884371e6fc0e72b30fc3dd8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:38 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Tue, 02 Jul 2024 01:19:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:58:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 03:58:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 04:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:00:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 04:00:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 04:00:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 04:00:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 04:00:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 04:00:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 06:05:35 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 06:05:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 06:05:43 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 06:06:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 06:06:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 06:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 06:19:48 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 06:19:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 06:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 06:20:01 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211022f2238239d5b5e5886c96179b5c458c9ba54b1f759cf7b336a257d9ebe1`  
		Last Modified: Tue, 02 Jul 2024 13:12:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7ad6c880e97a6df36706db31e132236fa47b9f336e8d67a2ac5aacdcd42a60`  
		Last Modified: Tue, 02 Jul 2024 13:13:46 GMT  
		Size: 72.0 MB (72022115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e900f12815c7beebd1f35e0d13d69604b1f6e85b3436808fb5086f6a5d1a1439`  
		Last Modified: Tue, 02 Jul 2024 13:12:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56da1f04557a92f662c9d3e2d651f415b921a25d96f2b7d75fba27f13e73360`  
		Last Modified: Tue, 02 Jul 2024 13:18:40 GMT  
		Size: 12.6 MB (12581883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d102665f33296d316a360e9d561bf7a9cc0423dcf7cb49cfd29ea876c205122c`  
		Last Modified: Tue, 02 Jul 2024 13:18:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a6b7216bf5de289aef237e68be54e86222c363e2b249711fcebcb17794442b`  
		Last Modified: Tue, 02 Jul 2024 13:18:59 GMT  
		Size: 33.5 MB (33493515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bce96f8d066fb32956553f10439433238e5ca72158f95b07eff18743fe4103`  
		Last Modified: Tue, 02 Jul 2024 13:18:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81d291302ad5125886776c6cb796d0f0112826e506ddd3eee72c1b2d9cfbf5`  
		Last Modified: Tue, 02 Jul 2024 13:18:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:393a6f79cfa42f382853c7a9330f6cfb02dd448270c41c344475683ff922561a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171538837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc8f9f20e176ec10efe2ab72c5b9e6c6adda49c4b32732a61531e668fed82`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:03 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Tue, 02 Jul 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:24:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:24:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:24:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:24:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:24:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:24:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:24:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:24:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:24:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:49:38 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:49:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:49:38 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:49:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:49:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:52:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:52:27 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:52:28 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:52:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:52:29 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339f489d1e564c9c7d91a1bafdbd753bea976cf7d4e49aac09781b3a7179dffa`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c23a5c69cce13d9ff3aa0ee9590ebb9a7850465f19d2721100e288312e7b9`  
		Last Modified: Tue, 02 Jul 2024 04:16:31 GMT  
		Size: 86.6 MB (86647997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4efbc073f0d2c267667e6f9fa4d3a5d430b0c9e921cd8823dc6cd7b4d22002d`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb96a192cd9b873eedb8876ae64b4702419603153894352c0b73a1c753e0e94`  
		Last Modified: Tue, 02 Jul 2024 04:19:21 GMT  
		Size: 12.8 MB (12799155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe97e0557b42c20b1bf1cc44a32e10e03e7314325902fed26a424c9124704138`  
		Last Modified: Tue, 02 Jul 2024 04:19:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f02ebb373cb4c4f4e800e9c10f1bffaf1a647acdba85ce32a212237b72a38e`  
		Last Modified: Tue, 02 Jul 2024 04:19:26 GMT  
		Size: 36.8 MB (36788856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b16be97225c941ab04d0377a13ef4ba8b1c429da5766c4b31b4048cfd2d569`  
		Last Modified: Tue, 02 Jul 2024 04:19:20 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e9f30286ce8f585ae30c09cefbd3c96d5bd63e8327f066db8f076d179e6c5d`  
		Last Modified: Tue, 02 Jul 2024 04:19:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-bullseye` - linux; s390x

```console
$ docker pull php@sha256:cf256169e875554d09f2ef9f114b5a9df88897d3e60bcb1eba5e2ed425e27362
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147928158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6da1634d5fb8be8355e43571d28a8082459dabb48017ae514b1622deae60371`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:26:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:26:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:26:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 01:48:25 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 01:48:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 01:48:25 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 01:48:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 01:48:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:50:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 01:50:34 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:50:34 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 01:50:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 01:50:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17d7bf4982e21c3386b6bdf8634c3d59503cac65f62f788141a1b7410b7dae4`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f9558ba7962aecc1f4c8fdf9a69dc59140624ff107a83d97ca9b2f2ea5f64`  
		Last Modified: Tue, 02 Jul 2024 03:06:19 GMT  
		Size: 71.6 MB (71641635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740b856ce936618b60f15e78d2808c90765f0df4fce2766a82eea320ba3d832f`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba92a8e96bea890800c3c7efaf1da800c40b43ca4460b94fad9877211b9b3d5`  
		Last Modified: Tue, 02 Jul 2024 03:08:28 GMT  
		Size: 12.8 MB (12798197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe48ca526a1c8743d51aa200c9e0e69993e4b1d693e200b5838fc5bbcf02e87`  
		Last Modified: Tue, 02 Jul 2024 03:08:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e220c9adb7e109e55c63b17ef030d510bb76ee3bae244061d5c9a273e14abe`  
		Last Modified: Tue, 02 Jul 2024 03:08:32 GMT  
		Size: 33.8 MB (33822343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb210872a40910988d1d34b53701aa37422bbf1e536639696e195a8d2bdee478`  
		Last Modified: Tue, 02 Jul 2024 03:08:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c8bef2bdace87e4ae7b5602f76183344311f41f9606736558f436e3535fa1`  
		Last Modified: Tue, 02 Jul 2024 03:08:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
