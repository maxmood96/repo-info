## `php:bookworm`

```console
$ docker pull php@sha256:787bc82035c8b123f08155cf98066a56d510732a18f04bc796b6b2041dd2f98d
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

### `php:bookworm` - linux; amd64

```console
$ docker pull php@sha256:e0ed00c0b0b7503535d1c1cb69ddf809f5e3f62e36dbc7649ee9149b96ae25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190082045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6f2e2b0748ac8e5621008a6987d2e85c3cdc2057052270665ec5c457fea9da`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:22:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:22:46 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:22:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:22:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:25:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:25:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:25:37 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2426c0c3f033757713f62b25edf899b99d0b7935c4860bb2314fd9cb920884`  
		Last Modified: Wed, 24 Jun 2026 01:25:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85c75bcc849f4189cd30b150a124164d045eb163124cbdd12a468c8ba7d2540`  
		Last Modified: Wed, 24 Jun 2026 01:26:02 GMT  
		Size: 104.3 MB (104344975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4706a37ce0736d1df3d410311def4fe803d7bab285e421639dccc735eea2d6f`  
		Last Modified: Wed, 24 Jun 2026 01:25:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85fdf0b4a8b7d262d5fa0cedf980db444e28491bda2fa1ccc643c7ead383a09`  
		Last Modified: Wed, 24 Jun 2026 01:25:58 GMT  
		Size: 14.5 MB (14508137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804c6c0acb5179f04c2d4575ad63912228ea644bf490c1cca04e2e1ef7e22b56`  
		Last Modified: Wed, 24 Jun 2026 01:25:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f5c6ef5c22ec71fc6741805a62827d42980ae433a94724c3e4dd01c9a3bb57`  
		Last Modified: Wed, 24 Jun 2026 01:26:01 GMT  
		Size: 43.0 MB (42987659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248695b288944fad1f5e3452c957606a3bac2fa9de1e1d2aa77ddcaecc1594b`  
		Last Modified: Wed, 24 Jun 2026 01:26:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91794ba4db04e5298394a226dbf77438341469764ba6c57394ee1cb18ceb2ef0`  
		Last Modified: Wed, 24 Jun 2026 01:26:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:97e0039517a6117e2c70b60cf72b8055979d9af25f8a9e3eb3d13f6aa0f38094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2654767922c010469613ba3b52a308417b1a91062780fdd442dd82fd09f8969`

```dockerfile
```

