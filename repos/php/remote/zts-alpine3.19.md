## `php:zts-alpine3.19`

```console
$ docker pull php@sha256:3caea233dbca270d7ecf3ddfa2bfc33682cd51c146ece190d365e449c8740aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `php:zts-alpine3.19` - linux; amd64

```console
$ docker pull php@sha256:7ee0e97743ba4e0b1ba194d73b16a7e261d5b52978c9be9b83ad2a4653cee303
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40692198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531ac08835cb5bffbdfb1f96d4738d343b97d4e64a9841bf1abda1bdf0eca7e9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:33:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 23 Jul 2024 01:33:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 23 Jul 2024 01:33:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 23 Jul 2024 01:33:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 01:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 01:33:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:33:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:33:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:59:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Aug 2024 20:03:03 GMT
ENV PHP_VERSION=8.3.10
# Thu, 01 Aug 2024 20:03:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 01 Aug 2024 20:03:03 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 01 Aug 2024 20:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 20:03:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 20:15:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 20:15:25 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 01 Aug 2024 20:15:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 20:15:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 20:15:27 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f931e8c4ee1eb9216b05b724540ce862c05cd47764c5430b1adcacafe7a0ca`  
		Last Modified: Tue, 23 Jul 2024 03:55:55 GMT  
		Size: 2.8 MB (2775544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701d11e42f9c63f01acc636a5c0ea3e4f92eda3047d8a1b0a56cd34c4565d1d`  
		Last Modified: Tue, 23 Jul 2024 03:55:54 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980d88e93b06bf737890c4df5068bb324bafc32ad3cbd0f4beced84645e382f2`  
		Last Modified: Tue, 23 Jul 2024 03:55:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd736a8cd150bc89cbccc960c456049645d8f39d5a142f19be09088492a2e1a`  
		Last Modified: Thu, 01 Aug 2024 20:23:44 GMT  
		Size: 12.5 MB (12505900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee14c5015a8fef4efb7c5af9aa4f5478f44196b1d7b806d1b795a2590620e39`  
		Last Modified: Thu, 01 Aug 2024 20:23:43 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbaa1f185ab3baeeb138ef4fc9b631ffbc85356a12b7e291331f66979e8d860`  
		Last Modified: Thu, 01 Aug 2024 20:24:23 GMT  
		Size: 22.0 MB (21967752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bfe5a54daab37b5d339bc90538e4527b5c6af906191d72497221c5462e7a18`  
		Last Modified: Thu, 01 Aug 2024 20:24:18 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86948df59079574256420c8145bbb431f14c71762b08c0556399377e3e9c295c`  
		Last Modified: Thu, 01 Aug 2024 20:24:18 GMT  
		Size: 19.6 KB (19560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; arm variant v6

```console
$ docker pull php@sha256:7d9e6af9f57b95dd60d16f284146d7c1a76c3bdafdb1a95a9abe5083300224a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38803462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d0b5c39b2d8eac8408a244115118ed442b097ed80a8d481facfa906577324e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:30:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:30:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:30:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:30:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:30:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:30:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:30:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:58:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:32:46 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:32:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:32:46 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:32:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:32:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:47:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:47:40 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:47:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:47:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:47:42 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cb1c01a3be753b130a8515ecd22aeffd2044f864c72c49d3d593157325e63c`  
		Last Modified: Tue, 23 Jul 2024 01:01:33 GMT  
		Size: 2.8 MB (2782256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ba3d39613af4d13b2c6eb33838374d2dc75e759de970cdb5ab22d15612ade1`  
		Last Modified: Tue, 23 Jul 2024 01:01:32 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ec1c27f23189ba6cf2238e46bd647cf82dffbb67ac7f521215eb6b50bf1b2`  
		Last Modified: Tue, 23 Jul 2024 01:01:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedd0be50641c1e4bfe301c85114c60d52c88ec3abc8facd0ed126c23d3142ff`  
		Last Modified: Fri, 30 Aug 2024 20:21:45 GMT  
		Size: 12.5 MB (12502116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4c6ed7eedeec1c2940a9e7f0dff10c2fc7752052ec6fc5f583da44c7fb5982`  
		Last Modified: Fri, 30 Aug 2024 20:21:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab415d3c2db8843d0074cdca792597c26a9252c882778a107f42d003d639b9`  
		Last Modified: Fri, 30 Aug 2024 20:22:30 GMT  
		Size: 20.3 MB (20319625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857b380ae82b565e9119ee40fa8d6fbb65e757956334926f40a333567e5ef2f7`  
		Last Modified: Fri, 30 Aug 2024 20:22:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5ffdcdcdc1c5842fc4acdc814be6f7d7175abe85dd52819a201e2756cf2365`  
		Last Modified: Fri, 30 Aug 2024 20:22:25 GMT  
		Size: 19.4 KB (19397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; arm variant v7

```console
$ docker pull php@sha256:235463057f88fa8b4903f7f4c31ec60e00d318848c31c717ce9c47aae6e84969
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37057213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2090f33b38993b906e8860ac0b8266032ee5d89b3d48b8dc1243d4d49be50630`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:46:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:46:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:46:53 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:46:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:46:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:46:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:46:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:46:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:14:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Aug 2024 19:51:44 GMT
ENV PHP_VERSION=8.3.10
# Thu, 01 Aug 2024 19:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 01 Aug 2024 19:51:44 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 01 Aug 2024 19:51:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 19:51:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 20:01:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 20:01:17 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 01 Aug 2024 20:01:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 20:01:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 20:01:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863aa9b51e5e1bbb394dd698dad31a25269c0ec73e5772d64f8377b4dd1345a5`  
		Last Modified: Tue, 23 Jul 2024 01:15:11 GMT  
		Size: 2.6 MB (2624619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08abe10421ea530a6bc3d6d4e3605c900736b36d5d0caf2437915e09a6472e51`  
		Last Modified: Tue, 23 Jul 2024 01:15:10 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0547dcde17bbff569bac562ee7e2af6598f418ebafe66e067c5e00d61194af`  
		Last Modified: Tue, 23 Jul 2024 01:15:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad229df3d5455d442f19c502e5e7137b69daa81c5ece0e416a1a2b5abd7ce8`  
		Last Modified: Thu, 01 Aug 2024 20:10:10 GMT  
		Size: 12.5 MB (12505899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4153bdd17839638ceb96b99133f1956e387f689e8e37b14ee18917421e289e9`  
		Last Modified: Thu, 01 Aug 2024 20:10:09 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3fb3958fc8e86c5f22e45d5a59ae4fb7c2daaac32aef9ba42f5c6c26d9c943`  
		Last Modified: Thu, 01 Aug 2024 20:10:49 GMT  
		Size: 19.0 MB (18975820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23381749e1040c095bc7fbf661f8de9f3881f74b6d2f1a104c2750f466a8ac0`  
		Last Modified: Thu, 01 Aug 2024 20:10:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8445c17e5e0139ae563d3673e1780d8f3e4c5f7b88a14f4ab21346cba48aa3cc`  
		Last Modified: Thu, 01 Aug 2024 20:10:46 GMT  
		Size: 19.4 KB (19375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull php@sha256:4860ed3de3f42d7b2eef0858738ff2471ad8b3fb246101dd23b9460b13221e77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40677229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d7703d71f2208273b64fc5034b16d91b1517df39bde618218b25abc588b08f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:40:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:40:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:40:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:40:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:40:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:40:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:40:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 00:03:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:10:17 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:10:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:10:17 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:10:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:10:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:23:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:23:39 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:23:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:23:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:23:40 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dd3cc0ccd192274dc1aa57ac755f47e23c2e9e929deeefb246ca1746a35944`  
		Last Modified: Tue, 23 Jul 2024 02:00:58 GMT  
		Size: 2.8 MB (2829082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64617542de43cbcdce9ef95a59e32048fe17476c22909e27f96fa97688a1a3a2`  
		Last Modified: Tue, 23 Jul 2024 02:00:57 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be00e8bbf9559953d90501bab240bffb094dc37b211d543751c5d35365e4ad5b`  
		Last Modified: Tue, 23 Jul 2024 02:00:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfc8f11a2543ea003efe3123b111031436495380727660e8cef6b37b2beb3e`  
		Last Modified: Fri, 30 Aug 2024 21:24:47 GMT  
		Size: 12.5 MB (12502112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073c0d0d699783744a6f4edaf53861ebeca31debcf42ed2e5eba8025a8e1b732`  
		Last Modified: Fri, 30 Aug 2024 21:24:46 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efb88c085e1970c7fad14b5a9bf96ec5890e7c06018db2628990154f418ca8b`  
		Last Modified: Fri, 30 Aug 2024 21:25:24 GMT  
		Size: 22.0 MB (21963784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56889c210f089324c09a3feedb58d5099231048d44d2ec2719fdb5f514a37d07`  
		Last Modified: Fri, 30 Aug 2024 21:25:21 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b855ab740c906913a04d370cc88df048c56b8d6ec04ef5e09232b45284164e0b`  
		Last Modified: Fri, 30 Aug 2024 21:25:21 GMT  
		Size: 19.4 KB (19391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; 386

```console
$ docker pull php@sha256:824fc2be12992692b9cf2f50b56936472fafe400cfea9046c41ac852ab915188
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41104227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05567bdcd0f229724be2f32d62c3b85bf285dcb7aabc9f63c663217ecb30af6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:20:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:20:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:20:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:20:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:20:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:20:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:20:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:04:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Aug 2024 20:48:48 GMT
ENV PHP_VERSION=8.3.10
# Thu, 01 Aug 2024 20:48:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 01 Aug 2024 20:48:48 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 01 Aug 2024 20:48:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Aug 2024 20:48:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:09:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 21:09:56 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:09:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 21:09:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 21:09:58 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83dfc65354b38d786dbce66dcc54fce8dc00fb50911d5f0b25891bac00d890f`  
		Last Modified: Tue, 23 Jul 2024 02:15:24 GMT  
		Size: 2.8 MB (2839257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569cc315ba4cbde39caf33a3761351d59d8268a4887485cce7f6d1e3a0cc8af1`  
		Last Modified: Tue, 23 Jul 2024 02:15:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b201215f8e0acb32ec7e5e0ea5f3a5935a73bbc1d96de15b4bc81e8fe59575`  
		Last Modified: Tue, 23 Jul 2024 02:15:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15935f9c3ed5235a4e0ab8bcce1d62708b418f8596aefbedb4af37c1d3305a79`  
		Last Modified: Thu, 01 Aug 2024 21:18:58 GMT  
		Size: 12.5 MB (12505904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f61aa0ae33d238eaa907a4cb3077782c85dce032f8814f56dc3852642b80e69`  
		Last Modified: Thu, 01 Aug 2024 21:18:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22408cc0477f2f5b275e19d9fba87647fbeec19270775451365a8ff8c9f9476`  
		Last Modified: Thu, 01 Aug 2024 21:19:42 GMT  
		Size: 22.5 MB (22482494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c3c0445217ba1431e215e48be099d9f568e916b51fd4f761d189f32ecc4e9e`  
		Last Modified: Thu, 01 Aug 2024 21:19:36 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce2e25b2ecda10685e042b83461cb5fb74fd13a29a7a8d16674c6a4194a352`  
		Last Modified: Thu, 01 Aug 2024 21:19:36 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; ppc64le

```console
$ docker pull php@sha256:0f16fe1f0362f7dfa17b8795352142980d4cd107d8387e7d29e86f5475aa32f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41977561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b33d3cc920f8855c4b2e0c14cc88ebdc8a4b95c82108307083d61560b88615`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:04:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:04:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:04:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:04:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:04:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:04:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:04:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:04:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:21:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:40:09 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:40:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:40:10 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:40:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:40:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:48:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:48:16 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:48:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:48:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:48:18 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa64b1043573f6ac2308b6f5430ef4a770c535ff8b83b429848c20e189019d`  
		Last Modified: Mon, 22 Jul 2024 23:41:47 GMT  
		Size: 2.9 MB (2858877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6634139ce07ac06623cd77c5881ede14b5cc55f21f0e5b2f9f32106561fad7a`  
		Last Modified: Mon, 22 Jul 2024 23:41:46 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6300702430dcbaa0ed8609ade6877914d6d103d9e38700e3e0676f68d0880e`  
		Last Modified: Mon, 22 Jul 2024 23:41:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978717127f846ae960d2947b707dadb602650123b91809a471c88b88b3717d0a`  
		Last Modified: Fri, 30 Aug 2024 21:41:08 GMT  
		Size: 12.5 MB (12502108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6136e33f84c943be4b39af2a3ced476833105da3e83c480e595eededccae80a0`  
		Last Modified: Fri, 30 Aug 2024 21:41:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6cbe21e6d17c4bd06fe05ae0a5503f0badf6a07feeff98bb834a741787ff40`  
		Last Modified: Fri, 30 Aug 2024 21:41:51 GMT  
		Size: 23.2 MB (23229690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8916dc8d066c9237f48e0f1c4d3494161b9f00249e223b0336364f57bd1ad44`  
		Last Modified: Fri, 30 Aug 2024 21:41:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4534193f5d8ac39dc55861de49ab456fe7fe4c53772197c3c9ff71e84b9b0b98`  
		Last Modified: Fri, 30 Aug 2024 21:41:46 GMT  
		Size: 19.4 KB (19379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:zts-alpine3.19` - linux; s390x

```console
$ docker pull php@sha256:89cf8f336c887187e691049ceeffff32523719eabc521f1eb8f69f4e731aa58a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41176313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126520a32808c68e2f82db5208e17ea0ec1ecfccc5ee89fbf9a979ed09330518`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:48:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:48:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:48:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:48:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:48:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:48:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:49:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:49:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:20:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:12:02 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:12:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:12:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:12:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:12:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:22:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:22:43 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:22:45 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:22:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:22:45 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cb9575cbbe9a0d8607f6f4f2b435272a0087e5dfdd6172276e2e614f416340`  
		Last Modified: Tue, 23 Jul 2024 00:56:42 GMT  
		Size: 3.0 MB (2956535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179a34f9209629c7317fd1710ecd639575dbbabbaaf43ae39e43b55067b4dd3e`  
		Last Modified: Tue, 23 Jul 2024 00:56:41 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb139f20db22ba99e5dff5af2902f3a733afdc409e5daca9a5ae2efabfb02d00`  
		Last Modified: Tue, 23 Jul 2024 00:56:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853db8ed4d14e0b5d4e7d284d3871924644606002ab26178a06980fea1fd6c80`  
		Last Modified: Fri, 30 Aug 2024 21:11:55 GMT  
		Size: 12.5 MB (12502102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091d3298b44e5ef7ea3a28988ff80a8e131ff7a11a32b7cb4dc6cb94b56de250`  
		Last Modified: Fri, 30 Aug 2024 21:11:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3508e3ae65bf328fd3719b803a960d21f768869f63c242df1740c8b1d70f5c`  
		Last Modified: Fri, 30 Aug 2024 21:12:26 GMT  
		Size: 22.4 MB (22440821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987a0d8444c38002b776761a0af1c43191dc2c8dcd3ce1cce128a398c81097db`  
		Last Modified: Fri, 30 Aug 2024 21:12:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cc28bcb73d626de77fef1931dea8f8a4081ad99925475f663919ba7aab7061`  
		Last Modified: Fri, 30 Aug 2024 21:12:22 GMT  
		Size: 19.4 KB (19378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
