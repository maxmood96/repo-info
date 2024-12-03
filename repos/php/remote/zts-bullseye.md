## `php:zts-bullseye`

```console
$ docker pull php@sha256:f7ab4fe010589404bdd001b546861531da18e96d6861e0a02dfb0b86bd6a9610
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

### `php:zts-bullseye` - linux; amd64

```console
$ docker pull php@sha256:f0ebbd87b79a430692d7c094bed5cb26335f503a031220ecdedcec3fd5f5556f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174978102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6262b86010a548592a1d95badcf84c1d92cb7af5fab60b7fb206a152e01c4046`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:ebde8add44485bd6797d283e6f4bd776e2ea9eef6a3c53a493469a9b179f1e5a`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3194c2121d17d779d172da93c83a50a2fcb96e74affe604eecb58ffa8e499d`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 91.4 MB (91448049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbc68a6d88e0f23e185a6206c6f2c09ce91b9132b6fe1145932c44464684be`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f3d7acea2556bfd3d574e97ba08bf404307c428a32af3a3639caad2605afa3`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 13.7 MB (13655549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d9c1b9d1eec52409bdfd5cc6f9976b22a0f3f13d87f3a51ceae32fbdb406b5`  
		Last Modified: Tue, 03 Dec 2024 02:23:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb635c9a74e24a41f08814ebeb546a7e426cea51183a81afcb88a5596ac83149`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 39.6 MB (39618233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541bf67140564cee0860910f0ffdeb68b248b586c8d0fbc3f44415e9820dda59`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05620a9ad60a3ed775836c7534b1742a937ff014d7929c699b6455fa040155`  
		Last Modified: Tue, 03 Dec 2024 02:23:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:5fff0aa0d676706171d1b46748605d9497a59f527746dc0581e90739c40e9c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6431587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976f359c5638c2d19802de2199f55fd2af7fabc1dfdb88dfceb2d98d931bfb8c`

```dockerfile
```