-	Layers:
	-	`sha256:f90c472e5b64b3765fa72b98c92d677eba8ca575c513485e45fdc8f75a4c8c84`  
		Last Modified: Wed, 24 Jun 2026 01:25:58 GMT  
		Size: 6.4 MB (6403814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1200cbc2e9d08e17b2277e91d48b127881412949b35ddb2f5f4a02ef2a43f612`  
		Last Modified: Wed, 24 Jun 2026 01:25:57 GMT  
		Size: 40.8 KB (40844 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:d2d7b3587a9e3006992f25b2ce82cf544bca2d2c02b68f0edcad88a2feb0c14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161098620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27654a967ce14b1e9cfbe847ee75c87f10fe2c74359fe3e26a271363a649c22a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:25:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:25:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:25:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:28:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:28:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:28:39 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0471ab86b4fdfe4f7e29ad683ce647a531fa68ad2e1a65562d8c55165a37232f`  
		Last Modified: Thu, 11 Jun 2026 00:28:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f1d5b68792002e9c2791db04d96b88b21f07b2ab02842ed81e8408852260a`  
		Last Modified: Thu, 11 Jun 2026 00:28:58 GMT  
		Size: 82.0 MB (81984675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dd2c90ceba4df47e0f9b43e63fba9a63557f2ceb0d1cd7d8d831172ba11b1a`  
		Last Modified: Thu, 11 Jun 2026 00:28:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcde792094aba2624cb0ef7f07a96c2c675f9d967bb815e9a094d56af933fc2`  
		Last Modified: Thu, 11 Jun 2026 00:28:57 GMT  
		Size: 14.5 MB (14506006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4875d45526553e9f81d199db38744bd5d7bf0237a4d01771985577cdc115ee4e`  
		Last Modified: Thu, 11 Jun 2026 00:28:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e76922fc400ed8e6b65f1c9e1805d10a450ef062473d482367108974e8b3e5`  
		Last Modified: Thu, 11 Jun 2026 00:28:58 GMT  
		Size: 38.8 MB (38831129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907be44f8aed4de7c09a1cfa9a474b91e9de732042c45d4972b440daca0be2b`  
		Last Modified: Thu, 11 Jun 2026 00:28:58 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1184c494e4dc7fdd7a28eac2f694dba6e4ecb931e3259cdc4bf636670abfe66`  
		Last Modified: Thu, 11 Jun 2026 00:28:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:3572811e81a443ae6be1193004ac76ce357d08350940374931594ccde76e7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f536f33bcbcddf52ae0ff2aaf3a726ee81e8ae53506d41ccc7b4136046dc2803`

```dockerfile
```

-	Layers:
	-	`sha256:0cd6515e3b4cf8faf59497db691cb3a9c6e11e7e16cc024e86d32539c457958f`  
		Last Modified: Thu, 11 Jun 2026 00:28:56 GMT  
		Size: 6.2 MB (6213172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793ba6635aa7b5906b46eea9fc1abdd9f27b9b4ba711228dac997717d228cd81`  
		Last Modified: Thu, 11 Jun 2026 00:28:55 GMT  
		Size: 41.0 KB (41014 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:43f81f529f6b45dd7a6be1390bfc5f6e875e5f419d19f4ceca5c400cdbdfbb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151805040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c691e6b3f20da456507cba034855470c5fc437e503fded86fd42813297ca1687`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:29:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:29:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:29:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:29:48 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:29:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:29:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:32:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:32:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:32:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ea28ee15f186311a643c5f137d537c28d506558078cde94570ef87786069d2`  
		Last Modified: Thu, 11 Jun 2026 00:32:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20391a36095e85b949b4a9f2fc1b68bace4c6286021463cbd826ffe07528cd6`  
		Last Modified: Thu, 11 Jun 2026 00:32:56 GMT  
		Size: 76.2 MB (76154108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9989f44cf2d845c96066376a62cef4ef5b2b9e3948a6e1230f8135ed1854f48f`  
		Last Modified: Thu, 11 Jun 2026 00:32:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd5dc6d292cfcb87036cbe8dab15faee18759b3f819fe93a0038c2843fd0ac`  
		Last Modified: Thu, 11 Jun 2026 00:32:55 GMT  
		Size: 14.5 MB (14505971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a91766240d76f219199c4f6cc513ff859ce86a68db0001c56ed55d158eb5d1`  
		Last Modified: Thu, 11 Jun 2026 00:32:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba79739497073685811e73dda01facc30aa009d28684b5d705278afd906f0b9`  
		Last Modified: Thu, 11 Jun 2026 00:32:57 GMT  
		Size: 37.2 MB (37196859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf90f6e6d47cea2342bbd0f94c7e57aa26f9720ee6ec1ea0585b104e7b33e773`  
		Last Modified: Thu, 11 Jun 2026 00:32:56 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f3e40e2efadbf2713c2c95ae103d969de342a7443b761e73dc636b45c1a963`  
		Last Modified: Thu, 11 Jun 2026 00:32:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:60f609d752030f8b4409c6e146c7609b29f3d5f14ecd777aed16c1eef927e66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145655ac0b6819215c36f18c686cf2e5ee677ff799bfef15fcd8d9f08a46de46`

```dockerfile
```

-	Layers:
	-	`sha256:44ad8a14cb709d4fafafd7769bac43e8fadd5efa21d92893e8ebb676d4808d99`  
		Last Modified: Thu, 11 Jun 2026 00:32:54 GMT  
		Size: 6.2 MB (6217116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9b183b951bbccfb4debf95c0eefc4903d11a65ad3af7b9387f8b2461344fac`  
		Last Modified: Thu, 11 Jun 2026 00:32:54 GMT  
		Size: 41.0 KB (41014 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:db5955d233c22f04992f68692e2378b922db8116f6dce1bb0502075ca90a64c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182949769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94000fefa9b13708d7375d0772cb2ec418ee60f25bde2bc4c366f0387df1590`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:22:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:23:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:23:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:23:02 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:23:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:23:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:26:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:26:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:26:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:26:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:26:17 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bae2446bb46b39bf215fad31e281cad6a118912a6e94d7fadcda26e40bc3c1`  
		Last Modified: Wed, 24 Jun 2026 01:26:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611597d355134648dc9d9df75806f937f1961e958078e3df258581322302bf66`  
		Last Modified: Wed, 24 Jun 2026 01:26:40 GMT  
		Size: 98.2 MB (98177546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4932fca8a74b0567f1b8f47b563f97f38fc4b5c5740590f4b631447a29e2f8`  
		Last Modified: Wed, 24 Jun 2026 01:26:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810ce667f9317e25b46ac8ad638c89fc9f377319c7102a477f1ac900bedec0fe`  
		Last Modified: Wed, 24 Jun 2026 01:26:37 GMT  
		Size: 14.5 MB (14507940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f10a74a32593283f8ba8dc9d72347ec1c09c7ce1e453e43de759104622b568`  
		Last Modified: Wed, 24 Jun 2026 01:26:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d2e33f5853c93157d0b09c1ed4e72d06ea755187c1bdffe59920635d2317e3`  
		Last Modified: Wed, 24 Jun 2026 01:26:40 GMT  
		Size: 42.1 MB (42138231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6313ffc523b2a5ecb66175e4e53db5c0241e7ac857f8c02c3747306abaae0b`  
		Last Modified: Wed, 24 Jun 2026 01:26:39 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cc1a8236dd393dca5e71f1bc8e20f32326b467937383a078143242b8d70167`  
		Last Modified: Wed, 24 Jun 2026 01:26:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:a87ddf37e6a4af6dce12b24c97ef905fd0cd97a2f838b3548575838a56a80e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b417e382f35b9ddbc26679a10605e707337344ec868d9ba663317d4df67cc`

```dockerfile
```

-	Layers:
	-	`sha256:812a962c90384c7c9c640c22333184d426ef4ae27f0c58646bf7ff699721c4f1`  
		Last Modified: Wed, 24 Jun 2026 01:26:37 GMT  
		Size: 6.4 MB (6432253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084e0536f30715a792b2d2475cbf15175d6fec7bcc44039929ca20abf3dadfee`  
		Last Modified: Wed, 24 Jun 2026 01:26:36 GMT  
		Size: 41.1 KB (41064 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; 386

```console
$ docker pull php@sha256:e4c657d3704ad5f79971162608c61c620d4a52870929ed8efe4ed06ae6529519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189111256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1762b2da0dc567472b7e15117e173c3d57a4b46f5e039e5c77d1b62bfb065b0b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:18:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:18:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:18:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:18:42 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:18:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:18:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:21:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:21:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:21:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:df519b11ac99d8e2d452cbd55f824e658d0b86f649745abaaf8cbe33e2736a30`  
		Last Modified: Wed, 24 Jun 2026 00:28:03 GMT  
		Size: 29.2 MB (29225809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe55457bcf046843166eee6200e0f8c0a624ebb0d18bc9cec41ee92da79ed5d`  
		Last Modified: Wed, 24 Jun 2026 01:21:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220ec54894bc3bd5420c98e7c577ecf9455f069421046c2ccddc55b3636e80e`  
		Last Modified: Wed, 24 Jun 2026 01:21:57 GMT  
		Size: 101.5 MB (101536560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3269222bdfd99efa4446c0e4ff39dd77e5d7623f911968c47696f679d2cfda43`  
		Last Modified: Wed, 24 Jun 2026 01:21:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e4e89470b2701b506460a9f3aec9567c2cce512f13c2a2ed14f6c4373a2cda`  
		Last Modified: Wed, 24 Jun 2026 01:21:54 GMT  
		Size: 14.5 MB (14507294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5dbc60e6c784afb10996f021b25af34d4e3dc1d464715a01a98e0d2e967fc`  
		Last Modified: Wed, 24 Jun 2026 01:21:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b323d6527af37e4339b6e5d192ecd2bc779f5ac3c9c4f990f6ebb6fa656f17b`  
		Last Modified: Wed, 24 Jun 2026 01:21:56 GMT  
		Size: 43.8 MB (43837960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c031cb10350593ca05d5634a390b9e3e1bd9577743f0cec743c4e304de4b85b2`  
		Last Modified: Wed, 24 Jun 2026 01:21:56 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8729e420ef84e89bd425743ab46b0722743c2747283a5b8f0df079d1ddadeea`  
		Last Modified: Wed, 24 Jun 2026 01:21:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:43b214a092f0b15797ba05d450cf8902681a6ba13d3f45e4834c47ed9b2f5d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33216324e5767530034a53a32a5ff433019920e375d0d7bdaa9c0f9d4cc26263`

```dockerfile
```

-	Layers:
	-	`sha256:b04e0405a713e78b13b60eda6cfeaaa43748d12c10d15e03545ac67dc9763cf5`  
		Last Modified: Wed, 24 Jun 2026 01:21:54 GMT  
		Size: 6.4 MB (6383586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feceea186e8480790c1aa415c797965d3b8861d9e88ffdacb45a2e17bc893d7d`  
		Last Modified: Wed, 24 Jun 2026 01:21:53 GMT  
		Size: 40.8 KB (40781 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; mips64le

```console
$ docker pull php@sha256:8ef251a19142b8c54ea19a2e9866c27ddace2b7a909852c51b0b5703582ffe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163490785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c152abd62adb9218f23ce2e32482217094e464768db148971e2613456b68695f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:17:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:18:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:18:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:18:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:18:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:18:41 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:19:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:19:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:37:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:37:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:37:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:37:45 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e3e59e5d9fba86ba9cccde17de0c09e1a6250f5fd1ae881c8b925031848b7a5d`  
		Last Modified: Wed, 24 Jun 2026 00:27:28 GMT  
		Size: 28.5 MB (28528885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b78e3fb504e6b1da0ac45c5317e81c8d8169fd4da46948f49891cc32616de7`  
		Last Modified: Wed, 24 Jun 2026 01:39:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00d92299366ea9be46c734e2b2f5917ed237a725727e257ef405a5c278ed74`  
		Last Modified: Wed, 24 Jun 2026 01:39:39 GMT  
		Size: 80.7 MB (80673906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe0a7e07eb2837f88862f1f946c200727816e4cf92cbaf0239adf36d7ffc6c8`  
		Last Modified: Wed, 24 Jun 2026 01:39:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24739c3c6227ea1d10f0a63f8c236548bc6ed51725b72b4e379f531d36d924d8`  
		Last Modified: Wed, 24 Jun 2026 01:39:28 GMT  
		Size: 14.5 MB (14505658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e55325247148a6edb89c2a25abafa9e5ce7feefe1f2f90b6fcad33bea7007a6`  
		Last Modified: Wed, 24 Jun 2026 01:39:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b1778efcf77a822a45c8dd3a496b0826a99727593233b92f40f53ff7ba2cd8`  
		Last Modified: Wed, 24 Jun 2026 01:39:35 GMT  
		Size: 39.8 MB (39778691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e7f69dd8b1b9d301fa58f590df55324132903dc15c1fea370b5bbd8087ca4`  
		Last Modified: Wed, 24 Jun 2026 01:39:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8361423014a3fdf4f86f2c2582ff2275f2899fe8e5e30443327fe09f8864765`  
		Last Modified: Wed, 24 Jun 2026 01:39:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:475a7c513a290a0a10a8e3faf9ab19de1ed0fe7b3555ca5dd19ff8a9a589ce4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849d4cd5ce8ca1e4c9b7affaeb202bb45220cc32fcb91f0d2096534c44ae835e`

```dockerfile
```

-	Layers:
	-	`sha256:61a52d5c78377666ecca4764f36aa10f17f54522bc642114b1f5361e4434e144`  
		Last Modified: Wed, 24 Jun 2026 01:39:24 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:873c302abb9774c95c58d796b0e071dc1de919a4c4f2a2d498bf266969162adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193540245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79916cfa82f0dbc3395ff18f905ef6e26d839be20a9e22829624f1deeb3e83c3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:59:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:59:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:59:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:59:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:59:32 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:59:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:59:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:03:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 02:03:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:03:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 02:03:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 02:03:53 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39314f5422678416016d627fa64008eb57fce19ca4584debca0f106d506d63e`  
		Last Modified: Wed, 24 Jun 2026 02:04:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bff081a7ee781aa04e2814e2e92ec15e6fab9080566187d73b8918229b0671d`  
		Last Modified: Wed, 24 Jun 2026 02:04:37 GMT  
		Size: 103.3 MB (103334344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cedaac615d56f8cfeb5c4c4288fb6b16113b26f0e598f8eabeb08039596c75`  
		Last Modified: Wed, 24 Jun 2026 02:04:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9280844ee87cc3f524e207d31009618d138fc200474a1c7ebd5f05b714d5ab7e`  
		Last Modified: Wed, 24 Jun 2026 02:04:34 GMT  
		Size: 14.5 MB (14507490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890405a3eb62fbcbacb04c0d7c2e37e50bf8df1db4ae1888593c913f9ae49a9b`  
		Last Modified: Wed, 24 Jun 2026 02:04:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45605547d2571446a396dd96547fa1cb5f3ad37e256bbfa8af1ef2f586ab2789`  
		Last Modified: Wed, 24 Jun 2026 02:04:37 GMT  
		Size: 43.6 MB (43612792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229a0848f290389008d5f98a4340ed32b2f573653a0bb670aaa5c6bd27b7bc4c`  
		Last Modified: Wed, 24 Jun 2026 02:04:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43574c6fdd6ff1c6a3517526a50f7996bdbcdd9d5d5f5e5bbda3cb8978690603`  
		Last Modified: Wed, 24 Jun 2026 02:04:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:34a3bb35399c0154477170f600ae09e69a30697aa57283443c2b037852ef4767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead9c61b1bbc0794473584b07d8fdca55be405a27f0a79313a3cf807354bb4e8`

```dockerfile
```

-	Layers:
	-	`sha256:7636e15243d1f33506ca1a302416c0ad5c3ddd5864905889ee8a66925f5f5868`  
		Last Modified: Wed, 24 Jun 2026 02:04:34 GMT  
		Size: 6.4 MB (6380508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab664ee811b959c204a1bd67352f917bb92462975770754379d7c25efefba3ac`  
		Last Modified: Wed, 24 Jun 2026 02:04:33 GMT  
		Size: 40.9 KB (40922 bytes)  
		MIME: application/vnd.in-toto+json

### `php:bookworm` - linux; s390x

```console
$ docker pull php@sha256:fe94caf0385c0cc32a0c05e101d61aa68badbf4e614fe50f43123a2997d2d336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162204126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad53a5b8210fc16dc005796c69f2c51c41219710704b0b4e9aa7a73164155db`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:26:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:27:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:27:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:27:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:27:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:27:03 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:27:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:27:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:31:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:31:30 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd1fd44024c3c2b01c65e2a3ae91ae402a73fefbfe72e4120e3d5df753d6e28`  
		Last Modified: Wed, 24 Jun 2026 01:31:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171e7181dd465d34fe8e234f2c7173279f3313efd6a79d7ae9f784251bf88612`  
		Last Modified: Wed, 24 Jun 2026 01:31:58 GMT  
		Size: 80.8 MB (80829436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f528b510344fd3b221bdc99bb679876ab45a2532e00e9252d8af7f61970f422`  
		Last Modified: Wed, 24 Jun 2026 01:31:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c392ad6b838abfb813dcad4abfe5ef26eea5890d82f6568813f05c387d6164`  
		Last Modified: Wed, 24 Jun 2026 01:31:57 GMT  
		Size: 14.5 MB (14506483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11db2e793e2d98f83d9245bcaff1e9930c817059b31778e1d073aa2f96581b6b`  
		Last Modified: Wed, 24 Jun 2026 01:31:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fccdf11a79c259709bbdfd66143ad264264c2cdffbfd55cbc3d1c59c3cd5808`  
		Last Modified: Wed, 24 Jun 2026 01:31:58 GMT  
		Size: 40.0 MB (39970987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caac4fda4414900a35ebc307da461c69c8378ee6af1144e3479697ced976b5e`  
		Last Modified: Wed, 24 Jun 2026 01:31:58 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615ec3e96b1b80bde1bdc7210883018e2d780fdc2a8c2873f62c5397866626c8`  
		Last Modified: Wed, 24 Jun 2026 01:31:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:bookworm` - unknown; unknown

```console
$ docker pull php@sha256:b7383bfbb909287331e165d0820bf0df3ce08b684e1b25970534ffb82322dcd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6281875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e663c34571382ae56bc04dd5ae5546d57f4007464e622dc7dfb45edfd57b276`

```dockerfile
```

-	Layers:
	-	`sha256:0906d2e9f24c91cbec03891a452f9cffa8d655842d47cae3a5f94782354c946b`  
		Last Modified: Wed, 24 Jun 2026 01:31:56 GMT  
		Size: 6.2 MB (6241038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac8944cb4ec74649c3aeee26018178ab2cefb33a70c2c92d9e7db8e4658e972b`  
		Last Modified: Wed, 24 Jun 2026 01:31:56 GMT  
		Size: 40.8 KB (40837 bytes)  
		MIME: application/vnd.in-toto+json
