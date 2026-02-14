## `adminer:5-standalone`

```console
$ docker pull adminer@sha256:2fb88b98da9f0ae0157d8fcb73f447a0747b09ee8d2ff8a8e0695b30afed2116
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

### `adminer:5-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:3e62b9e63dd55a7606694bd4625064c185d240e7f12ad8052e0027905cfe7f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46394580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4a82d939229e3dc71e1b24c8ebe0513ca18bbafa8a26d2d9adf565b6c77f1a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:32:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:32:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:32:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:32:20 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:36:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:36:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:39:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:39:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:39:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:39:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:39:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:39:19 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 19:13:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 19:13:12 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 19:13:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 19:13:12 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:13:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 19:13:38 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 19:13:38 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 19:13:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 19:13:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 19:13:39 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 19:13:39 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:13:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:13:39 GMT
USER adminer
# Fri, 13 Feb 2026 19:13:39 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 19:13:39 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08381aed3df3cc18dc2a1286530620d30922ef5b78c6f7e07f42c726cec050`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 3.6 MB (3591773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd132acfd6293c426673796aed4f02499778b0d9be7002e80614d7ecefa80b2`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac96957003c84deb1b639dd662bd0d111f010ae2d93a22a821577446322768ce`  
		Last Modified: Fri, 13 Feb 2026 18:35:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3555d8c03475f74b7cc2e1e42380124d18be674af3c6982d353656d62c567241`  
		Last Modified: Fri, 13 Feb 2026 18:39:26 GMT  
		Size: 13.7 MB (13699086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ae452070662fbb83c093708f541e5d8047f51deea2ec856551c562adbd0598`  
		Last Modified: Fri, 13 Feb 2026 18:39:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882a8fe5d66eaccb2b431026ebfc1e8fbc1595d7ea70ceb112d3530521ac9855`  
		Last Modified: Fri, 13 Feb 2026 18:39:27 GMT  
		Size: 20.2 MB (20169941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f1c4167070de57a8acc8efaa2f422e5ec0882f34cb37aa1cf9074eeecdad33`  
		Last Modified: Fri, 13 Feb 2026 18:39:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63500e9c2ba5eb4b51e4171c916ec4db83341e6344611bd76b882fab8bc5153`  
		Last Modified: Fri, 13 Feb 2026 18:39:27 GMT  
		Size: 23.5 KB (23491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad55e25f352aa12fcb6044cbe9f97541f6a3557478e92c817443fac3b360b0b6`  
		Last Modified: Fri, 13 Feb 2026 18:39:27 GMT  
		Size: 23.5 KB (23510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2c557e733208b4e2d4055c6a284baeb83f9ee0d4c6ff4d34344a5db116c1ea`  
		Last Modified: Fri, 13 Feb 2026 19:13:44 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0737844d94e6b3ad7130711d04b8d37f3f5ee52c41014aceefc5a2ee4b8170f`  
		Last Modified: Fri, 13 Feb 2026 19:13:44 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af02ea1415d1660d7aa61478112650e8b0912ed0ca62bb21f9150e20b2460e9`  
		Last Modified: Fri, 13 Feb 2026 19:13:44 GMT  
		Size: 4.4 MB (4371849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f621b71a136bb1d7178fb90e9ced78bfefa29d0de65e710ad0da05155ee85240`  
		Last Modified: Fri, 13 Feb 2026 19:13:44 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56aa987fc06125f6f33c818cb119e6b003e3f1aa2416499f43a832df4a44b47`  
		Last Modified: Fri, 13 Feb 2026 19:13:45 GMT  
		Size: 645.4 KB (645391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258ccff483a99e2525559dc0b1d3012638c9cce12db6a502ed77e69a4d65e5f4`  
		Last Modified: Fri, 13 Feb 2026 19:13:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:fc31cdb9495011bcc7d1614c90648d5f3df39821e6727b999092c923f6f44db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e725b520f656c1b60c6ad44bed78acd77931972c6c3ead7134e037b5633d8`

```dockerfile
```

-	Layers:
	-	`sha256:be0b27a2d1bec49083a85d1e2771ffcfc88de16be955901761014851d895c6e6`  
		Last Modified: Fri, 13 Feb 2026 19:13:43 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:bd51ad8a464e0c6ab7138ea370a2460c515bdacef79ecba18ab0e7c73f6b721f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43742136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af1de423d1a03e18172220cd63bd9a67ccec9a00501a9387d9b8a1cf158be91`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:40:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:40:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:40:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:40:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:40:56 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:41:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:41:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:43:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:43:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:44:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:44:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:44:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:44:01 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 19:14:28 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 19:14:28 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 19:14:28 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 19:14:28 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:15:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 19:15:04 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 19:15:04 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 19:15:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 19:15:04 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 19:15:05 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 19:15:05 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:15:05 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:15:05 GMT
USER adminer
# Fri, 13 Feb 2026 19:15:05 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 19:15:05 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c58a12b2cb647afc5b44b4b595dde5c3fbefccb74693eaa5fa334d8f4c301ca`  
		Last Modified: Fri, 13 Feb 2026 18:44:07 GMT  
		Size: 3.5 MB (3548695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d44df6a1d1d0d82eedebd87729b21de92b34085ab92309ad7b949b6a4a4e45c`  
		Last Modified: Fri, 13 Feb 2026 18:44:06 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9664528f15b75d6e87519ae21498542128514abd1714a535bf8f91ba799e341`  
		Last Modified: Fri, 13 Feb 2026 18:44:07 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290aff4c5282ae28b73112bd1ea5d0ea90037564c1033529c80c011d6a509864`  
		Last Modified: Fri, 13 Feb 2026 18:44:07 GMT  
		Size: 13.7 MB (13699096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab34ca90882a40dc4a72198089f0cfa5e54583719e61a625360db9e059a463d9`  
		Last Modified: Fri, 13 Feb 2026 18:44:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952d4df375612fd25110915a5fe047de2934bc763addfb4231d09155aa666870`  
		Last Modified: Fri, 13 Feb 2026 18:44:08 GMT  
		Size: 18.3 MB (18254349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831bd048fee19a7d9c9415f8b5d71cb7e34e1a5a9c384edc828f0645b5d03df`  
		Last Modified: Fri, 13 Feb 2026 18:44:08 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b560e715b1f21026a23ecb0e4d3a7cdaa6aa3d732202d09d87cff3286104ddac`  
		Last Modified: Fri, 13 Feb 2026 18:44:08 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222d0fe1b5e65878c39b8e9ca9021dff16f63cdef888668763f4a6e0ad7dd326`  
		Last Modified: Fri, 13 Feb 2026 18:44:09 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4c884a1c8acf625c115211ea4cdd342ac3f9bf54bc4ef5be5698e1b5c7413`  
		Last Modified: Fri, 13 Feb 2026 19:15:09 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97e0a28cc661ab383f8aefc95c0c678d9baae20160ab159c30dc99e4b46c616`  
		Last Modified: Fri, 13 Feb 2026 19:15:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dcd3a51e2e5f01d98a8a8fd7b3ac1440b691a9f1f36e66886777c8b6821f3d`  
		Last Modified: Fri, 13 Feb 2026 19:15:09 GMT  
		Size: 4.0 MB (3970402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e8d95e83def131dd5a4601d16d901e19072020c4bc83a5b569092e306c086`  
		Last Modified: Fri, 13 Feb 2026 19:15:09 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d686f5b1a35d43d5a9d0c1de3ef7259800c8bd6be85c11371287bccfcc8c36`  
		Last Modified: Fri, 13 Feb 2026 19:15:10 GMT  
		Size: 645.4 KB (645390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e7ece3120ad95f35b877763f405a21177be20a6bda3096c1064e46ef605634`  
		Last Modified: Fri, 13 Feb 2026 19:15:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:c33d3c6cbb4a372263227e850f602ba37039a8c5f31cbcd7d432f8b27ee3ebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ce390fc5cdcb7c3e9b9b0a4497c9308fdb6806ad30a948665570888b95d3f`

```dockerfile
```

-	Layers:
	-	`sha256:b9daec06fb8a70450cb761127c1c81d6748a9cf9ff337eb1ed84c70d0913cdc2`  
		Last Modified: Fri, 13 Feb 2026 19:15:09 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c96df83e6e1511f410499229d6830da3aecd285bab7e7cdddd5507ac706c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42281105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0259bef25e858b0e08958226340c74667ffa9cc6aef99584ad278274c4a2a3f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:31:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:31:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:31:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:31:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:31:52 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:35:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:35:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:38:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:38:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:38:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:38:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:38:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:38:46 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 19:16:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 19:16:27 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 19:16:27 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 19:16:27 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:17:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 19:17:01 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 19:17:01 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 19:17:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 19:17:01 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 19:17:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 19:17:02 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:17:02 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:17:02 GMT
USER adminer
# Fri, 13 Feb 2026 19:17:02 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 19:17:02 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f66b0889155ee9f7c1007e7b933de8fa68b92120ec9466bdc1e60689219e4b`  
		Last Modified: Fri, 13 Feb 2026 18:35:25 GMT  
		Size: 3.3 MB (3347488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fc1266ecc1e00b2c22b4d10beca6cf8bd8ca24a99df25ece41ba665ff85de7`  
		Last Modified: Fri, 13 Feb 2026 18:35:24 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d82ecfd8077908841a4fed66afe931640201bfd67870d7683d7ecf48edecd`  
		Last Modified: Fri, 13 Feb 2026 18:35:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09f5e952cf8128fc1ca500318486df95b294d28bb57ac8966a79eaf77c058ae`  
		Last Modified: Fri, 13 Feb 2026 18:38:53 GMT  
		Size: 13.7 MB (13699102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8daedffedad9d9fad23dbe1a33dbb03373428a561f04439fe8664ebe6c32f29`  
		Last Modified: Fri, 13 Feb 2026 18:38:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc18e76f3ecc9f5ef572a0b085ac4398163f8e0dcbd8e7542f2957519fb4219`  
		Last Modified: Fri, 13 Feb 2026 18:38:53 GMT  
		Size: 17.2 MB (17211405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928f3dc9ca908f7b7863b02d85cfde3d07dcf27c9af7e8697b90b145f98b48a7`  
		Last Modified: Fri, 13 Feb 2026 18:38:52 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d0edcace183b7c53e645aabf8a35662d99be9fdaebe531ba025c3486ea72b6`  
		Last Modified: Fri, 13 Feb 2026 18:38:53 GMT  
		Size: 23.3 KB (23326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42d9e9447f8a6a2380aff12aa21bc744365373fdf57f8050782b8f117303deb`  
		Last Modified: Fri, 13 Feb 2026 18:38:53 GMT  
		Size: 23.3 KB (23346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fed9338d8fcb3eb3d0893907ef528948dfb134745bd2086929a91d0ac88b2`  
		Last Modified: Fri, 13 Feb 2026 19:17:06 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3aa115b087facf0936ad6b034b73be3fe82963a51b3dcf218abc768ecd244c`  
		Last Modified: Fri, 13 Feb 2026 19:17:06 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128306de9291c443db7fe5c1e56e9f80b474561fd540209123e0c33cdb0d3fdc`  
		Last Modified: Fri, 13 Feb 2026 19:17:06 GMT  
		Size: 4.0 MB (4041615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef42ad4e2e8dfcc28af93c3d5d8f4884abec9b165d62aeb78eb436824feab9`  
		Last Modified: Fri, 13 Feb 2026 19:17:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c54fd8e365767d43cfbb9921372bfbccc46778c9f8d9d9713881652910f4d06`  
		Last Modified: Fri, 13 Feb 2026 19:17:07 GMT  
		Size: 645.4 KB (645388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7778d6d2cca626d9d352cf89767cc489772e89087eef4425bb636d1c439ae7`  
		Last Modified: Fri, 13 Feb 2026 19:17:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:9d1a6421c2e296d0ae8637f1d8b6f27ff357bee20230b8a2ea5557452034f102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdf3a288d70e378028ec000169c27973c11b851ae3dd531b803ad8c4a6c6083`

```dockerfile
```

-	Layers:
	-	`sha256:319add3d4d10273c82fafc24f957889dd7bebffbd551c1498327d68f4b47975f`  
		Last Modified: Fri, 13 Feb 2026 19:17:06 GMT  
		Size: 36.0 KB (35968 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d5a7e7957e922d887dac080d85d18856785b37561362186e2c7de06a555e4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c55fe2108ad00bf25c95e14c825358eb2b637fb374a063f9d48942d72e46f2e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:40:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:40:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:40:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:40:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:40:15 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:40:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:40:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:43:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:43:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:43:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:43:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:43:34 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 19:12:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 19:12:47 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 19:12:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 19:12:47 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:13:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 19:13:21 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 19:13:21 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 19:13:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 19:13:21 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 19:13:23 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 19:13:23 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:13:23 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:13:23 GMT
USER adminer
# Fri, 13 Feb 2026 19:13:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 19:13:23 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd16b72b3342f999c344567c91d9cbabe7e925ad666bdade3045590d0e4bb2`  
		Last Modified: Fri, 13 Feb 2026 18:43:41 GMT  
		Size: 3.6 MB (3602046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6b66cf116c62c8ba0d77c98c6f5bddda08e03eac3afaf9d262a27f7ac9ab79`  
		Last Modified: Fri, 13 Feb 2026 18:43:41 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b08794e63d8f1f627669c7e425f56f68f6dba34cff9572d67f02250171a547`  
		Last Modified: Fri, 13 Feb 2026 18:43:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e09f60150aa96b9ba8d97afe1681b701ef2fc5a7da3ece5c84c9a206e3e7a48`  
		Last Modified: Fri, 13 Feb 2026 18:43:41 GMT  
		Size: 13.7 MB (13699087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331385797a78f4b79b46918a3072134c576e01c175d7dac35b223d94fd00129e`  
		Last Modified: Fri, 13 Feb 2026 18:43:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df406beccb90af3f0f660845120489cb09bb340bc8ad425305029bf45821f3`  
		Last Modified: Fri, 13 Feb 2026 18:43:43 GMT  
		Size: 19.5 MB (19535018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545450af985fa94940dcf04e7d7b40a227b421f61507de27cca50450c8786e51`  
		Last Modified: Fri, 13 Feb 2026 18:43:42 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6e52219e6fd73f3d14b580a25273d648be96b6655efc50958ecfc665a93121`  
		Last Modified: Fri, 13 Feb 2026 18:43:42 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de92bdc6c687b37035a8c589e3e1201b65d5e506e4beca7b3a713c42ddb67b`  
		Last Modified: Fri, 13 Feb 2026 18:43:43 GMT  
		Size: 23.4 KB (23362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1089b38f3d356b0c0d9079964adc4a38947e22ac1bb23e0b9b4b5ea18f89f2b8`  
		Last Modified: Fri, 13 Feb 2026 19:13:27 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644175751d8fd3190541e9d1874cf0856f23340e1eb47c6388d6cd946da668b5`  
		Last Modified: Fri, 13 Feb 2026 19:13:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad6137a8dfbc922afaf7f23f3af24fde346eddfd53be93d7db89d99ee84a40`  
		Last Modified: Fri, 13 Feb 2026 19:13:27 GMT  
		Size: 4.4 MB (4364939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bc83ed0008adbbb44b783b04b839796419b0bc71ca4f8df12bea7e04a9cdcd`  
		Last Modified: Fri, 13 Feb 2026 19:13:27 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730af08470afdbd9e19d826fa90dc5e2be30a569a03dd2424ccd166d3d63814`  
		Last Modified: Fri, 13 Feb 2026 19:13:28 GMT  
		Size: 645.4 KB (645390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847383f593f66eb1d4410960548449c024c2fa05b03c90971c3f5c8ea15c8fb5`  
		Last Modified: Fri, 13 Feb 2026 19:13:28 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:635a2f79debe100047b11bb8556f0253634705bb1fff4ef7effc0bb7ffacab83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90fa58127f6478c6eadb8b4aa807e0f5618cf190d37e68c5f65a60aaa7aa956`

```dockerfile
```

-	Layers:
	-	`sha256:95654e7c5693a92e86308fd69e6d43aab1255ecc374ae3bc94ef3c3b8d92a59b`  
		Last Modified: Fri, 13 Feb 2026 19:13:27 GMT  
		Size: 36.0 KB (36007 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; 386

```console
$ docker pull adminer@sha256:0e6fa8fc0ea07de242af6ea9aa7e95cc3c7f45c4d7299d3de304972315b096d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46486446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8732e4d6cc10ba86e33802ec2ce192cf95daac193db3cb23ffca62c87d136e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Feb 2026 18:39:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Feb 2026 18:39:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:39:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:39:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:39:58 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:40:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 18:40:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:43:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:43:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:43:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:43:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:43:20 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 19:13:22 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 19:13:22 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 19:13:22 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 19:13:22 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:13:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 19:13:53 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 19:13:53 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 19:13:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 19:13:53 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 19:13:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 19:13:54 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:13:54 GMT
USER adminer
# Fri, 13 Feb 2026 19:13:54 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 19:13:54 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50edd4cf08fcd328168079bbf66b7b5b1e95520638744c0751d61fe90bf9979`  
		Last Modified: Fri, 13 Feb 2026 18:43:27 GMT  
		Size: 3.6 MB (3629406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f0701164a44b3d2ece5a0d0c0c227e2c71da9c447c1e12c13d6cf9f306fb42`  
		Last Modified: Fri, 13 Feb 2026 18:43:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588ec4e3967780a6235e12640b566e457ca3447dfb600c5e5941b86e0d3058a4`  
		Last Modified: Fri, 13 Feb 2026 18:43:13 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c160c48621224749da266e8d8d83f0bc5755420c91b1ebba2ac51b614848add5`  
		Last Modified: Fri, 13 Feb 2026 18:43:27 GMT  
		Size: 13.7 MB (13699080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36efb24f4d711466a558482b9ee443de5f11652420ff585bf8ec9062eb603a3f`  
		Last Modified: Fri, 13 Feb 2026 18:43:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b91913665a3e4de48afbb0635e2f7af4a8cd6f0fe9721ab887b317d2ba428db`  
		Last Modified: Fri, 13 Feb 2026 18:43:28 GMT  
		Size: 20.6 MB (20569664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9410f082a0281657f7cce594441901d768bfbdd113fdcca8cdfd156dba1e5dde`  
		Last Modified: Fri, 13 Feb 2026 18:43:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64db8cb2d18d212320b54be00c3a65388101e2e84349883f9fe61725daab58a`  
		Last Modified: Fri, 13 Feb 2026 18:43:28 GMT  
		Size: 23.5 KB (23522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49c9f10b14f6c8ef285f59248094c5da6d9c48b75d6b201c32d17f8474d26e1`  
		Last Modified: Fri, 13 Feb 2026 18:43:28 GMT  
		Size: 23.5 KB (23537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120883a2bdd3282fa8081e5eb8400b517225be245f1abdd7a38fd67378a914e0`  
		Last Modified: Fri, 13 Feb 2026 19:13:58 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6fc025aa40896d6ad93e6a6a1452bccdbfd3a574ab3f8b9be790068e364033`  
		Last Modified: Fri, 13 Feb 2026 19:13:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f466ea2c6e0191895e51eced045e006a2fbbea1b22da40ecfd13244a8b8495`  
		Last Modified: Fri, 13 Feb 2026 19:13:59 GMT  
		Size: 4.2 MB (4201126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810e9145554d8f367f939e25c49954e924744404c174f4139ed44aeab45c3c44`  
		Last Modified: Fri, 13 Feb 2026 19:13:58 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2b334ab333e0a7d73c61a7b00ccd89500221c1cbe99a1efa48d53f8c8a363b`  
		Last Modified: Fri, 13 Feb 2026 19:13:59 GMT  
		Size: 645.4 KB (645388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be46eff9e88c4777ce2dc8a9bacb54783daa14286f9d272c9281d4368066eb`  
		Last Modified: Fri, 13 Feb 2026 19:14:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:010025422a37c5e98c5ff9a6dc6c6849007312c0efff7ad59f1f7f0a94d03a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca692e5e13b982755975c356ccf2d6870872ade908519a34abcebbfe4f51a3cc`

```dockerfile
```

-	Layers:
	-	`sha256:75bb5b074e1aa8899d4b98c1de88981e73f0389e97119e709590bb40d074475e`  
		Last Modified: Fri, 13 Feb 2026 19:13:58 GMT  
		Size: 35.8 KB (35785 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:8a61e29e102dc93186be7f5bc1573ed301d92d047952f2bedc87e054725dd762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47444013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795b1d1004783a7656a8fd6c8f733bc3faeee9c8870bd52b7030ee7cc0c36c31`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:38:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_VERSION=8.4.18
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 19:53:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 19:53:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:58:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:58:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:58:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:58:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:58:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:58:51 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 20:35:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 20:35:24 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 20:35:24 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 20:35:24 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 20:36:27 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 20:36:27 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 20:36:27 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 20:36:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 20:36:27 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 20:36:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 20:36:30 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:36:30 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 20:36:30 GMT
USER adminer
# Fri, 13 Feb 2026 20:36:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 20:36:30 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7dd774a9daa9cc5f74d16d61155e614ceedece1fd19c05044ba6ace37dd4c6`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a002cadcf53d322e552c6a02f973915d8017427dfda71de122592386df6743`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b05b21b742c21780f39ad80c5babf4b1d13a4f41a2726c561bfb0fcc954e0`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff6babe288c0fe8b721533db77a800e93ce5e04983f89c6f760cf55a0b02e41`  
		Last Modified: Fri, 13 Feb 2026 19:59:09 GMT  
		Size: 13.7 MB (13699116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b32c493052c26eeb2a99ed19b58c9493e47b5f88e19e372e723b8503c41a13f`  
		Last Modified: Fri, 13 Feb 2026 19:59:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047af22c780a4f3cc08141c280d6f6cc78b40f3e288af24a111e4d1b9fe75096`  
		Last Modified: Fri, 13 Feb 2026 19:59:09 GMT  
		Size: 21.2 MB (21168794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f7cbcb2ac7d5028e86240edbde9b6e2d189c1225d2d9488a9eaf39c91a6b00`  
		Last Modified: Fri, 13 Feb 2026 19:59:08 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2710f1084d585a4d389314e88535e1999cd2e9526c460e1eb3158f9eb1878`  
		Last Modified: Fri, 13 Feb 2026 19:59:09 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b3267b042ecce674316416cf92cc1f9d8ce6c8252043480986212b44a60168`  
		Last Modified: Fri, 13 Feb 2026 19:59:09 GMT  
		Size: 23.4 KB (23372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d40c9f92f4878837fe424414a6a5f1b41fc42f65fc41378d36e7f064300d97`  
		Last Modified: Fri, 13 Feb 2026 20:36:39 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fe0e8d1f458b94e7cb1b3bcd21564707d250734d1a893e2b6ee886bd7b1a21`  
		Last Modified: Fri, 13 Feb 2026 20:36:38 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5672411c2539598b93e3beca9705a6be3eb70c480e4adfc1e3c54a903483fd77`  
		Last Modified: Fri, 13 Feb 2026 20:36:39 GMT  
		Size: 4.3 MB (4277765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7709660e794cf3197a9a0f46e5195f6f7c16bbb0ac479e89df8902768e7c0fc8`  
		Last Modified: Fri, 13 Feb 2026 20:36:39 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9316f223bf6edf8d557690eb8d106746f2585dca9c227f389224076162df4e0c`  
		Last Modified: Fri, 13 Feb 2026 20:36:40 GMT  
		Size: 645.4 KB (645390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57667b0755578157e48ddea9a25e2a766f0bac6b53b320453ad25f1e1ca79184`  
		Last Modified: Fri, 13 Feb 2026 20:36:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:6fcde7fd89b090242d0d536095583439940cf849bc84f3bed9e70e5fbf3d0dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596e988439a1d4c2b738933dc63c3da5d38392d862161ef8bb81cc999d572c67`

```dockerfile
```

-	Layers:
	-	`sha256:c9522aad19f9f0e3053767a9d293b2edd2efd939ee1b5f4b99c6b02870d84d28`  
		Last Modified: Fri, 13 Feb 2026 20:36:38 GMT  
		Size: 35.9 KB (35895 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:02799c2cf1c3fc7d35c6148b33db92a74fa521bfafc9408b48e7595ace1f0421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45053647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ae4985ffd905d4b6ea533d3aa3be9ecc455dbbcf38c0c2d5f59bf359e990c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.4.18
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Sat, 14 Feb 2026 08:57:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 14 Feb 2026 08:57:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 09:55:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Feb 2026 09:55:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 09:55:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 14 Feb 2026 09:55:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Feb 2026 09:55:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Feb 2026 09:55:20 GMT
CMD ["php" "-a"]
# Sat, 14 Feb 2026 19:14:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 14 Feb 2026 19:14:58 GMT
STOPSIGNAL SIGINT
# Sat, 14 Feb 2026 19:14:58 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 14 Feb 2026 19:14:58 GMT
WORKDIR /var/www/html
# Sat, 14 Feb 2026 19:20:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 14 Feb 2026 19:20:31 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 14 Feb 2026 19:20:31 GMT
ENV ADMINER_VERSION=5.4.2
# Sat, 14 Feb 2026 19:20:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Sat, 14 Feb 2026 19:20:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Sat, 14 Feb 2026 19:20:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 14 Feb 2026 19:20:33 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 19:20:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 14 Feb 2026 19:20:33 GMT
USER adminer
# Sat, 14 Feb 2026 19:20:33 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 14 Feb 2026 19:20:33 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d33e65fad64c7dcc0a0eb40481894f96d4b6297e1b0474c8116dd7a88b4b0ea`  
		Last Modified: Sat, 14 Feb 2026 09:56:23 GMT  
		Size: 13.7 MB (13699098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371bab6a76000274d63224d73ea7c45bf2194332302cf154b141bb42deed0de8`  
		Last Modified: Sat, 14 Feb 2026 09:56:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fef9720b331af3548f6f5430d8df11a2a5044ddaba2514de1c52dd35ce3bff`  
		Last Modified: Sat, 14 Feb 2026 09:56:24 GMT  
		Size: 19.4 MB (19391219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d311b8edbda881bdc4fe95414d2c48b41d3dfdc595486288b38d43b9e0db27`  
		Last Modified: Sat, 14 Feb 2026 09:56:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f19f190847ec4a92b7eceff0a88eb51535f01969fcb4a5cc4df33c4913964`  
		Last Modified: Sat, 14 Feb 2026 09:56:21 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4782799e82b6f71bf23c8dd0a097c3abad0a561de4f3552c2d77e3e0f80a2f8`  
		Last Modified: Sat, 14 Feb 2026 09:56:21 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a490e7f20ab2f3c69513233f75ebe02696aa2d07a3a32e862c6405e98a64a0cd`  
		Last Modified: Sat, 14 Feb 2026 19:20:49 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81bf496681a72391826af7062e78afaa929a6db591bc028617b710bf665fba0`  
		Last Modified: Sat, 14 Feb 2026 19:20:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576c04b1bc048a36bd16166416bd090f0fc37f547ba0289cade71920b02dacc4`  
		Last Modified: Sat, 14 Feb 2026 19:20:50 GMT  
		Size: 3.9 MB (3937220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2be0258812cd7053a325989ee543a6e4af2aeda3bdc5a66645ac4f9fdd8265`  
		Last Modified: Sat, 14 Feb 2026 19:20:49 GMT  
		Size: 1.8 KB (1774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2014347b2a7328eba01d2363a6a61d1a5bce4de518eda09ac5989b7668cf060a`  
		Last Modified: Sat, 14 Feb 2026 19:20:50 GMT  
		Size: 645.4 KB (645393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89c0c60ef8a849a2b54abbf5d0786b5e581b22e69cef81c2f78d155fa200385`  
		Last Modified: Sat, 14 Feb 2026 19:20:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:fb821b6e20498aebcc34a1eba9142d3161221a5f5310d556c477d18024bbe63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33dc112ff78726f9bfcede74d8e3b3b6d5637eb1fca5a89b0c640a1bd81a7a`

```dockerfile
```

-	Layers:
	-	`sha256:936c73739fddaf4a9bfa9f695b87764e187fe37199d03d080a9e2c7acb42736b`  
		Last Modified: Sat, 14 Feb 2026 19:20:49 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:b98655e2b075dc4901b7b7f7fb789f46cc3afc0f5b70ed102e5021a983608087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46090975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741a9693b034aa458045201b5589c80f7d2a539d3153f412fc83bd8e876ba670`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:23:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:23:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:23:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_VERSION=8.4.18
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 19:05:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Feb 2026 19:05:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:11:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:11:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:11:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:11:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:11:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:11:16 GMT
CMD ["php" "-a"]
# Fri, 13 Feb 2026 20:10:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 13 Feb 2026 20:10:27 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 20:10:27 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 13 Feb 2026 20:10:27 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 20:11:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 13 Feb 2026 20:11:01 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 13 Feb 2026 20:11:01 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 13 Feb 2026 20:11:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 13 Feb 2026 20:11:01 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 13 Feb 2026 20:11:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 13 Feb 2026 20:11:02 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:11:02 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 13 Feb 2026 20:11:02 GMT
USER adminer
# Fri, 13 Feb 2026 20:11:02 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 13 Feb 2026 20:11:02 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ddec292ce8d22cd45e25f291194336fe15e71a195e9527615f1f4cb93f051a`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 3.8 MB (3795094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3a271895fa21f842dc6a628c9be8ba868f3ab56244b4dba69e5063768250e`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb84f4380740d6c7657500d1fa1467fdcbd30beb8d1f4599234a969e915e28`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658edd3e08565739ec9d16296531d1b5f2a4698cfb0658a8bc17143c0cc529a`  
		Last Modified: Fri, 13 Feb 2026 19:11:30 GMT  
		Size: 13.7 MB (13699099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0de2ed8e5dbe4832f8fc82b2f87aa76aa917cf7f3ef4577baa66113e71051e`  
		Last Modified: Fri, 13 Feb 2026 19:11:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f9fb59a06a6a87f37fea5b818302d8eb7892a9bcf5eb9533303af84ffa6944`  
		Last Modified: Fri, 13 Feb 2026 19:11:30 GMT  
		Size: 20.0 MB (20018231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d283b06c86678716ae25d2a548a34f42f08fb4e809b5b6457d72307745809655`  
		Last Modified: Fri, 13 Feb 2026 19:11:30 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58beebe0a32bd7011ec7b2471320910b35c678d9ab6efa212925d66c4cf1df0f`  
		Last Modified: Fri, 13 Feb 2026 19:11:31 GMT  
		Size: 23.3 KB (23343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb07b831079bf5c0fab693669e7ca915c78c601a01c163354f2dffd3de593566`  
		Last Modified: Fri, 13 Feb 2026 19:11:31 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71f3f3ccb312e3dda056ddad21f504500dd769a42d3f24e02be45431f3eae1`  
		Last Modified: Fri, 13 Feb 2026 20:11:10 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ff0ea838265eb88c8346d798a498d57bbaeb6b1dede529bae861e735653c47`  
		Last Modified: Fri, 13 Feb 2026 20:11:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24196e1a63ad13e9049e766463a5e22814e2004398c0961d73eeceb3abbdb6d`  
		Last Modified: Fri, 13 Feb 2026 20:11:10 GMT  
		Size: 4.2 MB (4153386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a17c10b2c51545c3332c3e86497b8a7ddb8a5c90af9907b767b5bdb92ce79`  
		Last Modified: Fri, 13 Feb 2026 20:11:10 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eadfdaa01c345c8972c82147537e32e30862ea856e3079423e6af299b0f37d0`  
		Last Modified: Fri, 13 Feb 2026 20:11:11 GMT  
		Size: 645.4 KB (645389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314f40180b3ad2436675fca5cb6d740805466fa33cf5883eb3f30c6a999e6fcd`  
		Last Modified: Fri, 13 Feb 2026 20:11:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:a559d6f6f61d9b3ff056788e615e68307406b75344df4dc79da8cc274e1747d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652b863745685e5f699716b4c49ee03e2710495c04e77d49c2462bc42cfa1d75`

```dockerfile
```

-	Layers:
	-	`sha256:626916ee1da756778f3f57448689aaecd0db3485508d07b0dcc23806d0c84f94`  
		Last Modified: Fri, 13 Feb 2026 20:11:10 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json
