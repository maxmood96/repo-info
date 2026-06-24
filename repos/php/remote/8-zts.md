## `php:8-zts`

```console
$ docker pull php@sha256:a64c4620609a477bf9ffb8c2a5afb144a3c62ceadc2c7befd2a8ae983e26a756
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `php:8-zts` - linux; amd64

```console
$ docker pull php@sha256:d1a97b52d093c4701eeea753bc936a829e52b19577634cc7f3a1391e811a9682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189414939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1943dec5a2f928cac10e9dd9599f63550f5a29549a9939912365e275f6475bde`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:22:37 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:22:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:25:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:25:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:25:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388ff014ae4f6aeae0f0e3e0c673bf709b1747cf05c9a024228caddc065bfc7`  
		Last Modified: Wed, 24 Jun 2026 01:25:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9cb16acff12437879cb4d902158efc43a4bfe98a0291ae0f03ef4acd335de2`  
		Last Modified: Wed, 24 Jun 2026 01:25:52 GMT  
		Size: 117.8 MB (117840282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699677ea19ac583360037c29bd81be838be951ab2314b08dfe0d9acea16e955`  
		Last Modified: Wed, 24 Jun 2026 01:25:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85014b020aa816f5a1205f56bc0046acef64a7b00fabcacc59a8b0cd3b80e745`  
		Last Modified: Wed, 24 Jun 2026 01:25:49 GMT  
		Size: 14.5 MB (14545596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b753b208db6f9a0e4757b2465b142f0b12618553dfcbbf56a0eee00f122b9bf2`  
		Last Modified: Wed, 24 Jun 2026 01:25:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a317606c113c8fa0ee65d086aff3664781228bf6fbc461005ffc787518abd7`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 27.2 MB (27240003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9a3fca9aa166c62b6f7cab7f8bf132f7280cf6e4789304b866080d8d9eade`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48330ce3401baa08f6f9faa2d0bb240d763ff5c030645d2e40020724fd2544a0`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:925d9ce3e831a68eb23c7dd4c274767dc7d63e388d01c22a245def7cbb45e0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6724456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28584fa2d18f3fc589d845e2466c9d2838cb75d6a41edf238bffc83931e8dba2`

```dockerfile
```

