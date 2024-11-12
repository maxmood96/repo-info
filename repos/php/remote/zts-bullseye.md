## `php:zts-bullseye`

```console
$ docker pull php@sha256:6c596a0b4fcaba0a1ce62ffe3ff5b9042c64f92ea642bae293caa2632223541a
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
$ docker pull php@sha256:b83e9b126803a910c2c80aa396c6d7f4d5011012bef2b543bd7d5a8e74168346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170440410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539dcca0dbac02549df0796a82bca43cb2b3a1f43363b9cb85feb02ba6c4d575`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191af922c26f3931de073c5198191d738ad910bc66121ddbcf52f388d1671709`  
		Last Modified: Tue, 12 Nov 2024 02:08:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f558648dbee347c6ce54b4ca395cc7980f55c6401d15cf6803ea1b852a5046af`  
		Last Modified: Tue, 12 Nov 2024 02:08:30 GMT  
		Size: 91.4 MB (91448280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2140a022fa4ab315882b66e16cf410a0c4d3f006345c496c461e0f04eb7846`  
		Last Modified: Tue, 12 Nov 2024 02:08:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f471c9680e8e50a993feded94770171b24f98a621053a0ce2f87fced1c2443`  
		Last Modified: Tue, 12 Nov 2024 02:08:29 GMT  
		Size: 12.6 MB (12586941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3fa2199b8868bff8ec5a99da18cfad6bcfd258d381da8171eef79f0c5c4642`  
		Last Modified: Tue, 12 Nov 2024 02:08:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe82708fb0daf4a6aa60be9dcafbb4305831379e79979224c4213b4d01a54899`  
		Last Modified: Tue, 12 Nov 2024 02:08:30 GMT  
		Size: 35.0 MB (34950001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dcf9504c33e9489572e89f3c29692df9739e414b0979e89d133cae40763b46`  
		Last Modified: Tue, 12 Nov 2024 02:08:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68a28401b577d231257dcfa5ca59960825829822291c7fdea2308395f2f262`  
		Last Modified: Tue, 12 Nov 2024 02:08:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:41935de844377ab34c5a14f91e0b3fcf538bc621c5e07e671ea45ac67a35ac7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74b4afbc10216d13ea19356aff16b3d9911031a2038699a379f4fff8a3d3a4e`

```dockerfile
```

-	Layers:
	-	`sha256:ed10124e34a0246192de99307635023064e1aa8327d836f621168f1b4d8e7c98`  
		Last Modified: Tue, 12 Nov 2024 02:08:29 GMT  
		Size: 6.4 MB (6393888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09491d14663aa831f367fda2e0f9e91e2eac7e42547e59e0cab218d5d991d83`  
		Last Modified: Tue, 12 Nov 2024 02:08:28 GMT  
		Size: 39.6 KB (39594 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:5b2e88018d83dae238649b36f3ac5381861499bbd2759e28992737b99242b588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139958852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eedf150ba1600f50b41596a76aec22758e1f47976dc4df0ba57eefa26d07f08`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8516b12615a3e7a2a821bfa14ba9dd6f6761aadf1ebf4642a203f52c8e3818dc`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7345669dd3937e5ef95133666ed38ccd4ce9f43d25a81fc19533223b2f1211ab`  
		Last Modified: Tue, 12 Nov 2024 03:32:45 GMT  
		Size: 69.1 MB (69119360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef234fa44e31ba745b124f418b0d1419fe927ae1ee59212901e32e4379c7b7`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e90661bd4710730186a4a5c4d7c26be59b4f284535fabb466893102be1bc641`  
		Last Modified: Tue, 12 Nov 2024 05:43:56 GMT  
		Size: 12.6 MB (12585122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9eeafe4cb116d6f4fcaa5047cbc5a47178c351191cb64eeaf5a52bcd3b05`  
		Last Modified: Tue, 12 Nov 2024 05:43:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0f9c6ea7242352303b92d1bd47e0c9efa102ec94e6d2fc4fb7257fe670b94c`  
		Last Modified: Tue, 12 Nov 2024 05:56:02 GMT  
		Size: 31.6 MB (31641477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e984ec3259cf9ac03a6cae949e5bd02de8e10c9e6f567b26ecdf7320e6c5c477`  
		Last Modified: Tue, 12 Nov 2024 05:56:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c4d123ecf3057b5c49c0665774130ef99e955d4563e6ae44331f3e2e6f6b9`  
		Last Modified: Tue, 12 Nov 2024 05:56:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:9f2fda8cc95631859269ca7fdabcd0198c016bea329f7cea17e56dfc546c16a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6242209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab78fbf85de00b3910e4459872ab388181d8d9017060a241135bf1c4a9011a6e`

```dockerfile
```

-	Layers:
	-	`sha256:e2cb72626786b663643f719c117ce925c56f1d7519ed67991ddaaa27f4476cd8`  
		Last Modified: Tue, 12 Nov 2024 05:56:01 GMT  
		Size: 6.2 MB (6202473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9a1c4b531a9e84afe0bfc220f538b65cf1fe60968706515801e7640482b1a9`  
		Last Modified: Tue, 12 Nov 2024 05:56:01 GMT  
		Size: 39.7 KB (39736 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:ad615d6a7569057122e160bddceb98874fa1fcd2fedfc08b900e8d4f3ccd3be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164361324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c1dd7c9f3092db8067770f54111801fdf49442a61ebce73356b065937a4fbb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62450911e7081608687c1d17df91c35e3323dfa42d38e173f2a1e50a5ebe7ecf`  
		Last Modified: Tue, 12 Nov 2024 03:46:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fab06aec8688282ccf95c5b95a4d80307ac94e46b7d7941a82cc836c2051d55`  
		Last Modified: Tue, 12 Nov 2024 03:46:32 GMT  
		Size: 86.7 MB (86734483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3cd4d4a0eeec0f214403acae937aafd258b2f9a8cd4a9805aed71060885872`  
		Last Modified: Tue, 12 Nov 2024 03:46:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d280cd0f063900adec848dbc713f0f64cbf4f331d1a4e39ea29f7ebe216186`  
		Last Modified: Tue, 12 Nov 2024 05:39:15 GMT  
		Size: 12.6 MB (12586074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04324e697315cad5ca28b9c7cc735a5f30a43c4ad7a7bb552b9a126836f7a3`  
		Last Modified: Tue, 12 Nov 2024 05:39:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9211389c5dea75b017a5965c4845a7d5ed787a2b9c38dcb3f086b88f522cb948`  
		Last Modified: Tue, 12 Nov 2024 05:50:11 GMT  
		Size: 34.9 MB (34945539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f53d62b1422c1e46f247a3d35517a3b58497e11dff96de3e47ffa06ba63de59`  
		Last Modified: Tue, 12 Nov 2024 05:50:09 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9303fcb47cff57a507ed603fb67340a406f2bfb25e40c06d00585a93118a6940`  
		Last Modified: Tue, 12 Nov 2024 05:50:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:fd56def76ce5253b740716be053df4ec4d59fc2e39b70a3b3112c9ca5a1686bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d54a2235dde06dc07147bab1106ef2cbbb3370f20c28d196441f59beab739d3`

```dockerfile
```

-	Layers:
	-	`sha256:5e78584843696b25d2d48eed5cc2d06c89b2a5a2cfd93bc030f5922d6195bf72`  
		Last Modified: Tue, 12 Nov 2024 05:50:10 GMT  
		Size: 6.4 MB (6396661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74af4000ffa3c34b86f5e71a23a1287d35bf34979f08f702268bb36c627cf5cd`  
		Last Modified: Tue, 12 Nov 2024 05:50:09 GMT  
		Size: 39.8 KB (39774 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bullseye` - linux; 386

```console
$ docker pull php@sha256:80193cf26a3405c3cbb892c8a316f9a55ce206d2bde204c96ce65af92ce2fbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173120465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd2b81b70146b2dcc1cae3832b97ac10ae02cc5e29fa8a393a685ffc7d8d214`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 24 Oct 2024 16:31:40 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287f971e81ae820faf3b20e92fa844295a791a30ad7e65aa05da844c4a9f8406`  
		Last Modified: Tue, 12 Nov 2024 02:08:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ad95e937822b042533f087a27ff219dcad75f3acb82c070da4e757355d40ec`  
		Last Modified: Tue, 12 Nov 2024 02:08:46 GMT  
		Size: 92.5 MB (92521623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b589632bf8aa892a207bf2bb30ca0a2579e6a5315045d8ea19b1f6075c848`  
		Last Modified: Tue, 12 Nov 2024 02:08:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b1a58788797c1dd35244f84e10e04fb9bb8660f23d36866f4f027850a0ef6d`  
		Last Modified: Tue, 12 Nov 2024 02:08:44 GMT  
		Size: 12.6 MB (12586091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e572a6a1aaacd226d7ad6837896235db145db7efbaea39fb7df4ee414e21f7b1`  
		Last Modified: Tue, 12 Nov 2024 02:08:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecbd7732bf4ab39e1e149aecc9a1eba5f23c4197044d31d23c7028ba97d4b34`  
		Last Modified: Tue, 12 Nov 2024 02:08:47 GMT  
		Size: 35.6 MB (35585773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d5df69ed524a20d0ce7ba55d44dfd4e257b306f267af2ea94ee171258b1849`  
		Last Modified: Tue, 12 Nov 2024 02:08:45 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb9aca91b44f68f34fe0e875df609381b4e2d9825a95ed16168e60093d348f`  
		Last Modified: Tue, 12 Nov 2024 02:08:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:cb8d51d93b11fa083a7a2a6271d1c352db5db74e71fe9fa8986ac1a9604b842a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a785d725a4e05a0c9fac0d3816cfb43f6d0f8bcdb1bc74a127d8adf7abf1a943`

```dockerfile
```

-	Layers:
	-	`sha256:4bd610e257ce6d41af8a999919ca42c28a43cefc26208e6b98c342f111b9e007`  
		Last Modified: Tue, 12 Nov 2024 02:08:45 GMT  
		Size: 6.4 MB (6384562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3133dd638b6e54aad21ed64516ba3cfe9f217f4882df05c0def20d5db621614b`  
		Last Modified: Tue, 12 Nov 2024 02:08:44 GMT  
		Size: 39.6 KB (39553 bytes)  
		MIME: application/vnd.in-toto+json
