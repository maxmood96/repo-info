<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:4.8.1`](#adminer481)
-	[`adminer:4.8.1-fastcgi`](#adminer481-fastcgi)
-	[`adminer:4.8.1-standalone`](#adminer481-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:44223459a83fa100244ee5df586dbb380a94e13a9f018b99ef2877588c98cbe9
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:1348e94a278d265bcb4d717ac5ac7ea7fd2ca9dc14967c71491feedfda23c36f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34075237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbbb12f9a2e8a26e39699e7edbb039a063b6ef32b72bcb0c89e78e49488a79a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:05:11 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:05:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:05:14 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:05:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:05:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:05:16 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:05:17 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:52:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:53:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:53:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:53:24 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:53:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:53:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:53:24 GMT
USER adminer
# Fri, 22 Oct 2021 20:53:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e6be5f41de4dbf371cd6d25b5eb2cc1bcb7fac7671657833ca3634b19b0ee`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 14.6 MB (14604129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023e00679679013c1f113a6b80221fa81880b30d0125d3d3dcbe42a3510436a`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dd709f25a8120f332c10f2e38c685e390b1c82fcb68db5e7d0ac7beeef2c6f`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc24f0835cbdf6caf1fe898acd40c6c937880eecd0c787f787476da642c7f0d`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13696630b938326548e6ab57aee43d65c3e069ca106f38bb47de2e4f6e6d2d14`  
		Last Modified: Fri, 22 Oct 2021 20:54:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e0c411da46fddb345a2710ca032ace022b878d3bafc888a26f145946ec477`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981bb18c0515dfb2ce7580dd6ec7d1b9d149406feee30f98d458847f889858d`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 3.9 MB (3935527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9384a4df3d649e25099155d68572306897e863f7f6a9dbe2d50bfa74236c423d`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.5 KB (1495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfd6b73bf11629f40a226c7b021a51cfc0ac0d5d08d92638f08abd41301526f`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b95692e7e9c0c0b410e5f2df11ac402a389f724d47d798fae7de7a8ceccb5`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:52611c94996c3ec9ea2d7e602676118245ab0d14a6a12246ac32ecaed9064235
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27aaf4da700ff3c92779492b3eac2261bc18a8de62153aaf25fe80ee0da1e7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:18:25 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:18:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:18:29 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:18:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:18:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:18:31 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:18:32 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:26:06 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:26:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:27:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:27:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:27:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:27:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:27:29 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:27:30 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:27:30 GMT
USER adminer
# Fri, 22 Oct 2021 20:27:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657101197214564907b646a622ac6e10649f51041672ca2580eb668b847a7e`  
		Last Modified: Fri, 22 Oct 2021 18:50:20 GMT  
		Size: 13.6 MB (13593293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037c997ab205672e514031f727e28951c875f3ff94e25d10bc2d603db933ac8`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274889cd0cf6fd860ae79d32fb6e417a36ab25658f7fe007ccd277d21e50ce59`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 17.9 KB (17857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8503d6f58906910f1497a3a58c05ebc0b935c61eaf74b5f7d5d8296e930cedba`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a4ea939f355ddf0c2ba9c67dd86e9df078f16735fe1a7b60a8c46c2517495`  
		Last Modified: Fri, 22 Oct 2021 20:29:05 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9493ecd4e90536eae2e5eae2b09c81abf48d001d01053402c2c50154b4772`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c65248c28572e7c40a11a88a3993ee4b2128cfff35319124804db21c32198`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 3.6 MB (3608955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7e32d2c8347ff2ab7834c3c88914566f6bda243c4ad53641c2ff9ffe41f75`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813ae56a3f2f7b1086b7ff18584058b9b55adc8433a617e9deb1a16632d41d0a`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a095fd91f2150f0c50dff543975d8a4964c9160be1d06bf04bdfc2742450fd`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:d5adf6f661f20cfdd68ab37856335dbc069358d38ae0cb40173573c4f7662549
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab8d3537be1365781c30bca04319b8ea4ed47309c9c660fb6987441db7c95e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:41:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:41:59 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:42:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:42:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:42:03 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:42:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:42:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:42:06 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:42:07 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 03:53:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:53:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:54:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:54:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:54:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:54:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:54:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:54:39 GMT
USER adminer
# Sat, 23 Oct 2021 03:54:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d412c8b2dc6777f38353656dbc25132e5d4f60c957b950085dbe21e7bf6cc2cd`  
		Last Modified: Fri, 22 Oct 2021 20:32:13 GMT  
		Size: 12.7 MB (12713721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d05006ce64ec311fb3a8bf17e2ab0eeb95aeda0a0aebea4c03efac0454e3ecb`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd7f70c8efd9c72fc0651646f79dda8143b38750859ea69fea467e280889352`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a440b734b4474ba93058b372e01f84d0c053d53b4b0b88b7e5052bc69d2b2008`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399bb839dc4653fd73e402066f15de90952fe9fd9cfcce9c2abfcbf58de1c706`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1035acb7231671a349c19e7383691f8a539f413c4bef1cfa6bf58819f7a7d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ff1d90d2b0aedd530717a1a924f1839f3b686abfdaec7ba79eecc37e24d731`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 3.6 MB (3636928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314c2f4e7a96d1fa28c181bc2abb8af8b9d1b24ecc2d2e3f8cdfbaf30fbcdc1d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d46e8c9340c1942568a5efe2c186b6a4148720d9d1695acafbae72c519168`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c47b6a76d92eef5e21cecd7218541812c0f6c50fb97bc880f1e5472e7680d0e`  
		Last Modified: Sat, 23 Oct 2021 03:56:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b7701defeeca979938d1012508d25a9245c83beab732fe9732c41b8f7390cac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33491391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf69e593406793593962edb9d6c893735a33dcdde485a2afc51271a3688ad24`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:38:32 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:38:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:38:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:38:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:38:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:38:37 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:38:38 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:14:09 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:14:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:14:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:14:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:14:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:14:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:14:41 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:14:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:14:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:14:44 GMT
USER adminer
# Fri, 22 Oct 2021 20:14:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2310c5955764587eea0344f2011a760090a61e303962c54015f7029a93a00bb`  
		Last Modified: Fri, 22 Oct 2021 19:07:36 GMT  
		Size: 14.1 MB (14139955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507d1fc4a3d0a95a9027823bf98e6b13f1c800dcc4b2bbbfeac0d4668edc6ca7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23212800bd91286e59b200aa4479d2ba1dd3656c243aa1336a4f329870821a7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a981f17064af438d696fbf9ffc4d6275fd3fa48d9ae20bd0251cae4f8c7761`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee526188d9e1d4a2ad946644a7fc02fbe591873868f178039bad6c5c5de4eadc`  
		Last Modified: Fri, 22 Oct 2021 20:15:40 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f4275870d1cabcadd6a4b172f9fb5d85d67d735366f87955b29d7d478dbf5`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fc584c57c7e855c919ec77c203d0493a983366b2544d13bc210339f3f825b`  
		Last Modified: Fri, 22 Oct 2021 20:15:39 GMT  
		Size: 3.9 MB (3914687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6da532dae9d098052b14e049a882318ccedddd9624163c3a08bc8e6e7ab967`  
		Last Modified: Fri, 22 Oct 2021 20:15:37 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bb3f6bb58ea29a33104479c8795d79e94c6b3476d06c6738f1bd24fa520260`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65eee94a65d49e6ab6bdc22f1151b6aecf7660077ee4224010fb405b8e092e8d`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:d428625712e5f06fb4fafc3faaa7547197e99ef8805517c1a8b0c730bc8d71e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34693983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd11b365ac243ea9efb2e65cf9059b415a0e3b5faeb847240aacd28835d5aad`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:50:33 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:50:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:50:35 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:50:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:50:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:50:36 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:50:37 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 22:08:15 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:08:16 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:08:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:44 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:47 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:47 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bebea86fb8ce75c5427b40dc21fb5c61fd931413f2e98cce8c01a2a4610c74`  
		Last Modified: Fri, 22 Oct 2021 19:34:42 GMT  
		Size: 15.0 MB (15012615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11553391b492d22d8e79f77f0b4b2287e6ab2be30353871a29cd265d8999debc`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fda734499907771c3b18cb7ef49e6ea84f50643a2afacfa2deace9a4786248`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c705abb14c392c6f653d6d6079e0d66c073b319237587e4aebf40398127c2fd6`  
		Last Modified: Fri, 22 Oct 2021 19:34:39 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15af60d0e33847ebc7f2e0f82b9d5819ba13d78e46a2e94f50238fe64d0a3540`  
		Last Modified: Fri, 22 Oct 2021 22:09:48 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146a3cee0d08957416cb1026e70dfce33fc4c4de10cfed398f9add920da7110`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636aced19b75eca8177a005e2a9e0004adfe2f20a7c3d1f565e227e23eca334d`  
		Last Modified: Fri, 22 Oct 2021 22:09:46 GMT  
		Size: 4.0 MB (4039879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391c501c22c2caa53728ea9aa40a965210332a54f16b171a89ceaaeeb169a42b`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc721c47dff61ff3f0f3a539c7165573236a2e2be73de3fdd2c0b1dc3864e81d`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a4e53e806e259eae0a78fcfa89386f6c7d4774c2b3a527f8cb52bdbd59b430`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0071c622ac9800567b40452f3328bb29ff661055845731f3ccc575cc8adc33e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35155307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bac9fa27a783cc575926729bc65c8c2f98792bd4ec36d0be41080f51832f9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:03:10 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:03:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:03:25 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:03:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:03:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:03:35 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:03:37 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 05:15:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:15:10 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:16:03 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:16:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:16:11 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:16:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:16:15 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:16:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:16:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:16:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:16:33 GMT
USER adminer
# Sat, 23 Oct 2021 05:16:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4685c811f33ed6a084c0335b35a4bb4f86c09f55d43d828b94fb1355bb4979bb`  
		Last Modified: Fri, 22 Oct 2021 19:41:43 GMT  
		Size: 15.7 MB (15650843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff229e804c40dc864e212cd1b211840852b2b566cf7414c3f9aea2ff6848575`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bab88fb83f0cac5144755973465d02dd08aba6c0e054776b9b54a3a057282`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 17.8 KB (17843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263011277087f38f40f5f3a182d2892961e6d16a431d8909a50ad4df148d03dc`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e625f0e7149557feca2afaee38cc9aa3fa1829cf0581b8d6782137dd60d899`  
		Last Modified: Sat, 23 Oct 2021 05:17:49 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c69024619d5feb3603316cb9d7c6b28d67eb86bb4e6fb745879595bddfdbab`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29314335b7d8819243f01078ce5ced889058598deb294864b441df7b7eaf8d32`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 3.9 MB (3925176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a11d52cc941dabf83fc9c201b4d3ecfa2103ca40efb538ee548173df33f441`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae20c8cc8f338f0df22e9d140911920e41bde3b9469926b93a83215c1c8d5f`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90687aab1c7b9d0b3e571bd2fc97d559c85204672d0d2ba6ab983197b1d65f74`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:e8015bc81e841059431b6afe424a268a5f73188fceb3990342d03780d9c65ced
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32690951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef94949f1444e29a7dd4485a7548d2a2c22fbd72da3e97ac1cb16337731ca3`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:31:07 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:31:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:31:08 GMT
WORKDIR /var/www/html
# Fri, 12 Nov 2021 20:31:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Nov 2021 20:31:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Nov 2021 20:31:08 GMT
EXPOSE 9000
# Fri, 12 Nov 2021 20:31:09 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 07:10:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:11:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:11:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:11:13 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:11:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:11:14 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:11:14 GMT
USER adminer
# Sat, 13 Nov 2021 07:11:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d00c1ebd44b22107d0c321652526bf51f244840bc1d25a14d78ff52be2a58c1`  
		Last Modified: Fri, 12 Nov 2021 21:15:21 GMT  
		Size: 13.7 MB (13724037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14968d8f20b6b9053ad15a20303bc4a52bf5faea36abd5156f235d019c3a6e7e`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ddd05c94152081a83ab559f3b7caba2db8b50457ef8c850c3eca9f2bbb20f`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 18.2 KB (18206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5ef1c2bebe8cf5de59792c389469c6ec8c6bd3efe53130b99cfae8f9a792d1`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f787c08eb48752ddd9be25b7e866a95ccb1ab8501b82bd7ddc73e2a2a5b1f`  
		Last Modified: Sat, 13 Nov 2021 07:11:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d784ad0e5cf1913192c74ad778f6417af33d6ffcc7b5194df758f38827333458`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0d077df8c500630ade2de720f71bf41fe797221644c8943670fe0f4548f754`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 3.6 MB (3569571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a844cb0fd32a15f101c13967d649dafd2845e2a8c2c0bb7888d1db24563f1a7`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657f22461eca7bb90a6bf2ee05df2d2a688abbed73d04b8e97901a1961f669`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3cb427d3332664e87af0a4d0a3227707a4985969f2114864c9f3732adfb58`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:4.8.1` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:44223459a83fa100244ee5df586dbb380a94e13a9f018b99ef2877588c98cbe9
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

### `adminer:4.8.1-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:1348e94a278d265bcb4d717ac5ac7ea7fd2ca9dc14967c71491feedfda23c36f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34075237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbbb12f9a2e8a26e39699e7edbb039a063b6ef32b72bcb0c89e78e49488a79a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:05:11 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:05:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:05:14 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:05:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:05:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:05:16 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:05:17 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:52:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:53:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:53:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:53:24 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:53:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:53:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:53:24 GMT
USER adminer
# Fri, 22 Oct 2021 20:53:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e6be5f41de4dbf371cd6d25b5eb2cc1bcb7fac7671657833ca3634b19b0ee`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 14.6 MB (14604129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023e00679679013c1f113a6b80221fa81880b30d0125d3d3dcbe42a3510436a`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dd709f25a8120f332c10f2e38c685e390b1c82fcb68db5e7d0ac7beeef2c6f`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc24f0835cbdf6caf1fe898acd40c6c937880eecd0c787f787476da642c7f0d`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13696630b938326548e6ab57aee43d65c3e069ca106f38bb47de2e4f6e6d2d14`  
		Last Modified: Fri, 22 Oct 2021 20:54:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e0c411da46fddb345a2710ca032ace022b878d3bafc888a26f145946ec477`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981bb18c0515dfb2ce7580dd6ec7d1b9d149406feee30f98d458847f889858d`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 3.9 MB (3935527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9384a4df3d649e25099155d68572306897e863f7f6a9dbe2d50bfa74236c423d`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.5 KB (1495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfd6b73bf11629f40a226c7b021a51cfc0ac0d5d08d92638f08abd41301526f`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b95692e7e9c0c0b410e5f2df11ac402a389f724d47d798fae7de7a8ceccb5`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:52611c94996c3ec9ea2d7e602676118245ab0d14a6a12246ac32ecaed9064235
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27aaf4da700ff3c92779492b3eac2261bc18a8de62153aaf25fe80ee0da1e7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:18:25 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:18:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:18:29 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:18:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:18:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:18:31 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:18:32 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:26:06 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:26:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:27:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:27:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:27:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:27:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:27:29 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:27:30 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:27:30 GMT
USER adminer
# Fri, 22 Oct 2021 20:27:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657101197214564907b646a622ac6e10649f51041672ca2580eb668b847a7e`  
		Last Modified: Fri, 22 Oct 2021 18:50:20 GMT  
		Size: 13.6 MB (13593293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037c997ab205672e514031f727e28951c875f3ff94e25d10bc2d603db933ac8`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274889cd0cf6fd860ae79d32fb6e417a36ab25658f7fe007ccd277d21e50ce59`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 17.9 KB (17857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8503d6f58906910f1497a3a58c05ebc0b935c61eaf74b5f7d5d8296e930cedba`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a4ea939f355ddf0c2ba9c67dd86e9df078f16735fe1a7b60a8c46c2517495`  
		Last Modified: Fri, 22 Oct 2021 20:29:05 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9493ecd4e90536eae2e5eae2b09c81abf48d001d01053402c2c50154b4772`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c65248c28572e7c40a11a88a3993ee4b2128cfff35319124804db21c32198`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 3.6 MB (3608955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7e32d2c8347ff2ab7834c3c88914566f6bda243c4ad53641c2ff9ffe41f75`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813ae56a3f2f7b1086b7ff18584058b9b55adc8433a617e9deb1a16632d41d0a`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a095fd91f2150f0c50dff543975d8a4964c9160be1d06bf04bdfc2742450fd`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:d5adf6f661f20cfdd68ab37856335dbc069358d38ae0cb40173573c4f7662549
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab8d3537be1365781c30bca04319b8ea4ed47309c9c660fb6987441db7c95e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:41:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:41:59 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:42:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:42:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:42:03 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:42:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:42:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:42:06 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:42:07 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 03:53:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:53:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:54:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:54:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:54:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:54:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:54:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:54:39 GMT
USER adminer
# Sat, 23 Oct 2021 03:54:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d412c8b2dc6777f38353656dbc25132e5d4f60c957b950085dbe21e7bf6cc2cd`  
		Last Modified: Fri, 22 Oct 2021 20:32:13 GMT  
		Size: 12.7 MB (12713721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d05006ce64ec311fb3a8bf17e2ab0eeb95aeda0a0aebea4c03efac0454e3ecb`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd7f70c8efd9c72fc0651646f79dda8143b38750859ea69fea467e280889352`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a440b734b4474ba93058b372e01f84d0c053d53b4b0b88b7e5052bc69d2b2008`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399bb839dc4653fd73e402066f15de90952fe9fd9cfcce9c2abfcbf58de1c706`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1035acb7231671a349c19e7383691f8a539f413c4bef1cfa6bf58819f7a7d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ff1d90d2b0aedd530717a1a924f1839f3b686abfdaec7ba79eecc37e24d731`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 3.6 MB (3636928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314c2f4e7a96d1fa28c181bc2abb8af8b9d1b24ecc2d2e3f8cdfbaf30fbcdc1d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d46e8c9340c1942568a5efe2c186b6a4148720d9d1695acafbae72c519168`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c47b6a76d92eef5e21cecd7218541812c0f6c50fb97bc880f1e5472e7680d0e`  
		Last Modified: Sat, 23 Oct 2021 03:56:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b7701defeeca979938d1012508d25a9245c83beab732fe9732c41b8f7390cac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33491391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf69e593406793593962edb9d6c893735a33dcdde485a2afc51271a3688ad24`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:38:32 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:38:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:38:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:38:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:38:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:38:37 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:38:38 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:14:09 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:14:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:14:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:14:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:14:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:14:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:14:41 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:14:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:14:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:14:44 GMT
USER adminer
# Fri, 22 Oct 2021 20:14:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2310c5955764587eea0344f2011a760090a61e303962c54015f7029a93a00bb`  
		Last Modified: Fri, 22 Oct 2021 19:07:36 GMT  
		Size: 14.1 MB (14139955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507d1fc4a3d0a95a9027823bf98e6b13f1c800dcc4b2bbbfeac0d4668edc6ca7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23212800bd91286e59b200aa4479d2ba1dd3656c243aa1336a4f329870821a7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a981f17064af438d696fbf9ffc4d6275fd3fa48d9ae20bd0251cae4f8c7761`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee526188d9e1d4a2ad946644a7fc02fbe591873868f178039bad6c5c5de4eadc`  
		Last Modified: Fri, 22 Oct 2021 20:15:40 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f4275870d1cabcadd6a4b172f9fb5d85d67d735366f87955b29d7d478dbf5`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fc584c57c7e855c919ec77c203d0493a983366b2544d13bc210339f3f825b`  
		Last Modified: Fri, 22 Oct 2021 20:15:39 GMT  
		Size: 3.9 MB (3914687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6da532dae9d098052b14e049a882318ccedddd9624163c3a08bc8e6e7ab967`  
		Last Modified: Fri, 22 Oct 2021 20:15:37 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bb3f6bb58ea29a33104479c8795d79e94c6b3476d06c6738f1bd24fa520260`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65eee94a65d49e6ab6bdc22f1151b6aecf7660077ee4224010fb405b8e092e8d`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:d428625712e5f06fb4fafc3faaa7547197e99ef8805517c1a8b0c730bc8d71e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34693983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd11b365ac243ea9efb2e65cf9059b415a0e3b5faeb847240aacd28835d5aad`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:50:33 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:50:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:50:35 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:50:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:50:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:50:36 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:50:37 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 22:08:15 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:08:16 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:08:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:44 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:47 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:47 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bebea86fb8ce75c5427b40dc21fb5c61fd931413f2e98cce8c01a2a4610c74`  
		Last Modified: Fri, 22 Oct 2021 19:34:42 GMT  
		Size: 15.0 MB (15012615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11553391b492d22d8e79f77f0b4b2287e6ab2be30353871a29cd265d8999debc`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fda734499907771c3b18cb7ef49e6ea84f50643a2afacfa2deace9a4786248`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c705abb14c392c6f653d6d6079e0d66c073b319237587e4aebf40398127c2fd6`  
		Last Modified: Fri, 22 Oct 2021 19:34:39 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15af60d0e33847ebc7f2e0f82b9d5819ba13d78e46a2e94f50238fe64d0a3540`  
		Last Modified: Fri, 22 Oct 2021 22:09:48 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146a3cee0d08957416cb1026e70dfce33fc4c4de10cfed398f9add920da7110`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636aced19b75eca8177a005e2a9e0004adfe2f20a7c3d1f565e227e23eca334d`  
		Last Modified: Fri, 22 Oct 2021 22:09:46 GMT  
		Size: 4.0 MB (4039879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391c501c22c2caa53728ea9aa40a965210332a54f16b171a89ceaaeeb169a42b`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc721c47dff61ff3f0f3a539c7165573236a2e2be73de3fdd2c0b1dc3864e81d`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a4e53e806e259eae0a78fcfa89386f6c7d4774c2b3a527f8cb52bdbd59b430`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0071c622ac9800567b40452f3328bb29ff661055845731f3ccc575cc8adc33e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35155307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bac9fa27a783cc575926729bc65c8c2f98792bd4ec36d0be41080f51832f9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:03:10 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:03:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:03:25 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:03:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:03:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:03:35 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:03:37 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 05:15:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:15:10 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:16:03 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:16:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:16:11 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:16:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:16:15 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:16:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:16:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:16:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:16:33 GMT
USER adminer
# Sat, 23 Oct 2021 05:16:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4685c811f33ed6a084c0335b35a4bb4f86c09f55d43d828b94fb1355bb4979bb`  
		Last Modified: Fri, 22 Oct 2021 19:41:43 GMT  
		Size: 15.7 MB (15650843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff229e804c40dc864e212cd1b211840852b2b566cf7414c3f9aea2ff6848575`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bab88fb83f0cac5144755973465d02dd08aba6c0e054776b9b54a3a057282`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 17.8 KB (17843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263011277087f38f40f5f3a182d2892961e6d16a431d8909a50ad4df148d03dc`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e625f0e7149557feca2afaee38cc9aa3fa1829cf0581b8d6782137dd60d899`  
		Last Modified: Sat, 23 Oct 2021 05:17:49 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c69024619d5feb3603316cb9d7c6b28d67eb86bb4e6fb745879595bddfdbab`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29314335b7d8819243f01078ce5ced889058598deb294864b441df7b7eaf8d32`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 3.9 MB (3925176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a11d52cc941dabf83fc9c201b4d3ecfa2103ca40efb538ee548173df33f441`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae20c8cc8f338f0df22e9d140911920e41bde3b9469926b93a83215c1c8d5f`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90687aab1c7b9d0b3e571bd2fc97d559c85204672d0d2ba6ab983197b1d65f74`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:e8015bc81e841059431b6afe424a268a5f73188fceb3990342d03780d9c65ced
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32690951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef94949f1444e29a7dd4485a7548d2a2c22fbd72da3e97ac1cb16337731ca3`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:31:07 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:31:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:31:08 GMT
WORKDIR /var/www/html
# Fri, 12 Nov 2021 20:31:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Nov 2021 20:31:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Nov 2021 20:31:08 GMT
EXPOSE 9000
# Fri, 12 Nov 2021 20:31:09 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 07:10:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:11:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:11:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:11:13 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:11:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:11:14 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:11:14 GMT
USER adminer
# Sat, 13 Nov 2021 07:11:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d00c1ebd44b22107d0c321652526bf51f244840bc1d25a14d78ff52be2a58c1`  
		Last Modified: Fri, 12 Nov 2021 21:15:21 GMT  
		Size: 13.7 MB (13724037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14968d8f20b6b9053ad15a20303bc4a52bf5faea36abd5156f235d019c3a6e7e`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ddd05c94152081a83ab559f3b7caba2db8b50457ef8c850c3eca9f2bbb20f`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 18.2 KB (18206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5ef1c2bebe8cf5de59792c389469c6ec8c6bd3efe53130b99cfae8f9a792d1`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f787c08eb48752ddd9be25b7e866a95ccb1ab8501b82bd7ddc73e2a2a5b1f`  
		Last Modified: Sat, 13 Nov 2021 07:11:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d784ad0e5cf1913192c74ad778f6417af33d6ffcc7b5194df758f38827333458`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0d077df8c500630ade2de720f71bf41fe797221644c8943670fe0f4548f754`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 3.6 MB (3569571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a844cb0fd32a15f101c13967d649dafd2845e2a8c2c0bb7888d1db24563f1a7`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657f22461eca7bb90a6bf2ee05df2d2a688abbed73d04b8e97901a1961f669`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3cb427d3332664e87af0a4d0a3227707a4985969f2114864c9f3732adfb58`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:4.8.1-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:44223459a83fa100244ee5df586dbb380a94e13a9f018b99ef2877588c98cbe9
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

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:1348e94a278d265bcb4d717ac5ac7ea7fd2ca9dc14967c71491feedfda23c36f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34075237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbbb12f9a2e8a26e39699e7edbb039a063b6ef32b72bcb0c89e78e49488a79a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:05:11 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:05:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:05:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:05:14 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:05:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:05:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:05:16 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:05:17 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:52:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:53:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:53:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:53:22 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:53:24 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:53:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:53:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:53:24 GMT
USER adminer
# Fri, 22 Oct 2021 20:53:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e6be5f41de4dbf371cd6d25b5eb2cc1bcb7fac7671657833ca3634b19b0ee`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 14.6 MB (14604129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023e00679679013c1f113a6b80221fa81880b30d0125d3d3dcbe42a3510436a`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dd709f25a8120f332c10f2e38c685e390b1c82fcb68db5e7d0ac7beeef2c6f`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc24f0835cbdf6caf1fe898acd40c6c937880eecd0c787f787476da642c7f0d`  
		Last Modified: Fri, 22 Oct 2021 18:49:03 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13696630b938326548e6ab57aee43d65c3e069ca106f38bb47de2e4f6e6d2d14`  
		Last Modified: Fri, 22 Oct 2021 20:54:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e0c411da46fddb345a2710ca032ace022b878d3bafc888a26f145946ec477`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981bb18c0515dfb2ce7580dd6ec7d1b9d149406feee30f98d458847f889858d`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 3.9 MB (3935527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9384a4df3d649e25099155d68572306897e863f7f6a9dbe2d50bfa74236c423d`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 1.5 KB (1495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfd6b73bf11629f40a226c7b021a51cfc0ac0d5d08d92638f08abd41301526f`  
		Last Modified: Fri, 22 Oct 2021 20:54:11 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b95692e7e9c0c0b410e5f2df11ac402a389f724d47d798fae7de7a8ceccb5`  
		Last Modified: Fri, 22 Oct 2021 20:54:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:52611c94996c3ec9ea2d7e602676118245ab0d14a6a12246ac32ecaed9064235
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a27aaf4da700ff3c92779492b3eac2261bc18a8de62153aaf25fe80ee0da1e7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:18:25 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:18:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:18:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:18:29 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:18:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:18:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:18:31 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:18:32 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:26:06 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:26:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:27:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:27:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:27:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:27:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:27:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:27:29 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:27:30 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:27:30 GMT
USER adminer
# Fri, 22 Oct 2021 20:27:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657101197214564907b646a622ac6e10649f51041672ca2580eb668b847a7e`  
		Last Modified: Fri, 22 Oct 2021 18:50:20 GMT  
		Size: 13.6 MB (13593293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037c997ab205672e514031f727e28951c875f3ff94e25d10bc2d603db933ac8`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274889cd0cf6fd860ae79d32fb6e417a36ab25658f7fe007ccd277d21e50ce59`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 17.9 KB (17857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8503d6f58906910f1497a3a58c05ebc0b935c61eaf74b5f7d5d8296e930cedba`  
		Last Modified: Fri, 22 Oct 2021 18:50:10 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a4ea939f355ddf0c2ba9c67dd86e9df078f16735fe1a7b60a8c46c2517495`  
		Last Modified: Fri, 22 Oct 2021 20:29:05 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9493ecd4e90536eae2e5eae2b09c81abf48d001d01053402c2c50154b4772`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c65248c28572e7c40a11a88a3993ee4b2128cfff35319124804db21c32198`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 3.6 MB (3608955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7e32d2c8347ff2ab7834c3c88914566f6bda243c4ad53641c2ff9ffe41f75`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813ae56a3f2f7b1086b7ff18584058b9b55adc8433a617e9deb1a16632d41d0a`  
		Last Modified: Fri, 22 Oct 2021 20:29:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a095fd91f2150f0c50dff543975d8a4964c9160be1d06bf04bdfc2742450fd`  
		Last Modified: Fri, 22 Oct 2021 20:29:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:d5adf6f661f20cfdd68ab37856335dbc069358d38ae0cb40173573c4f7662549
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab8d3537be1365781c30bca04319b8ea4ed47309c9c660fb6987441db7c95e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:41:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:41:59 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:42:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:42:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:42:03 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:42:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:42:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:42:06 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:42:07 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 03:53:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:53:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:54:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:54:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:54:35 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:54:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:54:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:54:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:54:39 GMT
USER adminer
# Sat, 23 Oct 2021 03:54:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d412c8b2dc6777f38353656dbc25132e5d4f60c957b950085dbe21e7bf6cc2cd`  
		Last Modified: Fri, 22 Oct 2021 20:32:13 GMT  
		Size: 12.7 MB (12713721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d05006ce64ec311fb3a8bf17e2ab0eeb95aeda0a0aebea4c03efac0454e3ecb`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd7f70c8efd9c72fc0651646f79dda8143b38750859ea69fea467e280889352`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a440b734b4474ba93058b372e01f84d0c053d53b4b0b88b7e5052bc69d2b2008`  
		Last Modified: Fri, 22 Oct 2021 20:32:05 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399bb839dc4653fd73e402066f15de90952fe9fd9cfcce9c2abfcbf58de1c706`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1035acb7231671a349c19e7383691f8a539f413c4bef1cfa6bf58819f7a7d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ff1d90d2b0aedd530717a1a924f1839f3b686abfdaec7ba79eecc37e24d731`  
		Last Modified: Sat, 23 Oct 2021 03:56:05 GMT  
		Size: 3.6 MB (3636928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314c2f4e7a96d1fa28c181bc2abb8af8b9d1b24ecc2d2e3f8cdfbaf30fbcdc1d`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d46e8c9340c1942568a5efe2c186b6a4148720d9d1695acafbae72c519168`  
		Last Modified: Sat, 23 Oct 2021 03:56:04 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c47b6a76d92eef5e21cecd7218541812c0f6c50fb97bc880f1e5472e7680d0e`  
		Last Modified: Sat, 23 Oct 2021 03:56:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b7701defeeca979938d1012508d25a9245c83beab732fe9732c41b8f7390cac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33491391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf69e593406793593962edb9d6c893735a33dcdde485a2afc51271a3688ad24`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:38:32 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:38:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:38:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:38:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:38:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:38:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:38:37 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:38:38 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 20:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:14:09 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:14:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:14:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:14:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:14:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:14:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:14:41 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:14:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:14:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:14:44 GMT
USER adminer
# Fri, 22 Oct 2021 20:14:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2310c5955764587eea0344f2011a760090a61e303962c54015f7029a93a00bb`  
		Last Modified: Fri, 22 Oct 2021 19:07:36 GMT  
		Size: 14.1 MB (14139955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507d1fc4a3d0a95a9027823bf98e6b13f1c800dcc4b2bbbfeac0d4668edc6ca7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23212800bd91286e59b200aa4479d2ba1dd3656c243aa1336a4f329870821a7`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a981f17064af438d696fbf9ffc4d6275fd3fa48d9ae20bd0251cae4f8c7761`  
		Last Modified: Fri, 22 Oct 2021 19:07:33 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee526188d9e1d4a2ad946644a7fc02fbe591873868f178039bad6c5c5de4eadc`  
		Last Modified: Fri, 22 Oct 2021 20:15:40 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f4275870d1cabcadd6a4b172f9fb5d85d67d735366f87955b29d7d478dbf5`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fc584c57c7e855c919ec77c203d0493a983366b2544d13bc210339f3f825b`  
		Last Modified: Fri, 22 Oct 2021 20:15:39 GMT  
		Size: 3.9 MB (3914687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6da532dae9d098052b14e049a882318ccedddd9624163c3a08bc8e6e7ab967`  
		Last Modified: Fri, 22 Oct 2021 20:15:37 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bb3f6bb58ea29a33104479c8795d79e94c6b3476d06c6738f1bd24fa520260`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65eee94a65d49e6ab6bdc22f1151b6aecf7660077ee4224010fb405b8e092e8d`  
		Last Modified: Fri, 22 Oct 2021 20:15:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:d428625712e5f06fb4fafc3faaa7547197e99ef8805517c1a8b0c730bc8d71e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34693983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd11b365ac243ea9efb2e65cf9059b415a0e3b5faeb847240aacd28835d5aad`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:50:33 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:50:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:50:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:50:35 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 18:50:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 18:50:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 18:50:36 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 18:50:37 GMT
CMD ["php-fpm"]
# Fri, 22 Oct 2021 22:08:15 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:08:16 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:08:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:44 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:45 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:46 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:47 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:47 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bebea86fb8ce75c5427b40dc21fb5c61fd931413f2e98cce8c01a2a4610c74`  
		Last Modified: Fri, 22 Oct 2021 19:34:42 GMT  
		Size: 15.0 MB (15012615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11553391b492d22d8e79f77f0b4b2287e6ab2be30353871a29cd265d8999debc`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fda734499907771c3b18cb7ef49e6ea84f50643a2afacfa2deace9a4786248`  
		Last Modified: Fri, 22 Oct 2021 19:34:38 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c705abb14c392c6f653d6d6079e0d66c073b319237587e4aebf40398127c2fd6`  
		Last Modified: Fri, 22 Oct 2021 19:34:39 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15af60d0e33847ebc7f2e0f82b9d5819ba13d78e46a2e94f50238fe64d0a3540`  
		Last Modified: Fri, 22 Oct 2021 22:09:48 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146a3cee0d08957416cb1026e70dfce33fc4c4de10cfed398f9add920da7110`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636aced19b75eca8177a005e2a9e0004adfe2f20a7c3d1f565e227e23eca334d`  
		Last Modified: Fri, 22 Oct 2021 22:09:46 GMT  
		Size: 4.0 MB (4039879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391c501c22c2caa53728ea9aa40a965210332a54f16b171a89ceaaeeb169a42b`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc721c47dff61ff3f0f3a539c7165573236a2e2be73de3fdd2c0b1dc3864e81d`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a4e53e806e259eae0a78fcfa89386f6c7d4774c2b3a527f8cb52bdbd59b430`  
		Last Modified: Fri, 22 Oct 2021 22:09:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0071c622ac9800567b40452f3328bb29ff661055845731f3ccc575cc8adc33e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35155307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bac9fa27a783cc575926729bc65c8c2f98792bd4ec36d0be41080f51832f9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:03:10 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:03:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:03:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:03:25 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 19:03:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 22 Oct 2021 19:03:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Oct 2021 19:03:35 GMT
EXPOSE 9000
# Fri, 22 Oct 2021 19:03:37 GMT
CMD ["php-fpm"]
# Sat, 23 Oct 2021 05:15:01 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:15:10 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:16:03 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:16:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:16:11 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:16:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:16:15 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:16:29 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:16:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:16:31 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:16:33 GMT
USER adminer
# Sat, 23 Oct 2021 05:16:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4685c811f33ed6a084c0335b35a4bb4f86c09f55d43d828b94fb1355bb4979bb`  
		Last Modified: Fri, 22 Oct 2021 19:41:43 GMT  
		Size: 15.7 MB (15650843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff229e804c40dc864e212cd1b211840852b2b566cf7414c3f9aea2ff6848575`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75bab88fb83f0cac5144755973465d02dd08aba6c0e054776b9b54a3a057282`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 17.8 KB (17843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263011277087f38f40f5f3a182d2892961e6d16a431d8909a50ad4df148d03dc`  
		Last Modified: Fri, 22 Oct 2021 19:41:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e625f0e7149557feca2afaee38cc9aa3fa1829cf0581b8d6782137dd60d899`  
		Last Modified: Sat, 23 Oct 2021 05:17:49 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c69024619d5feb3603316cb9d7c6b28d67eb86bb4e6fb745879595bddfdbab`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29314335b7d8819243f01078ce5ced889058598deb294864b441df7b7eaf8d32`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 3.9 MB (3925176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a11d52cc941dabf83fc9c201b4d3ecfa2103ca40efb538ee548173df33f441`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae20c8cc8f338f0df22e9d140911920e41bde3b9469926b93a83215c1c8d5f`  
		Last Modified: Sat, 23 Oct 2021 05:17:47 GMT  
		Size: 583.0 KB (583038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90687aab1c7b9d0b3e571bd2fc97d559c85204672d0d2ba6ab983197b1d65f74`  
		Last Modified: Sat, 23 Oct 2021 05:17:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:e8015bc81e841059431b6afe424a268a5f73188fceb3990342d03780d9c65ced
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32690951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef94949f1444e29a7dd4485a7548d2a2c22fbd72da3e97ac1cb16337731ca3`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:31:07 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:31:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:31:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:31:08 GMT
WORKDIR /var/www/html
# Fri, 12 Nov 2021 20:31:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Nov 2021 20:31:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Nov 2021 20:31:08 GMT
EXPOSE 9000
# Fri, 12 Nov 2021 20:31:09 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 07:10:51 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:52 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:11:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:11:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:11:12 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:11:13 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:11:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:11:14 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:11:14 GMT
USER adminer
# Sat, 13 Nov 2021 07:11:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d00c1ebd44b22107d0c321652526bf51f244840bc1d25a14d78ff52be2a58c1`  
		Last Modified: Fri, 12 Nov 2021 21:15:21 GMT  
		Size: 13.7 MB (13724037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14968d8f20b6b9053ad15a20303bc4a52bf5faea36abd5156f235d019c3a6e7e`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ddd05c94152081a83ab559f3b7caba2db8b50457ef8c850c3eca9f2bbb20f`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 18.2 KB (18206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5ef1c2bebe8cf5de59792c389469c6ec8c6bd3efe53130b99cfae8f9a792d1`  
		Last Modified: Fri, 12 Nov 2021 21:15:19 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f787c08eb48752ddd9be25b7e866a95ccb1ab8501b82bd7ddc73e2a2a5b1f`  
		Last Modified: Sat, 13 Nov 2021 07:11:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d784ad0e5cf1913192c74ad778f6417af33d6ffcc7b5194df758f38827333458`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0d077df8c500630ade2de720f71bf41fe797221644c8943670fe0f4548f754`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 3.6 MB (3569571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a844cb0fd32a15f101c13967d649dafd2845e2a8c2c0bb7888d1db24563f1a7`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d657f22461eca7bb90a6bf2ee05df2d2a688abbed73d04b8e97901a1961f669`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3cb427d3332664e87af0a4d0a3227707a4985969f2114864c9f3732adfb58`  
		Last Modified: Sat, 13 Nov 2021 07:11:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:1e46edd9882e3df863f3fadd81ce8dacaa27b764e98eeba9f227ceb1464e1162
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:d1a8dc2ca00dd44c3e1f182cbfd987fe9b542beddfb63ea970a07bb636ec0194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33996527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80617cf9eb81c91147c5af090ac2968e19e88c348502972b52c1e46520646eae`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:00:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 21:00:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 21:00:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 21:00:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 21:00:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 21:00:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:42:08 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 17:48:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 17:48:58 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 17:49:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 17:49:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 17:56:50 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 17:56:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 17:56:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 17:56:53 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:52:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:52:12 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:52:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:52:13 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:52:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:52:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:52:40 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:52:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:52:43 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:52:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:52:43 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:52:43 GMT
USER adminer
# Fri, 22 Oct 2021 20:52:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:52:44 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153eea49496a46a69cf5f48803e9014824a6be1d3e04f9ee47cd3f395aba6d76`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.7 MB (1707843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efd0df1fcb3f56e825ef3449f199b261f44e0130a10cb77fcf78339cb88173`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3214c344df86e90fe2ae24d643d9dbc5dcfd6f229f4ee58f7c60c6f0cc895`  
		Last Modified: Fri, 27 Aug 2021 22:41:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd33e16cce149fdc9d0c2392aab5015aae1d2f95945bbdfa849f759bd6b62c15`  
		Last Modified: Fri, 22 Oct 2021 18:48:21 GMT  
		Size: 10.4 MB (10395932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63061f1c8976ed1d60076aa7a4616c54983ac9e907147e26afd085c8af3c1adc`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20a1054275544f2202f6b521a62c7e21957cf8d326ad1949a1ae9e6c2bd34c0`  
		Last Modified: Fri, 22 Oct 2021 18:48:23 GMT  
		Size: 14.5 MB (14533900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d942098e3bc6c976f101204aa3e90a0cbef1bd61947a5fa50927c3c6487be03c`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42908852fe94fee3b88c751fa470d13a8f124f1045b29f5659f43e08bde51e73`  
		Last Modified: Fri, 22 Oct 2021 18:48:19 GMT  
		Size: 17.8 KB (17835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f797d64f25192edb851afbb4400bc27c7896d278d76eb2ca05488a6fef01dd`  
		Last Modified: Fri, 22 Oct 2021 20:53:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9adbdc16fc4f0bc300ecb536f37c7e8cc57455b823bb7201c58132e4e3db8`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23975d1122bcdc58dd3ffdf803782ee736d70f6673ba45801e28f3071a989f2`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 3.9 MB (3935492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408139f67c162278ad469c81420501d7c18a5eb1e9850ff9f6bb3c8630fe573d`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720814720e5f20085d5f51514b1d815acf5d6ec2f3a4f2cfe9af4935ff166752`  
		Last Modified: Fri, 22 Oct 2021 20:53:45 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460f980d1c5dd16303f2e8fbb1f969e15b3041ed6799c5816b40ef5ec2eabb5b`  
		Last Modified: Fri, 22 Oct 2021 20:53:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:18f33d7f551239151d7e0fcbaeedfc54a696212a1543430f8c988275763e24db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32460996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa4abb6acc2443b320b8fb76e2b51c9a3fef524213574bec7f9cccb7d1a308`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:48:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:09:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:08:40 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:08:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:13:22 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:13:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:13:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:13:25 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:24:16 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:24:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:24:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:24:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:25:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:25:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:25:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:25:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:25:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:25:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:25:42 GMT
USER adminer
# Fri, 22 Oct 2021 20:25:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:25:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447ab18b85fc9d5d855178e63d92cee5bf8f0fef102373619e8ce2c9ce9616`  
		Last Modified: Fri, 22 Oct 2021 18:49:10 GMT  
		Size: 10.4 MB (10395941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8226c664bd76abc241b855f4949e9e7c7a4a3d3464165c346b053a92ed7f7b7`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db767f73886111228fe2b67caa323507a1e6ec8e2b0de537a8e16cb1a79ae83e`  
		Last Modified: Fri, 22 Oct 2021 18:49:17 GMT  
		Size: 13.5 MB (13522982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e9583a631d1452ca114e1d0aaae410ed23eb8882dac3e4b2be8267d9524c6`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa460f9d587ee8c70633aa2f249d71027a31d1bbe19090c0c77cf3e04baa5e2`  
		Last Modified: Fri, 22 Oct 2021 18:49:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd193810663444cf9cda92d0f78092bfd2b52fe9fb5d2d25bded9b9d274b13c`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa154b7a597e22ce1343628da56822c8af6bfc6fc6535289cb5fe1ca29fc201`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7438ea1c644d0591a6abccd0910104d89c3e4705bbf7d529ceb8dcab70b32`  
		Last Modified: Fri, 22 Oct 2021 20:28:34 GMT  
		Size: 3.6 MB (3608960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9229dd4ddadbfd43d4bef0019ce9ab096b22cc3a8a084a13be23741560f3d58`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046152c30bbee01d2eeef18b901cd37218c4cc2337d0623f116dfda2b887f4c`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b122846fb9800d0b77a7c9f35d25e65cb5b362d73704a04bb650517a96a046`  
		Last Modified: Fri, 22 Oct 2021 20:28:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:77aca2a3452c2aa58794506233114deacc890a0d3d63ddfa1947d056b5d8ed3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31285901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956608d13c99bc5e96393776ce9f67b88552155ea7c72f1fff0752ff61c30c9c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:38:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 22:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 22:38:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 22:38:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 22:39:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 22:39:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 22:39:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 23:03:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 19:32:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 19:32:51 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 19:33:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 19:37:17 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 19:37:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 19:37:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 19:37:20 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 03:51:40 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 03:51:40 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 03:51:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 03:51:43 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 03:52:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 03:52:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 03:52:55 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 03:52:56 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 03:52:59 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 03:53:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 03:53:00 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 03:53:01 GMT
USER adminer
# Sat, 23 Oct 2021 03:53:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 03:53:02 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1ef9481330a95ddf334887e1f8fce317a5ac59b648f285f67a4985d219de7`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 1.6 MB (1564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b9b552be19301d7e17adf942310cefe01c3c4c7bfd107dfa0db3768b973a3`  
		Last Modified: Fri, 27 Aug 2021 23:55:35 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1716cacc7a16c9894f45061a30c476d428c6142feadd35c9c6d4f7f6fd3f510`  
		Last Modified: Fri, 27 Aug 2021 23:55:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1df2315e88113aa47aac6024f5d99217af3c424b5ccd60d7072f2a51421157`  
		Last Modified: Fri, 22 Oct 2021 20:31:05 GMT  
		Size: 10.4 MB (10395928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a7492fe2bcd6b27c5e9b9cb5b7b1c9cc0d2563f78446dd5d9f4c9c409f77b5`  
		Last Modified: Fri, 22 Oct 2021 20:31:02 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf57bdc67eab511dfddf0cbe66b85f7ccc4565b75e9a099b92bbb9d734f4e2`  
		Last Modified: Fri, 22 Oct 2021 20:31:10 GMT  
		Size: 12.6 MB (12649097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739943fee400523aeb6cf648cc1939d4a1c0093617267d94e117cd553df2a8`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422a660017e7c5618dd06deb69265ace94f4320e9bd1bdceb8ece11bdb18fca`  
		Last Modified: Fri, 22 Oct 2021 20:31:01 GMT  
		Size: 17.8 KB (17842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b1e307616e246342551b95c4ff335c98e3bdc96c322f40d383514f79eb2b25`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162df5ea420066e752898150ac87664796832c1cf0d7a1f362bc03a1b73bf70`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe109d5eb75b7a850092cb2c60cfd51662cd01b5c1fd104139f1034964512a5`  
		Last Modified: Sat, 23 Oct 2021 03:55:34 GMT  
		Size: 3.6 MB (3636924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3a8cbc572c9cd08e50743bb8d7f9862d036e47d06da6bbb7758d077f4cd3c`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05db7e5e9143a017c78857824f27d8c089cd7054c8bc4a86524173ef65b8f7`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 583.0 KB (583042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b47ea673ca861841da766ec9fcbdb824c164b13e652a9074b8d761a441d0bb`  
		Last Modified: Sat, 23 Oct 2021 03:55:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1f7a2e2445165c79fc1291303157eca8d8adccacc51b8207419bdda843a1f290
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99f282ceb275ada8994776ebfdc5bf0b69032c0f0ffb17223c015f6b713b4e4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 20:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Oct 2021 20:36:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 14 Oct 2021 20:36:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 14 Oct 2021 20:36:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Oct 2021 20:36:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 14 Oct 2021 20:36:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Oct 2021 20:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Oct 2021 21:57:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:31:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:31:33 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:31:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:34:59 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:35:02 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 20:13:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 20:13:17 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 20:13:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 20:13:19 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 20:13:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 20:13:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 20:13:48 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 20:13:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 20:13:50 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 20:13:52 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 20:13:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 20:13:54 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 20:13:55 GMT
USER adminer
# Fri, 22 Oct 2021 20:13:56 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 20:13:57 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f327d3d40ef42fee7962b876cfb120bd90ebf3bfbb01a662273165a80f532bc5`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.7 MB (1711094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3586b69bdc11c600d1a1fa08218deb50a3359adfd5fe05c1401367547802557`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a5565cd990bb48f75a1947472074866fbc1221fc87002d4528f444557b48f`  
		Last Modified: Thu, 14 Oct 2021 23:10:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29c49208f7349e7300e6e325d5d0ffb3cd27f1ed3191581962f1d6fa325376d`  
		Last Modified: Fri, 22 Oct 2021 19:06:50 GMT  
		Size: 10.4 MB (10395690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04acff31b30e455255cbe66ba6d10db9c3bf20335d0ad54653acbdf61f47539`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd966f11fdc7ecdffca32a7d737434a6d49c5afe9d8b813bb1c5cb10c7d9b54`  
		Last Modified: Fri, 22 Oct 2021 19:06:51 GMT  
		Size: 14.1 MB (14071988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af329026e61bf26661819fe11dd7117e68d9ed3bac458bd2a28f6ed57b7d76c3`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c16c674cf68fd22b278bce60bcb9048f1e19c78ad7278fc75c49e9c746f148`  
		Last Modified: Fri, 22 Oct 2021 19:06:49 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79445e9e0559777e49f016e4770c80ab83ca0d9f81650789856b4c5cbbfa6c`  
		Last Modified: Fri, 22 Oct 2021 20:15:12 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c95209afffdec3bf895716fae944870e396e2dafd87861d80639dc0c6334d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8471d71259df9ce3aeeea634ebd6c2af18cc59d3949417ea3137531ad19bc1d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 3.9 MB (3914678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023144139a28dcea6f497b016e524caa7d713e33f33c2c574ab4c2c479d6dc`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46da6deea42f9250ccaed0b7d4861d7224a502c49f0371d8d6125fa33c63d`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 584.1 KB (584070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653012098a8e97583ee74210c14b744c1b85b09481f5dd92e9317762bb9d73e`  
		Last Modified: Fri, 22 Oct 2021 20:15:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:c57b015e5daebb2bfd79495cf42aba9ce493a017d1279152e1eea9b4e5051adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34616802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bae9200e281981732536236a0c46f54956259ff312f8b025917b7c277b4d4`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 19:59:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 19:59:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 19:59:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 19:59:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 19:59:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 19:59:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 20:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:37:34 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:37:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:37:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:44:21 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:44:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:44:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:44:23 GMT
CMD ["php" "-a"]
# Fri, 22 Oct 2021 22:07:33 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 22 Oct 2021 22:07:33 GMT
STOPSIGNAL SIGINT
# Fri, 22 Oct 2021 22:07:34 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 22 Oct 2021 22:07:34 GMT
WORKDIR /var/www/html
# Fri, 22 Oct 2021 22:08:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 22 Oct 2021 22:08:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 22 Oct 2021 22:08:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 22 Oct 2021 22:08:05 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Fri, 22 Oct 2021 22:08:06 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 22 Oct 2021 22:08:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 22 Oct 2021 22:08:07 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 22 Oct 2021 22:08:07 GMT
USER adminer
# Fri, 22 Oct 2021 22:08:07 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 22 Oct 2021 22:08:07 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa6b193871895593dd2e9300b768212b024272930161ab8524f40a5735edd63`  
		Last Modified: Fri, 27 Aug 2021 21:44:10 GMT  
		Size: 1.8 MB (1805371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f324621ef2d45fa9d97583b1efc3fb241066b4dbf696e2dd38327a90d1e6813`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d22e796392b3e282fea08fa6cb0da352053587b646a938425cb7c4171bf25a2`  
		Last Modified: Fri, 27 Aug 2021 21:44:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe642dc54ed8053864fec64f57ec7e1e2ee7593efd4c811e35e026c60c0084a`  
		Last Modified: Fri, 22 Oct 2021 19:33:48 GMT  
		Size: 10.4 MB (10395923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa560b708f0962c1a66115faef679c8a7077ab3fafa527ed104d7d46bf68870`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c5d12a980bef3ab35e576edb8de3895ba198af58ef6892e4796e2139309ab`  
		Last Modified: Fri, 22 Oct 2021 19:33:51 GMT  
		Size: 14.9 MB (14943894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a12b0162f1627c66847b1ddf275c3890f195b776fb844d215640c3ce38b5163`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6affd9d1aaeb98680d7d68c378113dadddf238514edfc10b5b282200976fab9`  
		Last Modified: Fri, 22 Oct 2021 19:33:47 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4d27b241b61163ea9bc09916fd08fa5ac4d254327f51d687017b2e6e0a5da5`  
		Last Modified: Fri, 22 Oct 2021 22:09:19 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b662a8118e827005852bfeda22b35cea5362fe7bf81e403ea6729105fe1fbb70`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061442d2869cb0c5e39568b95b297e7d5c0c31e7f90c9c5616ce41f9256741d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:17 GMT  
		Size: 4.0 MB (4039854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed0bc650caccfb4891162e4b1211fead10be8544c4440297c65b0918a0e5ff`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 1.5 KB (1494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61da981f0707d81b7aaba2b464fb861c817a675e858b477edb4014b3c231d3`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f08c34785bbcc6b490513adedaf95af7589910189acd082424d2483b6de12`  
		Last Modified: Fri, 22 Oct 2021 22:09:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:3cd854cae8dd54ec5efaf02fa339e77e40d00709ba9a62859da9bc79eae44cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35070593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8d7cb848eff2b16727f0aef3bc5685e9ad36a39b0b00e908a8432339b85d0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 28 Aug 2021 00:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 28 Aug 2021 00:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 28 Aug 2021 00:22:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Aug 2021 00:22:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Aug 2021 00:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Aug 2021 00:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 Aug 2021 00:51:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 22 Oct 2021 18:52:07 GMT
ENV PHP_VERSION=7.4.25
# Fri, 22 Oct 2021 18:52:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 22 Oct 2021 18:52:13 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 22 Oct 2021 18:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 22 Oct 2021 18:52:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 22 Oct 2021 18:57:44 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 22 Oct 2021 18:57:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 22 Oct 2021 18:58:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Oct 2021 18:58:03 GMT
CMD ["php" "-a"]
# Sat, 23 Oct 2021 05:13:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 23 Oct 2021 05:13:07 GMT
STOPSIGNAL SIGINT
# Sat, 23 Oct 2021 05:13:14 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 23 Oct 2021 05:13:20 GMT
WORKDIR /var/www/html
# Sat, 23 Oct 2021 05:14:12 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 23 Oct 2021 05:14:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 23 Oct 2021 05:14:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 23 Oct 2021 05:14:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 23 Oct 2021 05:14:23 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 23 Oct 2021 05:14:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 23 Oct 2021 05:14:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 23 Oct 2021 05:14:40 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 23 Oct 2021 05:14:42 GMT
USER adminer
# Sat, 23 Oct 2021 05:14:44 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 23 Oct 2021 05:14:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a4af98e0d6a07fca505c073eaef771202280f717e9eec5693da72e342352b`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.8 MB (1753694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f45086a93088805a1f9f81303c856d62fa5a43ec294f558743c42e803fa376`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bbbefa425da2cee0e640dda470f0cb14892652fd6f89c03319eff15fdf1720`  
		Last Modified: Sat, 28 Aug 2021 01:41:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef274c8efc1d9366d48d5c3fd0fa56eed3171885d42eee44179362b1060db77`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 10.4 MB (10395937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da48383246f6f6caa142638e464adf0eb2ced4f58d964c8e4d73aa2c2b3e31`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6646db21707eaaa67bb84a72e51eb298b8df20db056f0ab6bc7738cef72cbd`  
		Last Modified: Fri, 22 Oct 2021 19:40:57 GMT  
		Size: 15.6 MB (15574578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac00d15dd113bb531d6be0fb23db1124b017f5f3d8759d8166341e9c295266d`  
		Last Modified: Fri, 22 Oct 2021 19:40:53 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539b7385dcfcab92b7f12c13621c511de297301ea8945ff4986767c1f44f8c4`  
		Last Modified: Fri, 22 Oct 2021 19:40:54 GMT  
		Size: 17.8 KB (17844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984db0c4771927b1bed4e0653269291dd84ba70d3a2d67ae2d135b9e816a5dc7`  
		Last Modified: Sat, 23 Oct 2021 05:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411994cfa9d1285ff20334930a927b18a99a4d2754e67c61d9eebfc18075a6c`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7f2969bc8738d500c62dfd61c3d1150475fa6807f65ea0a8497c9fd28e1bb0`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 3.9 MB (3925165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fdc2603a493fc17e8f49cdd7457b7d0b7e99859d93dbfcbfbf0be6e77c18bc`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc090b2b9262b69f63d095401d82360e99c5689a3ccc2a5c2302579b83296`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 583.0 KB (583041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e84e495cf5edafe10e36ad8d49b442dbcc3e16a0028c4938623c807fa53390`  
		Last Modified: Sat, 23 Oct 2021 05:17:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:e58a37c27ea0d12097e0d395caefd539992012b57f4384cb81327a571a7ebfdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32615697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2f7f36ea27b8d1c80c11f504af03f7168b9e85f0b1230399543c565e663bd9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:25:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_VERSION=7.4.25
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.25.tar.xz.asc
# Fri, 12 Nov 2021 20:25:15 GMT
ENV PHP_SHA256=12a758f1d7fee544387a28d3cf73226f47e3a52fb3049f07fcc37d156d393c0a
# Fri, 12 Nov 2021 20:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:25:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:28:07 GMT
COPY multi:a00980ff863125d6071b93844e0a51dc89719405d95217aba6860be950a05740 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:28:08 GMT
CMD ["php" "-a"]
# Sat, 13 Nov 2021 07:10:20 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Sat, 13 Nov 2021 07:10:20 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 07:10:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 13 Nov 2021 07:10:21 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 07:10:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Sat, 13 Nov 2021 07:10:40 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 13 Nov 2021 07:10:40 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 13 Nov 2021 07:10:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=ef832414296d11eed33e9d85fff3fb316c63f13f05fceb4a961cbe4cb2ae8712
# Sat, 13 Nov 2021 07:10:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Sat, 13 Nov 2021 07:10:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:10:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sat, 13 Nov 2021 07:10:42 GMT
USER adminer
# Sat, 13 Nov 2021 07:10:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 13 Nov 2021 07:10:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2763bdc3efb5edc279d7e5737c763f802f650f566827ca669f6443046e0793`  
		Last Modified: Fri, 12 Nov 2021 21:14:50 GMT  
		Size: 10.4 MB (10396315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9adad41c867270b9dfc8fba14e747a055ea8ae2631a73df698c012c84d50`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba38b25bc1d48daa802d3b1100f9456c9a502220fe434b3324bb20a81a57b06`  
		Last Modified: Fri, 12 Nov 2021 21:14:51 GMT  
		Size: 13.7 MB (13657199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e7d31eb4453f5fb7ae42b127a652bb3d930d02c3387a926301ccc4bb76ce7`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360eb2460d3f0a64e9bc6419df7696437e887fb78832266e76f719e5e3339f17`  
		Last Modified: Fri, 12 Nov 2021 21:14:49 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d22ce769a652109b9b0b481940ae69c0d325243a7f0ec5e65417cb903c7a79`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d993b4fb9b0e42cb5b740c7dd2d925902d1dea0ce2156393cc2f8bef817c24`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc73eef2dac436727d96db4153000808dd2e4996451aa980d15f01371186a2be`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 3.6 MB (3569596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b312e861ba198730427393c40edeae20de63fe2486140610ddb8d1f397c3b71`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e40baa84d4a891a7a50a59fad6b87bea4a30a00750db8b3253abc3167d2a19`  
		Last Modified: Sat, 13 Nov 2021 07:11:43 GMT  
		Size: 583.0 KB (583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1889166ba6e470871e472f5596f2b9dff9e174259cb3a45db84802e196aec595`  
		Last Modified: Sat, 13 Nov 2021 07:11:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