-	Layers:
	-	`sha256:a65738015ee48922b9f8c5d626edfe5f0aaef8f8fd4920057521501be0a8fe61`  
		Last Modified: Wed, 24 Jun 2026 01:25:48 GMT  
		Size: 6.7 MB (6683411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f21f12d6c0188bf012d8f5c0241c08d0bc430e9d2e22a9d6abb3c27626e40e5`  
		Last Modified: Wed, 24 Jun 2026 01:25:48 GMT  
		Size: 41.0 KB (41045 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; arm variant v5

```console
$ docker pull php@sha256:7ed3b00ba80123808f8497a4371e997295d994035ac4023950fe3d58579a3d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161034802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0dbc2ae84fce66abdb9cf5b3189e31216a3a0200c15bd1e0dbca9e57c8768`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:23:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:23:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:23:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:27:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:27:04 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bf54f95024125573309488db85324d243776267a307faa7f94b26db1e248cc`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8be319a943f7b8abc6e4b1d4cf3571cb2c6e042d7cfd3bb02d4b931ae2c346`  
		Last Modified: Thu, 11 Jun 2026 00:27:26 GMT  
		Size: 94.9 MB (94885606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39530e62e350f67cad534ea575f3024d4018b676be4212ebd0ff185c2f12e154`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddc8fcc4bae1c8f17ef0d15ae15e86881645a987e09a269dd9253a627a39b07`  
		Last Modified: Thu, 11 Jun 2026 00:27:23 GMT  
		Size: 14.5 MB (14543161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b2ecb4f381e06a75f3d8f9eae5164599c1467ee1c38e4f7cde4b1b65ce3f1`  
		Last Modified: Thu, 11 Jun 2026 00:27:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2e177deb29b18f5b6ec0c08500ee62ebb70f876e3750e72e3d31d1682eccd`  
		Last Modified: Thu, 11 Jun 2026 00:27:24 GMT  
		Size: 23.6 MB (23643198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257b6a5d4a2b55923421e655e9ab39b47ea0fe9dd6a2282fcaea3452798d9c68`  
		Last Modified: Thu, 11 Jun 2026 00:27:25 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f416331d79787bd43fa3bba1d6caa40dcd29a50593a287e28a867ea8b7fb8cd`  
		Last Modified: Thu, 11 Jun 2026 00:27:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:06105f3727eb7b45f39726cce5999e00cbe6f78552fac760c7b91731b4eaa891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7967238040769ecb043dba280afffebff803a92dfda1a3a467c7467711b7dc9f`

```dockerfile
```

-	Layers:
	-	`sha256:15101509a5b49b4022ec43449f2ef10e24f7efd9df2986071ca44afeb51284d5`  
		Last Modified: Thu, 11 Jun 2026 00:27:23 GMT  
		Size: 6.5 MB (6483257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92583ebaab34aeb495a80b0bb2a5d914dca42bba608fb3691ec83b3822f70e70`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 41.2 KB (41214 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; arm variant v7

```console
$ docker pull php@sha256:0aab642185e0311fe2f65ab5e666d37601bd25bb4e4dc54f3b89c35a15dcbe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149242348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3660f497306fce6b58882e8929076d5ec9634b1a568529fe08c88107b21d5154`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:27:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:27:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:27:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:27:52 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:28:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:30:52 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c1683a0573fa26cfbdefd924e5abfb924b4e7646666d6f3c99a0e01168623`  
		Last Modified: Thu, 11 Jun 2026 00:31:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744d191355de41613daab9035626790328dc2266ce48afa6c8e57d5460a117c8`  
		Last Modified: Thu, 11 Jun 2026 00:31:11 GMT  
		Size: 86.3 MB (86256245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d15f8e33ec2c4154da22fd1e24433cd1ab40976c256ddc72217f949c2ac5ed`  
		Last Modified: Thu, 11 Jun 2026 00:31:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe989d334586cd362bc9fe498670de663422dbb1aaee24594ab31d4a9f3d53`  
		Last Modified: Thu, 11 Jun 2026 00:31:09 GMT  
		Size: 14.5 MB (14543381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f81576f9aaef9d06cafe83c052af56ad33b9cfeaa7e8e9eafcfdacc135cb5c`  
		Last Modified: Thu, 11 Jun 2026 00:31:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1415fb54434595dc91db7b7651fe47798445daf9cbaf42ece6a76f6dcc7078`  
		Last Modified: Thu, 11 Jun 2026 00:31:11 GMT  
		Size: 22.2 MB (22228087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb8c584ea638320e5ae6f89cbe6695d42ed3aaf44ba4d3ecee7223c719008b`  
		Last Modified: Thu, 11 Jun 2026 00:31:11 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ff60a16b6c1403571a802e7b96ced6c3b40df88d4084c666acd96fffbddeca`  
		Last Modified: Thu, 11 Jun 2026 00:31:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:010922a75a9477db9076d68fa55e96518d90289ab2d21d2ed6c7229a8156d001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e3189f7227e4b09764e4e21fb2ecad32b24bcac83ddb858a53e3564c2d8d53`

```dockerfile
```

-	Layers:
	-	`sha256:0e2724a25051c6e9148b54a23a6b51d60d4874335bcdf6b5126353e79db2f938`  
		Last Modified: Thu, 11 Jun 2026 00:31:09 GMT  
		Size: 6.5 MB (6487223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033bae1df96c93b6af3e708ee0bd314b086704a2bf72be400fae6f5f68796b63`  
		Last Modified: Thu, 11 Jun 2026 00:31:09 GMT  
		Size: 41.2 KB (41215 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; arm64 variant v8

```console
$ docker pull php@sha256:e719b7fc18b75eb05eacf8cc3ac7c7efb816b59f3f47f7668c8e86a685c462b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181476398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc69bb41ad032d737ac533ec6b3029c98e3b0a470d02227afd87fe25e54828`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:24:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:24:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:24:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:27:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:27:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:27:44 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd68c68bd2c9c5026a0f0d64dc4f9ba0977234322ed6fafa235bcdbf17dfa4`  
		Last Modified: Thu, 11 Jun 2026 00:28:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc996dc8a38d3e4c58fa4f08b9f5252b36d397c0a5df8d99cc972e938b40e85`  
		Last Modified: Thu, 11 Jun 2026 00:28:07 GMT  
		Size: 110.2 MB (110168631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4836bb3e1dbe32d6ed4ca04dc935afc686f259e9b4edb74cea8b720339e40d9`  
		Last Modified: Thu, 11 Jun 2026 00:28:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cdb0fb4fbf2f2d72daacc5c83ce78d93dec02fd12e6c9b7db6ebec6f77fa1b`  
		Last Modified: Thu, 11 Jun 2026 00:28:05 GMT  
		Size: 14.5 MB (14545290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284eb5b326fa82d9d14620919be7bccdfa22e2bee3ce59ec3ff6974e2229a6f`  
		Last Modified: Thu, 11 Jun 2026 00:28:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642b62c28b42d7132b028e1cf10b4d7c61e785e06a6d351e2f6a166b683d8a7`  
		Last Modified: Thu, 11 Jun 2026 00:28:07 GMT  
		Size: 26.6 MB (26610317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c18e02657b6c2c8d2ab86456600049332914ea6e77845b68b2bfedddf0640d`  
		Last Modified: Thu, 11 Jun 2026 00:28:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8d5c1d24ceb59a23d6a0ad8429b34be0c92e55a23d53752bccb7fc60a90f9`  
		Last Modified: Thu, 11 Jun 2026 00:28:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:29db0a43f84d223c29ccb7677042744ef299776b1810fa35eb8b20f3aa46ec34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9052206bbd9743d15b1c5084f09206c38be28d42f334b7d5fcd8d2c42e00074`

```dockerfile
```

-	Layers:
	-	`sha256:86e5345f6dfa1cbeb299b9070ebd5c1f49a9432861060c5ac6d30139a231c3f1`  
		Last Modified: Thu, 11 Jun 2026 00:28:04 GMT  
		Size: 6.8 MB (6780730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd39bb1a3abd325fd5621129a6535797d7f5841451ae121da3820f0374aafab3`  
		Last Modified: Thu, 11 Jun 2026 00:28:04 GMT  
		Size: 41.3 KB (41272 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; 386

```console
$ docker pull php@sha256:8ab3f57c6e984e8bdf10b5856c44809be362ae9f27a1b8bf6fdf2c8ecf53e34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189838832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03de0606cdfde9d3499f1edb307407b0bd52cd6fa60ed276fed0bbfe20e23e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:18:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:18:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:18:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:18:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:18:37 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:18:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:22:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:22:03 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b24a94f556d9658f69b3abd9b13a170e4d4fe28bf6a40afbf2fe8cd3c02c66`  
		Last Modified: Wed, 24 Jun 2026 01:22:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c1896cae5ed69298ca50ee2cf2af13f0d5dd5a456fb9cda819370172aba12`  
		Last Modified: Wed, 24 Jun 2026 01:22:30 GMT  
		Size: 116.1 MB (116142778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fc44a20d08c0257400235696146726f0c493f5edeb81df72e17506af590f41`  
		Last Modified: Wed, 24 Jun 2026 01:22:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db9db4708643788f565eb4bd2e2a9a76e5818576cc1dca1f648524f610b19`  
		Last Modified: Wed, 24 Jun 2026 01:22:25 GMT  
		Size: 14.5 MB (14544703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e76a6b9f6afb8b3dce52fcb552ce27f5e61a7af02a3f9a3ae24cbe003a878`  
		Last Modified: Wed, 24 Jun 2026 01:22:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2310561087e123b9ccec7065e72e5d20b542758552e5a119b62ac8efa654d2b`  
		Last Modified: Wed, 24 Jun 2026 01:22:28 GMT  
		Size: 27.8 MB (27846509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44d71637b25d269dd2d7b51c3cd89305eb8e5592707991634f8ecc94c3007b`  
		Last Modified: Wed, 24 Jun 2026 01:22:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e008f01fbc0f6fcf13bd67d6db7019681af75f99117549d16cd78d3d0dce87`  
		Last Modified: Wed, 24 Jun 2026 01:22:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:7316e2702ab149e868cbf6fe7440f1de6e3508258f7e176205b947c4afbc4bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6698272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bb951a714880ef5b6b7e5e43ce06f30488032ee5094dba774ee65c55fa86cf`

```dockerfile
```

-	Layers:
	-	`sha256:f6df920a00a1cc9f96a177f07c71c5e0476b32736e19ed34e47febdbb4f3600e`  
		Last Modified: Wed, 24 Jun 2026 01:22:25 GMT  
		Size: 6.7 MB (6657289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a442f59d7a8ae8d6120564e617c6853c1d15c8a6eef10e69fc58df3eb409c7`  
		Last Modified: Wed, 24 Jun 2026 01:22:24 GMT  
		Size: 41.0 KB (40983 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; ppc64le

```console
$ docker pull php@sha256:d551590a913d48354e7630382b584b8fac250b696daa5d54ba34b83b37f0fb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185145997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f362c61a981792aef4225fa0f8cabc6249bfc67d7358e63e857b73de2f2a7f93`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:47:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:48:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:48:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:54:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:54:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:00:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 02:00:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:00:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 02:00:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 02:00:30 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e77efe72bf9ab01112d6628b561df155e58c8abb9a5c50ca8c3c2d3054015`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a885bf66539705f27716480915d14f847c62afd59e7c77b0d7a2ec11fcf9f8`  
		Last Modified: Wed, 24 Jun 2026 01:53:59 GMT  
		Size: 109.6 MB (109598576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270c259f3728f03e6c19bf8bc89dd6cfe4f6a02bdbe4c4a66ac81d4e83afc0f`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b140bb9d271d56c45ac47e13bee622f19b66b686b88a6f00db04ac300131728d`  
		Last Modified: Wed, 24 Jun 2026 01:58:44 GMT  
		Size: 14.5 MB (14544748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340e7161b33b1f7854225f274d5897b05d3c8ad3fd543c1cca2d7c66ddbe6ba`  
		Last Modified: Wed, 24 Jun 2026 01:58:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b7fec1d4c331edf74eea6ab4b657c1298c25535ae22920ab386dd9a80aefd`  
		Last Modified: Wed, 24 Jun 2026 02:01:11 GMT  
		Size: 27.4 MB (27392651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739a328b5cb0bd3f55c1f60c91775107501edc3d87f7451fe34dab688e7f639e`  
		Last Modified: Wed, 24 Jun 2026 02:01:08 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f395f900034345df2edd009dba1ec558d519c6cd21c9c614c33a3388eddcd7`  
		Last Modified: Wed, 24 Jun 2026 02:01:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:aa1672cc8a9c7b1c1f843fbc1a80264afde0c562878baaf47f718459d67e9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6723253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665e598e8eadd394399561349bbb90e522ad773b0e6c101bba0befa7ab2eea0a`

```dockerfile
```

-	Layers:
	-	`sha256:fe47b2ed2d5c8a3f490be8c51fa5fed1964a4164c675f2141d42d7c9181eb8a7`  
		Last Modified: Wed, 24 Jun 2026 02:01:09 GMT  
		Size: 6.7 MB (6683085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92718dab35c6fffed5e7deb060024bd50744a2760a14d338005574a2ca28860e`  
		Last Modified: Wed, 24 Jun 2026 02:01:09 GMT  
		Size: 40.2 KB (40168 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; riscv64

```console
$ docker pull php@sha256:9f02641eb144cf1f500d14342072d63615d8cc6af9982d690a2c934d4a818146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 MB (214682694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ba53108374e2a764d9eeebd11aaec58c6ce8e34a7f20bb8bf927184af8dab8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 06:14:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jun 2026 06:17:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jun 2026 06:17:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jun 2026 06:17:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_VERSION=8.5.7
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 12 Jun 2026 06:18:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 12 Jun 2026 06:18:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 05:06:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 15 Jun 2026 05:06:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 05:06:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 15 Jun 2026 05:06:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 15 Jun 2026 05:06:06 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d877ba68e482a33a75fd5c2ad03cd220a291d8e1a9914f9501f41f97050fdf6`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbcfd8d49be980430164d80eb573cd408281b5735067cbdbe0d0ff42f6a5f62`  
		Last Modified: Fri, 12 Jun 2026 07:22:03 GMT  
		Size: 146.6 MB (146585237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cccce4250e607f18d72142d293e6bb27d27ab552c53e10d06fef4ba0a75bca2`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6198196592d98790f017e3fbe1fe28da4ce1c9b53badd7e4da86fe583bb6212`  
		Last Modified: Fri, 12 Jun 2026 07:21:42 GMT  
		Size: 14.5 MB (14544710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627aaea235e6ebb9aec43621bf95676b1a5a995ac538121059127d01453f90da`  
		Last Modified: Fri, 12 Jun 2026 07:21:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c212d9a22c1c970de320c050fd011a807f2014fefebc8e0d6b56f67d1aa8319d`  
		Last Modified: Mon, 15 Jun 2026 05:09:28 GMT  
		Size: 25.3 MB (25266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ffe5366ae73ece22a5c0040c9baf446d5604ac841efcc8ca2c7c3d28d898f`  
		Last Modified: Mon, 15 Jun 2026 05:09:24 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a1feba3b717b116cbe11a80e4e7f40e892f43e99e2634a1c4dcd290934831d`  
		Last Modified: Mon, 15 Jun 2026 05:09:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:6ccca18c1a891f13e22dc82321a06dba9e3b7f205f62ab4bca185fdcff118abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6796297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bfb6c35f6729a5ab6ada416c49f4e7f5349391d568525528ee9e94d8cb38`

```dockerfile
```

-	Layers:
	-	`sha256:faec6979ba9678a66b57428ba9195d2f51dff295dfb89bcb79bad078821dce00`  
		Last Modified: Mon, 15 Jun 2026 05:09:25 GMT  
		Size: 6.8 MB (6755174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714c0afe1103f66dd1b474c9efdba050f303a4fe8c87a8e6b53fdc439ec12b1b`  
		Last Modified: Mon, 15 Jun 2026 05:09:23 GMT  
		Size: 41.1 KB (41123 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts` - linux; s390x

```console
$ docker pull php@sha256:1e4de0b5a30b7155cf751d9f4cf051ad0249abf2ef649d5ff2f8f8a57e9da53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163035354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66da57518e8c3df6a3c752863fe86cef7091848c088e80aac8bd35a094f893c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:21:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:26:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:26:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:31:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:31:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:31:08 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf2c9700e0e4f03dd095a047ed5f955f54de6a434c19db4b06084ecb37afd57`  
		Last Modified: Wed, 24 Jun 2026 01:26:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421dd9979caf4b8bac83046bf3ab1846c8ca21480a96a701ef722744cc716dfe`  
		Last Modified: Wed, 24 Jun 2026 01:26:27 GMT  
		Size: 92.6 MB (92572669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19aeec7555f7de0e31335cb32f8ad59a4f09d3388ee6f2a039dffefd6887cf`  
		Last Modified: Wed, 24 Jun 2026 01:26:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802c01ce8c0edf41cf645e13f026833d1242820d9a54dd2308cdcbef6034a9f3`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 14.5 MB (14544111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01e5c9102d87d49ecd277830a21c05eebc61b892a09c9a673c1aeb677d00407`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90c252317728768e6df39d2366aef709bbcb0e988c77bb338f01c7d79b613a9`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 26.1 MB (26063561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5be0a708a7ac205dc681fc208355d88230dd70048b5906d1d279ca04734478`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b901bee7ee235ffbcb34465c554356c92bc1ca4d1c6f3ae61daf2c0a57ffd4d0`  
		Last Modified: Wed, 24 Jun 2026 01:31:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts` - unknown; unknown

```console
$ docker pull php@sha256:225654ed100dc0a44fce16fa0802ba57717d9557e93159fe223af3e20b55a058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3be5cee638471aba7731112a555dfd8c0383c476a7ab2271c60bef37234f15c`

```dockerfile
```

-	Layers:
	-	`sha256:e900b16930afb8c7ba3c2a0465f75939a10a151834ed22d2dd6af9fa959e3dac`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 6.5 MB (6500684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71abd6e5337a91ff663647475e05d159ae0428a8a4a117359c497b0e666a4779`  
		Last Modified: Wed, 24 Jun 2026 01:31:27 GMT  
		Size: 41.0 KB (41038 bytes)  
		MIME: application/vnd.in-toto+json
