## `adminer:5-fastcgi`

```console
$ docker pull adminer@sha256:959cf5949b7165242f24f2fb32ef09fe9e2096479811e60d9957c3ef06c9a44c
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

### `adminer:5-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:c0245834610efab941593ad97b6c70a02fdcc74a67489984275f3ba8ec92dbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40905516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bc088d54b6179b90ea933357901a5336ddb11d0a292898a3cddba5172a8321`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab72d8c43e64ba0dd781be2526327300d23651b677bca16549f7595530398cff`  
		Last Modified: Fri, 06 Jun 2025 17:41:26 GMT  
		Size: 3.3 MB (3339415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93d70e17ba4ca59c02aea3c4454739d82d91f2a440b584014b143ee4ae93ebc`  
		Last Modified: Fri, 06 Jun 2025 17:41:27 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193781f42acd75e23d3a5a6bd7d4da08c62e36d72ab3f635a2648f461581de67`  
		Last Modified: Fri, 06 Jun 2025 17:59:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4707bba4e2507649358bd2add10dfa3640c63673173b5f5f4f4e418d474687b6`  
		Last Modified: Fri, 06 Jun 2025 17:41:29 GMT  
		Size: 13.6 MB (13640340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c118f93978fa95f1d41b092385a0f705796fe517b8ca0ad8b2e0fb4d0088ad`  
		Last Modified: Fri, 06 Jun 2025 17:41:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cef87855f758aad29e530988a4d9b6f392352528bebb51f4e500309186e9d06`  
		Last Modified: Fri, 06 Jun 2025 17:41:31 GMT  
		Size: 15.7 MB (15695395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728ea9866f5699e45def536e8fe1304709aa125612b71961a9f9915a5ae05317`  
		Last Modified: Fri, 06 Jun 2025 17:41:30 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc74ba8d5291130700465b5a360a988c493c28f9efefde832bd0d7692a828181`  
		Last Modified: Fri, 06 Jun 2025 17:41:32 GMT  
		Size: 20.1 KB (20052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514f3f8784ede75336bb0df4109b2134daa8d16b9615ccff03b1e0fdee4d5892`  
		Last Modified: Fri, 06 Jun 2025 17:41:33 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312d3b71e5a1fc74aad91e15080817094702b185cf3ac496cf27aaa1f34c6b5`  
		Last Modified: Fri, 06 Jun 2025 18:00:51 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fb203b888be627f245da31eefa4ef7263c8c4fcd3ba9d7900f88c7e241e235`  
		Last Modified: Fri, 06 Jun 2025 18:00:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d34eb65a112ba0e4ea6be7d9912ebb7e2a79e2117ffec06b90f54ae187e4dd`  
		Last Modified: Fri, 06 Jun 2025 18:00:53 GMT  
		Size: 3.9 MB (3916527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3464947883361e24fe36356d32d97eac5f82a2a145dc6da1dae834121cdd6ef8`  
		Last Modified: Fri, 06 Jun 2025 18:00:52 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7d9ae20b9e8b4b2e972a223aafecf2473c8b1524979c477caf0c501749d348`  
		Last Modified: Fri, 06 Jun 2025 18:00:52 GMT  
		Size: 634.7 KB (634700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ff81b37daaeb1bb4406afbd4f57b790e2ad6740929cb650a6e7cd9263a4bd`  
		Last Modified: Fri, 06 Jun 2025 18:00:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:577428a191d3098a8aad70539329b8ddacf5632c5ae92bed7cf3962a1eea3b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa429362cdfd52248653d952c334dc0ce49eb04cd28869f9f40eec95fcbdbae`

```dockerfile
```

-	Layers:
	-	`sha256:7bce401216bcb575705ca49ce5b05d314c4dad96656c81a4f3572f4723c72afa`  
		Last Modified: Fri, 06 Jun 2025 21:50:20 GMT  
		Size: 32.9 KB (32923 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:e567b964cfa5fb3071a91b3313d4e04b2fde195c8b32eda232616b6654b86b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39460518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1e3ef30f5d61cfd603a644ad78a082f48e2f043f3f2e75288d969efad2ea28`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716792796cc38ee95ace894d8fb45f0a4d44a09080326e26266ee1b75042cee7`  
		Last Modified: Fri, 06 Jun 2025 17:40:24 GMT  
		Size: 13.6 MB (13640340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201103d1c440b9c525c0eb93b96b9eeb38bb9015af4c102c87ab13c2667b4a84`  
		Last Modified: Fri, 06 Jun 2025 17:40:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a3a26ed87b86d8b100ff797cf09a28baf108a87aa0b006d5a6af55f6a19d56`  
		Last Modified: Fri, 06 Jun 2025 17:45:50 GMT  
		Size: 15.0 MB (14958999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a09ccff4ed214fe42974be9b9230e37f86e99af3d5d7123faa3553c18e1db`  
		Last Modified: Fri, 06 Jun 2025 17:45:49 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e420fb63594ff19fdf6def58b3ef054c99c2f613e31748a56fc0dfb2c22cf5`  
		Last Modified: Fri, 06 Jun 2025 17:45:50 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493459311218ea6c7808917d4a8171bf7558c735ce567c0d4ef82790c55e95d`  
		Last Modified: Fri, 06 Jun 2025 17:45:50 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d285b75b9253fd3ef1b604d53ba2f06db1acadf57768e4e9e26996eb62b2fd`  
		Last Modified: Fri, 06 Jun 2025 18:40:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3d27ccd6cda93579695985828d9b376293af4a4f5b8053c4620c4e03e62f3c`  
		Last Modified: Fri, 06 Jun 2025 18:40:29 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e937a23dbe93e2a8cf4e760e828961d948eadc10d3bc5f7647c6487aa89f4d4e`  
		Last Modified: Fri, 06 Jun 2025 18:40:30 GMT  
		Size: 3.5 MB (3515959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5c1a7e6101c9cc4d788bbea31bf7d1d4911e1698dbb10c1319ddc3ac441dc`  
		Last Modified: Fri, 06 Jun 2025 18:40:29 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b14b13ad2b153fe144b1594bf01a9e3d156b5d4fb00ae41c7f5b1da87e2c6`  
		Last Modified: Fri, 06 Jun 2025 18:40:34 GMT  
		Size: 634.7 KB (634703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482030d69908e29775d44ca1d1651403c3b9adf3d079e1cf7289bf5697fa57ec`  
		Last Modified: Fri, 06 Jun 2025 18:40:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:99c00f8199e84e1c6f58613518ffa730072e24d8ad17e795886353618e86774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a3cfca0130a66193a4439f1f6fb1b0b021a8e8b2eea8f0bc63b1cb2dab6d3`

```dockerfile
```

-	Layers:
	-	`sha256:eb2a8214282ba5858056f932f74a983a9db031c5772fc72a7bb760749f8452f2`  
		Last Modified: Fri, 06 Jun 2025 21:50:28 GMT  
		Size: 33.0 KB (33030 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:95f7c8fadc69bcf3f259ec866dc6f31ebdd29517e899599886d407b92c971a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38255990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b350475c862f236b3dd38be1f7f047373155e517d47fb97be263bb00b0affd`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 21:49:05 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 21:49:04 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 21:48:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e389261b9c64b81e91f5a16347a7d45abc12e8f8be41e35d9d667607c4416`  
		Last Modified: Fri, 06 Jun 2025 21:10:57 GMT  
		Size: 13.6 MB (13640356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0affa11432fa3e90bc1ff3b1972f85eeb1fe87eea39abbb4936e184cf2faf79`  
		Last Modified: Fri, 06 Jun 2025 18:38:24 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab35fa3fa7ed7abcdca8e24b2b80311547ac47b4641a9041c03f7e696779248`  
		Last Modified: Fri, 06 Jun 2025 19:40:30 GMT  
		Size: 14.1 MB (14145744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abecfd9bef0e5f023c9c3fdcd9cf3bf6c9e5d05324d00ba425d75010bb2b6116`  
		Last Modified: Fri, 06 Jun 2025 18:38:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbae01fa458fc1689ca9d2b33ab3db4aa9472efeb2805aa1555cccdfcb7ffcb0`  
		Last Modified: Fri, 06 Jun 2025 18:38:39 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f89347e754d24cd93e22e75a8ab80e2016230b9aa6bd83e418d6cee4572c7c`  
		Last Modified: Fri, 06 Jun 2025 18:38:47 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c3170eef9be414445f6d575a8b359b7b02bba28a57cf44084b3f3333f9d404`  
		Last Modified: Fri, 06 Jun 2025 19:46:14 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4090b3ae21115204ecbabdeb3cc1c25df59caa29fe202ad35869d23809ede35`  
		Last Modified: Fri, 06 Jun 2025 19:46:15 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2175488a5c2e52d0c8bf29c8c19a4ba2ffc33253cda38c460d322e149473894b`  
		Last Modified: Fri, 06 Jun 2025 19:46:16 GMT  
		Size: 3.6 MB (3579921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06038b2e669a1611b2b8b0423a96c951b432cdf228c938d4d15fca541679a5d3`  
		Last Modified: Fri, 06 Jun 2025 19:46:16 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f429c56db3be654fecda60f597f6b20f44adc6e0509d63e6871bf331d84950`  
		Last Modified: Fri, 06 Jun 2025 19:46:20 GMT  
		Size: 634.7 KB (634707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd4abb5b88dfc4cf4138422976634c9b9ecb20c5bfcafd218c70024bbf064f4`  
		Last Modified: Fri, 06 Jun 2025 19:46:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:c897294b9bb4a47ffea44516f615beb3f2530b30238ba4652a0682ab6b40eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad783c1ec3d338e45c94ae15c00db50ea87169141d38f08cebbb7c4f82e79328`

```dockerfile
```

-	Layers:
	-	`sha256:41e45b2d824afd6479eebaa8413d6ef2f38741cca56b7409b9e818061f825f24`  
		Last Modified: Fri, 06 Jun 2025 21:50:32 GMT  
		Size: 33.0 KB (33030 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:0bafd1c47557cb3d886ca8b0603ff8a02d64e63de895859900c40075ec3b797f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40876394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922013800c85c237fadbb73eb34479198be03c477991477d69cab320ac73fc6c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83372af8a678b04e4062678a6e4749712b1fe89b6611f08010a941229230e7f`  
		Last Modified: Fri, 06 Jun 2025 18:10:42 GMT  
		Size: 3.3 MB (3332268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a04181e8579deb4c7737e06d7975655168e25be9a5a71b334a4c7cfdbefde`  
		Last Modified: Fri, 06 Jun 2025 18:10:42 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb24e42119e8047a1da41cf57b92f5aa3f71a0111ccbbd3fea2d1bfea9ee75`  
		Last Modified: Fri, 06 Jun 2025 18:10:39 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842039be5a88b80bf3b58f206c12c44a4586ec105dec961f99aa9198e83f67d2`  
		Last Modified: Fri, 06 Jun 2025 18:10:52 GMT  
		Size: 13.6 MB (13640371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb5659dc61b56f2bcd4efd0ea9ed787b3ea95e93b2a6444786845f75955c67e`  
		Last Modified: Fri, 06 Jun 2025 18:10:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea6ee89a5a964a821ce32912fb25c13c7588400c6f434f8be834dcd94d72b45`  
		Last Modified: Fri, 06 Jun 2025 18:14:57 GMT  
		Size: 15.3 MB (15324516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5f006c13abe5097c24e1d869e47d4da54d036ec65f2b3348531764b9b215e2`  
		Last Modified: Fri, 06 Jun 2025 18:14:49 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc529491590e28e7188a7059a0fce5da958f07a45f16a2f1e5d18bcd64feb9a`  
		Last Modified: Fri, 06 Jun 2025 18:14:49 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415c85f2320fe16a36913b02bd3f6906828c9536557cb7249c554c73a381d1f5`  
		Last Modified: Fri, 06 Jun 2025 18:14:50 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130d5d70ceed3df462b609c65a9c80893531ff36690cd152c438de1fb1ef8358`  
		Last Modified: Fri, 06 Jun 2025 19:48:17 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb528f1732bbcb51244224d4b318f88fe197d76c763d0989616112abb765e261`  
		Last Modified: Fri, 06 Jun 2025 19:48:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba83ed953f83f7c871e1e289a4c2f439bf8c638946defdd626d0bd2b5d86a343`  
		Last Modified: Fri, 06 Jun 2025 19:48:18 GMT  
		Size: 3.9 MB (3914806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b8d00ffd70ca8df66d76165063600e5d6fafd9c60e94e057eccb966b21eaeb`  
		Last Modified: Fri, 06 Jun 2025 19:48:18 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b397a7e861a59dfac0564c5819701ffe9b096fb519cb2357396084bd9414d051`  
		Last Modified: Fri, 06 Jun 2025 19:48:19 GMT  
		Size: 634.7 KB (634705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698cb2481068a52697efc335558a4d823a69840f3b59a8e0f876c30548e595b`  
		Last Modified: Fri, 06 Jun 2025 19:48:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:4db2c8fff37f8bc4479e092515e19153386bcf7e9d9019f2ffdaad9fedb4d59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e5832367bbc58704b48841985175085401619fe336ed28ec651fab3f8c5fee`

```dockerfile
```

-	Layers:
	-	`sha256:62a63b703d0745c4ed9af121844a3b7bbd8e7ff26514005b194561624b516681`  
		Last Modified: Fri, 06 Jun 2025 21:50:41 GMT  
		Size: 33.1 KB (33060 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:32ee4a89da25673a1339adad2d548a8455716fdb00a1957fb125d9277195419c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41031116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3823bc852697760eb297f1aaa3faa7739c4e58964e486d0131a2db2a2a83e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a98867943a24cf4bec9e43d9d5c0f90a3eb5436a6ea06b2c6dd43b32885b28`  
		Last Modified: Fri, 06 Jun 2025 17:41:34 GMT  
		Size: 3.4 MB (3379881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6aa4f4d277874391168f02338dd64d2f22f149cc2bec5fe3643f203673f41e`  
		Last Modified: Fri, 06 Jun 2025 17:41:35 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b4faa4fd024d0d0069787e0ad29203f83de5c21c93bceef3082ba9bf875fa`  
		Last Modified: Fri, 06 Jun 2025 17:41:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce9c97723ae55f52c4a7f90139c1130ad607236b820d082840cf63cf3e9645`  
		Last Modified: Fri, 06 Jun 2025 17:41:37 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e65c36912c7435dae5b5d5efebc3a12e9aa2f6fefba3490ad40fff3270d608`  
		Last Modified: Fri, 06 Jun 2025 17:41:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672981b80b86f62fc15dc24ea373bcb2328e543dcd5bdcdad9159aed5a57b25`  
		Last Modified: Fri, 06 Jun 2025 17:41:37 GMT  
		Size: 16.1 MB (16094375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4690270452de873de57fd8675d2db0faa361486b93daff07466346ae4cca9f70`  
		Last Modified: Fri, 06 Jun 2025 17:41:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb4d714b560e86926eb7bd146edf8b97ff50a3757df6000509b3df02171285`  
		Last Modified: Fri, 06 Jun 2025 17:41:36 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9f11cf6b8e257540aaac6aebae8f2043d05f111e50514518cdce69301b5ac0`  
		Last Modified: Fri, 06 Jun 2025 17:41:36 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c6db479269264b68d556c1392d849757f423b0f9144e210c514c1d5c9dea3`  
		Last Modified: Fri, 06 Jun 2025 18:00:41 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891560322a7f9f5d996739b6ada3279fd6a5cc33c669f21a96bf5d677b826b00`  
		Last Modified: Fri, 06 Jun 2025 18:00:42 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999a432e2a2590a47f483b1f7a365ad37002e5092846e33adaa82bec2cbf6600`  
		Last Modified: Fri, 06 Jun 2025 18:00:42 GMT  
		Size: 3.8 MB (3781304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952395a3504c8dae473b6ebcec38d4240c751e957005359d459b55a0905e7b3`  
		Last Modified: Fri, 06 Jun 2025 18:00:41 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836bd3783a93a53aed9f733927241ca9fe824e2fdd62956cb22652ac682c5287`  
		Last Modified: Fri, 06 Jun 2025 18:00:42 GMT  
		Size: 634.7 KB (634701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b724d891e1868b6b2c67524c5180bc2c38d3c79952b1f45fe1196868b6150fd`  
		Last Modified: Fri, 06 Jun 2025 18:00:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:e65029b0bfdddd717b05d2467920454e6dfd70853b7e87e247d35c0f4c337da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624f0be80b7f570c1414c43a77f64bc8b5f9f813355b17c7531f48335f16ad4c`

```dockerfile
```

-	Layers:
	-	`sha256:ee810e0c5fb193ae56826c9458f51fb1ac3a9f92f4e9dfb8e3b779701ca21d51`  
		Last Modified: Fri, 06 Jun 2025 21:50:49 GMT  
		Size: 32.9 KB (32890 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:9e4abaa6d06ea153d4950ae435255fa25d430b03c055cd3c0b77f0d676532904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42139640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f07d7c8c28e19dbaee0f6b78bfe3f9776eb27262edbb7540f2918607bd8343`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 21:49:13 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 21:49:12 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 21:49:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a72851212251f0d0be4b6cc66e090b172e5787b81d27c1cca7b595696e3940`  
		Last Modified: Fri, 06 Jun 2025 17:57:04 GMT  
		Size: 13.6 MB (13640361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c9a217cc4310151ea091bcb0c7fa4ebdba65a96c6514e31f7f57643dfab712`  
		Last Modified: Fri, 06 Jun 2025 17:57:03 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6555afed99a4530787d199fc7507b17149a253341f570af2243de6fbb0fcd6`  
		Last Modified: Fri, 06 Jun 2025 18:01:07 GMT  
		Size: 17.0 MB (17004970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84056943a5c49dbd6c2da2a60d5fc6ac93f951f98ce205bd65df9b88d6bd9a89`  
		Last Modified: Fri, 06 Jun 2025 18:01:04 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531caaf5f130ebd76794b0a01b5906dc4a9d37fb9baf3fe4f1f52401193e9e31`  
		Last Modified: Fri, 06 Jun 2025 18:01:05 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1dc89380aaf5e55937f8ebf59169cae7312cccc7d1a6401e3d44805db24037`  
		Last Modified: Fri, 06 Jun 2025 18:00:53 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35e087fad6da027e6c2cc7d0d50498cfc216b2a4265034c5eb5c57bd24feeaa`  
		Last Modified: Fri, 06 Jun 2025 19:11:06 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c3416cfbe61444ecc45d083f4270130a4ec5e1cb34da103a8bee7450ed8c08`  
		Last Modified: Fri, 06 Jun 2025 19:11:07 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569e047e898aa17df019b21847b7e8d61039cd340e4d6be4d6fa9f15f4e1991c`  
		Last Modified: Fri, 06 Jun 2025 19:11:07 GMT  
		Size: 3.8 MB (3767423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18878da4d199ee04c434acc4c178d74bff9e84a8140fccc6123b7bac12ce549`  
		Last Modified: Fri, 06 Jun 2025 19:11:05 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905afe13f7d4cce288fa5ac9c4a793f7604c557705e3906b9bc963c69e7a682`  
		Last Modified: Fri, 06 Jun 2025 19:11:06 GMT  
		Size: 634.7 KB (634707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871af55b8d33c3c1ff17a36c8577a7953aa8567a8e45c1a7cc8ac1831b5994ad`  
		Last Modified: Fri, 06 Jun 2025 19:11:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:c65189448aa7ece16ba609d75181d657abceb30a8d99fc5314478a41b9681115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b7b1880cede112b0a905dfa29c3a8714350e5f4783d99395e2f0cd2750dbc3`

```dockerfile
```

-	Layers:
	-	`sha256:c6c35112d03c9f7b81fd3cb102fb76818427a93f10d51bcca0aeb3bd12c32908`  
		Last Modified: Fri, 06 Jun 2025 21:50:53 GMT  
		Size: 33.0 KB (32966 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; riscv64

```console
$ docker pull adminer@sha256:2184d01e69c0e6cc4c93ef015b00032d14033a566676117cf5036aa9796b7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5cc5946244b2bcd2bef660cbe2ea6af4598a15871a8cde321f264e9af57091`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 18:45:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 08 May 2025 18:45:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 18:45:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_VERSION=8.4.7
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Thu, 08 May 2025 18:45:09 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 08 May 2025 18:45:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 18:45:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 18:45:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 18:45:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 18:45:09 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 18:45:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 08 May 2025 18:45:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 May 2025 18:45:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 08 May 2025 18:45:09 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 04:03:11 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 04:02:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 04:02:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 02:38:35 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 02:38:24 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e3844ad65bf5cf88d0849b27805de0e48a5324945105f742f3f4a8c7922d6`  
		Last Modified: Fri, 09 May 2025 02:05:43 GMT  
		Size: 15.9 MB (15885870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abdced2871470e34f098ee2dc65fe24902a1837a41e95b3cac2f8b2638f006`  
		Last Modified: Fri, 09 May 2025 02:05:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabb4c3a9ad44ad6f6e3b9f6c7f96504e3bb0462acc8ab48dca0a678f9f6a14c`  
		Last Modified: Fri, 09 May 2025 02:05:40 GMT  
		Size: 19.8 KB (19841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9d2089535ce2200043c4bba04ddaf0d7b211ead3e30a3f1031948cae9672fd`  
		Last Modified: Fri, 09 May 2025 02:05:41 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa73296bf03bf5b4dd12a58f5ece03c4a4add3fb5611544511032fc11089492`  
		Last Modified: Mon, 19 May 2025 23:16:02 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c597305d3018c3eba64432a0b0c85d747239c66029c6b1511c9b2f3b943c08`  
		Last Modified: Mon, 19 May 2025 23:16:02 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3ce729cae8112630f36a50607dfb0dc16c78989ef9080e2238e1785292bd47`  
		Last Modified: Mon, 19 May 2025 23:16:03 GMT  
		Size: 3.7 MB (3672498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1438ed2b4828ce31504c3d8c21ffce127764a3d9cad65228e7897f8a6602d30b`  
		Last Modified: Mon, 19 May 2025 23:16:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f107c8a237cab1e7630c0962b917b2ae3c31bb661f9179347ca9133cd8b5d6`  
		Last Modified: Mon, 19 May 2025 23:16:03 GMT  
		Size: 634.7 KB (634709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9189ff3bdecf4d6708e50758c0ef8fbc379599a14b5f6228b86f51d2b4c181`  
		Last Modified: Mon, 19 May 2025 23:16:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:3c5fc902636e7dafb4ff71e65a253be7ab68fcd3111c9ce3eddaaf0a3de056dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0d7a8fae0d3a6c09de8348e216319e8f4eb7f9c240bc36a1ba135c4d5e0021`

```dockerfile
```

-	Layers:
	-	`sha256:c4277eb0dc729d116762d5be448cd9a5378bdf5c2599b4bc263ab5d11e99c933`  
		Last Modified: Tue, 20 May 2025 00:49:37 GMT  
		Size: 33.0 KB (32967 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1935061831e65d293851ece361b5ec5a35b1e23646c6e3c837abb37d31c164df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41635489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15442f93d8400b07667ea0147f3447fdefdc0c3f4cee011c88c85815fe20c51a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 May 2025 11:19:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 May 2025 11:19:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 May 2025 11:19:45 GMT
WORKDIR /var/www/html
# Sat, 17 May 2025 11:19:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 May 2025 11:19:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 May 2025 11:19:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 May 2025 11:19:45 GMT
CMD ["php-fpm"]
# Sat, 17 May 2025 11:19:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sat, 17 May 2025 11:19:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 21:49:13 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 21:49:12 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 21:49:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780d17f930862563fc7e94895923943be50b28e27e96c0cff7ad5a9934c1e77`  
		Last Modified: Fri, 06 Jun 2025 17:52:28 GMT  
		Size: 13.6 MB (13640363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b3e50df4a279f945b5b37d3a22c8106c917b6b5bd49b933030962d5cd6d16`  
		Last Modified: Fri, 06 Jun 2025 17:52:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b265f04b256bc0dc1d87e37bc8e6f70a105bb2aa072ed919e7d44d5c978d8c0`  
		Last Modified: Fri, 06 Jun 2025 19:43:54 GMT  
		Size: 16.7 MB (16691086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90f0eb459bf49b8bd2236a7225f7ddfe72eb6fd1f64029b44784740b1db840`  
		Last Modified: Fri, 06 Jun 2025 17:55:46 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67454cd3ff51d91d846e8cee5e18c59af913191b2af9ba43075a04cb8f33f8d9`  
		Last Modified: Fri, 06 Jun 2025 17:55:46 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed421f694947999c9a2ab4734a48d25d6278362b9ce38cf42708eeb44529ea6b`  
		Last Modified: Fri, 06 Jun 2025 17:55:47 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f05d7e36b087f3b1586e64533bb74fef8ebb6bc9cc01757fa94cff220ac5e4`  
		Last Modified: Fri, 06 Jun 2025 18:54:40 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc38ed8fa44f804210ad636dc45361467aefd35f7dc9e297a7864abacea6b7`  
		Last Modified: Fri, 06 Jun 2025 18:54:41 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1fa8732535ec11fd298890ef0e3dc791b9c8f470545704a5587be3ddc297e8`  
		Last Modified: Fri, 06 Jun 2025 18:54:42 GMT  
		Size: 3.6 MB (3598842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635a881985c49c6d96615732c48918c13e980308a4b926bb3b1c0270258cb8a`  
		Last Modified: Fri, 06 Jun 2025 18:54:41 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ef086936dbd2ef24d48bf3c75b140a2a4d0210d695db19a637bf1c2d175644`  
		Last Modified: Fri, 06 Jun 2025 18:54:42 GMT  
		Size: 634.7 KB (634709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97069ad8d32ea9e5e51280ff4d1a30a12bbd48aec8a3ebf6536e93a051d309bd`  
		Last Modified: Fri, 06 Jun 2025 18:54:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:63de215da764cbbbb1ee152a949b270a379771d6242a4e37cdaaec6acd5eef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79a3a63a77dd368f30dfc8f32951a358e48f268627bc3af03cac04cb846ccf3`

```dockerfile
```

-	Layers:
	-	`sha256:11573461438db6935127e55948a4ab9e8e2e02e865ddc2d90d0bdd6a4a335e7d`  
		Last Modified: Fri, 06 Jun 2025 21:51:01 GMT  
		Size: 32.9 KB (32923 bytes)  
		MIME: application/vnd.in-toto+json
