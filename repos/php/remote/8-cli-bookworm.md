## `php:8-cli-bookworm`

```console
$ docker pull php@sha256:8f003c211309d89817cb3735ed0ebdc5b0c4717170cfa8213ff2982b436d9c10
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

### `php:8-cli-bookworm` - linux; amd64

```console
$ docker pull php@sha256:8e604d6891ffcf2d59c61201546b219bc767fae8e7a7cb4d6fe0108cd8f36768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189623228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bdd3109fb9331f4408ad066706128142dd9cab96e27c6dd2c0b05c4ca93f2a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:30:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:30:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:30:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:30:45 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:30:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:30:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:33:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:33:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:33:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:33:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:33:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f3c683e4b17989bdd98d9c30921135075361695c6d48166d7eeb9a6bc0f5d`  
		Last Modified: Fri, 09 Jan 2026 22:34:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d886929a2b4524a1244fb1ff5f8ee8b5d5133aed889384913e5099342e8cca57`  
		Last Modified: Fri, 09 Jan 2026 22:34:28 GMT  
		Size: 104.3 MB (104330351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab79f8f64397679f5ff58cb2c6942b980b44b93f04f1cc7a9b5d5eb9fe0cfd55`  
		Last Modified: Fri, 09 Jan 2026 22:34:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921cdddae2b173aedabf58a039c65e677635351b79e693d21b108f2fd43a6bc2`  
		Last Modified: Fri, 09 Jan 2026 22:34:19 GMT  
		Size: 14.4 MB (14436672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb4acaf0c3d9f1484f917e1f3d00ac7095ab8aae21d2ad2dec80e569ff5897e`  
		Last Modified: Fri, 09 Jan 2026 22:34:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfa585ce4613b12af7a138446d3ed18096e446f945be2c87624723bbae78ace`  
		Last Modified: Fri, 09 Jan 2026 22:34:21 GMT  
		Size: 42.6 MB (42624139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973580940710fe2ef2181d0d2c92b0d6ea7e8e0ef929e21783312e4b641db479`  
		Last Modified: Fri, 09 Jan 2026 22:34:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd78fdd7a2d4f63751f377a82495e0dbf47cd035c98bc8f2475828bb190e2da`  
		Last Modified: Fri, 09 Jan 2026 22:34:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:10bdd72eb9863f24045cf50515d3657add6f97e322c72d6a118aff6f736c7ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f37f9b82e7cf58c04a9ddc0e12432976e99026ac5618821f8f019a434b3755`

```dockerfile
```

-	Layers:
	-	`sha256:69f95610293a7a8cc284b92ca55143042527a5361c9611622ab209cf05956f5e`  
		Last Modified: Fri, 09 Jan 2026 23:57:43 GMT  
		Size: 6.4 MB (6403768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7fe2d71e836bb1fca2bd9d7f10452eecd5587bc2122b6590985e40d4a5ab1e`  
		Last Modified: Fri, 09 Jan 2026 23:57:44 GMT  
		Size: 40.8 KB (40844 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:b982eebe1616d85c78028585e16cfce883d91d93051b66d05a6a0a50259ac188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160767480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1755bb5de9a7f71a96525741e318f825e17e940925d277f8a1daf172ae4e763`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:24:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:24:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:24:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:24:59 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:37:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:37:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:40:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:40:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:40:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:40:24 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad6198271507f37c449e47172156a8d26ddf9c3ea9335c6a34772747a6392de`  
		Last Modified: Fri, 09 Jan 2026 22:29:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba96c74bfa1ab1bc778230d7a90962012ad1eb725b6d5c4324ad37ecd267c37`  
		Last Modified: Fri, 09 Jan 2026 22:29:08 GMT  
		Size: 82.0 MB (81981250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367196631f6bb21cbdc7a55537c8fc34132d915eb299dbe519cbfb2d85d0473f`  
		Last Modified: Fri, 09 Jan 2026 22:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db1a2c1c2f2de387a8d93ece53cc301af49479aa3c19c84297e91996f17b98d`  
		Last Modified: Fri, 09 Jan 2026 22:40:46 GMT  
		Size: 14.4 MB (14435002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419b2fb2f8e011269171f88d801fb441b930564d6abb9a47672bb0cfb6c5c01`  
		Last Modified: Fri, 09 Jan 2026 22:40:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f54b66c53517dc8b41b776eb42c044152276fc2534bdd2600c39f920a0d331`  
		Last Modified: Fri, 09 Jan 2026 22:40:48 GMT  
		Size: 38.6 MB (38590011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af1ed75eaa244af66e11a9987a20dea6ac6959511629495306514dfe8b1d64b`  
		Last Modified: Fri, 09 Jan 2026 22:40:44 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f885a144683650f43c85a76da69e7f002fbad9fc0d8ecfd9091fcf8eae906`  
		Last Modified: Fri, 09 Jan 2026 22:40:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:0b3e6906088063d3b4135dd1a6e09a3607fc223af5855b8ecb6831cb0f825955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713063f6c1cc9fe193e392ea3dc581c7604235645cbc2fd4f403ed6156d650de`

```dockerfile
```

-	Layers:
	-	`sha256:e24c27f332dd56df1ed91f15a3c9e85736bbb7e700ea77104abd4a0cf23d0a01`  
		Last Modified: Fri, 09 Jan 2026 23:57:58 GMT  
		Size: 6.2 MB (6213126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149758b1278d78bb5049e682a1516cf7c868f2356cd3c3ce96505c6e84e0dad3`  
		Last Modified: Fri, 09 Jan 2026 23:57:59 GMT  
		Size: 41.0 KB (41014 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:d3fd8550426142c94ff4e5b4cb754f9feba5d1d4460e245fe255f058a114835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151483593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ebc68aa40830029a9ac5320a9b9c3e1dd2655eb1e41d49f07fc2f268669d3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:33:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:33:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:33:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:33:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:33:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:33:53 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:43:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:43:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:45:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:45:55 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0021466ced27ac998f1df311136eacd39f43e33eed719f9ec4881adbaf7591`  
		Last Modified: Fri, 09 Jan 2026 22:37:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d087fbda0fa1392ca5ace12bb32b2aca1be29c98853082267103223cc8dbde`  
		Last Modified: Fri, 09 Jan 2026 22:37:30 GMT  
		Size: 76.1 MB (76148821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3923e8b0485e0cfc4e91f7b7d1b83e5020819071d80420bf46c3089b5603673`  
		Last Modified: Fri, 09 Jan 2026 22:37:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9889fb60d9b5c335205bba260746b73e1603e9a6a4610417982cb8f87348c`  
		Last Modified: Fri, 09 Jan 2026 22:46:18 GMT  
		Size: 14.4 MB (14434951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216aa029014ca38854f998f5b77d5807525ab801062dba688b9a381773f55f1e`  
		Last Modified: Fri, 09 Jan 2026 22:46:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c199f6a8cf4433573225931550d605ffefe0c38c7f1ee4940dec2effe4e47`  
		Last Modified: Fri, 09 Jan 2026 22:46:20 GMT  
		Size: 37.0 MB (36962132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd3b97a8f33d534a38b4e9280a25ea1fbabae3071682a363b20622ad8365d14`  
		Last Modified: Fri, 09 Jan 2026 22:46:16 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77886fbf68e3187b24adaa1b9b5092d75303ef9386c25412df86b3938f1ee566`  
		Last Modified: Fri, 09 Jan 2026 22:46:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:b0cf49d8d8e3acdd6fad09124628d76c6e6673f5e4d4ed4c881db71c9115fb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c7349b2def59214649836a13b5f2ebcfb9aeb55cb64fca0433e8a66767b596`

```dockerfile
```

-	Layers:
	-	`sha256:873fa5fe0168fd2f52dd09199254452225ea2d4163428f841d4aa54d4b1cfc97`  
		Last Modified: Fri, 09 Jan 2026 23:58:04 GMT  
		Size: 6.2 MB (6217070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ca6a244137a9212e31cf6e7a771cfad5059e2a0677f51af88833f4f60c4b15`  
		Last Modified: Fri, 09 Jan 2026 23:58:05 GMT  
		Size: 41.0 KB (41014 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:f561c1f5591dcda4de61472974d31b4164b1890ddba6ba43ee6f30496f6db190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182507963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7995805e09109f24570d47ee4dcac7911eb3bcb516b43683149aa7d026b36b3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:25:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:25:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:25:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:25:26 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:25:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:28:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:28:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:28:33 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571d2ff7e699d3b2cdd7a848aeebe4f1bd025df58ea057e888bf5aa98d64f15e`  
		Last Modified: Fri, 09 Jan 2026 22:29:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621b7dc794ea45dfd1366a4f0bb33ac0e6470d2c6fa10eb722c6da4a21e14b5`  
		Last Modified: Fri, 09 Jan 2026 22:29:13 GMT  
		Size: 98.2 MB (98165638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3920e1dfc138b4ce7f90d6d0d8745ce72df51e51a8405b5cf5d846731e845efe`  
		Last Modified: Fri, 09 Jan 2026 22:29:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a1c6a028515f6753fad6d6ebf154c821e31d63e87e117355fffc6323fae36d`  
		Last Modified: Fri, 09 Jan 2026 22:29:05 GMT  
		Size: 14.4 MB (14436494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2ec204bb06729a5efc9adf77898b86f492b1aa65db48658e0cb19294d70894`  
		Last Modified: Fri, 09 Jan 2026 22:29:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a344da8c70a8294cf38ff9d59457a57ac828241a0e9bdba9a0d2024ff7233b`  
		Last Modified: Fri, 09 Jan 2026 22:29:10 GMT  
		Size: 41.8 MB (41799975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608c84b70519f80394f3b894b8b2c97513467e209f04e338621f1bec111e276`  
		Last Modified: Fri, 09 Jan 2026 22:29:03 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08f8ee3c2c7dad6799d1dcc845a2f60e1c5d509d1407882851935839bea423a`  
		Last Modified: Fri, 09 Jan 2026 22:29:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:da123887c058a7bd0a918caad13344cf0651d4eb226a157d140e4218a8d337c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd099a26d76afb5f7493e20a383dd11d889234032d421070fa79c036fd104d17`

```dockerfile
```

-	Layers:
	-	`sha256:d94478008c18a08901c621b6ce5b884f6c22edcdcd0b5300a238e27de8e52071`  
		Last Modified: Fri, 09 Jan 2026 23:58:11 GMT  
		Size: 6.4 MB (6432207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1a4c5be90e5ad6d23497ea5e537599e7ce068474029a4e6998f264e30c7061`  
		Last Modified: Fri, 09 Jan 2026 23:58:12 GMT  
		Size: 41.1 KB (41064 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; 386

```console
$ docker pull php@sha256:c3f21d765dec174d76d8b91795992514b8ae8f165f7f8108481153c6bc95803e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9414fbc36e0a6c514d5335f57950bc88e3858e8f3d165f77fe92ebb0f08c329`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:30:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:30:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:30:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:30:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:33:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:33:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:33:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:33:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:33:21 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9597d7509177c6bd2de86881234312bf976a12800e8b06a43fd3db9d5eda3`  
		Last Modified: Fri, 09 Jan 2026 22:33:47 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8488fd1806c7c7e8cf929870adb00929283f5687e4aa178f834c441fc39d33e`  
		Last Modified: Fri, 09 Jan 2026 22:33:56 GMT  
		Size: 101.5 MB (101518585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334fad0c6b8c32c1d0d453bc33c5c13aa956cdb67d1def67519aa5af3bd55568`  
		Last Modified: Fri, 09 Jan 2026 22:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b94a37eed493fe277d90919d0e5320c38b58a4a7c8392bc55979fc301b12b67`  
		Last Modified: Fri, 09 Jan 2026 22:33:49 GMT  
		Size: 14.4 MB (14435980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28403f0f0ee33eb0a9f33ecb5754949115300eb9aa1c39445b803ea14f135e2c`  
		Last Modified: Fri, 09 Jan 2026 22:33:47 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3333471210c424c2b9b1279ca3982cd6dc62f3c9bf929ee1ed662f27a0289bd7`  
		Last Modified: Fri, 09 Jan 2026 22:33:53 GMT  
		Size: 43.5 MB (43467435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0a42f07854b30bcc5ba933c64d846abb7d3eec7b593d7dca17c9c569100fbe`  
		Last Modified: Fri, 09 Jan 2026 22:33:47 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3b4507d6cb90fdc45fe2969791189983a3a0c9917e765464796002b030f6fd`  
		Last Modified: Fri, 09 Jan 2026 22:33:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:62398e7ee72a723753c9a59fe1e80c34b68f67769f050a5de6de5135d632c26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfc906383cb2f581df5382200351253de0b6af9b66452c120c405ae0e54f772`

```dockerfile
```

-	Layers:
	-	`sha256:3e3d728a344b431e9359a3b900a3dfc762e187610cb7470140864be6c22fc83b`  
		Last Modified: Fri, 09 Jan 2026 23:58:18 GMT  
		Size: 6.4 MB (6383540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3225db1cd53509be5a15a0abdc6fad2cd0364bf804211ee054a5a662c80c808`  
		Last Modified: Fri, 09 Jan 2026 23:58:19 GMT  
		Size: 40.8 KB (40781 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:22ac8f77b2ad96352c44c0516176bc6d06a7abf53ae663715dc81eb6a6a08ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163149241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa442a4eaabe45c242c0db5b01d3428ed554d7fba3d32bea6e597fbcad7ca2c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:18:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:18:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_VERSION=8.5.1
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Mon, 29 Dec 2025 23:18:17 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 23:43:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 23:43:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:00:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:00:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:00:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:00:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:00:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d9cabd4aab99e194d4a41705774411b061e905a5607b5d68428e6c0fdfc3f`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa90b950d6df8880366223e469aa2861d9bff3782a34bbbbd8c49d4d03a522`  
		Last Modified: Mon, 29 Dec 2025 23:38:16 GMT  
		Size: 80.7 MB (80670513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39959c61c1a601c13b85fe9f2c5c8646ffe26d790e73c6bfb044a1a8b6891d0e`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80328574587ff3e09a28d2e7b4210fb36dbb323bd36ff8a443eccdb351e915c`  
		Last Modified: Sat, 10 Jan 2026 00:02:03 GMT  
		Size: 14.4 MB (14434623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327436c2049ca07403d134ef0c311e8afa5c51c41f642f143fc7da4fc8577a4e`  
		Last Modified: Sat, 10 Jan 2026 00:02:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1859b71ede8e308fb50eac4a3ecf96a2f710071cdc07340511889f4505de4b`  
		Last Modified: Sat, 10 Jan 2026 00:02:04 GMT  
		Size: 39.5 MB (39526656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ed04f544ba1e2cb09bcd4fca8dee74780ae517c7eaf1cad33f2f39de64452a`  
		Last Modified: Sat, 10 Jan 2026 00:02:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19382dd70b3c0445533bcec0c0f5fd2157a662308caaa13fc46d897944f18a9`  
		Last Modified: Sat, 10 Jan 2026 00:02:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:7518afc5b05d9b7855ed9ea882818225bd5e3bbc2c70fd62eceeaa287935274b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c048081b590174d5cd825a7163b439a1a7ca65078c48e06eb1599d9ca000e7`

```dockerfile
```

-	Layers:
	-	`sha256:dfb3e5e75fc5b3ae906fe7fa632ca15c852cabcb70c78794f9b88fc927288b7a`  
		Last Modified: Sat, 10 Jan 2026 00:39:47 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:fb43f93657d43ae4bffabf24cd3aee9d4c611689967e3ef0db15a399e7d0d7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193113312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885c408b105728f38aeb23fce212c1ab8bb1e7dfd837d1317ed37118165a050d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:15:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 02:16:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_VERSION=8.5.1
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 30 Dec 2025 02:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:22:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:19:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:19:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:19:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:19:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:19:28 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93a9966845dddb639588fdcde0ed0ecf405e81db5bf3e7b306c9cbebf976cb`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226cbc8a9cbea94e5a9e2e037754124cee088acdf931d11622ed35b2aabbfeb`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 103.3 MB (103328995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20082871cd07652f43cb1378561dfdd8cfbf23782814ff423bbb205eeab4afae`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92074af578061f521e5ebc3d9bd116d71211ea557b19e1ebdb116f389e5be84d`  
		Last Modified: Tue, 30 Dec 2025 02:26:38 GMT  
		Size: 14.4 MB (14436264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97689f332954625e17683ef324b607f750517b0d57d4d56b3e5c37d4073d488`  
		Last Modified: Tue, 30 Dec 2025 02:26:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ceca176b01575a5eb90a2afbdb9d674a7f730b9cb1b8471a9637ed319a8fe2`  
		Last Modified: Fri, 09 Jan 2026 23:20:24 GMT  
		Size: 43.3 MB (43275574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abddc461f55a850c2fe0c6c36fe3f7cb8f41e879927632861841d9105fe76bb`  
		Last Modified: Fri, 09 Jan 2026 23:20:20 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a517156c3083f929b2471c2893ccd8e00aa8073028d567e674794be3eaab5d0`  
		Last Modified: Fri, 09 Jan 2026 23:20:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:5cf8eec84423c3a36d8a8c4353093accf5b4a5b9148302bd82d7816afa953e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7839a58343f8b0e321124bdec614bd44a7cad120ee023db804b7fd72d4719a`

```dockerfile
```

-	Layers:
	-	`sha256:8c93e39fb47d3dfbaef15686c493e14dc2ecdd519d8036c464d55b801bb1e894`  
		Last Modified: Sat, 10 Jan 2026 00:39:51 GMT  
		Size: 6.4 MB (6380462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b261309877c9c04631ec2e6393da4a8305356c8c843cb8e97f42219392fddb6d`  
		Last Modified: Sat, 10 Jan 2026 00:39:53 GMT  
		Size: 40.9 KB (40922 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-cli-bookworm` - linux; s390x

```console
$ docker pull php@sha256:c57e0e3c1ad66e0585c1cce94842b07345aae07dcef25faeba2ef28b67e5df12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161834392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777730b48bca35f605e9b5a01212b35d705417ac8a4e5d11391634d5ae69f423`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:27:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:27:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_VERSION=8.5.1
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Mon, 29 Dec 2025 23:27:22 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:49:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:49:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:53:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:53:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:53:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:53:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:53:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2c08da5b713b6ffb7e10ce6c7b3ef3ecd2078ae90be2db77db37e189e8f439`  
		Last Modified: Mon, 29 Dec 2025 23:31:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a575c8dab9a96bc9b52b94d6cbc3589683f3bd36626cfc9073702c05785039b9`  
		Last Modified: Mon, 29 Dec 2025 23:31:57 GMT  
		Size: 80.8 MB (80826237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daeaec3ff0b4bf0aead303a9f0b355136d267f5b11654675d9196c9a3230b2b`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae166b50810bc261ae0a33f6da2864659a2e40a58ce7a61615e7cef76457bf`  
		Last Modified: Fri, 09 Jan 2026 22:53:55 GMT  
		Size: 14.4 MB (14435356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7783a64f8ffd8b5db06b347ce1fc3bed38bed903a7584e94abf0feb5cdd12822`  
		Last Modified: Fri, 09 Jan 2026 22:53:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667c17f1d26f6978491ec5ac888c040f4fc03f1f201a458a14eb7022cfbd2f5e`  
		Last Modified: Fri, 09 Jan 2026 22:53:58 GMT  
		Size: 39.7 MB (39684766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a415c8005fb8e528ca95ffe5e39b90701178f540015d41f58c9d6afc67ec586`  
		Last Modified: Fri, 09 Jan 2026 22:53:54 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5469c75e9e7ff0510e0b87db286ce9cbf0c819f0e46a705b03652c7ee529d153`  
		Last Modified: Fri, 09 Jan 2026 22:53:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-cli-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:d8d01853ba5b06e4eae372ceb3a5b6a3154c8ee58406aa434009b36d7bb00d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6281829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe8b69c94633263f77c4d5bd78a321cc479784bb30c1265d196232d1c22bb51`

```dockerfile
```

-	Layers:
	-	`sha256:727a92be8004573bbe6bbda0624b367e402796b08d550156aceed07d04b7de3f`  
		Last Modified: Fri, 09 Jan 2026 23:58:31 GMT  
		Size: 6.2 MB (6240992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e06e9c571004230701fb2f98f72eb94616888f38ae3cf01bee94c57289f05d2`  
		Last Modified: Fri, 09 Jan 2026 23:58:31 GMT  
		Size: 40.8 KB (40837 bytes)  
		MIME: application/vnd.in-toto+json