-	Layers:
	-	`sha256:866713b506046e2f38c0d7619e7df16706c596f5e98a7283a363df74358dad2a`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 6.4 MB (6392007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d0bd38dbad99d9983b1a4ba238cb595a15e87e9b0f61167d817d3e1777e0d0`  
		Last Modified: Tue, 03 Dec 2024 02:23:11 GMT  
		Size: 39.6 KB (39580 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:08877decef7bd8194e86d5675d76bed5aad0d439685973ae2e5b01284704c266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144217499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58c4dc31554a21bbf7f8da0fda5aef0bd99e64662977b9781dd12175a0c41a5`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:7092295fb04c36d1d50e127123f076d88516419d2449d24b09b5ecd3b2516f62`  
		Last Modified: Tue, 03 Dec 2024 03:10:31 GMT  
		Size: 35.9 MB (35906696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab76e7cb8d5bd37adce3324871262bc73ceb39e42d871b2c386e998e0c10525`  
		Last Modified: Tue, 03 Dec 2024 03:10:29 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e4ec4c724efae59fb1eaa40a23acd73ea641b4f2afa5ae654a502110aef2c`  
		Last Modified: Tue, 03 Dec 2024 03:10:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:00efb6667b614a348be2c80a987f3e1b3e1724859577127f2389d021f1d07b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6240313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566f4d9515c9d8e3b105522845f5581d60b967883d97586a2741b061b448fdd8`

```dockerfile
```

-	Layers:
	-	`sha256:ea87712144ac1d9f5013fc7dc7b3364331b01b2270b36a0a8ba99cc48b5c45b7`  
		Last Modified: Tue, 03 Dec 2024 03:10:29 GMT  
		Size: 6.2 MB (6200592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7014c53a9eb4d7e65a9ad7565104472c2495f274ae791523c92ba1f28562d480`  
		Last Modified: Tue, 03 Dec 2024 03:10:29 GMT  
		Size: 39.7 KB (39721 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1058cfe6f92f89fd35a2d4cd1feab383410c3d7596d970a8177d179c22197ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168398996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30db5e5572cab5b84c5db4fe4b8bd90c1c3839afd93826d74dbbb52559977f6`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:f503cfe3a1ec1c87096db1a3258862bfb25eaf39650af65177131f91404aa6dc`  
		Last Modified: Tue, 03 Dec 2024 03:24:00 GMT  
		Size: 39.3 MB (39261007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973c0dcfc0bd4a5db30c2d48be3b08c7e9859ab75efb1fc1fcf8f6c01d55f99c`  
		Last Modified: Tue, 03 Dec 2024 03:23:58 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce4113dc44685967b7434275eb2582b1496e2367b9bf308d727c428c518fd16`  
		Last Modified: Tue, 03 Dec 2024 03:23:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:3f9a2e0e6f098ddfec91ef081decbdaafd1cfb00564ebec1adf93ce2084971d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd3c49b1dbb23ff032fe90e497d21087dd71cad61b846d89a0bf4839197c771`

```dockerfile
```

-	Layers:
	-	`sha256:0fcfd92961c6326f8ce9b24f25255f83340bb6474e872a75c19864a16fe5e90f`  
		Last Modified: Tue, 03 Dec 2024 03:23:58 GMT  
		Size: 6.4 MB (6394780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc357ab1b543c73339468c7551e87a1289693b9f1405ba556a0ceabf224559a9`  
		Last Modified: Tue, 03 Dec 2024 03:23:58 GMT  
		Size: 39.8 KB (39759 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; 386

```console
$ docker pull php@sha256:afdd88361b8c089c7885cf2205d3d22ab89fb781a2efb2f8b2007f0f16477eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177717697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc90c5f9d969a8b57c657a647efd72275f67e862a688625810fa42e6dc7f8128`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:07509778d6f224ece8bad066119f1fe089bff4f1481d52858d1733fb7320bcfe`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5b5fbb6179a3cd9348a3e5c1036329ee0dea93d43416490df1813408682eae`  
		Last Modified: Tue, 03 Dec 2024 02:23:06 GMT  
		Size: 92.5 MB (92521392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4760e9c5f5efdc4bf9832197cb2db1459ce6b22e6280d5eec20031ff4b0a165`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c0ec276591be03f5a619317faf3dd2eab7bda45ad56a050e8134db45d0ff0`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 13.7 MB (13654845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2a41e94c7cf899d6b06fbe91dfb8e0c7f5d07a1d5f8124c8b7ad75dbf796b1`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0901a101773765b78e8d60e3f30a6931353fda306155d69b65b0a04f75c21`  
		Last Modified: Tue, 03 Dec 2024 02:23:04 GMT  
		Size: 40.4 MB (40358768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a37cb56f4a746251ef5b18deea0422635bf38cc21a17a376e6c4a81e0e7272`  
		Last Modified: Tue, 03 Dec 2024 02:23:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69404ddca18e11a6c9df08cbe0142ab140356aa98cdc09edabd58c24bfcd7e26`  
		Last Modified: Tue, 03 Dec 2024 02:23:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:e14f40b58fb802cf2096206a7cc46267265abfe1d7707e41e71bbbdc42f331ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6422219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e929465d7dbaecd44411385ae52576b9340ae5c68d38fd6838423350072de7`

```dockerfile
```

-	Layers:
	-	`sha256:cbd8a7065f267a4f996eacdb2064892a1f19490cd68e1d105528e78fa39b567b`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 6.4 MB (6382681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ecb19dd6b6c5b65ab1e19c96e04c6c32540ebba7018389a4fd9352fad9e3ef`  
		Last Modified: Tue, 03 Dec 2024 02:23:03 GMT  
		Size: 39.5 KB (39538 bytes)  
		MIME: application/vnd.in-toto+json
