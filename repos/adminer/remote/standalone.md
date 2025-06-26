## `adminer:standalone`

```console
$ docker pull adminer@sha256:730215fe535daca9a2f378c48321bc615c8f0d88668721e0eff530fa35b6e8f6
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:403964cfec38e5ef25c893c6ab2feaa1215dc1ec7953391ef247a723d6f83476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46590440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b97632654158cbd6dd4cec01eb0b4c05083570a398751cba9d11855bdb69f28`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b52dc45b57bdb10adcefbaf15b7407514b6e428c6ff3a204aa3de395930dc`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 3.5 MB (3468347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b59d780d3e14cb42593d46d17834e9d61fc53a2911c91756df543e237e72df1`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b91823d6518dfc3edda879a6c1b4570f00a9904ba181876588dd382ca14f3d9`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b85bfbf34452714fdd6bd0b6ae067d4aecd379d026d8a63005cb417e6aa2b00`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fa75df5070e2bf129ee9a55601fe4aeea9f6733ba7db7e875e0bdf86d5f6f`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e596a23157834bb6995c20124de68b3b4709f6f4e48eab120c27d3169ea683c0`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 21.0 MB (20969831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc997cc1a60339301e41f08fa620e72af007b9ae8e3a6653266631cbcc12b72`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548b03e157af72699a2b0c708ed1848139b85c1e825fae6010a7e9cd0d0b0d3e`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 20.2 KB (20196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92305aed9fff99346e89b6cf9fb2eaefa429b2ec81bb58c12b79849b4a9989b`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71db710fe34409eddb960fe38459d84269bc0e3c4407537ca582247c1d13ef05`  
		Last Modified: Wed, 25 Jun 2025 21:29:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f734962d4ce9fee7c0739ec066c3a4d3f6bf3e361055c0bc246298d55446bb06`  
		Last Modified: Wed, 25 Jun 2025 21:29:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c88194d33d4f73f45e3e9e76f4c80f34af0d6b1a4b5e438d6a4fed62df4d8d`  
		Last Modified: Wed, 25 Jun 2025 21:29:31 GMT  
		Size: 4.0 MB (4032145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8153cf848b0b80a44d8ce65fc2fd701cf85e7eb2e20f51472101354e7c183c04`  
		Last Modified: Wed, 25 Jun 2025 21:29:35 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5764c4ca80d9ec335d16893817daaa985fe361dfbba310727b88330603c8f21`  
		Last Modified: Wed, 25 Jun 2025 21:29:40 GMT  
		Size: 634.7 KB (634705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfbcf5aaaa9227819377bcb938374282608d1b555e8c3ad74da77af7d2eb9e5`  
		Last Modified: Wed, 25 Jun 2025 21:30:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:6b934fcb953007aadb32b824226b8a5408ece327026ce2d7c15aa09e24bcfa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec63f401ec1e5fba44eb8884d95344e9c7cd95461498ca9479f23d92b7afc85`

```dockerfile
```

-	Layers:
	-	`sha256:3dbf7c37d4c6efa798163227f556d6e7623835625fb1fb421715f3a346919a73`  
		Last Modified: Wed, 25 Jun 2025 21:49:08 GMT  
		Size: 35.9 KB (35865 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:2d9c609eb16ae81131cd612a605ac9fd79c57bdd8ee3ab638f39f26a93070732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43953714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb46f393a19961638e30c893c94f451fa9e2e5893c94000f70e8486529b2373`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
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
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5156ab784127c5f20a3284bc78069476b0aec6fca9f1c760d1c0247d2729bf6`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6fa42566fcd2f22f0fcb32f9d67be668fadec8dd660d6a59b78743cd2ffbb6`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5862e7e3209a4e6957f47484a85d22d2255e5a5d9b310782bb869fde48ebb`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2ff09c7dc8a46bb4e820dc2d50a62aad35398ab921b11d3ba8193ac3e0915`  
		Last Modified: Wed, 25 Jun 2025 20:15:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c80953e14c8cc719aed6cf143985e2537570d3069a1500f5b5b66fb88afa945`  
		Last Modified: Wed, 25 Jun 2025 20:15:23 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae51c4eeb15e128996ebe449611899f0566385a6a68419349c17ecd43f93f67`  
		Last Modified: Wed, 25 Jun 2025 20:15:24 GMT  
		Size: 3.6 MB (3605965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b650160e256456042fb85ad24673a0ce771d58876ed685a534ca955d672d0`  
		Last Modified: Wed, 25 Jun 2025 20:15:23 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad97875af4222d8508a379f7d9a4d542b022399aba71a694b15d6a970cc1289b`  
		Last Modified: Wed, 25 Jun 2025 20:15:24 GMT  
		Size: 634.7 KB (634701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8570041dc7a2dfd60b23a4f517ec6674f1584f5f501f8e646844ea9752f045`  
		Last Modified: Wed, 25 Jun 2025 20:15:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:37758199298fade7442cd15f74ed5784da6dca49c2310480eb39f2200ecd6482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f1e58340da92f068b4fe028e7c0af8328d039df96886ba550502d7336ae7b0`

```dockerfile
```

-	Layers:
	-	`sha256:def03ac9d5ce669c8feefa63d24d01ecb94a39d1a572fa2d58a7f314120620d5`  
		Last Modified: Wed, 25 Jun 2025 21:49:12 GMT  
		Size: 36.0 KB (35995 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0db6903d9a5ca43c7fffc8ce9bbdeff8a2167099419e18237ad59f6a56ca926c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42535848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b858230d6d3768d775eda9203ffb20671a91eeef5ada67a8e48f1cda59e847f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
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
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb43a513cc6b21818dbb94e80c2111720a53640ed898b33c7d23eaf2a793b99`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf5f26db369cad64f7244865d73d36a09009ff4cff9337925e0bf1233f4f81`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1b077491f1ad27d0d36553c589646b18751891cc03f34a6852b7d7036aeda`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03db35e833e9400c1fc500155969117cc8adf3862be3a642370424aa390967e2`  
		Last Modified: Wed, 25 Jun 2025 21:51:07 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc69c0d5fe0dfc9e8d8e11a6d19cda0e076cc5f7b9e73cb9c55ef2d5433795ff`  
		Last Modified: Wed, 25 Jun 2025 21:51:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b646d2e7f498a83279be7797c6ada51ac451412a8d31e740acc04ddcc7e0797`  
		Last Modified: Wed, 25 Jun 2025 21:51:08 GMT  
		Size: 3.7 MB (3679514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0310c5542a3d1ebfb3ba39d2bbb5ecad4710d602cb6306a85da13d626926842`  
		Last Modified: Wed, 25 Jun 2025 21:51:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333a9f2c40cc29c54cdcf1d3c7428762114b7854ce93e799ae3bf1f89896d15a`  
		Last Modified: Thu, 26 Jun 2025 00:49:19 GMT  
		Size: 634.7 KB (634701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d67530c1af7aae993e6178a3ee4b6b5c429f6746c6d28cf18f0999645b391`  
		Last Modified: Thu, 26 Jun 2025 00:49:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:756ab4e6a7b4e45b6cf5b22e95b91cea30c1af853b41bdfadaa1573cafefbe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05180e54a8569df3bba609bd9e930b3ac7233257ad9ddad3e236f89ec7223347`

```dockerfile
```

-	Layers:
	-	`sha256:f1dee9a3c4a018e685fb0b4d05340fb909efe296c9dc084388d4fc7389c7c508`  
		Last Modified: Thu, 26 Jun 2025 00:48:59 GMT  
		Size: 36.0 KB (35995 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:78742b7d1899e2d881aa6c36b5d1c7341d6628fbe60d8cdb440fa11ec29f0cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46477886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab05721bef82a0e906ccadc6b6aa43e5e3e0c3735f27c173d8b42a4a32e6911d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2160c382c8a176b40b436a0b1a268e7fa8ecc951327bc4095f044457e068b`  
		Last Modified: Thu, 26 Jun 2025 00:30:50 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec248c3be7efeaf0ea43613d090c93b9f4318d7d348127364766d710245a89`  
		Last Modified: Thu, 26 Jun 2025 00:30:52 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b458839ed157195a12954f47cb806bb5a130400c125c855fc6b13467eb11f0`  
		Last Modified: Thu, 26 Jun 2025 00:30:57 GMT  
		Size: 4.0 MB (4029270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ffa275a651a4e248ed7131ed1701cbedd7d1643e867833b86e975c69e0c4e`  
		Last Modified: Thu, 26 Jun 2025 00:31:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857467ce86743b20e0def74ac1fa05bf7d66a6c93bbd2d8d11c11a3444d325a`  
		Last Modified: Thu, 26 Jun 2025 00:31:06 GMT  
		Size: 634.7 KB (634708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3d9caf70618bcdc6b7847f72d7cd877b3ad90dac540d264f160a182a02ef91`  
		Last Modified: Thu, 26 Jun 2025 00:31:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:e3c774adf146dcde75b9ce464e7364c54f0e78cdae5ff7ef363701e306a1ef4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ef9921b3bfb59149232d5c9ca778ecaa45d10c68d2356a3f1a05f2f908c9f9`

```dockerfile
```

-	Layers:
	-	`sha256:0f508622f4ef54bcc1f4e1bcf58ddc6b2e87707b29542ecb4c33680acf865f29`  
		Last Modified: Thu, 26 Jun 2025 03:49:06 GMT  
		Size: 36.0 KB (36038 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:a7147a5422fd7c6f243a39180ab1e207e9ddd4965dbc1fd49cd6e01f789c1e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46849620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c79658575855f3833ce241879e8fea3b7b2bf4b7654d5c57f925336db18550c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec6ae0f7bd176cd3b23016bb9ee9698507770d28b379f7c3617105788ea8f03`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 3.5 MB (3527778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf97b1f594033871ab5310105351a00295f6cda0b3b6b64aa7c2530a313ff2f`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4d8bd5000c186b6ddd44f889cc89c9a18ef0e760f4f1b64c37f0d26f95b7f`  
		Last Modified: Wed, 25 Jun 2025 19:17:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d744be0c5e8ab473a7ebb7399f80c4408081f06ac83bbe63399fe642c76b21c`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c9cda8eae5dc08edb62412373f47a15a23be2a2ac313fcde2dd09cfa5a8593`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58194bae6a351287765b02dbcf39ac93de32f73428d63fbc828966a473110735`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 21.5 MB (21492986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60af96b687f55ce57ae78a8b6decc9aa61b3297f7f0cba4b1a3d94ce45651da9`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24f730e53b3974d094b1bd52b11a0bba281ada5aa6d9b8986ed3d828a592d7`  
		Last Modified: Wed, 25 Jun 2025 19:56:35 GMT  
		Size: 20.2 KB (20189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7f027fc3e2e72fee646df51013f516e6e507dc4e1c3d297ecd04ec8c3d388d`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa2c1dcad1d08fec6c9621e73eb8237533e652b1ba344e00fe155aa5ce83b93`  
		Last Modified: Wed, 25 Jun 2025 20:26:40 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bdb504d58db253495b5f15dd42da2d90dd22b5782c48948a464cdd9bb7bc3b`  
		Last Modified: Wed, 25 Jun 2025 20:26:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4474c148c19faa777bd1065995c617f726ba60e24e34e669cb07e933c27938`  
		Last Modified: Wed, 25 Jun 2025 20:26:48 GMT  
		Size: 3.9 MB (3889597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f7d78d8456de9fbbbb37605644d37c9d7a4348f101d4ce08ae932df03815c3`  
		Last Modified: Wed, 25 Jun 2025 20:26:54 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41214f61dd44105c87464927d12d57a276b3f8125d3066e36ae5701c05c6c98`  
		Last Modified: Wed, 25 Jun 2025 20:27:00 GMT  
		Size: 634.7 KB (634701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d706c56bc070c84780c27abfcbf0bd9164e2b9b6d3ac0303bc9b52361acd8a8d`  
		Last Modified: Wed, 25 Jun 2025 20:27:08 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:182cf3e3beba32643b15dda09513db06b64dbee063bca84a8546fb04bb978272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae6fc59b674c6ebc0e3fea5f57456aca4b88ec2a367f38e2f0f6115b995dbc4`

```dockerfile
```

-	Layers:
	-	`sha256:38b9585fc211a212af9a1c3ff67f9c1f9c7a5d1e842d9cb6d9b7af54b1712343`  
		Last Modified: Wed, 25 Jun 2025 21:49:19 GMT  
		Size: 35.8 KB (35816 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:a03b0c3f8e22223e95c78822329863b866275be32232db9a34ca0330d0e4a8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47424408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8347cf60f7eceef18953e8efcf98f40af41f30c697757fcea6046c97a8f028`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6bb6879849aac5b27aee39d2d94016f30c04c04f58ec31d2a54cdf9b9005f`  
		Last Modified: Wed, 25 Jun 2025 19:28:12 GMT  
		Size: 21.9 MB (21874143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0153508085a0eccd2c5a479136b3a5818dc0af2a9f519301ecc29d9e3ea57c`  
		Last Modified: Wed, 25 Jun 2025 19:28:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cd469cdf896f3397244a1ba52aacfb3295f1bfc89e70e4f7bc4f67113384f7`  
		Last Modified: Wed, 25 Jun 2025 19:28:09 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2dae6690e928ff0492599e654c93e0c755703f909cc4adc3e30c7818d0dd0`  
		Last Modified: Wed, 25 Jun 2025 19:28:11 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e6bef74fbbddc6d544b81e85d0b1c86a58ed383cf5f19523df7ecfb9b01f8f`  
		Last Modified: Wed, 25 Jun 2025 22:21:16 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e481add0e7434abf1ba20990952e4e3bf6576d21c78c88b6e5eef045a8beeed9`  
		Last Modified: Wed, 25 Jun 2025 22:21:17 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ef6f4a5a8677ec83a39d8126aeb3152bf6105b68266dfa6d474d6427342430`  
		Last Modified: Wed, 25 Jun 2025 22:21:19 GMT  
		Size: 3.9 MB (3878059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d792428f1ee8e264900ad7261b8afb72d30acb5109eacb8975d2169eb6b8b71c`  
		Last Modified: Wed, 25 Jun 2025 22:21:19 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69b6b8184606dbb88f95c9a842ce440a5ba5419f21675453400031db3b71dae`  
		Last Modified: Wed, 25 Jun 2025 22:21:20 GMT  
		Size: 634.7 KB (634697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20994d540c85636c133f211eba07e0d6539b236cffe1adc3da3635dd9ceb77`  
		Last Modified: Wed, 25 Jun 2025 22:21:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:12d1bab05b83408d1e8892eb020ce99f32b4c12d43cc8c5260ceb9418ca5d16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dd01d841f08b356ed992d4626afbda5f1153babec9aa8af4e1409da9a83e6c`

```dockerfile
```

-	Layers:
	-	`sha256:6661c7b0b389ac3a6294f375986b544b7ef81fbc203a58022629f85235eac190`  
		Last Modified: Thu, 26 Jun 2025 00:49:07 GMT  
		Size: 35.9 KB (35927 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:f4ebfd3a548ac91d2b2a0a5f265748e6851afb2b9289f88d2d1944e9cf74f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45634398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0911bbfb1ccc5e51b99b97b0a3f151100d1b58e2ec9fd8a7a265b60790d14f97`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
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
	-	`sha256:864f108a67404e7c30a0146417b3c89cdf579800c6bb81d8bf36727630b974cd`  
		Last Modified: Thu, 26 Jun 2025 08:19:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb754cdf595b2b188634190feac9826d30f1147e06423e4db03fcff29f1f772`  
		Last Modified: Thu, 26 Jun 2025 08:19:20 GMT  
		Size: 634.7 KB (634704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d20e1fc36673bd5dec0eea3c6fa9b4e292b12751d51748f6447fae42e28f5ba`  
		Last Modified: Thu, 26 Jun 2025 08:19:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:dec8326f694ba8411ebdafb738cffe1c0c128f5d0ab52d100f5e86a9309ca1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f67df511d879c967d34feb98e9ef71e49bf2a6dabe0b1cdc707749969d0076`

```dockerfile
```

-	Layers:
	-	`sha256:e8ac0d4ec5cc30b26b822d8987781bdcb3ace4e024f3ecde001f4c8e23b2c4cd`  
		Last Modified: Thu, 26 Jun 2025 09:48:55 GMT  
		Size: 35.9 KB (35927 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:2911339b4c6cb6300264b29d307de9648d7f9fca30f35327353022a99c50b0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46867069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b21e3a73dc24ab26385fbbe4a06aaa7d2ae3093a282edfa39de5845fc96ed7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 17 May 2025 11:19:45 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Sat, 17 May 2025 11:19:45 GMT
CMD ["/bin/sh"]
# Sat, 17 May 2025 11:19:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 17 May 2025 11:19:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 17 May 2025 11:19:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_VERSION=8.4.8
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Sat, 17 May 2025 11:19:45 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-a"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGINT
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY *.php /var/www/html/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_VERSION=5.3.0
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=7dcc196e941b18b74635afe1740dcd86970ab08b8eba0f00f149925aea3972ed
# Sat, 17 May 2025 11:19:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=b929336214ab94583dc35e7d492879d1de6e3ab75888a2ad2c86166651f2c6d8
# Sat, 17 May 2025 11:19:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
USER adminer
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c50b23d2f6267cb43b11b038938247a74fe9e643b50e59fdbb4b5a4b6fe7861`  
		Last Modified: Fri, 20 Jun 2025 19:20:52 GMT  
		Size: 3.7 MB (3699029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d657aded1e5f64f14aeb2f0fb46bb5042326900e94f375c02676e1df16f2c0`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773155ae64957d9bd56f77026e1934533d4df47e0e44a57e52cc2ecc33f78584`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822c9d5a1030ab3c3269394abf80c023151b1a59827d801166b5145f76b4b24`  
		Last Modified: Wed, 25 Jun 2025 23:54:39 GMT  
		Size: 13.6 MB (13640517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9dbb04ef645b5874aa35f37d0b50a07b7dbbb0a077a3a0f90c2f2f7578ada9`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdea73576f59da4b4d05095ca8c19d71770f99937b315c3b75175172222a0d8`  
		Last Modified: Wed, 25 Jun 2025 23:54:41 GMT  
		Size: 21.4 MB (21447113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4593ddbf6cac4b48dada192cd7a09c5f448702a71031f89e1d8a28932d7fb1`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e0b7d92cdad27b44de8c8a61cd63501a0e95d837956383b28b1ef267e3ecc`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c807aaf9359cb6ac7245e5f7d87b5958fbd2fb2575361ffec01837d86fa1b`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f28ac9bfe7782ff551de95669bc21913f712d9d5c22dc886236d210ac278ba`  
		Last Modified: Thu, 26 Jun 2025 03:17:41 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d591e1c81ad1a557adaf9e4c2b713ac846493c1b747d98549e31db36e0a736`  
		Last Modified: Thu, 26 Jun 2025 03:17:44 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19703a21b9ec6a09a9041d3a6c3c990ff3a9422ec24f02f0b6c2eec75d6b9a5e`  
		Last Modified: Thu, 26 Jun 2025 03:17:51 GMT  
		Size: 3.8 MB (3750507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2e975476ee3f9b07aec3a054bc7794d233c25e4eb0838658a28f3ac2cc0bdc`  
		Last Modified: Thu, 26 Jun 2025 03:17:56 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138edb8f2c42b6e19c8a0fdf8ab8a0939baca13c92d4ad0e8ef88c298fd16208`  
		Last Modified: Thu, 26 Jun 2025 03:17:58 GMT  
		Size: 634.7 KB (634698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50c814b05004db29dddf181d36137d27f4b50e2a9c3914ecceacd8302da282b`  
		Last Modified: Thu, 26 Jun 2025 03:18:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:8fa099a5d20ec539d354f720f61a6cb8d3a42429772367214b3abdd5f6e6ab39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fd03d26a92b4dd1cc3ef6e3c881d9ee40fcccffe711a51a604579fe152607a`

```dockerfile
```

-	Layers:
	-	`sha256:51c1d2c34f85a0de1545eaeea8024a560c7b99d8e6522d353304dd2959a0599a`  
		Last Modified: Thu, 26 Jun 2025 03:49:14 GMT  
		Size: 35.9 KB (35865 bytes)  
		MIME: application/vnd.in-toto+json
