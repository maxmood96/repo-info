## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:f0dbe5be1b8b871c012dfc5317bed5c2d150ad8066c63b5143ac305d32974f01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:18c1875ca8c914ec8786ef4b3367e37312a689f4a98611f6c7197e0e666fb83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49001910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1ddbdcb4dc41ab9da7f9aa985f41cdf4d45085fb27fd415bcc3c866156cf07`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d061d9aaea4bafc30467ca1a694ef85f9eb0c227cbbc91945df04b7cf0b99959`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87d66be1603186eba2db2bb031cce1d94446ab7934f98c4ccbc0d596855b332`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ec2ecb981cff9638816da92d291d9fe4f217710cb129e72191fdbaf02592f3`  
		Last Modified: Thu, 03 Jul 2025 23:12:45 GMT  
		Size: 4.0 MB (4032190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cda22e35caebbaf756879a466d77a3a9e9e80768c05495f6577a97b132aa936`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f25c2fd29d671243a1c81fd21f2f200a90bb430a09307aef2c17f59165ef57`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 562.1 KB (562106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7254a346fffef25162236368c3cbe7778b02e89da776c8e8853a54a7cd2c9417`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:0f027a77a05d9ea1d0120bd3197160edd197a69c4ad0d00772c285dd768b096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9192be1580cd54f24acb3fc0f872c3d2229f22e7ebf8c9be63aa1d035aab637`

```dockerfile
```

-	Layers:
	-	`sha256:96db40b77cab62de2ed275a7c7725a7575484de0de2e78decbff778ac2681af5`  
		Last Modified: Fri, 04 Jul 2025 00:48:28 GMT  
		Size: 35.3 KB (35274 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:ca993f14168e8285fd9613066882aa93ac5f9f60775a1f845abd2844cf093aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47012471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed74ee2c563d8e2d89e67506bbe8640ed070847df581578f0250f82df2ac1b9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5751d447378c9adc039875aab14a233bc8f24e97cc32b47e042660d1d5d4e6a`  
		Last Modified: Fri, 04 Jul 2025 01:04:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c767917c9566d9495961554b95eb0807e2b1885c4c8adf8cb75c42cb6217b4b`  
		Last Modified: Fri, 04 Jul 2025 01:04:28 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd9f1fb2afa19e498dc03501108a2056e41aa9d364b7c80057cc08e6fcbf1c6`  
		Last Modified: Fri, 04 Jul 2025 01:04:28 GMT  
		Size: 3.6 MB (3606080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9fb5ff0f9b2d3e9bcc5df7464ea80af9fb03169c33f7a767f266d147d9fcb0`  
		Last Modified: Fri, 04 Jul 2025 01:05:48 GMT  
		Size: 1.5 KB (1496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe7579ba4663339d5659872cfd83ac4eaa3039174f831184210c0e25e867b48`  
		Last Modified: Fri, 04 Jul 2025 01:05:49 GMT  
		Size: 562.1 KB (562111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d8a37f0abc4e86ec3e2d687d025464f3227ccfacc35926fcb6bc377749290`  
		Last Modified: Fri, 04 Jul 2025 01:05:48 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:a8ad5dcecf656498a157d1a48f2a9e8e49b2c13ad072b6e49a757492ee268954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0417fd619e5dbe80f24ebf237947d777857bb5d4cec9debc3c40c462fa33cb2f`

```dockerfile
```

-	Layers:
	-	`sha256:261d72db5213dbf3389992e8af2e8f8fd37aa21eb55e8917fa26327e6bbe9927`  
		Last Modified: Fri, 04 Jul 2025 03:48:32 GMT  
		Size: 35.4 KB (35389 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:92edcc51602d662bdf81c4faf18ff472059055cbb2955af404ca6a161d81687b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45371527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb306f1ff112e9e7cab428015ac273b8b3c4d426de235272ba6290271c1371d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25659badae5bd6d735e7a8151332a7d70260be40b9bd15903ae5024c69186a`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 21.0 MB (20968354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020d050ffd80f0ec4539c880f71565ba7987609cedfc9dc9ff78af7fb53b62b`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9a523c3a709bd62efada35a0a92295ac64b04640f1069b295c0d6889f2487`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbe376a53d9ebd8229f86a814b0d26ee3ca102f0e74c6dc09a10a9c343c58`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e439b7ce458a67de11129c061cbd99f619be033b7f5714c766dc1f280ebf72ce`  
		Last Modified: Fri, 04 Jul 2025 03:22:45 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb963bd1f35403debcaaa0825b0be9ef5aef4b2a4bcd1c6641260afb9e0f54b`  
		Last Modified: Fri, 04 Jul 2025 03:22:45 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf00f185fa9df030717328a737853a690c072ae53828059dfefc8d6e61ab034`  
		Last Modified: Fri, 04 Jul 2025 03:22:46 GMT  
		Size: 3.7 MB (3679712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7921dd2b62c90421e88fa127ad5ac01ec9bd8f78c96854e9dd687dbfe7b17c4`  
		Last Modified: Fri, 04 Jul 2025 03:24:03 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968b7f8d50856366b3b877946944d0459a3f3cc9d397b4f4c9201f0afb99d7f`  
		Last Modified: Fri, 04 Jul 2025 03:24:04 GMT  
		Size: 562.1 KB (562109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe55d5c1d56fd0f87fdc44bf748e0df1afaf8e3f16fac65c9e87f269b98cc7c7`  
		Last Modified: Fri, 04 Jul 2025 03:24:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:dd0cb88a5d7da8c14baddf6bff4d9efea412179ef327537e14070e3e297abfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877b0ebf76e0ecd8ab30e955f25b768ab2d09ea4d1099ba481ea8c612bffe81`

```dockerfile
```

-	Layers:
	-	`sha256:d4b315c11d4615d1083e22a32405ce4d073ddd2a1b62c1d5c459b3b750985f92`  
		Last Modified: Fri, 04 Jul 2025 06:48:32 GMT  
		Size: 35.4 KB (35389 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:0c331c0b8f2c8836fe426c82d2f4efb9c30d2c0b6be1cc47c9d4fe5afce8140d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49178800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a0aa7e87c970b156388ebb119d3d29692c417ad120820c5ce1fbf6d5e6138a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b220f2eaec9520ea981fe044dbd753069e82acc397dfa855f2a332e39b93468`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 13.6 MB (13647248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d569bf8384ea7859bc5bdebb7b303dc9b3a01a31162528b5298988b410fd2ace`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0737718bfdacae544948cd5c6a3f57a8994e0cb9db8f8013734d71477c2dbe6c`  
		Last Modified: Thu, 03 Jul 2025 23:26:02 GMT  
		Size: 20.5 MB (20524764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61f62f8fdebecf2c781d1e3ae99a78623c4caf681cf8cd3098037e40fb1d2b1`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06846154fb549cf7dbc84fecb75119d29a39fd6156a149adabc34556b1ee5af0`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d688697060ffba410fae97b62fad44f00d39a88080cce54016340c2f6153e91`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f0350c7798fc7d0135cc0120cf34d8ba7991cd8aecefc713326582a478faeb`  
		Last Modified: Fri, 04 Jul 2025 04:02:56 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dcbb834aa1cb840b1248266b684bfd89533213dd0669c3824fb59267c1e39a`  
		Last Modified: Fri, 04 Jul 2025 04:02:56 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636a3ddacb43ca93e7a0910d904f5974ae2dc8b9314d6d59d523aa5881c6e32`  
		Last Modified: Fri, 04 Jul 2025 04:02:57 GMT  
		Size: 4.0 MB (4029393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f9abc46960ed5d30f348c9f465ac74ebdfc7745ee6acdc540991bfaf477eab`  
		Last Modified: Fri, 04 Jul 2025 04:02:55 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeab9001d5f463d5923b1d6fb4aac327996b7c677ec519ded905795204d6423`  
		Last Modified: Fri, 04 Jul 2025 04:02:56 GMT  
		Size: 562.1 KB (562106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ed825ca03e2f45b84ca7eef27f2ab2eba7d84009e15ee6446ec210e7b8289b`  
		Last Modified: Fri, 04 Jul 2025 04:02:57 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:cd1ae1aa95982bdbe1536efa3dc4650a89171027380efca0fe12b51f1e5b3c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d199030448102d7eda19b88f504f213a375556f9f92b905b91fcb3635cd97c1`

```dockerfile
```

-	Layers:
	-	`sha256:8c9307a3ef055f73cef9bc00850a18b241215bc308dbb205c84b2a4e091ca88c`  
		Last Modified: Fri, 04 Jul 2025 06:48:35 GMT  
		Size: 35.4 KB (35421 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:ffd568d417acdaac4722b8ce029d34a86760615180dc62803fe8a461f911b36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49070728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8bd6665eae72f6fbe024b3839ce4266bab74900265ef726b900074975ee3a6`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f523736200c25d5430665e0a6a3f15f5be1be4bacccd4713eb5699e7f53f3edc`  
		Last Modified: Thu, 03 Jul 2025 23:12:17 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e239698c3ac185df84a4111a82b8817d023b83373f2f181dbc325b80c2371038`  
		Last Modified: Thu, 03 Jul 2025 23:12:18 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3e7764a4332c2b3d545fa5dee560ceba5c89337f0143bd75944a204e33826`  
		Last Modified: Thu, 03 Jul 2025 23:12:19 GMT  
		Size: 3.9 MB (3889893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0decaecad9579a77cad9cbdae2b361d34ec800c650a160231b8022d6d1fe6926`  
		Last Modified: Thu, 03 Jul 2025 23:12:19 GMT  
		Size: 1.5 KB (1489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb08f6c6d9a1048f45750c248fccc7109de863f2b7c7af5bda45ae20c485864`  
		Last Modified: Thu, 03 Jul 2025 23:12:20 GMT  
		Size: 562.1 KB (562109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6eb8c6654725daf83c039c513c362a2963d19985734aba3229203c1a967ff0`  
		Last Modified: Thu, 03 Jul 2025 23:12:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:c4eb6876ab01f05aecd223ca26d027d27ca6f61aa0445e2b77eee1741e3cddfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980af2f99964ab733eea953c0be8dd1b6176dd86db031941028229115cebdfa`

```dockerfile
```

-	Layers:
	-	`sha256:7872118daf459c748198ec28aee1322ae0eb08177891d3c1096cd057c6bba56a`  
		Last Modified: Fri, 04 Jul 2025 00:48:40 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:2e0b38e7193ef1cc6616252c22c88b12152265512fc8b71132669d19813db1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49689406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788a5f8249eaf399838caf22eac3cb61e5b98d2551502587684a4e4d4af0e906`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff158c4fec087bdd22d80d469c14bd7f5e8a7d72d9a682db56d77c7977e55f`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 21.9 MB (21877134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09d11c80e8896e162d36345eb3a1cf062f1ba207ed29c537b7783eb818f415`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09daff9fd7af3987bc24f46923dc89bca4e186069874ea11f88390e02dbca5a8`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1d9e25cff60aeed589359ca184c52454f63361a6309e3c363d0d97c227e006`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a718f176c3943cd29f667005ca912344ab3b878881d85decec43f3d07514a8d`  
		Last Modified: Fri, 04 Jul 2025 02:27:02 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518b4d11b5d7ccfe318d67315c62ac8142e36cd7026a275fe62b6d945abdec3`  
		Last Modified: Fri, 04 Jul 2025 02:27:02 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c528ffc8f7e05ce1d820e6d5f6faf77997e6595eb29245f02cfc25cd10a62c8`  
		Last Modified: Fri, 04 Jul 2025 02:27:02 GMT  
		Size: 3.9 MB (3878370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fce98bdb5a7290827341a45e1310af7bd4d0c700dcda01f2247a3474eca03d6`  
		Last Modified: Fri, 04 Jul 2025 02:27:02 GMT  
		Size: 1.5 KB (1487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff1ad27b848d8f66f8dd4eb0a9063f6307893e6268f1ed041b62994bc8198b6`  
		Last Modified: Fri, 04 Jul 2025 02:27:03 GMT  
		Size: 562.1 KB (562107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa87911ea4f57a9b3de92c32506bdb401bb63fad4b8e718146dd007937922b`  
		Last Modified: Fri, 04 Jul 2025 02:27:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:51b2615417f718d6d6f0aafa89024f47fd3371a0dd9be998a35fb4fe59037650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cf0acff9d406e155d7398aadf64b3218141fbeccfe6c1a1e790f9fea69e84e`

```dockerfile
```

-	Layers:
	-	`sha256:c3c0c450a52cf94d740e1f90acb3faf6a7dc3ac2c6ba2f9321c1ad50da50d5e8`  
		Last Modified: Fri, 04 Jul 2025 03:48:41 GMT  
		Size: 35.3 KB (35323 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:8a3ad9b668c47d94ebb83e91e6b40af18554f437d61aa4aed66280f77d635200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45561587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a750a7f5822dcb6338adc5e862b99e6913aa9b752bdf488db2bacfc1d9bc6d2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.8
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e959febbfec9aa43f7f777a07a152dfcd8f4afff0d6dcb0c51e51a92508179`  
		Last Modified: Thu, 26 Jun 2025 08:19:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a3770896e8ba6672822a80958e89d8b9ccaec438fb5a6439fd31eb09b9b90`  
		Last Modified: Thu, 26 Jun 2025 08:19:19 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9c24d1317c1297c77899291934ed9860c7e7d468ff9e3df29cf35e4495f3f`  
		Last Modified: Thu, 26 Jun 2025 08:19:21 GMT  
		Size: 3.8 MB (3805746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197eb6da684dfc7b5e36fff43f195024af3753d19c4716559b358c8c99ef5ce`  
		Last Modified: Thu, 26 Jun 2025 08:26:30 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0089be19d0f5aae390aba63929470ce0de62b1cff0cef7fb7a2c2f4081b856c`  
		Last Modified: Thu, 26 Jun 2025 08:26:31 GMT  
		Size: 562.1 KB (562106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143bf017a19f11c4937f3469ddc5ccd988429bc2ce6a845ff1ac55fe9273dd26`  
		Last Modified: Thu, 26 Jun 2025 08:26:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:e5484d3e609b0dfc951a30c8a81ccbadcdd118cd4d629e2771a523216d2aaadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa32172e729c9a4b88a851edc7876f41107035a54b07bc2e9758e2e9bb91529`

```dockerfile
```

-	Layers:
	-	`sha256:81faa1c0bf06c80a26fcf7f21e4aeb9c95e5ce614f8cb01739e8fa2815451d10`  
		Last Modified: Thu, 26 Jun 2025 09:48:33 GMT  
		Size: 35.3 KB (35311 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:5bd0ead639ff9fbcc5af3dadd7138655dc0dee649bdd01d2ffc82a85faf38623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c723d2f472eee991ccec3fe454eb3c9fc619978d12ca693bdc8d971ba21e878b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 25 Feb 2025 18:11:45 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Feb 2025 18:11:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Feb 2025 18:11:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_VERSION=8.4.10
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-a"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY *.php /var/www/html/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_VERSION=4.17.1
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=58956bc021b6b260b1a2ef32d03517f6f88f5ad4aa03ff2d0092c6f509e26d0a
# Tue, 25 Feb 2025 18:11:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=6e006c514a3f189dd14ee10fa98977141a00fe79beb2a515966c98f0914cbdd0
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
USER adminer
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc301a9ae8a743478269ed0a476a3abb5ea1e3f156da87ce855397d9ddef91`  
		Last Modified: Thu, 03 Jul 2025 23:16:26 GMT  
		Size: 21.5 MB (21450357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1074498264e134b44d0edcde237cf3cfadba39197115581cfd4b9a9c5ba0fa`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658861fe310f53081a1e605b2427a938ceddc66bacb97178d77404b333d65a1`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bedc3ea3fb0ab6591d908f480b2bb3c119411d1ba9dc0c0e9fd62b45f2a39`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a9278606ab2df8d7f0f9d8525d59b2ab35b5e52ce30b944bdab76008e10d6d`  
		Last Modified: Fri, 04 Jul 2025 02:04:16 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608ec22493d428bdfb1c428400dc5c7fe9e6db66b8fb9386860fcb15b14d54c`  
		Last Modified: Fri, 04 Jul 2025 02:04:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d52ec41008ed6478a53741785a70054e29ddf23eaaf4a73d9f1958bbcb491`  
		Last Modified: Fri, 04 Jul 2025 02:04:17 GMT  
		Size: 3.8 MB (3750597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c7279283a75ddb2193c88588cf5faf40babb6380f4d904a2377f03d4640c67`  
		Last Modified: Fri, 04 Jul 2025 02:04:16 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0fc8efd23eb95dbc4423ea7ec6d9bdf914256fa5ba02d3f38d5fc49f00bbc`  
		Last Modified: Fri, 04 Jul 2025 02:04:17 GMT  
		Size: 562.1 KB (562106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad846af3bb7461515d15203531feeeecc79fa1af095196f25b62b852064423f`  
		Last Modified: Fri, 04 Jul 2025 02:04:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:0652b3f512044918f195fad242c976a8912ada9d6c5ef4b0afdef87ce0b38701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edd266cb7d16cf8fc403f63423c32bb453abb154b06cfcf0b03d4cc2b20055f`

```dockerfile
```

-	Layers:
	-	`sha256:314063db29f55cb7d84edee7721c89eb5544880da5841325a503c2426f3d2243`  
		Last Modified: Fri, 04 Jul 2025 03:48:47 GMT  
		Size: 35.3 KB (35272 bytes)  
		MIME: application/vnd.in-toto+json
