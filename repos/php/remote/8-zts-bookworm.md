## `php:8-zts-bookworm`

```console
$ docker pull php@sha256:0a6b8ae96d6e90502f494d12d5c3c6fd7d760fb223faddbfe3b50289b2d3eca4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `php:8-zts-bookworm` - linux; amd64

```console
$ docker pull php@sha256:89c67b0ec9bca531650bde082b5fedff7f954472bf4d8a2d9a52ee6287b420f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189917075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daaef2b1680f5110f1cafe653938f3edab6fd345ba7a3c51baefe502b413f28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:24:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:24:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:24:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:24:20 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:24:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:24:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:27:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999107721eb6864e278d0efb49b0f5b23e3921d0a8fbb845ebab86e91fec6724`  
		Last Modified: Mon, 16 Mar 2026 22:27:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8a5a6e244685c858f580c8bb45a38310bf36dc99b13197962f64e321f24c83`  
		Last Modified: Mon, 16 Mar 2026 22:27:42 GMT  
		Size: 104.3 MB (104335633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a443ae0196cdb1f143a4674548f392b531c8f6e45c0034e0d0e5c73f162e8c`  
		Last Modified: Mon, 16 Mar 2026 22:27:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6429edfe848f142bb0a138ee9a7b47b8d796121bc966d800e9eefdedc6c6c9`  
		Last Modified: Mon, 16 Mar 2026 22:27:39 GMT  
		Size: 14.5 MB (14459344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5406329500f13be1ef112fc182dc71b827514b1c8035f290e83b971396509b`  
		Last Modified: Mon, 16 Mar 2026 22:27:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87e2a1def2ded6c7e4e72229f867ca1ec84c9a5883790f746ec71d2cf177a24`  
		Last Modified: Mon, 16 Mar 2026 22:27:42 GMT  
		Size: 42.9 MB (42882245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d43061bc878484ccbf8a3aba9764d749823b0ccd5d517ef45ba9a7740f13d8`  
		Last Modified: Mon, 16 Mar 2026 22:27:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03081932ed9913a4007428846b6fd4195d4cd3e8b4b6f5b873d76a0ead7ddac`  
		Last Modified: Mon, 16 Mar 2026 22:27:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:c703e63306c400b318f37362b7e353dc6926b90776e45dc1cac5197c1a7b1320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c850cdae0e4adede8867d7a68703c81eed5767c01bf82f5f9da2057ddbcc40`

```dockerfile
```

-	Layers:
	-	`sha256:7a4496bdc2ff3387eff881baea77d9a0b9dca99732a2f85fadcb46c8c8f28443`  
		Last Modified: Mon, 16 Mar 2026 22:27:39 GMT  
		Size: 6.4 MB (6402566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cc333eace8a3f6a78bbf5cf33621c1ecb14e14a8f8a38e0d3a95a49ca6d515`  
		Last Modified: Mon, 16 Mar 2026 22:27:38 GMT  
		Size: 40.0 KB (39967 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:dd5c4853541a365c0367bebb937759836b183a0e87642706b36ccf39f99886da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161298730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3552faf073000adb224eba8d3fcbfe77dd0b3f4003b44b97459f65ad9c698d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:23:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:22 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:29:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:29:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:29:34 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af7753225c0a79ef3c56194676dac85a2ade8fb9c256415f21600acb03a9731`  
		Last Modified: Mon, 16 Mar 2026 22:26:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e1edf83dcff61753f1b4c210674e9884d62f5fa2559539072d199314088a8b`  
		Last Modified: Mon, 16 Mar 2026 22:26:41 GMT  
		Size: 82.0 MB (81983890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f461fc8cfbdc9a99048b835db9554da83db524c5268dfb91dcaed4d58eb15129`  
		Last Modified: Mon, 16 Mar 2026 22:26:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d01b6999fa28292cf0a8bf8ea91ea2e8bdbb2554776784073e8f629e1c2dea`  
		Last Modified: Mon, 16 Mar 2026 22:26:40 GMT  
		Size: 14.5 MB (14457271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c305124727d43509ea70f1a4b8a7338a95e78d7f18d7e862daad8a61d10a66`  
		Last Modified: Mon, 16 Mar 2026 22:26:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5f0bd1c6ceeb473caaabd3f222ac11dc8564516922527b3ece1155abbc3b87`  
		Last Modified: Mon, 16 Mar 2026 22:29:48 GMT  
		Size: 39.1 MB (39088332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc593d7a22d3d3bf5a51d06ab8aa26170abce9d1b3db61dfea20fa9f46cb12b6`  
		Last Modified: Mon, 16 Mar 2026 22:29:47 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0dbe6451b1fac001f83ee8b76ceb0cff1f322460a3c2013c20803d65270d0`  
		Last Modified: Mon, 16 Mar 2026 22:29:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:7c745e1fe81a99951c26ddf618f7ee6ad8f063406b14a1f31205f5f7b812631d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8c3c01e0ec3474c2b244935dfb20c780b098942817032bd9c337d225f1d41d`

```dockerfile
```

-	Layers:
	-	`sha256:e4d8d9f10605183d9a681bbdcb3d6a0b833ce0fe1d49919810beeda1881eb3cc`  
		Last Modified: Mon, 16 Mar 2026 22:29:47 GMT  
		Size: 6.2 MB (6211892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66610d23c10719485b7fb8251fd899b72d196d011d88ccf62d772d6dd6f4ed9f`  
		Last Modified: Mon, 16 Mar 2026 22:29:46 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:41cbc86550f4f87022bf155b4f2a9c0131ff57f466ac524721ca941aff091353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151912596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746d2cc95efdf2a4cea0c12860e14738cabbb61c23559210f92ca2c43efd054c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:30:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:30:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:30:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:30:23 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:30:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:30:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:33:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:33:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:33:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:33:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:33:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf87ee9c9fce39472ad28258cde9f1937d89afb666e6cdc7c5d257ab4562a2`  
		Last Modified: Mon, 16 Mar 2026 22:33:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462a6d289eea02bb867aa9920b22a771be0e079b7638f292d759a1e511777b66`  
		Last Modified: Mon, 16 Mar 2026 22:33:36 GMT  
		Size: 76.2 MB (76154903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a25cb22d2854a4c65dd9425f90532a014e2ae359dafccc5fe19b743223e30`  
		Last Modified: Mon, 16 Mar 2026 22:33:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f6e9d8344bc3fff40cf09c35a19c094cfb91aa4573c5ae0dd70c861a46455`  
		Last Modified: Mon, 16 Mar 2026 22:33:34 GMT  
		Size: 14.5 MB (14457298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b77280e3ee73785865acf8379b1bed8870afd7c25adabd22569b99717bb61`  
		Last Modified: Mon, 16 Mar 2026 22:33:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b60751b0a6b9de806676075817ed493dac7c699b2a37bc3ffd2c4a6b991af01`  
		Last Modified: Mon, 16 Mar 2026 22:33:36 GMT  
		Size: 37.4 MB (37355424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5fbcd41b546f01f402a7dc161e389c4b4a97773b8e8799a10a897e34cbb4ee`  
		Last Modified: Mon, 16 Mar 2026 22:33:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c428ef8fbcc871bbbd8745cfd9f8ed636b706a4822b6a1bcf0f04ba3899931`  
		Last Modified: Mon, 16 Mar 2026 22:33:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:0ed9aef2742f3e99f92dd6190d3352ce139b0776b9f9e34b7cea9c3f614a8e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7328dc2b23a722f52421963b7bfc45bdf66d4526c4e1e45d475020609a63ab96`

```dockerfile
```

-	Layers:
	-	`sha256:05ff4ab3323cc0a6c189a62e95e554ce3282f9e5249d607039b18406202f0974`  
		Last Modified: Mon, 16 Mar 2026 22:33:34 GMT  
		Size: 6.2 MB (6215836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8e1f07670a1216c2bb6bfed763a59520dd4a9e2dc77b2d94e26f7bbb1a698a`  
		Last Modified: Mon, 16 Mar 2026 22:33:33 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:9daf53d9c6e1b5c1789a06919d41f27d24bf8b245b68370003c5282cf4fa4f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaa8a48fbff663ca15fcd746d8ceb05a47f6a79749b26dca69de683d7b547b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:23:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:24:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:24:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:24:13 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:24:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:27:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:27:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:27:28 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ca5ad7c9e3709bc7e97c29bf0daa21ce90fdebc21eb6267a2eb45bbce2614`  
		Last Modified: Mon, 16 Mar 2026 22:27:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116828957cc3de6a5b9fa742cb46263680890691f2fefca071c896432c890152`  
		Last Modified: Mon, 16 Mar 2026 22:27:51 GMT  
		Size: 98.2 MB (98168166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27d03e27f6560964197583bd630926e1f83f8b8f406a98734f5d04589a66f61`  
		Last Modified: Mon, 16 Mar 2026 22:27:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284d0da529d03d0b450fc32117e59e4007e9484a747cd781621640e70c79cb77`  
		Last Modified: Mon, 16 Mar 2026 22:27:49 GMT  
		Size: 14.5 MB (14459116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909574ab7e266079c185d1facad3f6fe0f7b670594df109c27ab4f0d524cbbea`  
		Last Modified: Mon, 16 Mar 2026 22:27:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e98b8d5f79b3534dd857e069d12cce72c820223df970b830e78c999dfd1345a`  
		Last Modified: Mon, 16 Mar 2026 22:27:51 GMT  
		Size: 42.2 MB (42162223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9b7c407e76fc235ebf9452735c9382e885bc160c1173d77296b2a05622ace`  
		Last Modified: Mon, 16 Mar 2026 22:27:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b500ba7f248b8951fd76c2aac357c7e00448fb8026397be50e5071a308464`  
		Last Modified: Mon, 16 Mar 2026 22:27:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:91254649ea4c4cbbb7c18ce4944cf3aad3579f90b7c036c534c4cbd81fef57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e7773447fb22938905d003fa80e46dfe2c9131917d3b9b8e8246d767a83e86`

```dockerfile
```

-	Layers:
	-	`sha256:d300d3c279f8ae4e6b696b7a63248387da9d682c63730f7550cddb29b61da334`  
		Last Modified: Mon, 16 Mar 2026 22:27:48 GMT  
		Size: 6.4 MB (6430957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f41a6bbc6c0e2c3dc41d7add57f0cd4926c2329878777b3bd2cbfa2137bab43`  
		Last Modified: Mon, 16 Mar 2026 22:27:48 GMT  
		Size: 40.1 KB (40139 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; 386

```console
$ docker pull php@sha256:c2c10eefd53db6a9a667d66509b5492a367aeeed9a93197be13689e38071b1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188971740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a6093eef082dd7701405f762acb86e38043b6c9354783e65148b7e787ba020`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:16:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:16:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:16:00 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:16:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:16:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:18:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:18:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:18:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:18:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:18:50 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9cfaa93ec9062faa97afce5e75841a26808030b3aaadb5a6b52f07141577da`  
		Last Modified: Mon, 16 Mar 2026 22:19:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836e8b0d61f8f62d78631de6528d9930cc05b1d5640f1b266a9f0af05039860f`  
		Last Modified: Mon, 16 Mar 2026 22:19:11 GMT  
		Size: 101.5 MB (101527114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9ed63586b09b74a8422973a44a1ae1fe6c24aaf85913f8b87acc3abd687cc6`  
		Last Modified: Mon, 16 Mar 2026 22:19:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01a416527b64a72ac96c30174a03e995e1db6a523f348899cac789ba960a604`  
		Last Modified: Mon, 16 Mar 2026 22:19:09 GMT  
		Size: 14.5 MB (14458467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88699ff7ec20169182a8a5793f5adf5abb6474288f1c91f79ca36100e870924d`  
		Last Modified: Mon, 16 Mar 2026 22:19:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0c1f62c1c30a9d674956c99069a933b6c604a52b56b26050d522c4153697f3`  
		Last Modified: Mon, 16 Mar 2026 22:19:11 GMT  
		Size: 43.8 MB (43760850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547675b9a0b2f945a4b743298acda5cdf10d04e0c905dd55df26b4871912835a`  
		Last Modified: Mon, 16 Mar 2026 22:19:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ac4275530ef134cae16abbf197ac20ecf5a8f2252b04ce18412850a4484f5`  
		Last Modified: Mon, 16 Mar 2026 22:19:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:976636d10702e6b89eb74c258467523bf351f9624a14df2bbdbd226b590cc856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6422283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0847d3551580a90170daa308bced3daa8412c3c37254ac2b8816451cc0c145`

```dockerfile
```

-	Layers:
	-	`sha256:f3309ffc8ee18dbd4484d3dc566e6cdeb37223455fcdec251f1d805622c9323a`  
		Last Modified: Mon, 16 Mar 2026 22:19:08 GMT  
		Size: 6.4 MB (6382358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4040e057ad759bb0550d4d02cb90f7f2a2fcdcbc9a3505dcb21b9012d311beac`  
		Last Modified: Mon, 16 Mar 2026 22:19:08 GMT  
		Size: 39.9 KB (39925 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:956d8f4f789800010d0ee1222217373ff144014990273364f266ba4cf684d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163437546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db754190e6dfcd62eac9bd69a1c883e2304130bce1a98fc8d6d97e563ebebe6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:20:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:21:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:21:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:21:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:21:30 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:22:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:22:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:38:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 23:38:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:38:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 23:38:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 23:38:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:036b690c37cf2dc49974818e200658ce29b93c4d917171332d28ada375e6f68b`  
		Last Modified: Mon, 16 Mar 2026 21:51:40 GMT  
		Size: 28.5 MB (28526147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c511bce2320fb1f752073a9e395234b89bfbe7ae283598eed4ae50481ba13`  
		Last Modified: Mon, 16 Mar 2026 22:41:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7cdc9b3e2a042695dff8f60b8e99544395595dbb6eb622853e3f88ef163d15`  
		Last Modified: Mon, 16 Mar 2026 22:41:21 GMT  
		Size: 80.7 MB (80674297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0daf0cd7e12b7f59b1f7e20c68f1c863817b27e3517bb1e81f995c18410b51`  
		Last Modified: Mon, 16 Mar 2026 22:41:08 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b03fec4c730be82b6e7b47d824ffcca5c337cf48f14abf8ed259669d64b2d0f`  
		Last Modified: Mon, 16 Mar 2026 22:41:11 GMT  
		Size: 14.5 MB (14456866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65ba1c72070499f3bac01c468a9c6e39eb1f23aed2ddd972c3791fe74ac24d`  
		Last Modified: Mon, 16 Mar 2026 22:41:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fcd9a2e9e1b121b5802791ee19a4a78eb7c1e99cc1ac276dceaaf9c6f17ce6`  
		Last Modified: Mon, 16 Mar 2026 23:39:50 GMT  
		Size: 39.8 MB (39776606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e404b6bfea7b6b40183c4d7413e71279dc61542b585a6cc3733ad049d5f99a65`  
		Last Modified: Mon, 16 Mar 2026 23:39:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42642bb1211e905e78ca03c75df1a620e6b83c902d382f9c07f6631909a668a4`  
		Last Modified: Mon, 16 Mar 2026 23:39:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:115c95531aa7a74043112d21bfbfb0895ad71375e7652808a58f5f37a262be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af99795ce775dcb5a803d11d768fbf2c8ddd047f662b1767a15c6729c222615`

```dockerfile
```

-	Layers:
	-	`sha256:5554ba1da59e3626558bb29d954048b7ae9f772a0140b530f5a5d0db290cf9b3`  
		Last Modified: Mon, 16 Mar 2026 23:39:45 GMT  
		Size: 39.8 KB (39827 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:858472ec1269fb779e301af3a77a1e0e1bee35ab87ec71f93920725a726f7045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193427133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d6df6710943b90efd60c16ac36830e37055e6fa8b43e8910ad1c287d2a6ce`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Thu, 12 Mar 2026 23:40:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:41:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:41:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:41:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:41:13 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:47:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:47:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:52:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:52:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:52:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:52:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b87d7abc35ea5b0240dcef5b74b75e6364defcde9ceb9c2c28a8e53fdb2cec`  
		Last Modified: Thu, 12 Mar 2026 23:46:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb21602f9bf1c6f3e43dfe8e60af6f1ead6cdbe686dc2c7a2aa8fb00fcd408`  
		Last Modified: Thu, 12 Mar 2026 23:47:03 GMT  
		Size: 103.3 MB (103330106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecdd744fb797bfbc3d4fb8480208f415defbd6d019718be9a750af8b5aa611b`  
		Last Modified: Thu, 12 Mar 2026 23:46:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f42f154b4d344d11f170f41a36f3d2aeb72f37abfcc75fc9a1dfd613c485946`  
		Last Modified: Thu, 12 Mar 2026 23:52:46 GMT  
		Size: 14.5 MB (14458775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd25efa77333c1a7be220a63a014a5af12ab76ad25926230280bd34d2908564e`  
		Last Modified: Thu, 12 Mar 2026 23:52:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a072d8c45f1904b70a62c38e3a9191afae26a813bc0cb2481320a0fb5b817e79`  
		Last Modified: Thu, 12 Mar 2026 23:53:13 GMT  
		Size: 43.6 MB (43556281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f9ad4c89dba998768ee2e058fa159f5d062128240cf768f1d053a9cd8f4c9c`  
		Last Modified: Thu, 12 Mar 2026 23:53:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c6dbc68d3a0766f1d6b31b4839e00da96dcb0f867fa1dd6f4ad4bad9003a59`  
		Last Modified: Thu, 12 Mar 2026 23:53:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:263da0dcfc7a66fc9e0ef2e8897eb3eb421d53c44e3901ec39765054f4a91eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6418304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa8080677ee70b1a6aece50ff6c054828aad58dc649b796223971c5aa7fecb`

```dockerfile
```

-	Layers:
	-	`sha256:eebe158c55b3d78e803e6db22b4210a502bf6c1256bd7ba9a2351a91cbb42b01`  
		Last Modified: Thu, 12 Mar 2026 23:53:12 GMT  
		Size: 6.4 MB (6379236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28e33fd8d5d7dc68b4f20297a800f6d8f231d53fedea21822810a1b9f1a6e772`  
		Last Modified: Thu, 12 Mar 2026 23:53:12 GMT  
		Size: 39.1 KB (39068 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; s390x

```console
$ docker pull php@sha256:310a8a4a3a3ee8fb25db8801bfa428a4c296639d6497d9b97d19e3a8059b21e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162188252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631a0350cfac860804445fdd2f3c609fa31e207f4f3a7981448201e0bb50a5b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:27:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:27:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:27:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:27:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:27:25 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:27:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:27:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:33:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:33:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:33:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:33:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:33:49 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47487a15675db59e92c013929312dde228e0351e63725ad6faf318c2b88bc3a`  
		Last Modified: Mon, 16 Mar 2026 22:31:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86294c92729c7a7e6f66069cdf96e50992eb78ab5ca281c70d8513bdb9534d60`  
		Last Modified: Mon, 16 Mar 2026 22:31:44 GMT  
		Size: 80.8 MB (80827843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e6733c271421f16923004f2e7f8ce97678b89f8b59c86af69bcb25ea9bb995`  
		Last Modified: Mon, 16 Mar 2026 22:31:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b112e1cbdd31891cee958fea6df4bc893e52021fcfd8b825af579219943a0020`  
		Last Modified: Mon, 16 Mar 2026 22:31:43 GMT  
		Size: 14.5 MB (14457656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7f5ef17899500cb82c25734d00cd277710afc0612e901613040859a809d160`  
		Last Modified: Mon, 16 Mar 2026 22:31:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98579c2225e0ca2820b33d9db0190cdc6e85921a8d6b7aad09cd2c5867d92477`  
		Last Modified: Mon, 16 Mar 2026 22:34:11 GMT  
		Size: 40.0 MB (40007606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5008b9a9c66fab2ccc95f7ecb23be3a570349233f1accb4a219da7f913d8ee63`  
		Last Modified: Mon, 16 Mar 2026 22:34:11 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54770ec205dc9cc2a96d8b7fb4c4a6b7d8082ad6eacb1d382bb5205908b1ddbf`  
		Last Modified: Mon, 16 Mar 2026 22:34:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:ac33571608f8e46c5e326bbfe15d166ff1eaa691f5d373ca9c6e68935e471fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6278798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcbe9b5e4fdd51f12863dfa67bc650b41256c38961baac0646734c905d1b1e4`

```dockerfile
```

-	Layers:
	-	`sha256:984bea79a878197eb0028b459c412d848012e4111f00421ee16ad8b3a8f634c1`  
		Last Modified: Mon, 16 Mar 2026 22:34:11 GMT  
		Size: 6.2 MB (6239790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2566c0fdb11599e631a8d3e1fa9faae93bfe0e9209b31f7229885862d29ec7ac`  
		Last Modified: Mon, 16 Mar 2026 22:34:11 GMT  
		Size: 39.0 KB (39008 bytes)  
		MIME: application/vnd.in-toto+json
