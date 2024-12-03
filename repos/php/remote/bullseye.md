## `php:bullseye`

```console
$ docker pull php@sha256:25cfe3e5956e4e9b49c4a8ae823d4720e45fdd6682613b69a780874cef231cd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `php:bullseye` - linux; amd64

```console
$ docker pull php@sha256:0ef3aed7b6b76f337b7bda30bd4b53364b1482173e18e6dba57a9fc2a332d989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988863f94461024b7f97cbcc55a9197d90306d0bcb9647fe0f558236efcff43`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 21 Nov 2024 14:39:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5558e64ca0f7fbddb4c43eace99f17d1ae0390b9ac918683fa104079e36c66`  
		Last Modified: Tue, 03 Dec 2024 02:22:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a949dc094364c2edcb5da30f1348e947f6c8b3c8adb968b3641c2c7d731f7`  
		Last Modified: Tue, 03 Dec 2024 02:22:41 GMT  
		Size: 91.4 MB (91448404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b6ddc3b4182af588f9df4602c386f2bef62d6bc3851f420301cfc6f3e499c2`  
		Last Modified: Tue, 03 Dec 2024 02:22:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904bffd4d38a3504fef152e0e3a5d0a82d543a4d3b9fb86b42378639c7a1fd31`  
		Last Modified: Tue, 03 Dec 2024 02:22:40 GMT  
		Size: 13.7 MB (13655545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bccf539b4ecd8232938859d1a813665fde07da399e7d09cd473a493e6da9de`  
		Last Modified: Tue, 03 Dec 2024 02:22:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc4d245e0a8b279ee9661469abdf747e99999e60f64a840ae520541cc3e6921`  
		Last Modified: Tue, 03 Dec 2024 02:22:41 GMT  
		Size: 39.4 MB (39429411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3148c24c98f71275551e1147d5cfaccfaeb5de5df4f4bbd6737e73c9a43c9`  
		Last Modified: Tue, 03 Dec 2024 02:22:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3678f7dc522299b45830f0907f4f30ce57884988bcaadffbb81984b90b636f`  
		Last Modified: Tue, 03 Dec 2024 02:22:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bullseye` - unknown; unknown

```console
$ docker pull php@sha256:f0eb38728fe90abd4ec21ff8b683bad88412fd18f086c42825f5737bcb04ce00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f481ba0c5e8f45d4c7c9df049536820ef3dfc161b0e06e85e31f8b0e040af16`

```dockerfile
```

