## `adminer:5-standalone`

```console
$ docker pull adminer@sha256:a3bea217657c5fbe995695a3c582e7860491b9bab90c827f12c03436f07b7c37
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
$ docker pull adminer@sha256:30243e664e185b1892203dd152839e56bf719f2c7251b4352b7b3e640279e368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48067311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454bb59d2a3ee4510d889c4ff3536a51b23193f9692793bdf6622e2960b56d1d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2a936c44a3f90ca9bb77c75706af43b3d2f44ed6ede4e171329a78a790db6`  
		Last Modified: Thu, 25 Sep 2025 21:18:05 GMT  
		Size: 5.9 MB (5928419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e20bee4789b3efba3eb9880aeaaf4c13e6263cd79978da3db73d0c25127be8`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103731ea806d2baabba81246429d8da0b3c89d8ad9856bf92415acd5f9c80d15`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34de792613dd7edf3c6766483248c2fe987230e18957bec472a65d5023ec4f`  
		Last Modified: Thu, 25 Sep 2025 21:18:05 GMT  
		Size: 13.7 MB (13667225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34ce04f95166a53d64e0a20ba204ef7b91ef4c3507f5e200fb6ef60eed0a24f`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85efba01306816714aefb1d018a4f07a989049e5ea7fec8bc3cf2e9ea732ca`  
		Last Modified: Thu, 25 Sep 2025 21:18:06 GMT  
		Size: 20.0 MB (19953079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3fa80949cbcc4888a1e2cb3f866086f5a7fc49dbc12df17e6db2ea06b1a0d4`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe723748b5fa36ef1dc7d2400ff6536108dff6ce8d3baa2e175a82b9156cd5`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585a1c45dbded911fac84d7d7b4cc920931f87d41bc5353ae28a4bbc65f7356d`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 19.9 KB (19944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674fec1834daf15546d0aacf205510e57439f36002bccf4400bec0ca8413d5dc`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41be3dfd705ef6df40c20954c5d43676b3d899930f1aabb9878b2bb8dbacc5e`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bece037d7c7e3d4726b006d97ac9e391933ccd4fb7cd96d20058b704b57c59a`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 4.0 MB (4030449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e850c4dc47ce5a9aa72fec716146390d31fb7630af2d36aad8b348bf50b8a5`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56556a2fdcca85313ebe30b23adec817891ce7397a0ad2cdd2dcda3af5722b`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be059d3a50edfeedd522875a71ddcc3dd3360331086f772cd202db45225b64`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:652248cb77149c89c696ebc1b8c0a952f8f2249d702f12282995c27b7ccc872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28431e536ee4f5a03988364b566b2075419d6684ab8c33dd20f005930124e379`

```dockerfile
```

-	Layers:
	-	`sha256:93d756ee95febd8e8380a3726fde13db1687c2c5525855383fd1a28868f63294`  
		Last Modified: Fri, 26 Sep 2025 00:50:08 GMT  
		Size: 35.9 KB (35877 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:b8b1603884199294d69ebe6162940bf084cc23b8d3cbc5c1ae9eee833195cd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45053815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bd810029d0b932cda160d3994999923c9db2c0da03c60aabe7352a9bb6c409`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd09a08e7ae23c77a346f98490dc9a93aa7619b29e0da6004f45067b309f868`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 5.5 MB (5532146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca2b81b6487deabfda220be61cddbf420c57d23eadfd158c8e507e436298bf`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d111b1e5dd7470e5c2bbea737ee759887649d96bd552d10e916c97db5abce`  
		Last Modified: Thu, 25 Sep 2025 21:24:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2582584a0acae70db7f889e20dc84c4119374967dc732f38631574cbdf48ec`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 13.7 MB (13667211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c98c83b217968bd586f2d78bf5419a8f85f0687781ec5849db4a081a234283f`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cc377747602b8b554f2259c0c3af06454fe925206218ca22735faa88090d5e`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 18.1 MB (18061226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f599a6afaf9545b123598fb95102ae946c30ad36c2e4f9d6e32a75e38b4153b1`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47803ddc2db992bf692b562a08f786e8b8d7c3e5aac1221e2ae3564edc4c86c5`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a0481bd982dd27026ecf9bec57d20e786b1f0580456611cee2c74b934b294`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53921507ea695d6a707da0e50e2f5d82a896f2e2c2627c3b448d4ab6efcbdd0`  
		Last Modified: Thu, 25 Sep 2025 22:16:55 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3448d52213a7520e7c7fa5fd74cf500b78bd494967492400a5c627c560698456`  
		Last Modified: Thu, 25 Sep 2025 22:16:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bc69732baad7db980a6b38b52647dca35e95325bfacc69fdeadc0c7330cc53`  
		Last Modified: Thu, 25 Sep 2025 22:16:56 GMT  
		Size: 3.6 MB (3604306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa71b2d0a37a7b21ad45824f7c0686a4d232d23c337de49edbf0caeb1787d305`  
		Last Modified: Thu, 25 Sep 2025 22:16:55 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b196ee44e8833b23daa60691f2ec72c913bb1f5f4abed5df2adcda286bfefc48`  
		Last Modified: Thu, 25 Sep 2025 22:16:58 GMT  
		Size: 640.9 KB (640901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a1ee42126b1edc2c51c5984b8ba5ad173fd36cd3088e68703d1681373129a2`  
		Last Modified: Thu, 25 Sep 2025 22:16:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:80b064f07c20cce79a94606a74416d3276c9a9369fbd45ce11660d3120fb714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873e9e052f28889661437f1217b7021b99900068c90b94c2330f10ba77edad6f`

```dockerfile
```

-	Layers:
	-	`sha256:4696f75d319ee222076cced12b5941bf76432c6aa2c83d766cdb76bb82e606bc`  
		Last Modified: Fri, 26 Sep 2025 00:50:11 GMT  
		Size: 36.0 KB (36012 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:2becabf723d70abf38d0ef3adb4d52b1e1908e8acbe9a68a429976f6c9689c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43479386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0fcb23878fa3d53c943ff1ca27218272a0888419ceecad929987e679765844`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef01fcfdd81544962f52d1296ff7005ef278a0a5371204d8be529ad6dff7d8`  
		Last Modified: Thu, 25 Sep 2025 21:24:10 GMT  
		Size: 5.2 MB (5180930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2f09e837701e70a2c802ed277086e62090638c577442184ed7833eaa6a2553`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785795fec154feea6a5a87ef118bc10303547523c70c312098aaace4b6759ab8`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4562f9188b70feacf2ed27be01a27d2c63497c40132611eb5a8ed637eb0a7`  
		Last Modified: Thu, 25 Sep 2025 21:24:09 GMT  
		Size: 13.7 MB (13667207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22a95aaf38d25c9cf9b5fd68f3cb5ee8b6e894f3c143aad26de024ef1afee3`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3362f22ea6fbee659e43f98af9fbf4147b20771fba0d73d00cb3976c8086f626`  
		Last Modified: Thu, 25 Sep 2025 21:24:10 GMT  
		Size: 17.0 MB (17046725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f640effe716c26ce15e6574f6e26e4566c86b3306fc66dcad66e17fb1103d`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc6d31f2e4c375f33378f56b58a952e46b391be5f76b26d6a9eed865668812`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 19.7 KB (19726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13877332dc17fb5f31c0918a0950987759b9f5cc822da2df7c5201130f1612b0`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ae2681dc329a6b21e9220ecae621129e98e9285ad9bef3e835fd5871f97583`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbc95756232ac1c641dea70f6a51a5c89b3c9b8805c745ae8b1658d3e5c0503`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eb774809845926f6b4c639956ec7fbec5dd615be314885c9e2727879f83c03`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 3.7 MB (3677497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4ba2fdc1c7204da94083aeee74b3e5c8f1704ac24ca217a4c018e7b1ceb6c9`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d29b102349666d5a16744644300e66751cc6120b12450d0cae7717e6a7da8f7`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4d6cd407c766400e87436079df779acd98c144198e10c0a6c2743d92528a9`  
		Last Modified: Thu, 25 Sep 2025 22:17:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:9a301e99d7867c3463244567b7e97fb527446d0698061b414e5b4e1a7509fc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65aba1ed1f536c7755ab86a8a2ae3177720deb7bfa758c139e1502030786eb5`

```dockerfile
```

-	Layers:
	-	`sha256:0b77474a350e368b92f24a91eb797d5ee533f9bd7603a4883830c738b8f3a04f`  
		Last Modified: Fri, 26 Sep 2025 00:50:14 GMT  
		Size: 36.0 KB (36012 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1351c25a249228d13edb92c2e917eac73386ac59085a42d5e5ea44965706df8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48242980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d01e1e5f155c3cd4455a21434ada21a240ef661feedd9cdedf45ced5f64c72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8c7b2e9c217784e61b3c0ddb6b4e26fdb133bf2f34e672bd485cb10dd58757`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 6.2 MB (6228299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde80131a1962dbd6d57b20933c4648d46cb0bb76e4ad6b54de65c2d6227749d`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd787753b28919747a6ca2ac47ca1f5bae696309b63f8be4da507cf6681439`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73fdb35f594ed257b49c4a666fc7dfb05289b41771ead420baa3c20c25c986a`  
		Last Modified: Thu, 25 Sep 2025 21:16:17 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48193100f3dd3d5c046113859b2ab492b66451f5faa0f4b2e7c9f9f200bd023b`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47452b946469b77ef895a0c46efaca1b0957aad7c7f568728c81aa4bbe859a`  
		Last Modified: Thu, 25 Sep 2025 21:16:22 GMT  
		Size: 19.5 MB (19501217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c20e27e5283c45c9d98786db88a169b3d6a0967f50f91d19b372d3eb47c28f9`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0fc3a77a24e631ed41af821f3dab1a0b4d9a3e811cd1ce25ec3c988b203b85`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394c37dc426f092c33723bfe5af85ca3b1dcde4616898abcefc61270b98213a3`  
		Last Modified: Thu, 25 Sep 2025 21:16:17 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3623aecbd2340fa6565053c0c1d72af02329836b1bf9cdde0d65eb679ed13c`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e288b74eae7779ed251050e27a7a05abfa598e1c56ce2bd8272f421f935f3e40`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55b8ec15f8534ddc7f8add8c76a7ecc67498c9cf3b1096c6badc4186c42a29d`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 4.0 MB (4027470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7638fb5fd7c125049d657ffcb6dffd58780433052f99e6cdb649b954315bc696`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25486356434e4b3ab47783e991b0708f62bb2d9ad4a6fad267155fe7ab70ccb`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 640.9 KB (640895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada97f91cc635c8a46da9c1da678cda137fb409e49ace7cd8fceebcc3a5a59b2`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:199fabbefc58185c710d67e307184b40aae5bcde90e86d24fe90b6b8d03ab51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e6bdaf788911c3665ca030f5c00316a104250a34568985993c11377e59c9f`

```dockerfile
```

-	Layers:
	-	`sha256:0a0179afce110fc6c12ca396d7622aaa1aef534ac574b63cf63191ec9452bf66`  
		Last Modified: Fri, 26 Sep 2025 00:50:17 GMT  
		Size: 36.0 KB (36050 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; 386

```console
$ docker pull adminer@sha256:59e2114582ab08daedbbaf66b27eb7d414214be9503c343157ef2d0a09cf6ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48135024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd8addb9faf10ee5f4be3685e9e8d055aec581d4a7b2ab694da2d45538f37ab`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332bbff38a1e31cdb20e66cd96b6a5b08d6387b1d3d9b058c12db5ffd401b33d`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 5.8 MB (5794092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fce9b7b48fe4d9091443c377dece5d044c9d041ed44cf3b4e58af1583102f5`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534d94fbedd306099ec13c6fa95796a0e3c7edb14e786fea7c962e9d57939e82`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065783a28d08e93267bef06fdae9d8136d2b2ef95c7dd9937951c88b1761376f`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 13.7 MB (13667218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418bed6d3ee75d62fd239cee84136cf186c3dd8e7970b735d30cfb7d6b0f3fa4`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0797cadb17bdd7b3693738f2a6572e161695f6a3d3336e82dba36b360b0fd3b9`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 20.5 MB (20481834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cd29a4a0ac3d8310bc66a3d3ede08b40bfb2d9567023c8f1c391cedc586d1f`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9b8cf276fc5686128892f5695aa8d72c5db4f84366dfc128b99ffbefcef12`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba92da4e721cb04cda9898bb953d8405540f7fc004957407bb1772de783bc45`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 19.9 KB (19923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50d5abd82371998980315efc24fe2a1df6b69b5637ea300b3969c7f733d9c31`  
		Last Modified: Thu, 25 Sep 2025 22:12:56 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef0bd6f5cde5a6f328e3f4cb3192c99c000ccec0f14e285423d9b2e5b16003a`  
		Last Modified: Thu, 25 Sep 2025 22:12:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d45795c1c0aa257c080d45d2a86910b05c096f87fd5865e69559ca6cc1c0e3a`  
		Last Modified: Thu, 25 Sep 2025 22:12:57 GMT  
		Size: 3.9 MB (3888470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f8fc589e2d767e33529eabb730100cee206d48e26f47e95807d2cd13d4305d`  
		Last Modified: Thu, 25 Sep 2025 22:12:56 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bdbc6519b9639fcfae8db3d799bd672bbdbcb843d11f4ecf9793f099586bb7`  
		Last Modified: Thu, 25 Sep 2025 22:12:57 GMT  
		Size: 640.9 KB (640899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24dcac2d6a6c1eb218aa8c8d42ce1b65127ae305c265ca03374531ee3cd939`  
		Last Modified: Thu, 25 Sep 2025 22:12:57 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:1c5fab8634fe620b0c438552b6f709818114aedb438f0fb4c41665cd8c49f44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64a26286bb31be9f4ab63e60f5b371ed68cdf55febca5cd4fa5d6606e61483e`

```dockerfile
```

-	Layers:
	-	`sha256:4924ff7c91cae2a30e91b0377436a3f12e5dea61aa35992950abb3a958d5214d`  
		Last Modified: Fri, 26 Sep 2025 00:50:20 GMT  
		Size: 35.8 KB (35828 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:c926b4c31cc229607410350bf11c7113ea74277c089c64f952ae4bcbffbbb97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da63e4ac67c15e2fff51231ff7ca6b5dfe8b17af615aafb7a7091d001de07b76`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d165415cc65159456128153815546067ca89254c2ee16739d9a593915c2bbe`  
		Last Modified: Thu, 25 Sep 2025 21:50:59 GMT  
		Size: 13.7 MB (13667229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf9d58c2d24e175afe73c83186c70a54653d4a7a9e169b42a187588df2f087e`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c6b86280f0d78ca867fdc85683b4bd147d316f6690434860270cded233fe23`  
		Last Modified: Thu, 25 Sep 2025 21:51:00 GMT  
		Size: 23.7 MB (23658979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a03266532d2f40547f2998637ec30ab8daead8d5647cda1092bf759010e726`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68735b727384e36cb229e8a569527bed6d29607ef0fcc184b9ec6245142bbaaa`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a327693df1b9b6206d9f570299a84275c02003ba38d4a91e11c142da596913b`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475305a4954bb3e34306ddb9f0c225ca5bec5088684826840c805869848fe928`  
		Last Modified: Thu, 25 Sep 2025 22:28:29 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f265a9d17eca7cb68ca50a743b1b9149b8dc5df05bd5ebf68a5dac9eff415726`  
		Last Modified: Thu, 25 Sep 2025 22:28:29 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d46799be1c840f46f5478390b263b4943abcde1380f6256ec72c8a72e2d535`  
		Last Modified: Thu, 25 Sep 2025 22:28:31 GMT  
		Size: 3.9 MB (3877125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262735d7d87a2e988b04ae0079af6fc423235425e83525e5fcb4b3b47a57ab00`  
		Last Modified: Thu, 25 Sep 2025 22:28:30 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12003c28c3ce0a45828747f435067465b626cee3890eaa0e349f3eab261b47d`  
		Last Modified: Thu, 25 Sep 2025 22:28:31 GMT  
		Size: 640.9 KB (640902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b682596d34a45a333dcbd048b5a0e7dc11bc7a925ac1c42217db32fd039b926`  
		Last Modified: Thu, 25 Sep 2025 22:28:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:e1c065ed59134a75336f774afba9d0cb4a007e0b3d43d80ed3a568301ff5a4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c191ac6e8c67d5185bfb278aae9b6bbecddfe888c230994d7e9e9bc4d2d63aa9`

```dockerfile
```

-	Layers:
	-	`sha256:a97658eaacd50020fa024ea4a90eebdea5ad41ca810a4363c5dabea4b4ce872f`  
		Last Modified: Fri, 26 Sep 2025 00:50:23 GMT  
		Size: 35.9 KB (35939 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:8727ff6aeb925319110b840bb0b773b8978ff78c6f0e57a47f9648e5378d63b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47248236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d9325f254fd6d5ab561dffe7aee3c8b92e0321b32712cf7ce5d8a6ad62d3e2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce54772840e390ce79b2bd312dffccae5a0404b88de7d2cec073f06bfc4a7447`  
		Last Modified: Fri, 26 Sep 2025 06:57:14 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6b22cf755134f26369ac0039e67fee0e571a02ceb8a94e09289af33125353`  
		Last Modified: Fri, 26 Sep 2025 06:57:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0365b3ab37d3f9b715bd780ad485c95ad15ed5c5b1c3bfd8970387dd36daf`  
		Last Modified: Fri, 26 Sep 2025 06:57:18 GMT  
		Size: 22.0 MB (21981498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b317aeae2dc6ed4a866738e3dcf9f1437efcbb8375680cb0494c81ae062b0a`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf49bc5c019b48fa352706ee9f2a45f3f399db6053ebef12e34dc331889673`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f239dc1f19e52fdc0efc9ea8ed3770da45c53b5f01033f7ed075a4ca9389f8`  
		Last Modified: Fri, 26 Sep 2025 06:57:09 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d467a6eda6524860774c0b26530feb558e187c39e6ca3a6bff113652070bb6`  
		Last Modified: Fri, 26 Sep 2025 22:34:55 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35822f3486a14e657355484e83f0b2e9f82a7685967cc3a248936c001d79175a`  
		Last Modified: Fri, 26 Sep 2025 22:34:55 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f5f2037b622bd64edb5f9f4ad07eadf8bf8452df49e5e5cb399436b764385`  
		Last Modified: Fri, 26 Sep 2025 22:34:55 GMT  
		Size: 3.8 MB (3804491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23dbbfe416b82f40c98a6f3105085fd77309ab6d761958c198b2611c9d7a013`  
		Last Modified: Fri, 26 Sep 2025 22:34:55 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b4858c6ce6e1704364c58e18003094866815dae2df6734926dcd607320a134`  
		Last Modified: Fri, 26 Sep 2025 22:34:56 GMT  
		Size: 640.9 KB (640904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75a0ef2afd6b6eb642062cd6435641a66ae856e68e252dbd3bf93be7bb5e8d6`  
		Last Modified: Fri, 26 Sep 2025 22:34:55 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:b7c7ae2309befda8e456d819133481413e374afb5aebc5f91d62b9dd2d0707e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bddb607ce8f5cba7b3fbf263351f9a2954f3b91dd4f87de0103f98ad1935c08`

```dockerfile
```

-	Layers:
	-	`sha256:241875f52a9143d3286e3ffb7af6dc4ef2bb4a371708ab5c7d9c32934060050d`  
		Last Modified: Sat, 27 Sep 2025 00:48:54 GMT  
		Size: 35.9 KB (35939 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:580bc2642dcef904d987284b3f1f5c56d199aa9bcea48055a2f418d952d14b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48163040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74a393ca217824cb3a7e862e2dce356523d1b9ae1f3698d744e15d3120daf9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 08 Sep 2025 21:09:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Sep 2025 21:09:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_VERSION=8.4.13
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 08 Sep 2025 21:09:19 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-a"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_VERSION=5.4.0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=7a572ddc4e512d4752902b769ebb400465583d814c9d280c0b7175d51a3159e0
# Mon, 08 Sep 2025 21:09:19 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=1bb363516dc674fed3d7f3823437d9a4ecbbbfca0615612fc3a8a04fe184ae9d
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
USER adminer
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a3d587fe45527c5fb9d0f6c3e87577a24ab838aa52feae75c98a13d113ba79`  
		Last Modified: Thu, 25 Sep 2025 21:48:21 GMT  
		Size: 13.7 MB (13667205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aa7a56f2ffb6e0181fc8c56485409ee3e9cdccb2244fa89a1fb4aee0d3d31`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e447a71c18dfb923b3d4658f94697f99b4f8f9a7b92299e4546daf0e926f1`  
		Last Modified: Thu, 25 Sep 2025 21:48:21 GMT  
		Size: 22.7 MB (22734313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e163e1f49f7cbea36f0daedf566336c2669b7cfe583f6db78f875a6017afa`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554b90114c9d70edcb59ea26af2028ec3598be22240434bfba9bf6372499b22d`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 19.8 KB (19755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac8d5741ab97dd8cd75dd42c45280daab21984e353e1710a0e09c13fd204c39`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31bcd7f22f35b8bd935e7b0cd1f9ba46806634b0b755503623aa1a600d3e4b9`  
		Last Modified: Thu, 25 Sep 2025 22:23:53 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ad42d466e12327ddf0a34b6e204fd4c349bb1a0fc24956f72126064e9f44c1`  
		Last Modified: Thu, 25 Sep 2025 22:23:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33422fb42fb00f29edad65d4a07ff2c2e8e8f82b9de97c312edbc738961f98f`  
		Last Modified: Thu, 25 Sep 2025 22:23:53 GMT  
		Size: 3.7 MB (3748616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8639407fb1543ea62f88a7a6841058047ba48b04031283f8dd5a0ddac70690`  
		Last Modified: Thu, 25 Sep 2025 22:23:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ff227aff8f417db70963b9c1b5e918ba16fbf379ac6d87b1bc93a066596091`  
		Last Modified: Thu, 25 Sep 2025 22:23:55 GMT  
		Size: 640.9 KB (640906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de43ac2063cf3a9ceb699b3b7f897f157d4c95bc28600f8d928db3127de0421`  
		Last Modified: Thu, 25 Sep 2025 22:23:55 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:e3efd73e1740bfeaf439e17031b20f429aa1dc91337b14d5550740c1a17c0522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bee7e93337377a5c28c5b01e5bfcdb0288e518c140562d0db60f81193945f5`

```dockerfile
```

-	Layers:
	-	`sha256:3d4b3c0e9154186f026f1d97a50cf2cef417c5f975c59924f1723ae90a7438ee`  
		Last Modified: Fri, 26 Sep 2025 00:50:28 GMT  
		Size: 35.9 KB (35877 bytes)  
		MIME: application/vnd.in-toto+json
