## `php:8-zts-bookworm`

```console
$ docker pull php@sha256:9425c2a45b6d9aa817afc80c190355f32e25a1585d2ea57fb08e1d80c77fd4bf
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
$ docker pull php@sha256:037960a1e14fea2707efa66fe37c040abb8e730e2093ef65c56857b685db7d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189825072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b891296777598967eeb0274b3df21f69fed36f325c6fb2d0a6cca53d4a37c9a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:33:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:33:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:33:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:33:17 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:33:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:33:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:36:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:36:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:36:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:36:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:36:04 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f889eb77f0241830a086f7915d940155886af5b1e4cd9b962359548ed7c3b`  
		Last Modified: Fri, 09 Jan 2026 22:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ea84ffc45239814c7e0517d5b21e4d71af80f10c09330171537b859f0fbb16`  
		Last Modified: Fri, 09 Jan 2026 22:36:42 GMT  
		Size: 104.3 MB (104330439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313549f35ce6cdbf932bfa47a4f0645638704fcf38348b48d86a0ffbaa9a15a2`  
		Last Modified: Fri, 09 Jan 2026 22:36:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627a02208efa29012f40a3041b468c66e7bcb52ee30ab62ac65356bff3b6776`  
		Last Modified: Fri, 09 Jan 2026 22:36:34 GMT  
		Size: 14.4 MB (14436687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67081f86e8e5b5316b005f85ec263cd575fbb2d434bed4b1b9894b8437c27438`  
		Last Modified: Fri, 09 Jan 2026 22:36:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63444e334784d65afc3c55c7e07ed211fff751e55e555016307ec025fe2dc1e`  
		Last Modified: Fri, 09 Jan 2026 22:36:35 GMT  
		Size: 42.8 MB (42825883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b92d06ff4ea7ffdbdfa23b62c48c548823ec2676a9a92d33f4302a1a8c124e`  
		Last Modified: Fri, 09 Jan 2026 22:36:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f015e4456ec9f3bc4776dd63695369347c146b50d0d1deda0f05a0f40643a0`  
		Last Modified: Fri, 09 Jan 2026 22:36:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:a51c06156fbf811e768740d15fb4606ca5a645a9b5d9b4ba7726bd9dc8ef45c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be529e40aa9f968c1fa19d7c45dc1a7ac695515e67f1bb54d9130380db504383`

```dockerfile
```

