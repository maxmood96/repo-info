## `php:8-zts-bullseye`

```console
$ docker pull php@sha256:73176012a4e2b82a96ab28c779237fff989f550270a2c24915809f107917c3f6
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
$ docker pull php@sha256:d29ee83527e16dadc9353b8caa08772deec02d2d9dee4f3d733c666db139033a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175311571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d1a52f3f12dbb2d8a0a24efc99483b6ef0913a5667ae58c71648d59306520d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50be08804a77bde16f85473e07a4a5e618881bd8116acbe4ca3ae192f8da78`  
		Last Modified: Tue, 10 Jun 2025 23:33:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016d292762972acdf5585c0086d7f88fd8ae3b95be75595e4f35aeed96a75d2e`  
		Last Modified: Wed, 11 Jun 2025 02:29:23 GMT  
		Size: 91.7 MB (91654679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb32eedbde8ac6e19ab38348e439c2e7846ec13f6c384e6ae46dc617c8aea0d`  
		Last Modified: Tue, 10 Jun 2025 23:33:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49ef344edafc26600a7f3fee9ce7f2583608865894458feb2518c11b58c91ea`  
		Last Modified: Tue, 10 Jun 2025 23:33:30 GMT  
		Size: 13.7 MB (13723050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e2ec6764438301bf145a97fc5ebdb409a54a107da8e59b15e8f29610ffeae2`  
		Last Modified: Tue, 10 Jun 2025 23:33:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c93a2e01babdfdf6cdc2902d892bbfa673f0928d5443e3abf4d23c79a45fdf`  
		Last Modified: Tue, 10 Jun 2025 23:33:35 GMT  
		Size: 39.7 MB (39674146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7e3d92d2361805790016a62ca910e6537ce6b8ac28542f0878dfaea338be79`  
		Last Modified: Tue, 10 Jun 2025 23:33:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d500e9101984fcd0f00760227aedff9d0420cc01c72587fcb3485efe896ca8c`  
		Last Modified: Tue, 10 Jun 2025 23:33:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:35fe6695ecbeec18552c0eb932ac963f4cf464e3e53846c18854d8a713a9afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6592886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b4ce7873a30ea335f50a4fd6301b6d9d08090cdb9431cda48fe93fddf7c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2a921fdc252d1159c6e554ad490c5973e141bfb19366358087953c43e6990619`  
		Last Modified: Wed, 11 Jun 2025 01:58:01 GMT  
		Size: 6.6 MB (6553306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962422a721f06be689607f9edddb3a35c682209144cf38bc890a8c3f6d7e26d2`  
		Last Modified: Wed, 11 Jun 2025 01:58:02 GMT  
		Size: 39.6 KB (39580 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:d6edb6f202df353bdbe052ac381adb2d8ae7227915909662049ccedacfa81d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144542661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb00ced4acddf5e71e4212ba78cdb4b1d99c451713117588559e60b04041cc0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad6673cebc90ab6de18533ba0930b8c2a04aedaf3fc38e7ad478a5a3bf65fe`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0f6a80aba762784bd149c214bb34433118513f1aaf602bd59a2955c01fc68`  
		Last Modified: Wed, 11 Jun 2025 00:14:18 GMT  
		Size: 69.3 MB (69326502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a6949a51563c9f0a673e97cc2e3ac553e26bf7c6d1701cdc61ffbc4f14be0`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfc43035a18e657e9d70e52c7906dd84a8b862c1192967b08c82fee3e480529`  
		Last Modified: Wed, 11 Jun 2025 00:14:15 GMT  
		Size: 13.7 MB (13721667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22656ef6e28a599eae60f5f99cb8544f9e77b5ba69ca8c641f7602941367286f`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d9cfc6d97c1d04e07ffab2a1586f69a70922d1626593837bfd44f82515552a`  
		Last Modified: Wed, 11 Jun 2025 14:26:16 GMT  
		Size: 35.9 MB (35946668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42205da5534ede93dee015e2e8e6eea8879c8ab4841dd528f6964c26cc2ce11`  
		Last Modified: Wed, 11 Jun 2025 14:26:05 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda93d8c23381a0f8fa49b768f39b5fbe1fa974ed1701b1016f28ed2d54b0271`  
		Last Modified: Wed, 11 Jun 2025 14:26:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:628c452891533b07189c8743ff74dd8802f75c49c5aaf37ace5727bf230a4909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590af991375e5155ff6b4898a30965f76054a835572eae313bfa52dca6db243`

```dockerfile
```

-	Layers:
	-	`sha256:6b951bec01f4fed2d6bf9ee5403a9b263a3d3a1280cfcaf51daff95d8352ec4e`  
		Last Modified: Wed, 11 Jun 2025 01:58:08 GMT  
		Size: 6.4 MB (6360964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b350bccc62ab12c73d37147ddcb5ab80ae437d8516f1ac39a87546b95c7484a`  
		Last Modified: Wed, 11 Jun 2025 01:58:09 GMT  
		Size: 39.7 KB (39721 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:efe06198f037e099f1c9f1256fa3cdbe46a99424c2f798da991b3369ae5c4e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168734642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b2050d6911ff0f5975ab2975f18b23eb8a9136fa0fd2aafc05a0454c1429e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65977ff69501a7dc5f6e26302db9f945a47530721a001a3ae4baa1384ea7848f`  
		Last Modified: Wed, 11 Jun 2025 00:44:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82a527151d12965d37878cfa80a9f76151d3f1ea0f4df493f325df37cff3f11`  
		Last Modified: Wed, 11 Jun 2025 00:44:16 GMT  
		Size: 86.9 MB (86941837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363d60d40db13be926f62e34f82e495ebb264495e58500092c9d7d6f3c24cdea`  
		Last Modified: Wed, 11 Jun 2025 00:44:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab52589597c92d8d219267fb2fe4677da80b82f173666b7800ac0152da571a1f`  
		Last Modified: Wed, 11 Jun 2025 00:44:13 GMT  
		Size: 13.7 MB (13722361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed99024308a548802629dac9ce416a99e82cc5e08ba8919a3903f51b4ca706`  
		Last Modified: Wed, 11 Jun 2025 00:44:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bad5c555685e2b9b1472953fdfdf89478160306c4ccbde9e7a81b60546e1b`  
		Last Modified: Wed, 11 Jun 2025 00:49:57 GMT  
		Size: 39.3 MB (39322633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321ce64d6eb49d63851313531ccb648605a7c5364ecacf9dc761cba175f50bf2`  
		Last Modified: Wed, 11 Jun 2025 00:49:54 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb65dadf71d097c938f0434c374419a2c0b6e46d51152adea139603240c1265`  
		Last Modified: Wed, 11 Jun 2025 00:49:53 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:a21e40bfb5caf670bcc344d9c8313d4ef599a223b1d687add53de84ccffe67df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6595544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d334df7c8ec01eeca444378846ff8940b6f75d3645fccc534dca8b61fc17948`

```dockerfile
```

-	Layers:
	-	`sha256:ad2ab203c4b6d4c0d9603e7697f21f270ba1712b85e8a81521d9ff6831fc81bb`  
		Last Modified: Wed, 11 Jun 2025 01:58:15 GMT  
		Size: 6.6 MB (6555786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580a1757c995721587adfed23eefbc7c3d4eab06c3d8b993e0e24fc94343ec07`  
		Last Modified: Wed, 11 Jun 2025 01:58:17 GMT  
		Size: 39.8 KB (39758 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-bullseye` - linux; 386

```console
$ docker pull php@sha256:c38c0368f4caedf48d7dac10952be40161e9dc1a0fa12cb0ca02bb6bdc9d2ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178059449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3a948a94a43b3322b9331b6fd867ddce96cfec028ab34b741b324ff0f242a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6396a1fb1b59dbe00fe600f6cf479686531965dd2ab6be9131eb8888be68aa`  
		Last Modified: Tue, 10 Jun 2025 23:33:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423165508495b7079f8b2009fda791a18a66a6a03a94afefabca0323ebbad3fd`  
		Last Modified: Tue, 10 Jun 2025 23:33:48 GMT  
		Size: 92.7 MB (92725565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02b9a7e568e07f29ad14a8273e932099e3a369d08ff9930d929b1dff4caff6e`  
		Last Modified: Tue, 10 Jun 2025 23:33:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b008d7929e94d1e81630d792b423f9a40a0424f7d4ac041b347fbe9310cf1`  
		Last Modified: Tue, 10 Jun 2025 23:33:41 GMT  
		Size: 13.7 MB (13722369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70f245f33d8d6922a68be014dae2209213dfbe48e1036d1447452a6fd380411`  
		Last Modified: Tue, 10 Jun 2025 23:33:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c359428e6d104898faa4fe4d6c702c05981381aa0450d1e3c9b5daf07338cd1`  
		Last Modified: Tue, 10 Jun 2025 23:33:43 GMT  
		Size: 40.4 MB (40418199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d121066c4068ffe92fb4431d63deefb40a45449c49f9f37b377f99123d65c3f`  
		Last Modified: Tue, 10 Jun 2025 23:33:39 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa70bc3c8d2ef582581fb6fccf8cd8511f87e415118e246de697766a691f40`  
		Last Modified: Tue, 10 Jun 2025 23:33:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:ae239fc7b283efbfdb3ea8f9bcf0e2512fc2d58a4cad7185e532e52c05eaa341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8d4b283a84480bfc05032f142426395154cdc1a585caeb0447f12eb8d2a1ba`

```dockerfile
```

-	Layers:
	-	`sha256:b65aa7329373fffbe320df2f208411d8adba2ee95e09a02337192f55a43ec2a9`  
		Last Modified: Wed, 11 Jun 2025 01:58:29 GMT  
		Size: 6.5 MB (6543483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86271680368d09242cdd2f70a3d58acab933a2e1d72b8af3e72b882c104523ba`  
		Last Modified: Wed, 11 Jun 2025 01:58:30 GMT  
		Size: 39.5 KB (39538 bytes)  
		MIME: application/vnd.in-toto+json
