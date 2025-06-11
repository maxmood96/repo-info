## `adminer:5-fastcgi`

```console
$ docker pull adminer@sha256:7c9dbfbb63f80fc1fea73a2dd49d997fe2f1af8644862ffc45ca57bd1fc1f6f7
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
$ docker pull adminer@sha256:b04dec2c2fd502a26d248e859062d5df25ab5c7bac12158e850d8056af8f3d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41313190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93595b3ea1880a3c77cf4ffaa0e249eaa6d2ed165bbd6f21b1bd3f779aa00b8d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f896ec01cf02db411672be62f368c6417cd797ba4ac276cb094102820fcc89`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3468343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e8913045ee8a77ff25236b174e5b5270a0420a1fe8390a3b6f8ad0e0d20ce8`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d7d5d5b71e3cd3e8d9c1684eb5d30d7429531153a8ba4053f6abcb6cf690b`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fd6c290c910b96c08d96e5cb89bed95b6128732bfad3e447c577af0fd87745`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17eb8dc33b9b4e3f65f9a6e37a480e944276361d70b0f633c3314521470638`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b900a019361d96a7f12ade9f0a4f5bfa230148a52ccf7da5245a6b195d491d8`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 15.7 MB (15706263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f524a204b4c5fc11d1551f24f1fb624e722b67f2f7b17f5e308df6778c27fbfe`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72000d5649d1c71aa1c3407ed74025a7d0b89682d49fa19b0c5ea234d44fc955`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 20.2 KB (20201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dfcfa68f8f4a3901f938a1ed50a22cbd612b6d3e4d999d59cf294898113d55`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca29c5bf6463f7d53ed40b7ab632376c694fa462bb0ec402ec64ddf68910367d`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae622f7184a5e55fb794637f843f094fca3984a52ff98d30145c12144f43a2`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbbcc7b2032b5fcbf4fc59a482d298f252bbdae58bd4434f1002a4e8cb54dda`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 4.0 MB (4029464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4676af4aaa69d3edcee1ba1c73e2d18a5d63b45e66d6652699e8aea2bc0d0`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90484e04d3839e88b89d59f1f6afbb279fb4256b561a56d2dabdaa9e1a4bd51`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 634.7 KB (634700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e493f166fb8372abc1111b24fa1a4d80ece434fc32b38de3075c24fecfef434a`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:68f2af35852bf9186bbd5effa4d99f3a10bba23c8ecd7312bf14d346918254e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8747cd24a1e9cfe0c106871014008eb396e84de41320d43b899253cc2dede11f`

```dockerfile
```

-	Layers:
	-	`sha256:f7471fd721d540cec6721a64868ba0e49ae8bab44aa31070f5e06207950e0834`  
		Last Modified: Wed, 11 Jun 2025 03:49:20 GMT  
		Size: 32.9 KB (32923 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:562473666cf8919dd4f99b8d2cf2e3769d01c833c2f2869adcf6551a9c9a8bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39071738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1268ad155cb77a1fc9dd23b91ec7c4c728ff74de690a5f86c5cbe690183cf09`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
	-	`sha256:b4687138ef1b3e99885659dae1a5cf5349f783843ae00824004e438ab7ed8351`  
		Last Modified: Tue, 10 Jun 2025 23:58:25 GMT  
		Size: 14.2 MB (14221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0744f400b10ac6f4b3cf435d4e3ef449c59b28a5999fd5b7097dff792a0ee9`  
		Last Modified: Tue, 10 Jun 2025 23:58:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e812a32f76d7ef633d060ca2ed16cc333fce43a92341c1a8285a610af3191`  
		Last Modified: Tue, 10 Jun 2025 23:58:25 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0966900079d27d1ee2bc63b304027ae72dbeffbd8c77619ac24ef0ab45b9ca8`  
		Last Modified: Tue, 10 Jun 2025 23:58:24 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca06cdf1518fdc61c1077418079358edb9fa6be6babdc965fde78f3b2d0575be`  
		Last Modified: Wed, 11 Jun 2025 01:32:53 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59686b1d96577edcc373ab5e3b7e7fd9e4ee786b502b81fb29a420c1a562bb04`  
		Last Modified: Wed, 11 Jun 2025 01:32:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792ec0754cd82e4f6a91fcb47c7b57f76d8ddcd1e81b7ff636cb7d184548315d`  
		Last Modified: Wed, 11 Jun 2025 01:32:54 GMT  
		Size: 3.6 MB (3604544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe71f4b80e15273f79a03f8b181ddcfcfb784706ce46059ce8cfccecce82fa`  
		Last Modified: Wed, 11 Jun 2025 01:32:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43211a392569debdb3e2a53f5bfd29a2bbbb77d3dee0c616c1c4abd362a27b57`  
		Last Modified: Wed, 11 Jun 2025 01:32:54 GMT  
		Size: 634.7 KB (634703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cee18fc59918f47f6b58001a13e432bd2d124c7716ab0c39c3da7399b5a557`  
		Last Modified: Wed, 11 Jun 2025 01:32:54 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:d7336bd43596a4fd3af8c178de8885396e9ab9b6b01a5ecde690bc1070f269d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5d880d0a76ae6647448e308d40d40929a797fe43b897f4bbbb272bdda9d71`

```dockerfile
```

-	Layers:
	-	`sha256:0f145147a61c8d1fcb6cbe2e35582eefd5e59d94f70d23a2226b03738bc6e5da`  
		Last Modified: Wed, 11 Jun 2025 03:49:29 GMT  
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
$ docker pull adminer@sha256:f13350ba39d18d969250b861cfb8c0edb5411c443a5489db3897027546aa5528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41442828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e978643a345897c1d678794eff7af35cd9f26b421ff03fe758dfa29ec007bac9`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527bd29aef5241e34b340256391e5f3892945ecd834ed23ada4c7a1e28fb7aa2`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 3.5 MB (3527783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6792ddea86a3f97df62a6befddf412803268834373b0ef544f3f2b1587b73db`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d7d5d5b71e3cd3e8d9c1684eb5d30d7429531153a8ba4053f6abcb6cf690b`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fccf898fdd5cbee119e3e1ac47546722e332be49a545c0148b065868494af8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 13.6 MB (13640485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17eb8dc33b9b4e3f65f9a6e37a480e944276361d70b0f633c3314521470638`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba819796aff4a25a71559119bbe3426b4c50ef8106192029b45b8c81babc83`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 16.1 MB (16099708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9356444cb387ae516483ff866b21883fdc5100d3387ebc2a373086619a18c56`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37c383a8d9cc29556868a2a8bbcfe357991e0b915aec5541a5f21adce65e584`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd78e2dbadda7fc4bb16203c0f3455586a10ffc83f774dd86fefc88251afcc5c`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053d59943c0a8ab46555841ed1666753115cf260290c1238502a6dae72a0613f`  
		Last Modified: Wed, 11 Jun 2025 01:14:20 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f6fbdab6d0cd8d12c5e290a57c7c909cd8f9a62e02d4af82e21e8af99ea6`  
		Last Modified: Wed, 11 Jun 2025 01:14:20 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bed90968b9027cc9fb6b4423131472f38bf0fb42cd0903a4d95a5f677b4248a`  
		Last Modified: Wed, 11 Jun 2025 01:14:20 GMT  
		Size: 3.9 MB (3887100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e585d4e1c23d336bc00773cd323cda36b544ed021aa07bebacf24739c02eec1`  
		Last Modified: Wed, 11 Jun 2025 01:14:19 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e96519b1b35888c819591526d28ad5564684ced6879cc479f9869263a6bf445`  
		Last Modified: Wed, 11 Jun 2025 01:14:20 GMT  
		Size: 634.7 KB (634699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c4b9412f0102c529c7799937a290202603921c765dc467f0cdf93579ea40e`  
		Last Modified: Wed, 11 Jun 2025 01:14:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:946c6ca3c0107e2f332429bf4b84e5016f92a949065aa87422730c137f9075fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5a0b614ac6d874d50073d4e850accc0b43b491e9285428bf55de184cd84bf8`

```dockerfile
```

-	Layers:
	-	`sha256:578c85c5945f28f1b25d5b617ebd1fe13bcc9fa31dc47315e714328676db2ffb`  
		Last Modified: Wed, 11 Jun 2025 03:49:45 GMT  
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
$ docker pull adminer@sha256:556d0f61ccdcf094b2f669a102bc2795c92655914ae56921f37df4d0ec776283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40685008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f98e94516e241af84bd359f4e7f1a83cec4e394a2f54970994b3313b605ac0`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:90909189cbe4016c904ae91ff7405e7d92d78374e7b624781af184d356ae026e`  
		Last Modified: Fri, 06 Jun 2025 18:33:12 GMT  
		Size: 13.6 MB (13640344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408fdc472937fd709fb9b1b23f96ac32f9d1511eb41f25c82abdce8ef2eca02`  
		Last Modified: Fri, 06 Jun 2025 18:33:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae376d1d57274f4b2b6c630ffee7004462272b9195484f5d9db54bf45e78793`  
		Last Modified: Fri, 06 Jun 2025 19:31:53 GMT  
		Size: 15.9 MB (15886201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6055b6cae2c88e482c7d68d6030bd022d12081a32d1931852203581637f8711`  
		Last Modified: Fri, 06 Jun 2025 19:31:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dca92876a2a78ee0d6980e40143d996c9a306c779ac4bc736f22da4b2b33929`  
		Last Modified: Fri, 06 Jun 2025 19:31:52 GMT  
		Size: 19.8 KB (19844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d4ed27efc535d121a5c61eb2d2355d410fcce903b092096c26bd53669bb07`  
		Last Modified: Fri, 06 Jun 2025 19:31:54 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1bccb29cda3d89a821b6609386f2abb1c9a00f6ce6712fb44f876c81492178`  
		Last Modified: Sat, 07 Jun 2025 05:39:39 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685dff70a1520e6b17e15accb245f5cf826ffa864418c8f452af12dd4065ac79`  
		Last Modified: Sat, 07 Jun 2025 05:39:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60967d3c6643be9a5b2aab1670beccba79c3426a4c49d841252bcfb2d5f81138`  
		Last Modified: Sat, 07 Jun 2025 05:39:40 GMT  
		Size: 3.7 MB (3672651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bee919bfeb34839f19637b6b290c5ca1731d9da0cc8b8c1a0895e888b71872`  
		Last Modified: Sat, 07 Jun 2025 05:39:41 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889396c336843f6ee1a58cb59c0b3bbd29dfc695c00f2f836a0f4dc304d4b343`  
		Last Modified: Sat, 07 Jun 2025 05:39:41 GMT  
		Size: 634.7 KB (634709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19442fa069c26843a686143d48d67103d346f7f087f8c336e8b5f71bae862c3a`  
		Last Modified: Sat, 07 Jun 2025 05:39:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:ddc373a88525273ae26ca8154fcd17c8b93fbe0a47343291876fa98165144608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d00e418b262e53e8c6aabc1c268b6807f6532e1a68d1ff3462de32b6fa1a476`

```dockerfile
```

-	Layers:
	-	`sha256:bac1b5fb7a44389fdb0281de746a01e15bb386a53ca547bb4ee65d1e470aeef3`  
		Last Modified: Sat, 07 Jun 2025 09:48:59 GMT  
		Size: 33.0 KB (32967 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:0dcbaee9ab50f5122f96f01db3eb0bd081731d3f7641783ccabbd81445cd1667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41293909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3617a3625974245e7ce5700b4fc286578d6997dc8768525fc719d2ea4b6b5ffc`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869e89e860a0e8efe4b13fabc220788c0f1938fe54d423cacf0d87024d0c858`  
		Last Modified: Wed, 11 Jun 2025 08:13:39 GMT  
		Size: 15.9 MB (15886808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e55c0f834ebc37dce366fd44aa345e322607bdde81376395f5739edd01046c`  
		Last Modified: Wed, 11 Jun 2025 08:13:44 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276a4796f856b8a46f6948818f7eeec7af4badd16db241f076b8cc3b9bb4f20`  
		Last Modified: Wed, 11 Jun 2025 08:13:48 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab310fd6a38773f1b897350464ee4ae855982514b7c0b268a0f5124397693708`  
		Last Modified: Wed, 11 Jun 2025 08:13:51 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e960a39aca807470c7e570a4e4879386a6c9af45d704686955a974088428b`  
		Last Modified: Wed, 11 Jun 2025 10:54:40 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9c6875e2741ecb426b6d6acf51b73f891f35f487eecc4f1cbd5fe313fbee97`  
		Last Modified: Wed, 11 Jun 2025 10:54:40 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3800e4bdc8fbf97c502e223360bb4ebc8b3f5728e785e6cb648f78eb281b1f0c`  
		Last Modified: Wed, 11 Jun 2025 10:54:41 GMT  
		Size: 3.7 MB (3748511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc3b48642261b0a62bebe18b850f6def4367a164ac36c0cae39c819bb43956a`  
		Last Modified: Wed, 11 Jun 2025 10:54:39 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884df46f27e6965d5ec9b70c7b792aa93bb3cd28729247c93f454e3399e9dcc1`  
		Last Modified: Wed, 11 Jun 2025 10:54:41 GMT  
		Size: 634.7 KB (634701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700d7f50de9e32e2a178442bd70fc5c24795d45c1420c5bc71c66ebeac1b2032`  
		Last Modified: Wed, 11 Jun 2025 10:54:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:f2e9ca218d26e30985cdbbae7755dd80e18b22daf8205aa61536b8373e6a401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 KB (32922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4365a5ab7bbe3524983ca4d6c34b043101e8c456d3659617c55769e7dcf05f`

```dockerfile
```

-	Layers:
	-	`sha256:db756f4d3bb593a295ec7c5554a9612855cde8a72577f7160d2097c23889bf34`  
		Last Modified: Wed, 11 Jun 2025 12:49:03 GMT  
		Size: 32.9 KB (32922 bytes)  
		MIME: application/vnd.in-toto+json
