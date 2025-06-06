## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:8342ac379806774eda48358a696a1370ef402f234923147bbd6c96bb3956b03f
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:e1a72d8e79a5274eec01626d6fef5b0da888d0f5f4c5c0013610e2378dc8c4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40832705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c0c71e1db7a6abc8494fd0867bf72ce2591f59e237a56fff25b9b615133f8e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:255b765a7ce76688b1daff4b9c1806ca74c403ea40c23478f42c66884396b228`  
		Last Modified: Fri, 06 Jun 2025 18:01:10 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2a5bbbf1875dea51527f61a56b0cfe632547a524f152311b0b8f81bff9a5b`  
		Last Modified: Fri, 06 Jun 2025 18:01:11 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c40bc0525899704934a31fe8dd9cdff1ce6ce4e3593cadb1214441930c502f`  
		Last Modified: Fri, 06 Jun 2025 18:01:19 GMT  
		Size: 3.9 MB (3916518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ac2b12d05e15108f8e5f8078d3befc0868eeccb677db52ba6fffe87ba3b34`  
		Last Modified: Fri, 06 Jun 2025 18:01:11 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb0a21a75043d61e1ea4d5f708fe46a166a7fcf895b0412fa4b7eff17bf7c9f`  
		Last Modified: Fri, 06 Jun 2025 18:01:11 GMT  
		Size: 562.1 KB (562105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b02a8a84d71507eef6798bba0a29bf99e34bcfccc841c90427680c17cd5e50`  
		Last Modified: Fri, 06 Jun 2025 18:01:11 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:1c9fdc5647f88550a10f35d30f10674f0616b26894f2970bae22d0af4e852af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deee64c4e91316bb4325d6402f0036b36fbe6017e30dba77bdbe1fbe32a7258`

```dockerfile
```

-	Layers:
	-	`sha256:24da2f55b3c675d36862f2eeaab9431c50faa6e2a5b132a44412ee4e2bdb191e`  
		Last Modified: Fri, 06 Jun 2025 21:49:18 GMT  
		Size: 32.6 KB (32628 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:ed8af0427d4116e7179b030adb53097b03a0555ab89429206a210292f8e47fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39387713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67075ab8c6f23b8b986c2180e96e0f2fa9016452a02c264f72ce9559b735e383`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:3bfe3aad02f51d0e8eb7c672608e26a55405573ddfabcf2f5b0e46bb31cc06ac`  
		Last Modified: Fri, 06 Jun 2025 18:40:59 GMT  
		Size: 1.5 KB (1496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110def64e5a43b3073349c316c03bddb3746fba81cb50a4f5286442a83a2a3ff`  
		Last Modified: Fri, 06 Jun 2025 18:41:00 GMT  
		Size: 562.1 KB (562112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92a11b1ffe1719a57f520ce27e32b6a1896cd619f0e09e07b18053cc3f79ad3`  
		Last Modified: Fri, 06 Jun 2025 18:41:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:a16f95a9eaefefcd9b8c2248219b8b22217d8ebb0e76a9a36a73e3b608167a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f347438348f47efee366d825e7697781763290f5ccc7503cd1f84ba86e715487`

```dockerfile
```

-	Layers:
	-	`sha256:b74967e198ec07a431ffd3dba499bad18b8d0d7784fe4e2ae5cebaec095a5b59`  
		Last Modified: Fri, 06 Jun 2025 21:49:27 GMT  
		Size: 32.7 KB (32727 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0e9bb64d6a4600fae859ca5654aa2260a074e1452c2a1aa781033abde8dcd6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38183174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990dcdc837ee08ca5bd638a7044d065e16ac79a230ee003f22255b73546ae0a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:af4fcae847eef1495fd95ff5002991b3f372f248204c4487c05a1dbc93dd9ecd`  
		Last Modified: Fri, 06 Jun 2025 19:46:39 GMT  
		Size: 1.5 KB (1490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f93b1edf7af5c2cdbd7e1c364448a76adf9b25fe191ab5ccf0d21e23ab34e9`  
		Last Modified: Fri, 06 Jun 2025 19:46:40 GMT  
		Size: 562.1 KB (562108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ba66547ca76c5a9e132244b97b49ac4b5be12018e00a384dae0e3b922f07d9`  
		Last Modified: Fri, 06 Jun 2025 19:46:40 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:3a1d4137865f23e7236a97275812f092acc153b70980f49da6d545a4e6b4daf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8608328d011200eac6a6f615c24922a9bd893289b05755650e15aa0340c1ddf`

```dockerfile
```

-	Layers:
	-	`sha256:99ed2d9f79bc9b72d3c18e5bfedc06b7aebf3e907a5eefdc1c9de34986ab4fb7`  
		Last Modified: Fri, 06 Jun 2025 21:49:30 GMT  
		Size: 32.7 KB (32727 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:03bc124f54b34770b3ce64f1a64a6c5b08cc86758321a7590bafdf1cb0862192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40803575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c1077e4cc3354bdc7019f4cb1d8f55c238b80198af2daae9f94877b771214`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:3ab00fd23d1d48828a815e6c2488f2335302a8a3e253a844382ba6663a084db4`  
		Last Modified: Fri, 06 Jun 2025 19:49:50 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2f184c9e96794a2bbc4601a26ff48ff7bb94628d57d8f467f8269e62de4b47`  
		Last Modified: Fri, 06 Jun 2025 19:49:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44596777470717818f830830ba06cb08da8e107e19ec3b74c6dec697d316350`  
		Last Modified: Fri, 06 Jun 2025 19:49:54 GMT  
		Size: 3.9 MB (3914794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d90985f4f4f168ea32c19335c1fc00ddee766708bc4412a7ecd329bb6efb6f8`  
		Last Modified: Fri, 06 Jun 2025 19:49:51 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04a19d2bd4063ba3b204682ef6b56082f54ed59b81dcbd8a6ebc6ac59a8b5c4`  
		Last Modified: Fri, 06 Jun 2025 19:49:53 GMT  
		Size: 562.1 KB (562107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c219c5a701a501615aa2447de94d79b77f77538a2615e1d68d10ea4861a7064c`  
		Last Modified: Fri, 06 Jun 2025 19:49:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:eed0cfc5cf2b4c1b840a63280810c13b5f9308a416e5b847024c1a7536c9f67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabc2e66e875d158f758668c22237afc58d133ae3db52459692b63c0eb62283a`

```dockerfile
```

-	Layers:
	-	`sha256:2d41bc524f4741b9b725108839c59c170f236aef5a54753caf40df4d7706b247`  
		Last Modified: Fri, 06 Jun 2025 21:49:34 GMT  
		Size: 32.8 KB (32753 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:6c8711b30bc7eb5438ec8763791cffcfe8d52aa31671ea182c0f089bad2a9d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40958304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a00cda31ca8609e515127cad3fdce4166c0dacb944d1a42c4aab23925cdc6`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:e55abbe1040e571d2632b02c2cbcef22fe8dcf6a5109bba05a147ccecc92f5c5`  
		Last Modified: Fri, 06 Jun 2025 18:01:14 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4403cdede1b2d6a24bf2e29ba62dfa1a21453a9557824bdb48e6883e5b37991e`  
		Last Modified: Fri, 06 Jun 2025 18:01:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9c87a43bdf9398ff24b62ae5b20cce368b338ac713395356f266b55b415a61`  
		Last Modified: Fri, 06 Jun 2025 18:01:17 GMT  
		Size: 3.8 MB (3781295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce8e922acd2bfac1c21e4c33eac0ef8a9ec14bc7d042fcdb76e893eefd05bf8`  
		Last Modified: Fri, 06 Jun 2025 18:01:15 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17850ebdf81ff8ea4838da388491de144bd887e07ae8500efb165ed77cf11cd`  
		Last Modified: Fri, 06 Jun 2025 18:01:17 GMT  
		Size: 562.1 KB (562108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b0f3e3e3331c9c96a8649264dd23911ea5aed815c864173f27c0e542ab9e2`  
		Last Modified: Fri, 06 Jun 2025 18:01:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:fae07da12c5b2722686df16e133a10c6517a1d7d4432db1f8c2fbc93d62633cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6dfbb335ac73ce20e900c7389610a72678a86370347285caa91d8326b08bd9`

```dockerfile
```

-	Layers:
	-	`sha256:1419df8f1fafacf7ee3301ccf1ec433cbea40ccdcdaf603ec8f76c8ed919371c`  
		Last Modified: Fri, 06 Jun 2025 21:49:43 GMT  
		Size: 32.6 KB (32599 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:e684092bae64bef7693ab236dc3b23989dae32387acda3a5e5963417469b6b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42066822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce950c888480f355ec8c330df3b061ae9593dbfcc38327f79db3d2658ac1f438`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:cb090c7a5cfc04cd4883aa9e43a7749f64d0cda38233f3c19393a58595ca816d`  
		Last Modified: Fri, 06 Jun 2025 19:14:32 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91294c186c6056f402e89191b8f08797116eec555a9b3daa9513543cb684dfde`  
		Last Modified: Fri, 06 Jun 2025 19:14:32 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525d527173a1f179c15f14a350e1a489a858bd91abbe00e78fead21f8d643707`  
		Last Modified: Fri, 06 Jun 2025 19:14:36 GMT  
		Size: 3.8 MB (3767423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7492ebd027333504290d018ef5104dc685b59872b9cdf50b83a29f78b1abbfa`  
		Last Modified: Fri, 06 Jun 2025 19:14:34 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df910a8780ed42d1c9ebf91b5b458ffe3941d7c7da6521726b4f8918b338705`  
		Last Modified: Fri, 06 Jun 2025 19:14:35 GMT  
		Size: 562.1 KB (562110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5892e478789b7315951ee7d0a6f25f6073695a1ebe4239be9e5b6c269ef158d`  
		Last Modified: Fri, 06 Jun 2025 19:14:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:2ce95fe7380a82a9529bc25453589f8661db7cf90f10a1d21233d87e8fba1b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f3fd972a450709864708279f6f53ba8c9a18551be8ee86076c2cda745046fe`

```dockerfile
```

-	Layers:
	-	`sha256:a634043e4a1eef6f7dc7bbfd087fa73b8a3b05d1e0ae56a772eee02d924228ea`  
		Last Modified: Fri, 06 Jun 2025 21:49:51 GMT  
		Size: 32.7 KB (32666 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; riscv64

```console
$ docker pull adminer@sha256:bec9ded3ff8d1c31f7be9ffb59780d8e8c01d52561b21a0220dd88e025ef4961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40609710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48737833e2b82a18f7d7859d12af6fd8fca59d81efa5cdaf33ec43b9f7f88aed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
ENV PHP_VERSION=8.4.7
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 25 Feb 2025 18:11:45 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:bc7dded31b773711a788c2eab0f221deacd79decf3fe775a18e0e4d969e36d3c`  
		Last Modified: Fri, 09 May 2025 15:57:46 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9677f42355c2615609ec9bece6a1c9ac22f749af7233ddc1e2f77553cf07f`  
		Last Modified: Fri, 09 May 2025 15:57:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0490b00c6eb3e226ee8f00d20317d57a706f99b7beca692c3f91cb5eef44fa`  
		Last Modified: Fri, 09 May 2025 15:57:48 GMT  
		Size: 3.7 MB (3672496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2c0d3dd91ad434529b421bea445c4dec3add8b3baa31cb5c50dd8e0860c14f`  
		Last Modified: Fri, 09 May 2025 15:59:04 GMT  
		Size: 1.5 KB (1495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c07464b08e6abd09a94470c9782847bd0e6415d81094d43a54e58716292227e`  
		Last Modified: Fri, 09 May 2025 15:59:04 GMT  
		Size: 562.1 KB (562112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5612ee963ac529ce2b25415467b1d0dc89cd2ed845f032d2905b4ab983491`  
		Last Modified: Fri, 09 May 2025 15:59:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:af0c07af5d2b805d135a82fae7e0e7e61d7efc869af4ab08d4aaa18f448d9a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2e29fab1dc2c891fcd96fd6a71a8689c47404bfc639c7d34be62d12c150f4f`

```dockerfile
```

-	Layers:
	-	`sha256:46587c0eadbf2efbb57c6aad1837e616e0b93025cd2e83c2320d0e8726f76cec`  
		Last Modified: Fri, 09 May 2025 18:48:40 GMT  
		Size: 32.7 KB (32666 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:101588f61382ab8a36e9aa9c751a969622c59775e02e326d02b1c04f723a80dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41562676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93e851406ac88ffec1eaecc1c2c5eed74de0e2e8b84a5f7a9ddced826189654`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Feb 2025 18:11:45 GMT
WORKDIR /var/www/html
# Tue, 25 Feb 2025 18:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Feb 2025 18:11:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Feb 2025 18:11:45 GMT
CMD ["php-fpm"]
# Tue, 25 Feb 2025 18:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Tue, 25 Feb 2025 18:11:45 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
	-	`sha256:e973fc5cb14ee7de0390cfcb2a1fea3fc87a7ed35fdcbd75dec3b9574499cac7`  
		Last Modified: Fri, 06 Jun 2025 18:56:18 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52516e79abf006423ac19163eb456f41beda632254b01c9790045fc06d2fc110`  
		Last Modified: Fri, 06 Jun 2025 18:56:17 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa63bacdebdb1073af63dfc94458b8b2768d87035af0b676578e0ed43fe094`  
		Last Modified: Fri, 06 Jun 2025 18:56:20 GMT  
		Size: 3.6 MB (3598846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226a6a37b9b2882ac7733f42f8eca1a10b9c037004f1dcda024eb42bef3db162`  
		Last Modified: Fri, 06 Jun 2025 18:56:19 GMT  
		Size: 1.5 KB (1496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfb9de62de9bdc565c8fa48a6560280017c26d065623b133d9ac0d25a1cf37f`  
		Last Modified: Fri, 06 Jun 2025 18:56:20 GMT  
		Size: 562.1 KB (562108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba647d281e12ef978905a974a1519061cded6d6e2e600e9d21f6e237534b1d6`  
		Last Modified: Fri, 06 Jun 2025 18:56:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:4-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:95469107119af189c19d30feed1259ed9e76b606be587086ed9f785e4310c050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b500d7aaf955152f0bc6d82ce724e120e0503648d99662f93fb58191b924e1e3`

```dockerfile
```

-	Layers:
	-	`sha256:ce92602edfb81f2b215b1f1dc0df55ecbc8fc5ea40be71b4c13a44dcece421ac`  
		Last Modified: Fri, 06 Jun 2025 21:50:04 GMT  
		Size: 32.6 KB (32628 bytes)  
		MIME: application/vnd.in-toto+json
