## `php:8-zts-bullseye`

```console
$ docker pull php@sha256:5cac96ab3941102890d69aa15485f448e75f0e52c0828568a2a449c107e0eac3
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

### `php:8-zts-bullseye` - linux; amd64

```console
$ docker pull php@sha256:81689e50a99959bbce743fc4aa045406ec0d9ce30ebc537e7af54472417231c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175040082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860f06acaca51e9958c36f1837d942b5e7af2ffecf1ad259e3304a449b57388c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a02bca5cc47f06045396a56cb0197c4d9f68cc14f80b93230d9327c7a3d19af`  
		Last Modified: Tue, 25 Feb 2025 02:22:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88905fe0b15289f737261d3dc903a0edff73f750481337d8ed2fa70e6585537a`  
		Last Modified: Tue, 25 Feb 2025 02:22:26 GMT  
		Size: 91.4 MB (91448497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9069447723b0b2f9f140675671130fbf0d3e263d787099a963e347164f2c26`  
		Last Modified: Tue, 25 Feb 2025 02:22:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a990638bad90d9d02edd2ed7182f6785b03c7b13ac61beaaa1b999314fe300b`  
		Last Modified: Tue, 25 Feb 2025 02:22:25 GMT  
		Size: 13.7 MB (13691958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33a1e8cc56e7699e380baa049a4165369185ac127a657c2ae5b8da4eefce55`  
		Last Modified: Tue, 25 Feb 2025 02:22:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3088e36f1e7cf878ac0182c76a626166ec818c218ab794936a7f58b77edd833`  
		Last Modified: Tue, 25 Feb 2025 02:22:26 GMT  
		Size: 39.6 MB (39642070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29df4f76b7b282b13829dbb9564d170efa5d639506d7de69b2b863991d7f407a`  
		Last Modified: Tue, 25 Feb 2025 02:22:26 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da5fa69ffccd9b407bd927fc2a08aecc789157ce65b8667101e0e5f9bf8fc0e`  
		Last Modified: Tue, 25 Feb 2025 02:22:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:bb7b346b668220c394c173aafc11070de650a8c5d238fb06936fe2ce42246c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6551bff9dcbbf4aed422ad80e619d5089fb40adbc4825a91f8f0436b00b60afa`

```dockerfile
```

-	Layers:
	-	`sha256:6c2b4a98b4551488c83774ccfe958a9009e4dded104e90112bf92b76ba534321`  
		Last Modified: Tue, 25 Feb 2025 02:22:25 GMT  
		Size: 6.4 MB (6383989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b5d59613d373665a065dc6fc1347a9952438644ea8e85997526db938889179`  
		Last Modified: Tue, 25 Feb 2025 02:22:25 GMT  
		Size: 39.6 KB (39580 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:1487bed302644437051b25e3f257f209d718b8081148fa87731afbaba08bb923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144276886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4286dd7c653e19ba46a1cfc98f6301c2a173c01d8b0b1ba0bcc4b8ec264673a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6376edd46dda2c697c237efb83c17a91a0979b8e59e202d593f0446305d10167`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29853446d3cd05c0eb401a13f07135f89a449ee487663701b45fb717b9b8e4e8`  
		Last Modified: Tue, 25 Feb 2025 03:00:39 GMT  
		Size: 69.1 MB (69119400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b785546b44d4e782b7e6d1ac072a5cb20d9e0432b17127beae71a8577c4cd2`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c40b9cf61f5214620b2107de9d8cc0435a94ef2eefb2598bcfd994343b7ef70`  
		Last Modified: Tue, 25 Feb 2025 03:00:38 GMT  
		Size: 13.7 MB (13690726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716894c5207cbb8e7c86b7bde6661f72a279df0280c9a9331425cc0f96f230dc`  
		Last Modified: Tue, 25 Feb 2025 03:00:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3293cfea822d15edaabe22da6fbcd49f835f0d6427e1a349afbf8d60dfd1298a`  
		Last Modified: Tue, 25 Feb 2025 03:11:29 GMT  
		Size: 35.9 MB (35927690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375809d9f53ae28081a853ad8c964441459e09ac6c5347f73c03f7c0c55e9c9`  
		Last Modified: Tue, 25 Feb 2025 03:11:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8197192220f112327444302d6717c5b2185e17dc2c5d4fe623038b6c06beb5`  
		Last Modified: Tue, 25 Feb 2025 03:11:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:f25b97a8880db4f01a64fb188cd7a168713608af99828968b2c6d35df3bd7a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f441299406b9ce6b0a0284c2fab1d0ef52740d0e25df8acd7538867745998701`

```dockerfile
```

-	Layers:
	-	`sha256:cd9ae3b16ddac5f985f26f69e81103b85bc008ef4fdc487c5a1c8e17bb334056`  
		Last Modified: Tue, 25 Feb 2025 03:11:27 GMT  
		Size: 6.2 MB (6192804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f23598c3893568482f1b6d328412ab3dad2a87b0ac3ca69a7a74afaf67b6657`  
		Last Modified: Tue, 25 Feb 2025 03:11:27 GMT  
		Size: 39.7 KB (39721 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:85cfe46abbb507e10f6840d9defdbb50f39879155dddb8670a6630546ed6a572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168490258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14a5a4fbd217167afdcb68040fd7d025409452d2e3f861db2c66eebfcfa4740`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cac8d80438c7d8c825ba99a93071ef755fedf47f61ec6695e1a497258d4a6d`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf5e32e0b7c2e87599c9d64521fbaff9ea36e3fbfb51f931baef0cb2e19803`  
		Last Modified: Tue, 25 Feb 2025 03:17:38 GMT  
		Size: 86.7 MB (86734530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bd05e74457394c989762746be7fe63b0dbcf517102c6b331508270af1b04b`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accff7783f66bef408e4ef99994e7b75cba6252a9c3d689b5b2ad971faba4553`  
		Last Modified: Fri, 14 Mar 2025 03:52:14 GMT  
		Size: 13.7 MB (13707528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f80467bbbfa8883a10c6ec2861d9f5ca5d4a29259fb21c9aba3eb4ed40a70ac`  
		Last Modified: Fri, 14 Mar 2025 03:52:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e3e305dcf25608dbb5372ecf7d8605802533a81ab2aa472755f2be3d8ed573`  
		Last Modified: Fri, 14 Mar 2025 03:52:15 GMT  
		Size: 39.3 MB (39298579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486815bcdc674c96dc6c9bed395468583c6a4f8df899e288a15fae2756c9077`  
		Last Modified: Fri, 14 Mar 2025 03:52:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850d6394262074c652a8e44e6037e8692fc7bdaf4ab6f56fc4cc1a7e72881ae`  
		Last Modified: Fri, 14 Mar 2025 03:52:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:5d12aee0e7a1fa626b6bfde759a8a1f6478f8422a51f75104d34739567f45f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6426517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3a4636730a3663a02f53c73f30f0c79d5e43f412fd9906d8c0c7dd4ad1f51f`

```dockerfile
```

-	Layers:
	-	`sha256:0adf4ca20060d03dd0879225e4a86d9314c44f4ce7309519c2d19cd9a49da886`  
		Last Modified: Fri, 14 Mar 2025 03:52:14 GMT  
		Size: 6.4 MB (6386758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4906f8c9269043d718680fe9751c7f9ff6405486e8659451ba09dbd7f34ebff6`  
		Last Modified: Fri, 14 Mar 2025 03:52:14 GMT  
		Size: 39.8 KB (39759 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; 386

```console
$ docker pull php@sha256:78f88922cf71fe4e5e476c3f2c14923e313cd89cad8e6ce9ac904babff03e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177813275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e0397f9f53de3c080d62359083c75fdb1e8f5dd10e812d59cd8fed7b03fd20`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501387466c051b886913dd072868a6eed812b1ffa91dab5199274398fe912f13`  
		Last Modified: Fri, 14 Mar 2025 00:12:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80019263324474d5eb2dcab416657f2392eb9b6e9165e69d4b7640567abb0ad6`  
		Last Modified: Fri, 14 Mar 2025 00:12:56 GMT  
		Size: 92.5 MB (92521229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b91e76e0a872662d3147e3c281472484fe20ba259db9e9dc9e0bb4127c7775`  
		Last Modified: Fri, 14 Mar 2025 00:12:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a40d31d203b36dcfd61ae498a69b590196fd150eaeae919da820156b711d7`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 13.7 MB (13707498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8250cf11d0b5cf913097bb0564e78ba41999f28a3f87ab6084d9689c73e5313a`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a522e32b972a94847fd7cc29acf0cf060c5d6a3fc08ae6a1f6d062ab5eae3018`  
		Last Modified: Fri, 14 Mar 2025 00:12:55 GMT  
		Size: 40.4 MB (40400486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b49c83af15011528381804c9e697c1074000ad07fd0f5289d85df69541fa2`  
		Last Modified: Fri, 14 Mar 2025 00:12:55 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131380131fb907c97f3f79af108c2b24fdb68ff1afdd3fd61c258e35324c8e55`  
		Last Modified: Fri, 14 Mar 2025 00:12:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:622e2a50572e6ad154af4cf95c2f661f581124fc3442e563d343d0c7d3dc9916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d537da0b8d62d3b78555dbaf6c4da8c565e13ba29fa0d785270c7a2f8e862e7`

```dockerfile
```

-	Layers:
	-	`sha256:5732c586716c5031fde629dda8079c9a1f6ddaaada0f73f2976b95ac1d27deb3`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 6.4 MB (6374661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554bf435ab0f25671620583ec896d2620e5390cef92e4d7d48683b0a94a25254`  
		Last Modified: Fri, 14 Mar 2025 00:12:53 GMT  
		Size: 39.5 KB (39538 bytes)  
		MIME: application/vnd.in-toto+json
