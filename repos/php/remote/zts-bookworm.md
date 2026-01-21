## `php:zts-bookworm`

```console
$ docker pull php@sha256:763e51557ed114fa394b16d24431ef5019a524d9190ea45a43bbd48bc755fc2f
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

### `php:zts-bookworm` - linux; amd64

```console
$ docker pull php@sha256:fb9b20d55bc30f9adf2a9dc2832037c6f56bbfae0c7ddda6f8a83101af46fe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189844193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c449427d025d29df644f3cfa2eae1e29910630609521fec10a82e73496eaa2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:20:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:21:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:21:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:21:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_VERSION=8.5.2
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Fri, 16 Jan 2026 23:21:00 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:21:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:21:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:23:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:23:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:23:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:23:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:23:36 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e43f9f312a74a9a2459405a9002c484fb3cfc7dc9d5d358dbaaf9687463267`  
		Last Modified: Fri, 16 Jan 2026 23:24:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedfbf955141e740691cd4034618e8e34b1ccd1cc931c0cf676848708005ebb3`  
		Last Modified: Fri, 16 Jan 2026 23:23:58 GMT  
		Size: 104.3 MB (104333016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac68b2817079f5fb8a5c8eaf2e4e91a8ca3d9f7b6ca6ba9432052fdb57542259`  
		Last Modified: Fri, 16 Jan 2026 23:24:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898734f47ca423bc6b417430d5506ab5477bb98aa209d111bed27af3ad89c32b`  
		Last Modified: Fri, 16 Jan 2026 23:24:07 GMT  
		Size: 14.4 MB (14441766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe71d5b411f0bd9b341bd3a4d52edfd4de262d15e21552f66f9e401394ef2c1`  
		Last Modified: Sat, 17 Jan 2026 00:28:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738808eb5fd73bea281b7054d25873c170f5690fd8bfd4bdbbe90d870e2956b4`  
		Last Modified: Sat, 17 Jan 2026 00:28:51 GMT  
		Size: 42.8 MB (42837197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3cc8f36d0e04921d48a19756defb257f80a14781ff2e1e42380a4ac39de8dd`  
		Last Modified: Sat, 17 Jan 2026 00:28:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5443c6f6a126825a61fd2aca7fb9c3e380b57c7298c7e3e3e4787e4039281ae`  
		Last Modified: Sat, 17 Jan 2026 00:28:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:314d7047545b0d0267e883c41c065e0471920474bb668d11f2b7c6a0f639980d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1da6031e24a3c20444d3cc9d253c61fb01f2d66b113da8999c661c06998e1ca`

```dockerfile
```

-	Layers:
	-	`sha256:01a9243d1199eb8bc28450f01fc697e40a72523749c97546347fc8532043b768`  
		Last Modified: Sat, 17 Jan 2026 00:02:39 GMT  
		Size: 6.4 MB (6402566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ade1e7d360757cf1dd2c6dd66c2d109eea00a6d707d28447733e232dfaeedb`  
		Last Modified: Sat, 17 Jan 2026 00:02:40 GMT  
		Size: 40.0 KB (39968 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:4497733fc986b6832a420012352413419237a538e62adc6829542f5107215b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161271662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85377e84abee8c7bcc6d5e40c4ac6373c5dd754c2e2e2c892ab63746381cd724`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:25:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:25:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:25:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:25:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_VERSION=8.5.2
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Fri, 16 Jan 2026 23:25:42 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:25:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:28:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:28:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:28:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:28:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:28:50 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b38b3f6fa04bd973f42c4dcf753d459eaa65d586b486dc7e18fc24d302a38`  
		Last Modified: Fri, 16 Jan 2026 23:29:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c2fc895d65c4e81944952383724797c234b6cac64be244702be0eb061ad52f`  
		Last Modified: Fri, 16 Jan 2026 23:29:24 GMT  
		Size: 82.0 MB (81983557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108360f561543b205088d2ba03c3c9189db11b3dbe48c99d34fd806965b4050`  
		Last Modified: Fri, 16 Jan 2026 23:29:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4010a23ad94d6caba96999d069800e303764a68885ff0524620fe8b84cc77806`  
		Last Modified: Fri, 16 Jan 2026 23:29:09 GMT  
		Size: 14.4 MB (14439595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8466a229237ad329152fa4d993313ab2487ad88efdedbb9edd87cd1715ed2e`  
		Last Modified: Fri, 16 Jan 2026 23:29:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a4ed6c7fac3db6f322a721df732c32442a711aff255cab260da4eed08d561d`  
		Last Modified: Fri, 16 Jan 2026 23:29:25 GMT  
		Size: 39.1 MB (39087175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d653d013764be65a0cdc921963b5830b857f4bac304b1b300b3e6f02e58da972`  
		Last Modified: Fri, 16 Jan 2026 23:29:19 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e28232f74d3e256bbbd288497339c40a67fc968e107a2bbb39048bd50c37dd0`  
		Last Modified: Fri, 16 Jan 2026 23:29:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:17732adf61c891de860deb0dd1f73e6006bd9e044f91e52bbb57899c6d2049ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f2c840e954554f9f1172513cd212d8fd75ce5d075357e9bf962c0cc08650f`

```dockerfile
```

-	Layers:
	-	`sha256:788ef938fac9834fc14913c5ca43aec9ca92dcdb7a2fbdc0624214573fc4e9e4`  
		Last Modified: Sat, 17 Jan 2026 00:02:48 GMT  
		Size: 6.2 MB (6211892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba5bb3ae33cf25edd3ed435727edb534ee72aa7016ed66db495b77a4f2a8f89`  
		Last Modified: Sat, 17 Jan 2026 00:02:49 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:c3e4d9c52c196d82f840e1e3299baf39a17612f7708e708448c807b78952af47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151878393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7aa16722f1f99446d4ee46378bf8dc37b47fcf56e87f45e11f1a3b9dd90a55`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:16:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:16:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:16:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_VERSION=8.5.2
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Fri, 16 Jan 2026 23:16:55 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:17:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:19:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:19:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:19:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:19:44 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fee7c177aa8ca4b44b4ef2d265c6038633d514233f40bbc0f6d181ec2aa95`  
		Last Modified: Fri, 16 Jan 2026 23:19:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d0f60b706ba2365574d3998bcb1aabb8cfe3734194de70159f004ade55e53e`  
		Last Modified: Fri, 16 Jan 2026 23:20:02 GMT  
		Size: 76.2 MB (76151909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c85958368acedaa45e8685eb57a97da909b14602ba16eee378ff658af4b27`  
		Last Modified: Fri, 16 Jan 2026 23:20:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0c06765c0955cd84dcda5bd720cb7e0096aa96a292c198ae35576156749be8`  
		Last Modified: Fri, 16 Jan 2026 23:20:00 GMT  
		Size: 14.4 MB (14439530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696a65cd70280dbe17948faa94d3d08a1236a65e61fcd94b03bbdc0744d9982`  
		Last Modified: Fri, 16 Jan 2026 23:20:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899af66cba4281236cd9f9e031a2898b4215dda4cc45c60260dfbee0a12eebab`  
		Last Modified: Sat, 17 Jan 2026 00:29:30 GMT  
		Size: 37.3 MB (37349207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f7ca9c7a8b217f02795da1b40bc56a2747c86acc80d218bf8f34ad41575d3d`  
		Last Modified: Fri, 16 Jan 2026 23:20:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b3c66857cdb2959750cbaab219b02249bc5af13ac56e93b5fde25b7c45d51`  
		Last Modified: Sat, 17 Jan 2026 00:29:32 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:87bd43c1f4c62f44aab04d1570f9caf6131ea9524bc12fcde08c82160f7bed6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1761ce67d64fef70628810692134de534a46954da037e15b0e19f8fda9649dfb`

```dockerfile
```

-	Layers:
	-	`sha256:3bc7ace18a98d3d508e4403c192af29737bbf8ca31b6d69feca99f834d712f9a`  
		Last Modified: Fri, 16 Jan 2026 23:20:00 GMT  
		Size: 6.2 MB (6215836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daab874f9982e2c0a3f378bdd4300ed8a1a6a929e7e6f69c1d4ba5dcdba8707d`  
		Last Modified: Sat, 17 Jan 2026 00:02:56 GMT  
		Size: 40.1 KB (40106 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:e8c10deb6602a0b4e47b37966cc3d7f1fdd6e457b0128526aecb68bf81d31aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182869438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51950d80b489a00a39f3af4d9d3d444b315a83ef500f4db3693032b6855cbe78`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:18:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:18:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:18:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_VERSION=8.5.2
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Fri, 16 Jan 2026 23:18:20 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:18:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:18:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:21:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:21:29 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74193e2c56203cc6238b62424411051ece5e1958a87bba40a4ac3ff4c2f1fa33`  
		Last Modified: Fri, 16 Jan 2026 23:22:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264cf4385c032435125f95555042c38163dbc1d296603824c348083b2e03c97c`  
		Last Modified: Fri, 16 Jan 2026 23:21:51 GMT  
		Size: 98.2 MB (98167005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887c2af87a2bdc0a6b0761beec26a9d9f791eefc22a7a737c05f0eb0897deca9`  
		Last Modified: Fri, 16 Jan 2026 23:21:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f8e96688763e9548929700e1708998cccc2b14ba4c87f7018cd0aef9faa84`  
		Last Modified: Fri, 16 Jan 2026 23:22:06 GMT  
		Size: 14.4 MB (14441533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9928018c54b265d239213955d43aee4c31b8b794fadc049c954af12408e11b`  
		Last Modified: Fri, 16 Jan 2026 23:21:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90bd83440b820bd1f344a1d6bd495a8d62937996cf12c8e84b2388008a1e429`  
		Last Modified: Fri, 16 Jan 2026 23:21:51 GMT  
		Size: 42.1 MB (42149374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fad87f7d5fe0de4f9702968dd349c0fb1959f6cbf4a107c314655dcea84ac54`  
		Last Modified: Fri, 16 Jan 2026 23:27:54 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82882f70e3d8859a6115ed85baaab41b84c2136a0cd05406fc6998e79e87b8b0`  
		Last Modified: Fri, 16 Jan 2026 23:21:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:1eae32b8cb29ef1d7ec3caaf7e00125e74e81b59e981e6ea7f62e3271bac35c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbd7ae7cd93328309599c2952515eed653556896224620393a3edbd0b2e3299`

```dockerfile
```

-	Layers:
	-	`sha256:6ad2bf34f5024de4128775d70305abaa8a1173630494a1d48849f161871b8835`  
		Last Modified: Sat, 17 Jan 2026 00:03:02 GMT  
		Size: 6.4 MB (6430957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e70aab61d03515eb2070cd72799811de85d126923886381f29d7936e6783ba4`  
		Last Modified: Fri, 16 Jan 2026 23:21:48 GMT  
		Size: 40.1 KB (40140 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; 386

```console
$ docker pull php@sha256:49bed3823457598d1863d305f879ba9278f7e73d7dc1f9162ff69f430b4f1aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188905684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cf846ef9a5517e00661ad378e062215dda8db99d5634325ae10870c9be92ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:18:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:18:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_VERSION=8.5.2
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Fri, 16 Jan 2026 23:18:38 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:18:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:18:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:21:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:21:29 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc8343aeef7626c1aa248b43d2c38149f015294513e2b5c93e6e4e5f80fc67`  
		Last Modified: Fri, 16 Jan 2026 23:21:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6933328dad865324cbb42d837b7fcc7073527155c8373d6d23a781e701754b`  
		Last Modified: Fri, 16 Jan 2026 23:22:10 GMT  
		Size: 101.5 MB (101522093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fffe2498de2104c993cc1dd9eb211c248b2bd69f6b04dc4562f00a17c67dd2`  
		Last Modified: Fri, 16 Jan 2026 23:21:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e5380edf49d426b343dfa86cfdc5de9cee2f65a824e2c4ab6ecd57b3e40427`  
		Last Modified: Fri, 16 Jan 2026 23:22:00 GMT  
		Size: 14.4 MB (14440805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b6f4c719fcfee4994502e79733069de148db5b14bad51ec621521fc3720c1`  
		Last Modified: Fri, 16 Jan 2026 23:21:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebffc1888dc0c9c4d13d60eafcd1b87a105dd8ac5f1ac9232aaf640126a2466`  
		Last Modified: Fri, 16 Jan 2026 23:22:01 GMT  
		Size: 43.7 MB (43729081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ced17d0f6d181a7b7e238966b785317b53977315b0d3f40163edfb4f4f2edc`  
		Last Modified: Fri, 16 Jan 2026 23:21:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394436fa14178f3319137d8208711c60d1fd417fadc0c47fb057d1ad622a8277`  
		Last Modified: Sat, 17 Jan 2026 00:30:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:d5c1b05b584bb82ce939429836f4f9b6155bd8c852dbb89e756f7fd84dabed50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6422283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42402db539e7b2e1a8d6105404eed36f9929174bef6bfd0c456c478851a6c024`

```dockerfile
```

-	Layers:
	-	`sha256:4bba46445f6148495e80da2967f7c70f34093c26f22d7b62d279513a32f400cb`  
		Last Modified: Sat, 17 Jan 2026 00:03:12 GMT  
		Size: 6.4 MB (6382358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53ebc2142daccae8deb9b01f3f1f8c92d84d2692186659af66c8984c23a544d`  
		Last Modified: Sat, 17 Jan 2026 00:03:13 GMT  
		Size: 39.9 KB (39925 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:757b1bdbbfdd89982c817833eb4ec32dd1eb869e5204c12b2fedeeb6969ac51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163396546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d702b6b0fabea2b89de3ac11e010cc70e1e145501dc988b0644fe4b823923aa4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:19:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:19:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:19:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_VERSION=8.5.2
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:13:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 00:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:29:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 00:29:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 00:29:14 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:41:02 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51a9bfcf7cf609d0809aa35fe905b8337228e88a749e1ab55783bf9036c2f1`  
		Last Modified: Tue, 13 Jan 2026 01:39:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031cebecc9a3bf8a4330bb9afd89498969466d0b89923bfe83d8b23d200df1ad`  
		Last Modified: Tue, 13 Jan 2026 01:39:25 GMT  
		Size: 80.7 MB (80673057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d27ad6411f6e09f08f7101bc8738b0def3a7fc371dd25183cbec81d8e5129bc`  
		Last Modified: Tue, 13 Jan 2026 01:39:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df0f4e26ffba7e01a2f724c9e044cbfa1a2ca0b8f8b4736727ac29556f9e02a`  
		Last Modified: Fri, 16 Jan 2026 23:31:41 GMT  
		Size: 14.4 MB (14439160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f66290314368065858444f2202cad16b1203e64d6825b7ef6a22b33f41aa768`  
		Last Modified: Fri, 16 Jan 2026 23:31:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359e3d8e60cb3f7a61ce86d3dfb48d46cb9eeae845fd61bbe9590c2f5fa431b8`  
		Last Modified: Sat, 17 Jan 2026 00:30:17 GMT  
		Size: 39.8 MB (39766935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b23aaf716ff7d9d9704a70e72dd41e6f12ee698608bffb6a8315cc6d77bb12`  
		Last Modified: Sat, 17 Jan 2026 00:30:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577bac7985850bc60975156493c10f99d7004466eb2f41b1f762a504d83e62d3`  
		Last Modified: Sat, 17 Jan 2026 00:30:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:516886029dbe7a3e5a52f310d06fd869b3eb6b966afaed751cab0476539cd8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d43848155dc196725f2523abc0b01eed3a6078010a3b020f74132f22e3ca50`

```dockerfile
```

-	Layers:
	-	`sha256:5f7b8268833cb14469202181ce2e016c9d2384b698e31791b3de20b82ac125f0`  
		Last Modified: Sat, 17 Jan 2026 02:55:34 GMT  
		Size: 39.8 KB (39827 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:1afdcf3c71d59ac577e02d169e767e7f407b0defc58c39eed5c82a605a0751e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193389693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c84b46f5468ed31a488246ec3d963de69378a7bb81d1f53eb32aa0b1636051f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 23:27:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 23:29:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 23:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 23:29:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 23:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 23:29:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_VERSION=8.5.2
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:27:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:28:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:39:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:39:14 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00c9d4d1f21b6d304a55b7e116c52ef24850215b997b0a7114c53786a7900dd`  
		Last Modified: Tue, 13 Jan 2026 23:34:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b37bde8bf655d33e96bd4868142d3ae6d50517082efa680a17e47b74d623b4`  
		Last Modified: Tue, 13 Jan 2026 23:34:59 GMT  
		Size: 103.3 MB (103329187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b68a31428e2045dc30793a85499acb8c152ace336ad3f0098f98076ea7a713`  
		Last Modified: Tue, 13 Jan 2026 23:35:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d55b0a87b1ee60e2d017000a48f83972b7ad690f234db9120ab905e3352327`  
		Last Modified: Fri, 16 Jan 2026 23:33:48 GMT  
		Size: 14.4 MB (14441447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de8344019b12fd5f478c59c7fbc0d056533c73efe19d0893556cc966ca0da9`  
		Last Modified: Fri, 16 Jan 2026 23:33:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a5d93d9ce23c1a2839e0e31f2f9c07f7c7c35c74adc1944a7bdbca68f584f5`  
		Last Modified: Fri, 16 Jan 2026 23:39:58 GMT  
		Size: 43.5 MB (43546718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652df7a9c7cc791d32efaa8ab4438f1b48e9d9cc4e3c15762a560f7b5eb6623d`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766f0cbf8d44a02bd7aad9a9505c17a384e16fc2353284bcf3e722cdc500351`  
		Last Modified: Fri, 16 Jan 2026 23:39:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:f566fa7c71923485e31b14b04274031a523f9268345b7b651342399c1060a5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6418304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb13befd9dfde17caf89ce9db2f152ad10ff9269a1347703f100fafbcc68716`

```dockerfile
```

-	Layers:
	-	`sha256:7fd66cebe2cd36307d70793a97e6bfd02a6bee92f57d7e7b9f1fa1f01b44b792`  
		Last Modified: Sat, 17 Jan 2026 00:03:22 GMT  
		Size: 6.4 MB (6379236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401560f34d19263e6fd0e1ab16b89d58e6f228f08f30a3723db1bf2d0ea2182b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 39.1 KB (39068 bytes)  
		MIME: application/vnd.in-toto+json

### `php:zts-bookworm` - linux; s390x

```console
$ docker pull php@sha256:6f4576108a1f19473711e2351b3ca376233966cabaefe0efce7545282b741fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162161095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c1ca2dc4560c9ea99856db3760e1c42699e5b949aa9341bbf08a6da8f56cc4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:15:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:16:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:16:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:16:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_VERSION=8.5.2
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Tue, 13 Jan 2026 01:16:06 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Fri, 16 Jan 2026 23:19:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:19:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:23:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:23:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:23:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:23:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:23:52 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3766798529cf3b6bb78b89f92c2ddd3c8d692bdbefd74a009535cc29fc6111ec`  
		Last Modified: Tue, 13 Jan 2026 01:20:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f3524fd2fc0fad2d1735b4e8710e6a4ca75fee8f6d05751fb7556521ceeb6`  
		Last Modified: Tue, 13 Jan 2026 01:20:52 GMT  
		Size: 80.8 MB (80826790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8bf183de4ac6f7175a3a79396bee838b2d235222044e6f398dda5a5d2de72d`  
		Last Modified: Tue, 13 Jan 2026 01:20:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d97624eda7eb660efc52fb5434c1cee459c1ed9c80abe2d2a40abd7e64084c5`  
		Last Modified: Fri, 16 Jan 2026 23:24:26 GMT  
		Size: 14.4 MB (14440017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f143d4787e4f302f3641f4bc0fd10be3f495ea26ac26970df5f8d6e7897dde23`  
		Last Modified: Fri, 16 Jan 2026 23:38:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f2b3566e16c390d2611e7de4ab46e51deb43834ef8211ecff9e450ed4c05a7`  
		Last Modified: Sat, 17 Jan 2026 00:32:25 GMT  
		Size: 40.0 MB (40006233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abb621375af7f1a599f0b3a0e1594730d0a7be0539e8884ef7b7fe52a3499a6`  
		Last Modified: Sat, 17 Jan 2026 00:32:24 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd09aceefbfe009887c0325ff7d5133061bb98901f3a622a7a8cf664b7426e5`  
		Last Modified: Fri, 16 Jan 2026 23:24:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:zts-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:8fb0e0d825e4af4ee72989c657dc70a89bf259974a4a8f8c020cd92eb55f90be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6279751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d103d55dbb10495295dc2bc2d5826b7fd32845b928eb914407a8e1f129d4e0d`

```dockerfile
```

-	Layers:
	-	`sha256:44bd50ab332bad176feaf326c12b04f4d9c1da0969f5c9eb1ab513b80af78dd9`  
		Last Modified: Sat, 17 Jan 2026 00:03:30 GMT  
		Size: 6.2 MB (6239790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962a31fddb35996217f7b7112a8194e95e464ba58497b9f20d1ce0dd2ab26ef5`  
		Last Modified: Sat, 17 Jan 2026 00:03:31 GMT  
		Size: 40.0 KB (39961 bytes)  
		MIME: application/vnd.in-toto+json