-	Layers:
	-	`sha256:29a2bd2251703ef57f2062141c07b77a4f21f8566ae59732d9eeebfb89609036`  
		Last Modified: Sat, 10 Jan 2026 00:02:06 GMT  
		Size: 6.4 MB (6402556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390b9a0e4e455dba43cc8d3430b42d115feef67ec9645712f0d7a72ba2a2626b`  
		Last Modified: Sat, 10 Jan 2026 00:02:07 GMT  
		Size: 40.0 KB (39966 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:4938db15cb850f9ae49a320c4da671ab5a098e124ebee4a50371e5ed5e1ee355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161254007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3eefc8246c6be42588ce30c93bbd41efe9d855c4be7ae2ceb7bdc3d72dfba7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:31:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:31:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:31:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:31:18 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:31:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:31:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:34:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:34:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:34:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:34:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:34:31 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59432dbb9dfb1cab2838719babaf19851eafb29d55d969f2a5d36bcef1e6aaeb`  
		Last Modified: Tue, 13 Jan 2026 01:34:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c02140b52860e46666b9a0c3ac040413fcd458d8c78280429c30d32a437a561`  
		Last Modified: Tue, 13 Jan 2026 01:35:03 GMT  
		Size: 82.0 MB (81983517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c95436aab87afa4e76a7912955dacea564ef7e3fdf3df1ea275145c6717f79`  
		Last Modified: Tue, 13 Jan 2026 01:34:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1015e757a7529e8ae0329e7f69285352d8b153528a2fd7f764bef925d5d91b42`  
		Last Modified: Tue, 13 Jan 2026 01:34:59 GMT  
		Size: 14.4 MB (14435003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d49a5e8d2d1a6b5aabf8b64b4e25ad528551e1454849df17e5265424f6c2c`  
		Last Modified: Tue, 13 Jan 2026 01:34:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3a8ba3296f11eb06386ff3b106f7935fe977f05c914b8a4bf4d822ad9099dc`  
		Last Modified: Tue, 13 Jan 2026 01:35:02 GMT  
		Size: 39.1 MB (39074162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01664ad50441c48298ac51be5a340ed85fee4c1fd994a7fa0dcc5c7186a9917f`  
		Last Modified: Tue, 13 Jan 2026 01:34:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c0390561a2b830d9450410a0e068575e7f96dd18e3a55d97a8ce2a7691ab49`  
		Last Modified: Tue, 13 Jan 2026 01:34:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:992372f0845a18b8a63a799154472dae322ac5f0494ff759e221e41aa807e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628a0c2e66f87ce4e70e96d9b27a5c53c39d75d54d463777c767c9ca73af4f8`

```dockerfile
```

-	Layers:
	-	`sha256:a35a832041a91515bce07f58f854181c59000679a04d6c5c44cd8dfb6dea2d0f`  
		Last Modified: Tue, 13 Jan 2026 02:59:48 GMT  
		Size: 6.2 MB (6211892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb8ae5ba772122ff499a62d83125da238f4d1913fbbfab8ff30168a076316f7`  
		Last Modified: Tue, 13 Jan 2026 02:59:49 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:25b425099673a951fce279c154a9481601190de15c27eaa9339b2d705ea79506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151866315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8d84363874fa2c66a5700639fd5570759f4f02ba808c89cd8d795f0c988995`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:34:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:34:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:34:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:34:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:34:33 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:42:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:45:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:45:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:45:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:45:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:45:22 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f68fce27998fc820c46bbdb68383e9423af946796e20ee7672bfbe2783ffc6`  
		Last Modified: Tue, 13 Jan 2026 01:37:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a1818abf42bfd3dd9260b65f47fc2afd661982040159d3047a3d846600982b`  
		Last Modified: Tue, 13 Jan 2026 01:37:56 GMT  
		Size: 76.2 MB (76151875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8c8d62116aec2133ef6f1195ed354aa32823bb2d58ad27cbadba0b78c4aa0`  
		Last Modified: Tue, 13 Jan 2026 01:37:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595bfdf1af05ecebe8a34bfcaa5d980470cae037f7fe58c31d87f5da53e7c6be`  
		Last Modified: Tue, 13 Jan 2026 01:45:47 GMT  
		Size: 14.4 MB (14434982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06701f36241c80f3a44578c2db1e31bcdc31428449ad94a2e732f2bc13b0cd6`  
		Last Modified: Tue, 13 Jan 2026 01:45:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f03491f56cf551e4e9daca4fa6be260e5c8bdc8f25591a1e8bde428d1ada04`  
		Last Modified: Tue, 13 Jan 2026 01:45:44 GMT  
		Size: 37.3 MB (37341706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9b483f359b8bc933f585797e21a9c59fba70f20d51750cd6ff580a95d2c74`  
		Last Modified: Tue, 13 Jan 2026 01:45:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c4452138762b0acde45f81d048ca47dd260238dfeebce52927ccc8847911de`  
		Last Modified: Tue, 13 Jan 2026 01:45:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:8db14b0e522151b23ad1c2a2023c33090912a89b9e7199ee98f3632abc0fa26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766d8463753e1957cb62748e2f6586d9bef074dea981871ba28de9ad824b49d5`

```dockerfile
```

-	Layers:
	-	`sha256:ad2c98be4008900ef95e0d8391a61b1434379b5deb192ed5b3a1f106ee8a5a82`  
		Last Modified: Tue, 13 Jan 2026 03:00:01 GMT  
		Size: 6.2 MB (6215836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e87256510bd08edf3db746184862ec718dd35a9394253076a2abd684e1e9f9`  
		Last Modified: Tue, 13 Jan 2026 03:00:02 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1ba41b4130b8674de8bd60a5b3723de25ec2d9d353417aaf171f4b12c2e16b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182858462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a2c131283d6f4251810fe3ea0662bcfbe4a9ddeae6d8d87f267b6af866a145`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:28:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:28:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:28:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:28:51 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:29:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:29:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:32:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:32:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:32:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:32:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:32:04 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4405a82b71eb7cf1924284d02e7d0f7145c370646f6563c3a63e32079fa90`  
		Last Modified: Tue, 13 Jan 2026 01:32:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dbc4e03badded3de2c577b1a3ea34c7eac3191164a560fb1f561779f1f8660`  
		Last Modified: Tue, 13 Jan 2026 01:32:45 GMT  
		Size: 98.2 MB (98166773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229cff7b3a1d416da2a46a353c6377556339e5170a128ea03c2f0eeaba90faf8`  
		Last Modified: Tue, 13 Jan 2026 01:32:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dc539cf7d72df6e697fe381fb6ccc4612fe7ce2e12584061e20081b41658b1`  
		Last Modified: Tue, 13 Jan 2026 01:32:37 GMT  
		Size: 14.4 MB (14436510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0fe3a966fb87fcb2106bbea4603f00bf9ca8b0b552720db29876c640bdcb3e`  
		Last Modified: Tue, 13 Jan 2026 01:32:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621f472d2ae6cea94312b288add0f3f2cb62023204f4ff4c4933d190b6bd298`  
		Last Modified: Tue, 13 Jan 2026 01:32:39 GMT  
		Size: 42.1 MB (42143660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75536cf234882c7c62014f3668ac3e0b9b99c18aaecfe165a1f4b4e5575f0228`  
		Last Modified: Tue, 13 Jan 2026 01:32:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4042ff4d7e969f0b466a1a73931940ae5e58cd6ee377ff480a46803e83ad7977`  
		Last Modified: Tue, 13 Jan 2026 01:32:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:13e5ea08bf532f25ade52bbf083fa3f0647cb30854b94eaef0529faf9051e2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad162319a04a9c9470bcd584a920d0e5c95cd4e09e55ec9e1bf73f0d767c7df4`

```dockerfile
```

-	Layers:
	-	`sha256:e72a71d8a2c12adbeccac78e9cdf54ac5fd81085ddbe63458cab078ee3bfdeba`  
		Last Modified: Tue, 13 Jan 2026 03:00:11 GMT  
		Size: 6.4 MB (6430957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f493eccc6463e3a7c918bf2d5aff26e674e09476bd2ba27b46389ed8f2c87ee2`  
		Last Modified: Tue, 13 Jan 2026 03:00:12 GMT  
		Size: 40.1 KB (40140 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; 386

```console
$ docker pull php@sha256:3d7f43710a9f069b553bb15d92b4db3c08a532d0c5692737e3bfb6fbe7f6902b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188888018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312cf5965951917a3c1096398b3a2f1fac756d40d73dcc23a5d990facf95fd3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:26:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:26:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:26:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:26:58 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:27:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:27:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:30:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:30:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:30:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:30:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:30:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b148b2c255305f0011784cbdd1e8f355d06f061e5237ef5bcaba70f30b938c27`  
		Last Modified: Tue, 13 Jan 2026 01:30:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dff6d0c1e870584136df4d6e3e8bbe7c2c8d920518a39d9fbecb538d6f610d`  
		Last Modified: Tue, 13 Jan 2026 01:30:55 GMT  
		Size: 101.5 MB (101523050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15fd2be855635086952094cfc12dc662a66c227c749138d57af8a78d9a0c485`  
		Last Modified: Tue, 13 Jan 2026 01:30:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639a13627dd395462fcc4d7f2b6667f96f2570a4bb45d87d1eaa2f838ae19f2`  
		Last Modified: Tue, 13 Jan 2026 01:30:49 GMT  
		Size: 14.4 MB (14435974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa60c8486bbd48741e640c58ff859fe2116878fb4f8437b3f778ff3ddc0d603`  
		Last Modified: Tue, 13 Jan 2026 01:30:47 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4945d62080d9d4e94f8773b244bb106b669b00ebf1c6dea0a0f403ad451e053f`  
		Last Modified: Tue, 13 Jan 2026 01:30:51 GMT  
		Size: 43.7 MB (43715290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb16f0526f256511c3d500de70cae518101dbc1cfe5708ce790c040507e9ce`  
		Last Modified: Tue, 13 Jan 2026 01:30:52 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a141fc3a86f89397acd52e9ef3bd5a563056ddbc51d90c12143aa0478ee965`  
		Last Modified: Tue, 13 Jan 2026 01:30:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:1fda82182ec9a435b8d6d571b283a57f72bb5bee5657e6b627531f474b748472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6422282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7072515cd683c7d59dbfb835742e567afd80d8a21b672cc00322aadb24fc074`

```dockerfile
```

-	Layers:
	-	`sha256:2efb0d0ff470d4f19c44fb45081343e2993c1ad83f58e469be037d897f29e50b`  
		Last Modified: Tue, 13 Jan 2026 03:00:20 GMT  
		Size: 6.4 MB (6382358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752c8c860aa4f51029c52b577293b880c086be155ee473c89b3c10a843675dad`  
		Last Modified: Tue, 13 Jan 2026 03:00:21 GMT  
		Size: 39.9 KB (39924 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:7ac2f3899cd96132e89c0c010423d9a153adc4e3706aeec60568733de1142798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163383994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62f5796ec5fa9d4277c04534c48532824f34369d802e4a17435c0fbee900455`
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
# Sat, 10 Jan 2026 00:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:59:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:59:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:59:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:59:24 GMT
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
	-	`sha256:755c34e643a27bb0b0a031cf725890cc4cda8d16ebd4fb2fb8e6bff1a1bf8a7d`  
		Last Modified: Sat, 10 Jan 2026 01:00:45 GMT  
		Size: 39.8 MB (39761411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d065cdac8b789265f31a605a5b1aaa089c6bcaaaf0e2ef57092b94e1333735`  
		Last Modified: Sat, 10 Jan 2026 01:00:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e943643dfba756232487aa84992ccaebc27f1db9646cb24aad8f0c84da7f4db`  
		Last Modified: Sat, 10 Jan 2026 01:00:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:d7afe9c3801e2075b7b9b70cf5407ef48b016c33ff8ed5dc961b15300a857493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d6470a58bef4e188a9d27037454475fac8f86acd09d1bd58e5f513bfdf0f2e`

```dockerfile
```

-	Layers:
	-	`sha256:183bc7a6829646b8c499a133917263f385fba81664d2c8f3efc294762e370a68`  
		Last Modified: Sat, 10 Jan 2026 02:56:31 GMT  
		Size: 39.8 KB (39827 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:6608f59144f65b06be6d2685ed04951859ea57f4db3126fb3836b6be21a19672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193375790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225a48ff8b04eb77269d1da85453f3e2df75ea11f22a6a2295e7b4839e2b5e65`
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
# Fri, 09 Jan 2026 23:25:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:25:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:25:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:25:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:25:42 GMT
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
	-	`sha256:a63dcad0c158b08e3a88b2debd6f6492590e8baa0e939c93f7d691693ebc4992`  
		Last Modified: Fri, 09 Jan 2026 23:26:21 GMT  
		Size: 43.5 MB (43538046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123acf6ea30553b3194c8c6ad9af902d1f24174d10705b2abb5ce7ad4515873`  
		Last Modified: Fri, 09 Jan 2026 23:26:18 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc79336fd377cc3e411012d37100d8000c8a4fc64ef0a9b6eb2cd566eb95e72`  
		Last Modified: Fri, 09 Jan 2026 23:26:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:bb9a46d93bde1dcdd0ad0882231edb3cf83450e341615e7a01a2ae123a7c2445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6418294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45c7fc322fdfdbafbffd4e0cdc37de087b30445e673ee6dbfae2eeee3c4fd29`

```dockerfile
```

-	Layers:
	-	`sha256:9c386982488414acd97632b495da65d9f87735026d8699fb87c1e0cdc7ab6566`  
		Last Modified: Sat, 10 Jan 2026 00:48:46 GMT  
		Size: 6.4 MB (6379226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78c1c3e963d25d0486207e803ae023b45ea32e458d3eee5857c4895ed5d2764`  
		Last Modified: Sat, 10 Jan 2026 00:48:46 GMT  
		Size: 39.1 KB (39068 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bookworm` - linux; s390x

```console
$ docker pull php@sha256:bff9a4dada86c2306bffba8c076ad5774cc4d5b1bd71ed1c485fc81347efaf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162149957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e617922517e404c3703bfd308a2176b8bce03f9ec3f488d93e1236f4566bfa05`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:16:21 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:21:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:21:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:25:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:25:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:25:46 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e6e14812c7e54396f415d6014813037f658715594f0b42666ebd475403e655`  
		Last Modified: Tue, 13 Jan 2026 01:20:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a215d0df5c84164f0ef7022f6b8d351f30d7d311b1972e160e3372c4db98d`  
		Last Modified: Tue, 13 Jan 2026 01:20:58 GMT  
		Size: 80.8 MB (80826754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6d70cdf5271476252f9bcccd7c6a723309f9e4c8a2c694084e682ecd4d8c9f`  
		Last Modified: Tue, 13 Jan 2026 01:20:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f42743e474cabfbac6200547dcd1f46688a97364c5376c86db36b0d9b991640`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 14.4 MB (14435319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc593ef9d9968d69ee84066f6d1b1c758f4b1495e4130f02437cff050b8fa76`  
		Last Modified: Tue, 13 Jan 2026 01:25:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1be946d4e83c5f4541e892f05767ae1bd7dea5a65ec6eb51ff9b965e61f302`  
		Last Modified: Tue, 13 Jan 2026 01:26:15 GMT  
		Size: 40.0 MB (39999838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193889930e0a027b2b2e52bcf6e16eab3c9b762f3845bc0160d9b978f2ba4ec`  
		Last Modified: Tue, 13 Jan 2026 01:34:50 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567c640b87fce8369fc6398a1b2ba43f0da60cb27a65c23cd56371f37ef99099`  
		Last Modified: Tue, 13 Jan 2026 01:26:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:09cf79f1632e268862345d76d3bbce7c8351b33210fb4d5f8f836b6c3d4ce0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6278798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f666bb5f68efafeaba69711888d5976982748583c5d13b14b2d540476a88138`

```dockerfile
```

-	Layers:
	-	`sha256:834dc0e16c0a3d28a9214bd4312a8f02805dd2e939713f9087ad1d1b0f084b67`  
		Last Modified: Tue, 13 Jan 2026 03:00:39 GMT  
		Size: 6.2 MB (6239790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb56c27d76fee5183cc9cd05d6196f15b582fb858871a06bb7ae74d07da1f983`  
		Last Modified: Tue, 13 Jan 2026 03:00:40 GMT  
		Size: 39.0 KB (39008 bytes)  
		MIME: application/vnd.in-toto+json
