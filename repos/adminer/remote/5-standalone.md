## `adminer:5-standalone`

```console
$ docker pull adminer@sha256:b6d3c299d1754368031415e567609d500a4a5a22c17b7812749a8f677d93f066
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
$ docker pull adminer@sha256:3a2cf526c68e912107c6e1d0f1ee6c549ebd4e7ac148799efc1dea813bb17318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46374560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa647030c240d881d0bfe767e9ff3374ec61f5936df10ccc13d06e4967a707`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 23:02:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 23:02:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 23:02:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 23:02:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 23:02:23 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:02:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 23:02:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:05:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 23:05:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:05:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 23:05:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 23:05:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:05:32 GMT
CMD ["php" "-a"]
# Thu, 15 Jan 2026 23:54:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 15 Jan 2026 23:54:41 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:54:41 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 15 Jan 2026 23:54:41 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:55:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:55:06 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 15 Jan 2026 23:55:06 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 15 Jan 2026 23:55:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 15 Jan 2026 23:55:06 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 15 Jan 2026 23:55:07 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 15 Jan 2026 23:55:07 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:55:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:55:07 GMT
USER adminer
# Thu, 15 Jan 2026 23:55:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 15 Jan 2026 23:55:07 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419f64c5eb0c10f2484e0d69e595476f75a7fbf2288be8a69d5c77282df465ad`  
		Last Modified: Thu, 15 Jan 2026 23:05:48 GMT  
		Size: 3.6 MB (3591441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4aac13b4de494ed716c8c76801c26bbc1c9f80abc2ecf0db663fe10925772`  
		Last Modified: Thu, 15 Jan 2026 23:05:48 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefcc3227b6b93f51613a419a65916ca7992c8e514f86ca2833f2226faee405e`  
		Last Modified: Thu, 15 Jan 2026 23:05:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664191f5e753b34dc1157f143af0530103f63abc707e36be29685b3c17886d1e`  
		Last Modified: Thu, 15 Jan 2026 23:05:40 GMT  
		Size: 13.7 MB (13694310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288c7ef78098f36523c01757f2a533c4c5e27cc0ab7de16308c52b87920678ec`  
		Last Modified: Thu, 15 Jan 2026 23:05:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a8b9c4c9a48c174200e4569bb5ea9705efa0bca4990a0886fe20c7849caa5b`  
		Last Modified: Thu, 15 Jan 2026 23:05:50 GMT  
		Size: 20.2 MB (20161575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5324520ce298ff9cf236b5f903d2591930d1f3e47e261bbd4803b6c9e11114`  
		Last Modified: Thu, 15 Jan 2026 23:05:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51f97f82d454c817dcd07659223877854f46912d64c36b9dc533500c4a1529`  
		Last Modified: Thu, 15 Jan 2026 23:05:42 GMT  
		Size: 23.5 KB (23487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e994ac1b89cc73324b12d09c67aeec31650737133225d5ef09bb3c681e40ba2`  
		Last Modified: Thu, 15 Jan 2026 23:05:47 GMT  
		Size: 23.5 KB (23507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f67ce5cde36374d78a36a214463c9d395f392691c9b80f70ff82f0376c9884`  
		Last Modified: Thu, 15 Jan 2026 23:55:17 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5b54352d620b9ccde5b04ebf1db876ed6f4705fab80f674af73c00c11310f`  
		Last Modified: Thu, 15 Jan 2026 23:55:18 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af7d5a6e5ec67f690cf52234afcc38b785c4fbc711ea5840294bb221e2d1fb`  
		Last Modified: Thu, 15 Jan 2026 23:55:11 GMT  
		Size: 4.4 MB (4371616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba47037c36ed92d1e63531c200b13f176b1ac19b2a8cab956955c3deddcf29`  
		Last Modified: Thu, 15 Jan 2026 23:55:18 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca1d73fb8af54ae37d488cbb5a1c15d7803abd984e3952b3f8f1b7e62612fc`  
		Last Modified: Thu, 15 Jan 2026 23:55:18 GMT  
		Size: 640.9 KB (640870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc5ae4377dfe2876e18eca72f50139826f2bf8f23144dc72f2f688bf8045ae3`  
		Last Modified: Thu, 15 Jan 2026 23:55:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:18ebda64aa82180eff10166b8e5473d583ed6197f14c93ff5f57401d31bd95a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ad6b2253db07656a0f9180d4a95e532e58672276efcc9a9727b50d5d826e3`

```dockerfile
```

-	Layers:
	-	`sha256:a21b58525b5cf6c09320d506f2a8a0baa468acd3dbb7df7d54fac84c64a5fa38`  
		Last Modified: Fri, 16 Jan 2026 01:50:51 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:597e259e2dc9b8e5ee314db2e83f24820a864c1418f3eafd1123944ff3215166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43725421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22a2940c7de67843de48ee2a1227b63e616aa43f80cc3e8c1fab47eeaa273df`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:19:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:19:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:19:09 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:19:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:22:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:22:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:22:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:22:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:22:17 GMT
CMD ["php" "-a"]
# Thu, 15 Jan 2026 23:20:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 15 Jan 2026 23:20:36 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:20:36 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 15 Jan 2026 23:20:36 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:21:10 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:21:10 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 15 Jan 2026 23:21:10 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 15 Jan 2026 23:21:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 15 Jan 2026 23:21:10 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 15 Jan 2026 23:21:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 15 Jan 2026 23:21:11 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:21:11 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:21:11 GMT
USER adminer
# Thu, 15 Jan 2026 23:21:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 15 Jan 2026 23:21:11 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad0ea67a7105a0dbb026f839aca07b46656a1577e457796c984633261460369`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 3.5 MB (3548073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e281cc61cb07066455fe5d32709e46a6e8120b783262daa2befb1aa33cdc9aa3`  
		Last Modified: Thu, 15 Jan 2026 22:22:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6d6835b8e4d48246d13bb92e3608432dd506bb58860265d6fe55d922391c7`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee6aa4a18fc2b751f8a604a93f625f14033088dc04f872e193816c54158d73`  
		Last Modified: Thu, 15 Jan 2026 22:22:32 GMT  
		Size: 13.7 MB (13694324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5f1e8758d88a8fcd485dd50c07a4ff68dc12b6610070dae712451df4c167a3`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a03c453ac853faf34e31882064b70cdb0a43cb40248887d3f9612109984ee0d`  
		Last Modified: Thu, 15 Jan 2026 22:22:31 GMT  
		Size: 18.2 MB (18249222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bccbfce4b6ed3e3fba7d0fffb5cd998b0f924d29cce53b60fda34a0469c2ab`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eec3b050734d0926a71f006c8a798d2176577d750d34fbd68db0ae7dc44625`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56773973a5ff4bff1d4eb09bfbb9345d98931a8d1ea88ee76d1b6d0187a085`  
		Last Modified: Thu, 15 Jan 2026 22:22:30 GMT  
		Size: 23.4 KB (23352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b627781b80f77e9b2d21e0247501207869ad26e5290cebf19fcf86f67e127cc`  
		Last Modified: Thu, 15 Jan 2026 23:21:15 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3aff12bc397cba20ab1c0274656f3ca9a07c807ef3ff73acbb8e0d39684a9cb`  
		Last Modified: Thu, 15 Jan 2026 23:21:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e535607525cd0b534632db49fb668ea3250643645b8b626aa5c4972e8bfa279c`  
		Last Modified: Thu, 15 Jan 2026 23:21:22 GMT  
		Size: 4.0 MB (3970155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1e8ddf8546b9644f7f082a5de24843f6d6e67fa01e0ae716ebff8352177831`  
		Last Modified: Thu, 15 Jan 2026 23:21:22 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddff9b480c79d03f4c2359b450f72358d0427cb43e2ef49adddaf023a55b1f0`  
		Last Modified: Thu, 15 Jan 2026 23:21:23 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a46b6826b1583b2497a8dda3044cf3ff027a98f490d83fef4cd164fe621c03`  
		Last Modified: Thu, 15 Jan 2026 23:21:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:c06420c31c0ef475325f1d0a9152997c4ff3f47ec14cd47c523a5479e4ef9767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a383545573f1ef02645a184814a1e8027f85ed6fa2db607cd2e571c6fa7e30ce`

```dockerfile
```

-	Layers:
	-	`sha256:4f32f6042a6148ccff3755e4323e8ed055fd1c8911acedb192115e4fd7fc5695`  
		Last Modified: Fri, 16 Jan 2026 01:50:54 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:ff2dcc1db8dca5ef2762e04eb844043ce18915a06db75f20046cd6b83724214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42263244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42a429324537a2040b809cd379b9974fca175702d581b10e087ddf6802a5b61`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:31:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:31:03 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:31:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:31:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:34:12 GMT
CMD ["php" "-a"]
# Thu, 15 Jan 2026 23:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 15 Jan 2026 23:26:23 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:26:23 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 15 Jan 2026 23:26:23 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:26:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:26:58 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 15 Jan 2026 23:26:58 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 15 Jan 2026 23:26:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 15 Jan 2026 23:26:58 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 15 Jan 2026 23:26:58 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 15 Jan 2026 23:26:58 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:26:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:26:58 GMT
USER adminer
# Thu, 15 Jan 2026 23:26:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 15 Jan 2026 23:26:58 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe7c4542bee490eed1abbaf17b24fcb18dbf490503a585e0f62731c293c7659`  
		Last Modified: Thu, 15 Jan 2026 22:34:19 GMT  
		Size: 3.3 MB (3346810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142a69c2c8868ce74f900dd03f1312e5117e324f11be04dc52052a04192c5d3d`  
		Last Modified: Thu, 15 Jan 2026 22:34:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867aeb0c5d35b7c3dcce6e5c13d2eb37ee4953a4ea4850797b5b77723fb3d5f`  
		Last Modified: Thu, 15 Jan 2026 22:34:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359416204ef7223f3d52aa32a5a1b5f837ce00ddd51ea822968822e7b8fde9a9`  
		Last Modified: Thu, 15 Jan 2026 22:34:31 GMT  
		Size: 13.7 MB (13694315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615fa6cef4bfb2abd488204c7d3f7c8140dc6827537b776fc80ebcf881576daf`  
		Last Modified: Thu, 15 Jan 2026 22:34:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f2cfb59a883b2618c5524132493855fd9deb1eac4b532c953bafbb72315533`  
		Last Modified: Thu, 15 Jan 2026 22:34:20 GMT  
		Size: 17.2 MB (17206336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48eb6958059363217b6c228fbab225191cb07cba2f72cf4219cdc9182efd86`  
		Last Modified: Thu, 15 Jan 2026 22:34:20 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a28ba04abaf1505334624155eb5d93a9a877a50f4d7c9a4e8794da28cbb01`  
		Last Modified: Thu, 15 Jan 2026 23:23:58 GMT  
		Size: 23.3 KB (23327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5dbb6bb156c24d164add56541a0d33316a34bcfde56690150e48ed45882d11`  
		Last Modified: Thu, 15 Jan 2026 22:34:30 GMT  
		Size: 23.3 KB (23336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e9266f65e6d5ca2d07552ae7c74e253bd7813090f7de61d6bb676f5592b4f`  
		Last Modified: Thu, 15 Jan 2026 23:27:07 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482eeff2e50a44b92be0c696c533ad5c153057a732a888382fe480570822634f`  
		Last Modified: Thu, 15 Jan 2026 23:27:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb2a46ee897e756a97faf515bb9d598bbb453e63b569293b405761b17163bf`  
		Last Modified: Thu, 15 Jan 2026 23:27:08 GMT  
		Size: 4.0 MB (4041213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a212987f5a0bd377628e29953f1fce5f62051f3a790edaf26cfe187f0e060e8b`  
		Last Modified: Thu, 15 Jan 2026 23:27:02 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5f26804e4a7f8bee356cf9c28b5c547093d0085fc20a383c640311b72f8851`  
		Last Modified: Thu, 15 Jan 2026 23:27:07 GMT  
		Size: 640.9 KB (640866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25397ee3bf25422d9995a0d03fbc233f4627d0feca5399a83be4a0ef2595f60`  
		Last Modified: Thu, 15 Jan 2026 23:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:fa8aef780999c09b041fb644d22ecdbec74166fb0750998c1c35a5a7717d6fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990df5db5ec64131d873141934c1a4e9053c67c0464b1178c83f0335848e8152`

```dockerfile
```

-	Layers:
	-	`sha256:f8fb8a64cf73d4d51b647b59bc7271bdb4f68bf311dfb8abb32f9bbec8a19dc9`  
		Last Modified: Fri, 16 Jan 2026 01:50:59 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1e2f4d136fdb972633f894795f0dd086ac08a531381729f6ca569e4d7b771308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46081989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34092e787188941f63d1ab93d2ff9d2984bdbce1c96047e704db021c52c0c1a9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 23:11:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 23:11:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 23:11:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 23:11:39 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 23:11:39 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:11:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 23:11:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:15:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 23:15:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:15:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 23:15:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 23:15:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:15:08 GMT
CMD ["php" "-a"]
# Fri, 16 Jan 2026 02:31:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 16 Jan 2026 02:31:51 GMT
STOPSIGNAL SIGINT
# Fri, 16 Jan 2026 02:31:51 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 16 Jan 2026 02:31:51 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 02:32:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 02:32:25 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 16 Jan 2026 02:32:25 GMT
ENV ADMINER_VERSION=5.4.1
# Fri, 16 Jan 2026 02:32:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Fri, 16 Jan 2026 02:32:25 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Fri, 16 Jan 2026 02:32:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 16 Jan 2026 02:32:26 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 02:32:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 16 Jan 2026 02:32:26 GMT
USER adminer
# Fri, 16 Jan 2026 02:32:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 16 Jan 2026 02:32:26 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b3f02863a3276e5b8bf9a35e4643ed7ecbbef4a3dbe71185be539d5c37b143`  
		Last Modified: Thu, 15 Jan 2026 23:15:24 GMT  
		Size: 3.6 MB (3600981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8644fc7b9b7edb643a7e76fc9a2f5b8b1cf04c99a3f49ab87800efadcf7157a`  
		Last Modified: Thu, 15 Jan 2026 23:15:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bc6ea271d9f6ab7523169691da55e4554f3a176feaca76cd62a350a38a6ba5`  
		Last Modified: Thu, 15 Jan 2026 23:15:11 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2234ffbf7723294fca72f586a7e1a2adcd2dfe0717c1efb873612b7efa25639`  
		Last Modified: Thu, 15 Jan 2026 23:15:24 GMT  
		Size: 13.7 MB (13694306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbee614c24731cd28521f224888b96f6f86eddd702dc915b92a7b0971f4909`  
		Last Modified: Thu, 15 Jan 2026 23:15:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42268dfedcb42738f99314ad51137c97b7f1e5daf87f477df5d1a166ac98733a`  
		Last Modified: Thu, 15 Jan 2026 23:15:25 GMT  
		Size: 19.5 MB (19531090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9ed7bba2d39030bb68e86745d85a9e20fb419ae516861078651fa77da9d19c`  
		Last Modified: Thu, 15 Jan 2026 23:15:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6078ed757912f9f8cca8739f5b77cf86e8178943cd152d358a8ab71c4c7ad3`  
		Last Modified: Thu, 15 Jan 2026 23:15:17 GMT  
		Size: 23.3 KB (23344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45474ecd69873f996a66c39e309b98247ca8c1fd02fe139228244af244f59d`  
		Last Modified: Thu, 15 Jan 2026 23:15:17 GMT  
		Size: 23.4 KB (23362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e33713abd741d3f55e9d6c61591d3ba73a60ea806fdb4d422b970149389e75`  
		Last Modified: Fri, 16 Jan 2026 02:32:46 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef78f8be4b12fded1f49db0d7f955b08dbfa09a899030a65c3c805cf70b09e`  
		Last Modified: Fri, 16 Jan 2026 02:32:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c27a93b4c400b34030a76db5695eec9a58a847ac3b1830abd58dd22effd67`  
		Last Modified: Fri, 16 Jan 2026 02:32:31 GMT  
		Size: 4.4 MB (4364641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e571ac8ab5055122538c126b1c03ac2dd6908191b2e16b0317dd2854eeecd41`  
		Last Modified: Fri, 16 Jan 2026 02:32:46 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f97d142924ddaaf04058bb5adf82531a5e5eb28f030a1a371b26574159dd7ec`  
		Last Modified: Fri, 16 Jan 2026 02:32:46 GMT  
		Size: 640.9 KB (640868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec8fdb5ce1746f552c8cfac686f040f654cec2aafe4582f6bb04e7a0465ce4e`  
		Last Modified: Fri, 16 Jan 2026 02:32:46 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:3ec59db4887d3dc74c8f5c3b5245d05d3919f09374cc3f82e12dd6d4e332e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d6b1787740941fdae602407caeaf7e5fd88ab6db9e98cf145e3a9d230dbcb0`

```dockerfile
```

-	Layers:
	-	`sha256:571eef9b54b6f796daebdc67cb00f1d6d7840d5a587cc90c20f55156f2bf452f`  
		Last Modified: Fri, 16 Jan 2026 04:49:07 GMT  
		Size: 36.0 KB (36007 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; 386

```console
$ docker pull adminer@sha256:f717d0e13e256a8d58111bcea160f8391cead842258f9901c5be1c83b10f010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46471975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f32646efae93bd93438be0df122b8064c41e1bde36cee050a170038031f645e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:23:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:23:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:23:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:23:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:23:47 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:23:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:23:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:27:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:27:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:27:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:27:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:27:04 GMT
CMD ["php" "-a"]
# Thu, 15 Jan 2026 23:18:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 15 Jan 2026 23:18:37 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:18:37 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 15 Jan 2026 23:18:37 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:19:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 15 Jan 2026 23:19:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 15 Jan 2026 23:19:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 15 Jan 2026 23:19:09 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:19:09 GMT
USER adminer
# Thu, 15 Jan 2026 23:19:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 15 Jan 2026 23:19:09 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a4fb0389c86752f9c5dd3dc0599ebd2efeb2a28e616eabcdd0a5c81a07b87`  
		Last Modified: Thu, 15 Jan 2026 22:27:11 GMT  
		Size: 3.6 MB (3628751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d50e40b4e738b735b610db4518dffed0d06293a1d78f8506430699a6515607`  
		Last Modified: Thu, 15 Jan 2026 22:27:11 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bab2a432cc9adf5f12d424649e6eb851dc458959a4da202d2028b98e607f13`  
		Last Modified: Thu, 15 Jan 2026 22:27:20 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e63afb635e678d309d6a2051d66f37ff58468b0cbba33a41b647ffbc24d8db`  
		Last Modified: Thu, 15 Jan 2026 22:27:21 GMT  
		Size: 13.7 MB (13694299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d68cc7e3dd73c35a7ae030edfa5094d80ad73d46f0095d740519cb80ffac91`  
		Last Modified: Thu, 15 Jan 2026 22:27:12 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bfd3a920b44bb70027c637c73988afb141e948e3d3a4d8aa32781ca942eb40`  
		Last Modified: Thu, 15 Jan 2026 22:27:13 GMT  
		Size: 20.6 MB (20566462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492aa3e0d555d7a5a83eb4c6e4dd9ffe343b031b696618fc41d1b730e9106706`  
		Last Modified: Thu, 15 Jan 2026 22:27:13 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74181da78bb7f0b084ceb7f601bbdc62ed98cef46bc2bac49a5fa01741a88f`  
		Last Modified: Thu, 15 Jan 2026 22:27:13 GMT  
		Size: 23.5 KB (23508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79966ceb08f89a6a3ba655cc569fd6ff4e8362851398ecbd432b7e7ecca360e`  
		Last Modified: Thu, 15 Jan 2026 22:27:13 GMT  
		Size: 23.5 KB (23527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fd46f43c84e6368b7e5c6d3a49a59b633bdb390efaa06b64d6e6f10a6d139b`  
		Last Modified: Thu, 15 Jan 2026 23:19:20 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe00327e0e5f433a01a918f3e520d5313f4e838ff3a5d377408a019ebc279a4`  
		Last Modified: Thu, 15 Jan 2026 23:19:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cba4a3f84f09c6e4fa8001855fad5abf152cc3adc715a06fbd1f5a1f414e45`  
		Last Modified: Thu, 15 Jan 2026 23:19:24 GMT  
		Size: 4.2 MB (4200807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2997043fafc65771a4732217318c25bd251477b38e177b677f847ae9fa7476b0`  
		Last Modified: Thu, 15 Jan 2026 23:19:14 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c4d0e806de3757eb80a9c92e20eba7fadec0c6afe6f0d49d12cfda45c41298`  
		Last Modified: Thu, 15 Jan 2026 23:19:21 GMT  
		Size: 640.9 KB (640864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34a6c44e09376acfbcd7c79457f33031870004b778a18fad4aff56826af534e`  
		Last Modified: Thu, 15 Jan 2026 23:19:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:2de20c1762baff3f02bfe9f98b9025de5d674553d40ba21de55ad61f7e71b87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d810af5d68ecc780d9d1983949c4e765909c34d63b6d3afe5d5c97f548ed765`

```dockerfile
```

-	Layers:
	-	`sha256:0f5061ea18ca8435b7287c2123ba2810029331d58273510eec7febbb8b9a57b8`  
		Last Modified: Fri, 16 Jan 2026 01:51:03 GMT  
		Size: 35.8 KB (35786 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:c81387b0e9eab3789123f37213833ddc9f7fc1e5b6e0179608947957558e6ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47425334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860db4e2a35874c2c4a4920038a74e07981427aa5477ddc4a3e45defd01d4b1`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Sat, 03 Jan 2026 02:13:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 03 Jan 2026 02:13:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 03 Jan 2026 02:13:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 03 Jan 2026 02:13:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.4.17
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 00:12:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 00:12:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:15:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 00:15:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:15:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 00:15:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 00:15:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 00:15:49 GMT
CMD ["php" "-a"]
# Fri, 16 Jan 2026 04:07:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 16 Jan 2026 04:07:45 GMT
STOPSIGNAL SIGINT
# Fri, 16 Jan 2026 04:07:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 16 Jan 2026 04:07:46 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 04:08:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 04:08:48 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 16 Jan 2026 04:08:48 GMT
ENV ADMINER_VERSION=5.4.1
# Fri, 16 Jan 2026 04:08:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Fri, 16 Jan 2026 04:08:48 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Fri, 16 Jan 2026 04:08:51 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 16 Jan 2026 04:08:51 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 04:08:51 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 16 Jan 2026 04:08:51 GMT
USER adminer
# Fri, 16 Jan 2026 04:08:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 16 Jan 2026 04:08:51 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f2b3f69e5b5cc8308fa39069e1dc5b69d344006bb70780e36be0078b758f1`  
		Last Modified: Fri, 16 Jan 2026 00:16:13 GMT  
		Size: 13.7 MB (13694341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57646fbf28999a726342d7622036b3cfe4859a4aacc500fbceae9cb0b7edda7`  
		Last Modified: Fri, 16 Jan 2026 00:16:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e401225e56ef47f6b6348f2938628870f519c42d03cad862795af7658af611f`  
		Last Modified: Fri, 16 Jan 2026 00:16:22 GMT  
		Size: 21.2 MB (21161667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7616896f2d4a667d0f982483cd52881c6a78a01616dfb4e35eff21168ae4d79`  
		Last Modified: Fri, 16 Jan 2026 00:16:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe593842ea700d4f9b90622f576b2d02b51f5f5a37b06bbc37c680ce07fe5f93`  
		Last Modified: Fri, 16 Jan 2026 00:16:20 GMT  
		Size: 23.3 KB (23348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c2db60c28c69eb3f8437895e070eeab31888a40cb4e4a1050e928c1a985234`  
		Last Modified: Fri, 16 Jan 2026 00:16:22 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce0906c63fe75125e54eabce0dbb1798747f6d77899d728d5f55109d3a79397`  
		Last Modified: Fri, 16 Jan 2026 04:09:05 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28262ef0db10b3bc43162f6321f32a7a24408eb381e0ed66383273bb93618cd1`  
		Last Modified: Fri, 16 Jan 2026 04:09:11 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b3c94481c84ee57d6208e13a224f0c44a348a1fb3e36e85aa697ac3681a08`  
		Last Modified: Fri, 16 Jan 2026 04:09:11 GMT  
		Size: 4.3 MB (4277453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd4b259d122fa391e090f96babab9a48576873303824fc639d89b5e14c3086f`  
		Last Modified: Fri, 16 Jan 2026 04:09:11 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a0db65b31ad3a8947d420d2fe90092fbf99a472b3551b0c2f5695b357cdc57`  
		Last Modified: Fri, 16 Jan 2026 04:09:06 GMT  
		Size: 640.9 KB (640867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f1e40532f7442ce420d7654e96fe8772bf3aea5123320a503d3b6b9dbe1a6`  
		Last Modified: Fri, 16 Jan 2026 04:09:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:2495e4640bce56d5b7247614a170c4643574411b47800f7cdfbe226ab6a183a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc159761984eb7930e712e937ec1220b4f2d11eb1978cd4584bd71a72c5297a7`

```dockerfile
```

-	Layers:
	-	`sha256:34cf142963fd38e141b65b5aaee4ed6bd4bf108121506a2617677dcdd4f24946`  
		Last Modified: Fri, 16 Jan 2026 07:48:59 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; riscv64

```console
$ docker pull adminer@sha256:8548cae56e4c196ecff71215ef877b5b25d758986f3e05aaa3694d843be4788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45227307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe441104b62b61ab0559cec6571a3b30e9b9ea03289e9bef51221fe9f4c84266`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 07:08:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 07:08:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 07:08:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Sun, 18 Jan 2026 04:44:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sun, 18 Jan 2026 04:44:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 05:40:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 18 Jan 2026 05:40:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 05:40:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 18 Jan 2026 05:40:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 18 Jan 2026 05:40:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 18 Jan 2026 05:40:49 GMT
CMD ["php" "-a"]
# Mon, 19 Jan 2026 16:43:37 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 19 Jan 2026 16:43:38 GMT
STOPSIGNAL SIGINT
# Mon, 19 Jan 2026 16:43:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Mon, 19 Jan 2026 16:43:38 GMT
WORKDIR /var/www/html
# Mon, 19 Jan 2026 16:49:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Mon, 19 Jan 2026 16:49:14 GMT
COPY *.php /var/www/html/ # buildkit
# Mon, 19 Jan 2026 16:49:14 GMT
ENV ADMINER_VERSION=5.4.1
# Mon, 19 Jan 2026 16:49:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Mon, 19 Jan 2026 16:49:14 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Mon, 19 Jan 2026 16:49:16 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Mon, 19 Jan 2026 16:49:16 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Jan 2026 16:49:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 19 Jan 2026 16:49:16 GMT
USER adminer
# Mon, 19 Jan 2026 16:49:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 19 Jan 2026 16:49:16 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf0b22e7f711d7a73eeeca6cf324b7c89075066b43de770508d227e2a46509`  
		Last Modified: Sun, 18 Jan 2026 05:41:51 GMT  
		Size: 13.7 MB (13694324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b1a5f09a97344003260afa6b2f030a26eaf82ef2283415da091a63a24ea1f`  
		Last Modified: Sun, 18 Jan 2026 06:09:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c5290fb334cf407fdd774b366fda6d3c8ad24516ac763c185acca385ffa186`  
		Last Modified: Sun, 18 Jan 2026 05:42:05 GMT  
		Size: 19.6 MB (19576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e1ab9b8108de32471554327efd8fffb4e89f59399cc64394375e5daa508205`  
		Last Modified: Sun, 18 Jan 2026 05:41:59 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494dff6ce48ef87d51d73de76f5b252f72f987aa8b96333a68a4e2bf7fc5cf4d`  
		Last Modified: Sun, 18 Jan 2026 05:41:59 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94c5636c5dfe802ab21b1d75938e9dfe0831a20e7138943cc1c89cfc76f3b5`  
		Last Modified: Sun, 18 Jan 2026 05:41:59 GMT  
		Size: 23.4 KB (23392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a6d7f87d218585b9e358e9eebb972c597e4a870bb9abc15cc9bb6e483c0e1`  
		Last Modified: Mon, 19 Jan 2026 16:49:49 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e850754c95772b357acf5777289609835d2404ec0a5511dff78a8d73dc09262`  
		Last Modified: Mon, 19 Jan 2026 16:49:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4027afe96beddeb804f3b04cea65afcd46c10da25daefebea0821185f37cf37d`  
		Last Modified: Mon, 19 Jan 2026 17:17:10 GMT  
		Size: 3.9 MB (3936835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acffd2e0bfcfa8c39db4a9ab347259edabe0dfc574517da1fa0fb78d5293061`  
		Last Modified: Mon, 19 Jan 2026 16:49:34 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3bd26b6f544c96b5d5020e1d76eae566dbb95635766729440eae9d78f8da54`  
		Last Modified: Mon, 19 Jan 2026 16:49:50 GMT  
		Size: 640.9 KB (640877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625da6e8fec7d6b48b729a422779edda2e0fae3d2e957446b34ccdf31556b00`  
		Last Modified: Mon, 19 Jan 2026 16:49:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:6a69705d1f3e98ed5348653dc87c7fcdd22b018c19bf3b7d6a370572852f5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ed0cc256368e32a2ed84bc277d679a3b1fdf0720edf13cc3d1e5ff1bfd048c`

```dockerfile
```

-	Layers:
	-	`sha256:8a592c500bb0214a6ef0c8d7d617fe2911792811b28ebeb8e3eab1f1c9ddc235`  
		Last Modified: Mon, 19 Jan 2026 19:49:00 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:4859a996a8a83fc6a8df39f6d9291a2f94f63e79e0fffce47cf4c6c50c0286e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46076036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd45755ce275296cdf4780ecac7d4dc044abcb66f03078aad4390e4765f98b5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:30:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:30:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:30:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:38:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:38:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:42:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:42:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:42:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:42:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:42:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:42:31 GMT
CMD ["php" "-a"]
# Thu, 15 Jan 2026 23:31:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 15 Jan 2026 23:31:25 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jan 2026 23:31:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 15 Jan 2026 23:31:25 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:31:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:31:59 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 15 Jan 2026 23:31:59 GMT
ENV ADMINER_VERSION=5.4.1
# Thu, 15 Jan 2026 23:31:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=3f65364b4cc96b5e4cae1b3e448b7b6fa42b0da1eeba78bed9b3774ade830fce
# Thu, 15 Jan 2026 23:31:59 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=fd96585b1f8728b729551c5a7de3371724c1ccd701afde4c75fd6b990d935a63
# Thu, 15 Jan 2026 23:31:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 15 Jan 2026 23:31:59 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:31:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:31:59 GMT
USER adminer
# Thu, 15 Jan 2026 23:31:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 15 Jan 2026 23:31:59 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af672712b2dab3c8a68ddbd40990098668c349a31bf4fe54360519012d2e9`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 3.8 MB (3794529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82f0b184abfa92d79d92b03514acd8b9f92c2ca083f9fa2e62587fde8871a2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b827f069b40835efda3a88ba34853291bec4baedd59564b9d33abc39667950f2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9915ee6e7bc986c6bc00ae2c7377c4d1c1da6dbf61e114f2c04afb7dc64a0bce`  
		Last Modified: Thu, 15 Jan 2026 22:42:52 GMT  
		Size: 13.7 MB (13694323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f9ccec429d4e1a40b769a08c6f8d17f5bff7a5d62fd841f4289153c436a1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7619846063cec831d03d7182ea2db9768d8c7ed2767ed1cac73c159318bde9`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 20.0 MB (20014646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b094bd982076ab0cc805135f0b5d8a9621fe2b37ffd1f661a4743135cbf8ded5`  
		Last Modified: Thu, 15 Jan 2026 22:42:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36a0675563aa0f05d105adf073dc34de4a4dfa88ddf1eba632f892320fee799`  
		Last Modified: Thu, 15 Jan 2026 22:42:50 GMT  
		Size: 23.3 KB (23343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7c1638c810d6f0ff6d37516940c251dda92793ca5d0dc41a2a83451ccb5742`  
		Last Modified: Thu, 15 Jan 2026 22:42:50 GMT  
		Size: 23.4 KB (23360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8c0fccb497b234e5e8ebd48581a6b6dde174c14fac2af7e09d6ba1e3a1bf9`  
		Last Modified: Thu, 15 Jan 2026 23:32:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98763db8894c1900e0024707efd1a1671491de61ca193471e11d369abe7fd32`  
		Last Modified: Thu, 15 Jan 2026 23:32:06 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01942ff1f9bc3e4b7aedac39e3c5a7d2b13643dec258fe97d9fbf6792f812529`  
		Last Modified: Thu, 15 Jan 2026 23:32:13 GMT  
		Size: 4.2 MB (4152979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d9db3948d01447a54f0c5f273603f410384c289c3e16b54a5aeafa09bacdd9`  
		Last Modified: Thu, 15 Jan 2026 23:32:06 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363fb59c186e4a5c4f24782b7a2f9917c9e935cf0b5741101eed45808a162f0f`  
		Last Modified: Thu, 15 Jan 2026 23:32:12 GMT  
		Size: 640.9 KB (640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbd5b50d4c80e563df35930aaa1be3f361b89341ac7f841dcfb4b8bd2717e2`  
		Last Modified: Thu, 15 Jan 2026 23:32:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-standalone` - unknown; unknown

```console
$ docker pull adminer@sha256:e7883c793e3ad74df3221c2cdaa8c5b73d6548e9ce0e6f566c8a2411cc041a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d8961baffb94e1adc3667f08f9f0e099626deef5cbb373063f92d05abf43f9`

```dockerfile
```

-	Layers:
	-	`sha256:1f09a2bd901f8a4a8036dc2bee37d3a8166e5c45e566967e60fcde09abafc6dd`  
		Last Modified: Thu, 15 Jan 2026 23:32:06 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json
