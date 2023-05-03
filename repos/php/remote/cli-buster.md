## `php:cli-buster`

```console
$ docker pull php@sha256:8f8f4b555d3b092f0f2ba2efa1b07ddd107b1d670292c7891d971a0bf991876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `php:cli-buster` - linux; amd64

```console
$ docker pull php@sha256:d6376fa3ecf643050028881c5fa52e218e59a57ba1621e1b49b4f6eb932196f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150174173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23c8f762d5af4431967c0ddb3f585b9ff8d7ba7ddd553589c1cab4cbc97e3fe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:50:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:50:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:51:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:51:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:51:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:51:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:51:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:51:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 04:51:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 05:17:41 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 05:17:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 05:17:41 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 05:17:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:17:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:20:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:20:51 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 03 May 2023 05:20:52 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:20:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:20:52 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3d015c1fa7a3af0b569a81f1cfe3b87e431dfcddf71804acddd55d0bfa981`  
		Last Modified: Wed, 03 May 2023 06:52:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058e31a42150f01798a961cce13ad998b84d941d7eeddd3ac51cc45e2023a6`  
		Last Modified: Wed, 03 May 2023 06:52:29 GMT  
		Size: 76.7 MB (76694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3572c237247dcd37531751b12b991e78e0bdec8e04c765b14cac1212cafbb3`  
		Last Modified: Wed, 03 May 2023 06:52:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377fbca192cebf1511d316215e6d0860629ba3e856deb0e1a74135704acf091c`  
		Last Modified: Wed, 03 May 2023 06:55:18 GMT  
		Size: 12.3 MB (12324202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f62006abe89b0a3afe74530e287241b230ad5188ad6d365b3967d4418046dd0`  
		Last Modified: Wed, 03 May 2023 06:55:17 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96ab24df047b4852dc5f0dc888539bdf190f905433e49e1d751939a2abb23ab`  
		Last Modified: Wed, 03 May 2023 06:55:22 GMT  
		Size: 34.0 MB (34012866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640495619365402649fa684e12c249851c14dd09283c17ae1b5e2962b5a8e548`  
		Last Modified: Wed, 03 May 2023 06:55:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a50b1a91ce55e1c8847bdb382af11773dbd364796106d6def6633eaa8b7eb`  
		Last Modified: Wed, 03 May 2023 06:55:17 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-buster` - linux; arm variant v7

```console
$ docker pull php@sha256:be992a6916b94a25f213a904b8fcc018f079dc0d2700780c2c36ab375757033c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125227673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be91d570da5f800c8587afa7904fef0cc3abba045c0896e924f56d392e1efb41`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 02 May 2023 23:48:16 GMT
ADD file:b8cf5ec32175731f2e4d1320020ed59d77bffe001218886fdd42e5aa3d5eda22 in / 
# Tue, 02 May 2023 23:48:16 GMT
CMD ["bash"]
# Wed, 03 May 2023 06:13:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 06:13:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 06:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 06:13:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 06:13:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 06:13:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:13:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:13:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 06:13:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 06:33:46 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 06:33:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 06:33:46 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 06:33:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 06:33:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 06:36:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 06:36:15 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 03 May 2023 06:36:16 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 06:36:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 06:36:16 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:238786c487af66dadc8fb598b41ed76a08602b2a8a746d9c0cea9574cd9c9774`  
		Last Modified: Tue, 02 May 2023 23:52:11 GMT  
		Size: 22.7 MB (22747671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede31f46c158a526498ef550ede187d94e4faef9e08dc9213a3d7307ab725c7d`  
		Last Modified: Wed, 03 May 2023 07:47:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d210339e665109f3a91e697b427e246217dff83418bd8426f085a237cfdc57a7`  
		Last Modified: Wed, 03 May 2023 07:47:56 GMT  
		Size: 59.5 MB (59544406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d697f7e3a5f4e9e47e13f96e90137ecb51158897687a5f5ab181b13246b334b`  
		Last Modified: Wed, 03 May 2023 07:47:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaa07c234a728afed58f063fa1eac2b3030a23c04f6b4452bdbf337584dd1f4`  
		Last Modified: Wed, 03 May 2023 07:50:44 GMT  
		Size: 12.3 MB (12322470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9a45a469eb5b5863bfb85a4261947c85fa21b039d8cc7e9eb8685a32b25953`  
		Last Modified: Wed, 03 May 2023 07:50:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40958f699d3f544dfae2e8255795d1a8de12e2007e8feb0199501f2c7b1f756f`  
		Last Modified: Wed, 03 May 2023 07:50:47 GMT  
		Size: 30.6 MB (30609445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2efec55643ef63fe44b87261b3faa817e169066a1f06e494e4c0706bc1065e8`  
		Last Modified: Wed, 03 May 2023 07:50:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8361539b5f351165180c37b46938329c0329499a41bb272fa8bb73ebad047f1`  
		Last Modified: Wed, 03 May 2023 07:50:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-buster` - linux; arm64 variant v8

```console
$ docker pull php@sha256:f23fe5fe25287cd2fc05c27960c36f5ee8a9c53122b6faeaf40c202335ca91d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142577920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1553a5ccd4b01a091045155f396c0004bc9c19b652d82e6cfff101a28617ad1e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:05:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:05:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:06:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:06:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:06:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:06:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:06:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:06:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 04:06:08 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 04:30:33 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 04:30:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 04:30:33 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 04:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 04:30:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 04:33:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 04:33:29 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 03 May 2023 04:33:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 04:33:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 04:33:30 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1eed75396074e4a334cbfa2e9f018727d6d9645818e26f818e58ab869b1cf6`  
		Last Modified: Wed, 03 May 2023 05:52:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237165e9d0718003bf4f084a14158d89f600091e3e6fad044addb827e4c02e1`  
		Last Modified: Wed, 03 May 2023 05:52:18 GMT  
		Size: 70.4 MB (70366411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63fae9b8b287117dd852404d06f2982cedfc392773a3550a80f8a890263b8c2`  
		Last Modified: Wed, 03 May 2023 05:52:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b510ecf60e3460b935661eda27d61421c02cf60e7c71d62d46b88ac3c889d5`  
		Last Modified: Wed, 03 May 2023 05:55:03 GMT  
		Size: 12.3 MB (12323107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93c5d0f6bd7bfa56ec7c602e3fda30737461ce8be5c54e1c9ae063dab180dd6`  
		Last Modified: Wed, 03 May 2023 05:55:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1055e22b32f80a755dd8b98deb7bfc6cd7333dcd4676e1082c581594198a7`  
		Last Modified: Wed, 03 May 2023 05:55:06 GMT  
		Size: 34.0 MB (33962682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53e766a1f884c8dda0de2508e27b5e6de54c22700d29da1d673c0b1b66778c9`  
		Last Modified: Wed, 03 May 2023 05:55:02 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209d3f323638d6d674e42e7515d4d0aa3030d07c7e1d60170d97091072c670aa`  
		Last Modified: Wed, 03 May 2023 05:55:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:cli-buster` - linux; 386

```console
$ docker pull php@sha256:49259d32a10a04bc3e1c4470b243e0baff224a946856935f59b51d453d6433f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156030027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b1af243e7bedde1359e0bd7a99032096b8559a79baa478092fc20e01cfd7a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:21 GMT
ADD file:0f4c5475f636be52b419806a7ea7d8d81fc1203c9228544c1324e79277739a3f in / 
# Wed, 12 Apr 2023 00:39:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:32:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 12 Apr 2023 05:32:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 12 Apr 2023 05:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:32:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 12 Apr 2023 05:32:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 12 Apr 2023 05:32:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 05:32:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 12 Apr 2023 05:32:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 12 Apr 2023 05:32:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 14 Apr 2023 17:59:32 GMT
ENV PHP_VERSION=8.2.5
# Fri, 14 Apr 2023 17:59:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Fri, 14 Apr 2023 17:59:32 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Fri, 14 Apr 2023 17:59:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 14 Apr 2023 17:59:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 14 Apr 2023 18:04:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 14 Apr 2023 18:04:40 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 14 Apr 2023 18:04:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 14 Apr 2023 18:04:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 14 Apr 2023 18:04:41 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ae6c02ab25c72d784ae8832cdcb583320ab9a3046938adc3c659ae607da19b43`  
		Last Modified: Wed, 12 Apr 2023 00:43:29 GMT  
		Size: 27.8 MB (27797581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e1f48a4bc80b7054b42143701c08cbf89d22af9c6c80dcc460033912c3d57a`  
		Last Modified: Wed, 12 Apr 2023 08:43:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4147d8a2fa45b9efa31f62f7bc8571416934b188e6d65672ea939ec7c11d836`  
		Last Modified: Wed, 12 Apr 2023 08:44:17 GMT  
		Size: 81.2 MB (81237423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accec47a5a7eee4ceb9702fa00d0efd5137fd4c2c280d2c296fa4ad1dedd982d`  
		Last Modified: Wed, 12 Apr 2023 08:43:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32c93ebaf1bdf96e5a612c2b38b593a93eb12ae6232b29d5d755acff695ae0a`  
		Last Modified: Fri, 14 Apr 2023 20:29:18 GMT  
		Size: 12.3 MB (12323646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb2b3824a4e46f1bc9b150af5786c4e9786ae22358e8ff38bf8976633814848`  
		Last Modified: Fri, 14 Apr 2023 20:29:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaba647d4275fe41a4ce766c8b274759d48c2e78b39c55d4b2e74befe438ec81`  
		Last Modified: Fri, 14 Apr 2023 20:29:25 GMT  
		Size: 34.7 MB (34667695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1a92aacd08b7ad18116abecdb95cc5a5d6bf6a075cbe6c6663e6d017c0a531`  
		Last Modified: Fri, 14 Apr 2023 20:29:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c8a33e67c54552a258d626e5e79afaabff88e20133ff7f7ade15ee17b431b7`  
		Last Modified: Fri, 14 Apr 2023 20:29:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