-	Layers:
	-	`sha256:d1d679f24d45a2d8fb2f5fff564f74621cf147f531a7e5d29ab9d6686ae8296b`  
		Last Modified: Tue, 03 Dec 2024 02:22:39 GMT  
		Size: 6.4 MB (6393215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76126468e5db1567795ce6290f30bfadf0b6745644f03c63fd6778ccc8da6219`  
		Last Modified: Tue, 03 Dec 2024 02:22:39 GMT  
		Size: 40.5 KB (40456 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:c4348a1cc95e37b4c27b8e7e499d8f38e2d294b4cb9921d4e907d8eb804cebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143871118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c0b9dfde5f9d245717d077e434901e9d98696be1baf905db74b5b6aa7f45d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 21 Nov 2024 14:39:47 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:79ae44024aa8e358b5fbaad284a41a7c359d47ad28af854839c0e44435b875ba`  
		Last Modified: Tue, 03 Dec 2024 01:28:54 GMT  
		Size: 25.5 MB (25533944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f4cd0ed182c41a7840e3bd6aeb9858708e8c6b99baae88a51faf80b4559a51`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682dddbc2d895e7263b87741543ce754592ab412d0d97e492925c117dfb408e3`  
		Last Modified: Tue, 03 Dec 2024 03:00:19 GMT  
		Size: 69.1 MB (69119217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f7c0f9947f1b2a09b6fb724d5e29aec91c63413c8b1ab8510d897d0b179b52`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b779b65597147e0022c8212996b936fcca6c94bda2f812219fcdfbb9a4c55975`  
		Last Modified: Tue, 03 Dec 2024 03:00:17 GMT  
		Size: 13.7 MB (13654010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78c7a228f0c44b42355b3aa4152b2122bcf451ec3330536f0a44afa1fe1d059`  
		Last Modified: Tue, 03 Dec 2024 03:00:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb99be412dcff4dfc3a34a481010e9935aabae8ad67746384088e656b3305c`  
		Last Modified: Tue, 03 Dec 2024 03:00:19 GMT  
		Size: 35.6 MB (35560318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4290cd9e207838de1f01d51975a93ede37af62cdac70b3d4b7217f5ae1d20b`  
		Last Modified: Tue, 03 Dec 2024 03:00:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dfb18e272927a12c7b35ee62d1a0bc4aca3322fb278c16d795811f621686cb`  
		Last Modified: Tue, 03 Dec 2024 03:00:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bullseye` - unknown; unknown

```console
$ docker pull php@sha256:4c0d50c7a36f02dc8fdf07aed66a2e4f02b3ffb21af6b88a1b7a473926b88a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6242461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888ca639e0f4f763df379376db9d6c205769045c6a2cbdeb699f779b13045a5c`

```dockerfile
```

-	Layers:
	-	`sha256:22a750868e3760a1cbf14c3003110e29d0c6531897a73a128ffd539e0907e350`  
		Last Modified: Tue, 03 Dec 2024 03:00:17 GMT  
		Size: 6.2 MB (6201832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9067d314076f5a1b5ae09c5bcfa1ad679bd57bce564a970c13248dc743a8eb63`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 40.6 KB (40629 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:5626f65f94e1def3a869db9bf0bcf84270b7e1e2dd7feb8329663f3c4508643b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168079658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04c6f999326295bd255277190a24f4f2a12807940d76418059a20f850982ba8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 21 Nov 2024 14:39:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa51b96f45aeeeac0da5ce8bef54768006d2f3f15d75cc62bf2f673af4c4ee`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf1193220d0cc95806c6408988e7d5348f9ad83ddfb796cd2261f04ce83160a`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 86.7 MB (86734618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80085106d7b6b1e2208214a2555ef1f1d0e5a1cfb68b48454784f2843f1cdc7e`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036bf2bfbcccc33a91506bbd2a2d16ce983d529d18548be17ba1eee6868fedb`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 13.7 MB (13654819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83105b2e440f57f2d2dec490bb02557b566550347a4e4372d8cf0362ba908bc`  
		Last Modified: Tue, 03 Dec 2024 03:14:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d293ac92eaea6d62d607b0e541d639ce5bdf5854e1d00bd5bf94b427e0779d`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 38.9 MB (38941668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dfbc24c175f1d84fd359f9e23a9953205e26ea715e2e0f1f1c418323aa3bcb`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba734f0c826ad03d50fa9406f6f1a6a5527b79d3a028169ba7db6cd2df339c`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bullseye` - unknown; unknown

```console
$ docker pull php@sha256:e77521cce4f9fb4f4eb547fa56f1de15e9be93c281eacba254821048a2dc408d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1173846a94bc63e81c0ae8b9f260c5f24f2365a50fa63cb7d75d3dd35f84414`

```dockerfile
```

-	Layers:
	-	`sha256:e48a229795f316e63e319a4266450c583ac6c07064270809cde296e4aa103f25`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 6.4 MB (6396036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d4bd85643aca0b2ac725ef12278d30158ef5f21e6dae113b8d807510060f6d`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 40.7 KB (40683 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bullseye` - linux; 386

```console
$ docker pull php@sha256:8c3a92050f9f9b434adcde2daa5cf19407146468856622bcdab1e5de6a895b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177504813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2e98225ebc5322f1ea161d1babbb0467d4c3d56f0f6c66b5dd2e6d1b88e15e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 21 Nov 2024 14:39:47 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 14:39:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_VERSION=8.4.1
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 21 Nov 2024 14:39:47 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 14:39:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 14:39:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb943d3aac80628632d629b09aa12e1693d85309468905c798e1329d88ec358`  
		Last Modified: Tue, 03 Dec 2024 02:22:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59b88f925464cc8fb79c157c13ecbe139b2b0b9817a04187e2a37b82b2676`  
		Last Modified: Tue, 03 Dec 2024 02:22:22 GMT  
		Size: 92.5 MB (92521111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64701e100ebbae55371362b8be96a314686200eddb2acc987a84ea46240d1241`  
		Last Modified: Tue, 03 Dec 2024 02:22:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7e534737cdb92d6d5255f435709473ab27247951e7d41bd9f2f60572958832`  
		Last Modified: Tue, 03 Dec 2024 02:22:20 GMT  
		Size: 13.7 MB (13654835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4077addbe6372dd77f3defe158a2fd082351a46f8c650546f33d7c9b9e4625e`  
		Last Modified: Tue, 03 Dec 2024 02:22:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b9f305bd11ab05df5641ecad59d238520d53eba0eb74d96f526085b2a352ac`  
		Last Modified: Tue, 03 Dec 2024 02:22:21 GMT  
		Size: 40.1 MB (40146180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa189e6f772d984d6f0749f19781a568bb1f17333962aec67ec48f7a1adbc8b`  
		Last Modified: Tue, 03 Dec 2024 02:22:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298188ad32e4cca641a72e516380c5ed86293a5d2385d32d4e7b71e103026ffc`  
		Last Modified: Tue, 03 Dec 2024 02:22:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bullseye` - unknown; unknown

```console
$ docker pull php@sha256:27787ee93fd893e307e75623eade3b868a17710d8c87f2e47226bd3d47821eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526406281ed7bbf1a491d2fe06c3a4fd4fc179bcebb04a81d021eb408d53c25`

```dockerfile
```

-	Layers:
	-	`sha256:15e551f1406a45cca12e1a65e1aebf0c049929d27531b23ed1c38fabbce726a6`  
		Last Modified: Tue, 03 Dec 2024 02:22:20 GMT  
		Size: 6.4 MB (6383869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce5399c1e211e60d1cd2cf221c60bda226d971efb56f564fd046a8452f7a4d1`  
		Last Modified: Tue, 03 Dec 2024 02:22:19 GMT  
		Size: 40.4 KB (40394 bytes)  
		MIME: application/vnd.in-toto+json
