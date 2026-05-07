## `adminer:latest`

```console
$ docker pull adminer@sha256:1c2c6052a0a07d02749d590765ebe5591b8d2b7f337c9b727c9ccf31f7f3597d
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

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:d6113021d369b3d07ccd9c33ac9b21a29bebe7c6c45a6cf1f3855f6b86d62771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46627659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1460ab3cacda3a566ab81e09bb5423b7446234bd09858dad30420885d5eb927`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:40:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:40:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:40:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:40:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:40:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:40:19 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:40:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:43:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:43:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:43:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:43:47 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 17:16:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 17:16:25 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 17:16:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 17:16:25 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:16:49 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:16:49 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 17:16:49 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 17:16:49 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 17:16:50 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 17:16:50 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:16:50 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 17:16:50 GMT
USER adminer
# Thu, 07 May 2026 17:16:50 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 17:16:50 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f6427067d398d56bdb73f7154611cd5706091f1d4914d7e0d9eba3227a841f`  
		Last Modified: Thu, 07 May 2026 16:43:55 GMT  
		Size: 3.6 MB (3587637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd898383974c869fb3feb5ee8d3ec3ef57ac9121ad9927246a044e008e81b9b`  
		Last Modified: Thu, 07 May 2026 16:43:55 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f44699c055f3c170afd35bcd1657e007ad8c9cb712de504db03b5bf5b9db5f`  
		Last Modified: Thu, 07 May 2026 16:43:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610bf841e250ce22fe6049daff36a88ccf7b4b15db0c21ebc9848e61270aa696`  
		Last Modified: Thu, 07 May 2026 16:43:55 GMT  
		Size: 13.7 MB (13742469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5aae6ee556f99534b74a8b62b69a6db61ae59e94b0e7035575336098e3a660`  
		Last Modified: Thu, 07 May 2026 16:43:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad35937783d5b365b0a558dd445920989b5d3a1be9aef7b7b2cfd7d5bafd8d4d`  
		Last Modified: Thu, 07 May 2026 16:43:57 GMT  
		Size: 20.4 MB (20360133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4364559f537b569c7005d755caae684939155bf482e9eea4a450dd15106cbc67`  
		Last Modified: Thu, 07 May 2026 16:43:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5df58c2be1f3405ff092e6011832afa5564c95be2f29c2493a457c1a6e4c1`  
		Last Modified: Thu, 07 May 2026 16:43:57 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d8410e6e11b97ed460aa3d9481ff725560d9110b172ff7ca972c32557c4aa5`  
		Last Modified: Thu, 07 May 2026 16:43:57 GMT  
		Size: 23.4 KB (23397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aa97d0990d69feca7de95be8a05504a0e4e49b6c15671f6a54c3672a4e923c`  
		Last Modified: Thu, 07 May 2026 17:16:54 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364cf86cee974b52a2bcf5cef41f2afca619451a650e9ca642b51b66215fcf2`  
		Last Modified: Thu, 07 May 2026 17:16:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3a539184ba7ae64efbf1dd9b78408a67197bbc619008ffd6cf15783fd9465e`  
		Last Modified: Thu, 07 May 2026 17:16:54 GMT  
		Size: 4.4 MB (4373344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a003e2cdc5ce9b609f3c2b4221c27fec183f3352e2a56f66616db96466c99445`  
		Last Modified: Thu, 07 May 2026 17:16:54 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e8c9749c589d2ed089b61f85db7da309da8a6f2a6922945cccecf47dc19f28`  
		Last Modified: Thu, 07 May 2026 17:16:55 GMT  
		Size: 645.4 KB (645389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be52852a197f36faadb6a76584e5b151e01a3b870093816c9e12c9c7899009`  
		Last Modified: Thu, 07 May 2026 17:16:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:32653a57d2ff6b81af986e31181cf6356b7b953446cb89078b4df2cfa5e084f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4b9a7bae17bca0966180e02adda69a29e974975d81445e906730dc487945ec`

```dockerfile
```

-	Layers:
	-	`sha256:576fee9ce021af28154dadac7a59795ebc53458c4721f06643cbbc814d9fa4fa`  
		Last Modified: Thu, 07 May 2026 17:16:54 GMT  
		Size: 35.8 KB (35834 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:19bb3ef314686a420ed8a01c00ffda648ca96a472cc9a9c28775bdaf43aa5e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1b6b3bcfff63027126faa5a2481f6bc7fc87bf436892dc77baf7b22704494`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:39:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:39:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:39:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:39:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:39:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:39:22 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:39:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:39:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:42:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:42:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:42:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:42:25 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 17:14:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 17:14:58 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 17:14:58 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 17:14:58 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:15:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:15:36 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 17:15:36 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 17:15:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 17:15:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 17:15:37 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 17:15:37 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:15:37 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 17:15:37 GMT
USER adminer
# Thu, 07 May 2026 17:15:37 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 17:15:37 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481a6ef188cbadae240dd24329a9d4de57c397503c832e6c0437ab984883a7a4`  
		Last Modified: Thu, 07 May 2026 16:42:31 GMT  
		Size: 3.5 MB (3543635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44245e73fa1f91920dfec03a20f6fd1b5d3ba5514ff1f4c0951fcb583ec3d27`  
		Last Modified: Thu, 07 May 2026 16:42:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72226e283553dd6b2812a106f2c16e59e2d8621042e5b1c7cca82c71edde63b`  
		Last Modified: Thu, 07 May 2026 16:42:31 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfca358fb0e4fe0d23542ef5e2708cff1c94ba5a541bf62a5d27d40b4a8e6a01`  
		Last Modified: Thu, 07 May 2026 16:42:31 GMT  
		Size: 13.7 MB (13742477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbe550befbf1bebe37741bc40c8e6901c4343d3132df4896162a3ca3686d7cd`  
		Last Modified: Thu, 07 May 2026 16:42:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb682b3986db907f13ff9b14d04dbbfb1859431c489dfd094b212e0314be1ed`  
		Last Modified: Thu, 07 May 2026 16:42:32 GMT  
		Size: 18.4 MB (18384409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486c244ffc666147502a67222ce970027713c9ecd21766d39ac04284fa9210c8`  
		Last Modified: Thu, 07 May 2026 16:42:32 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07cb77b07a4db29e4b4249f5092d5b26f9d1e5be9ea092f3ec4206dbf80fb5`  
		Last Modified: Thu, 07 May 2026 16:42:33 GMT  
		Size: 23.2 KB (23199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946de4248ffe56e60adf6c112cba1eb3445eaa706ee0b6da45d9341c6167ccb3`  
		Last Modified: Thu, 07 May 2026 16:42:33 GMT  
		Size: 23.2 KB (23221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f19a05c2c42e78d3a98e2fc0977dbe845135af3aac6759ea3edc5eb6daf80d`  
		Last Modified: Thu, 07 May 2026 17:15:41 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e579392faf8ef6d83761439739ad10a35a6136b1accac50084682c3a77084efe`  
		Last Modified: Thu, 07 May 2026 17:15:41 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b246a36184efc6e0bf176e253cc4464d759fea145f9545d6c97ed63bd2d704`  
		Last Modified: Thu, 07 May 2026 17:15:41 GMT  
		Size: 4.0 MB (3971042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cd3e74c91b2d26f906ce65ccfe51802ee84386bf44da22085a5355a9e5ccd`  
		Last Modified: Thu, 07 May 2026 17:15:41 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e04d85047facf4bc09ad4928fa170d6b7a24198c18a04fc4bcb24b1521e8c7`  
		Last Modified: Thu, 07 May 2026 17:15:42 GMT  
		Size: 645.4 KB (645390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40afde23f0e8f12f85a1db4dc95f2d4ffcf3450733bbcf26eb29c3011f24af`  
		Last Modified: Thu, 07 May 2026 17:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:82109596a187303179372a8b21783087ad187c8a6ab87bd179320481a82455b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70b38f989a9b88ebf78bd7eb165536f073f98222e2207c3b17ad3701fc37cfe`

```dockerfile
```

-	Layers:
	-	`sha256:599b4ce4ceb7b738bf643f44ee259634d44fcddad52da2e16f6f4d4f396c5151`  
		Last Modified: Thu, 07 May 2026 17:15:40 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:3b875cf849062d6a5f963eb917e0f0452d35b63def0da140458900cd83fe164e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42450106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decad384d13c7b95aa6d43fefb61d053ac3e9842cacd47532dc5a3fa7ecea05b`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:47:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:47:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:47:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:47:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:47:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:47:20 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:47:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:47:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:50:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:50:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:50:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:50:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:50:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:50:31 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 17:37:12 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 17:37:12 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 17:37:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 17:37:12 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:37:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:37:48 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 17:37:48 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 17:37:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 17:37:48 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 17:37:49 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 17:37:49 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:37:49 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 17:37:49 GMT
USER adminer
# Thu, 07 May 2026 17:37:49 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 17:37:49 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20155a809a0693a3fe4ceca0dc180e7ceece52a8760c2eb8ba1012be67a4792`  
		Last Modified: Thu, 07 May 2026 16:50:38 GMT  
		Size: 3.3 MB (3343507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bd90947ec7a552943f764018a154b336c9a788f79e1c62ee67655363deb977`  
		Last Modified: Thu, 07 May 2026 16:50:38 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb23e7a6e34e15503f3c4e189c7fbd4ec0725e1f73a4bb816e3647f3d57cef4`  
		Last Modified: Thu, 07 May 2026 16:50:38 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61149dc7aa910303aedd7da289d47efdffc4c157d60c0d565fa60d4c07341a`  
		Last Modified: Thu, 07 May 2026 16:50:38 GMT  
		Size: 13.7 MB (13742489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876cb9fdf869823ff84868376700e8beda2639e9eaf44c9be0729e525742f314`  
		Last Modified: Thu, 07 May 2026 16:50:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b781f1f022fbe3d36b26e7f2f71903d5b28c8d4493ffbc4b67c7c7bdbe5b504`  
		Last Modified: Thu, 07 May 2026 16:50:40 GMT  
		Size: 17.3 MB (17338814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9b3b557a71b94270035226ae5138cde9414584986dc2d9cd9e12322b106a0f`  
		Last Modified: Thu, 07 May 2026 16:50:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11fedba482660f09858914eb9c7295105a32e728f42554b295625a9dc2b48e7`  
		Last Modified: Thu, 07 May 2026 16:50:40 GMT  
		Size: 23.2 KB (23212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2c33a490dd8d99b62edd980a0d88fa4eb44411ba68eb18300e3ac1330d714`  
		Last Modified: Thu, 07 May 2026 16:50:40 GMT  
		Size: 23.2 KB (23229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150c39232175906a5943493d50699673d60ba73adabc49f9b6c1d52a1ab1087d`  
		Last Modified: Thu, 07 May 2026 17:37:53 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e17c5781e14037858cd6c7df3a05047333d9dcc1a7e7cd38b37f3c2e93cda2`  
		Last Modified: Thu, 07 May 2026 17:37:53 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de47ee8779fcde74e084f660a8f157d2d0bfc39683fa1add464472cfdf886216`  
		Last Modified: Thu, 07 May 2026 17:37:54 GMT  
		Size: 4.0 MB (4042639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd1d1c7d968570bf5ef38e42109717a2da9e529b9c0f820cee526bbcf1b9b3f`  
		Last Modified: Thu, 07 May 2026 17:37:53 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90a1dc07b2243e9847c65e04ebb23f4641898fa3c0582a1b9aa5530aeb69ce`  
		Last Modified: Thu, 07 May 2026 17:37:55 GMT  
		Size: 645.4 KB (645383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1605d4c91fcaed1469d5ffbfb8bdf0a8743bae7d718d8872cc11a682d63569cc`  
		Last Modified: Thu, 07 May 2026 17:37:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:a076d88146acdb4477779b405a3b35decce60cf7504e035868bfd84c83582315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d78f528d61a8eb90168e9602a47c13e1f0551745ddfcc066e2a2df51695816`

```dockerfile
```

-	Layers:
	-	`sha256:3257e2f5f5de8ab4cdc7cbaa9cc191a20a29513767ef336e4a635d705cd12228`  
		Last Modified: Thu, 07 May 2026 17:37:53 GMT  
		Size: 36.0 KB (35969 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:cc03482b84dd096e83f61b7e41e04a793350e1772252789328c74b390da8b934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46328124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cab0a21c0b42d62d2e2ec9461df3208a2397f68b70ac9fdefcd0008ed80fe1`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:40:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:40:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:40:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:40:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:40:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:40:12 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:40:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:43:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:43:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:43:35 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 17:17:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 17:17:39 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 17:17:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 17:17:39 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:18:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:18:13 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 17:18:13 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 17:18:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 17:18:13 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 17:18:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 17:18:14 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:18:14 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 17:18:14 GMT
USER adminer
# Thu, 07 May 2026 17:18:14 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 17:18:14 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f37790fb7ad837034a930926ca6d0fb8b19d312645f4924c05d42d07abb860`  
		Last Modified: Thu, 07 May 2026 16:43:42 GMT  
		Size: 3.6 MB (3596136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322b00db5154bc88b0f599823b2f2cb63eff5b4a7907e9c953af54494817f84d`  
		Last Modified: Thu, 07 May 2026 16:43:42 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d64f77f4c2794b7402a85f0ef4e4058208f60a1f9b509ea00515a8b6a00df`  
		Last Modified: Thu, 07 May 2026 16:43:42 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7acf85159482983f4ab70a6e7778082351561ffe22c39f4986b11aad92b96`  
		Last Modified: Thu, 07 May 2026 16:43:43 GMT  
		Size: 13.7 MB (13742473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac7c6dd1f007bd57e53a448a41f5bc876c6a7670e00e04d1f4df9f0c6b3e99c`  
		Last Modified: Thu, 07 May 2026 16:43:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca9b9017e031786bfd6aa30be7d540828d1a90053ed3b9c084441433bfccc17`  
		Last Modified: Thu, 07 May 2026 16:43:44 GMT  
		Size: 19.7 MB (19723601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13db2da7fad3cce05048184e0b73c8481474b0317ac45c77c8caaf1f4043a62b`  
		Last Modified: Thu, 07 May 2026 16:43:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4246fdc8680028c8c14ba60c01ad181913e5677b66ac59e31d74f14114acc7`  
		Last Modified: Thu, 07 May 2026 16:43:44 GMT  
		Size: 23.2 KB (23215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d093598b4641d1605fb0ebdf92bc47526720e7f22afdb5dc78c8af2fc34f9b`  
		Last Modified: Thu, 07 May 2026 16:43:44 GMT  
		Size: 23.2 KB (23228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78511a069cf0b6813bb2260fcc11c64ef45dcfdddd8c623e4e613ca6e287fe58`  
		Last Modified: Thu, 07 May 2026 17:18:18 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b518bb5216d152fdc033f231b0583b4a047d7f74dad238e5d4ba21b79be7255`  
		Last Modified: Thu, 07 May 2026 17:18:18 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d8571c9d855adaa11e2a8309a467e700d55000d68ede01a780ae33dd95bc9`  
		Last Modified: Thu, 07 May 2026 17:18:19 GMT  
		Size: 4.4 MB (4366503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c23ce3bcd8ebf82b943cf80b6df5e1f2e6ea6ef7b72df06b252b6ef1a15ead0`  
		Last Modified: Thu, 07 May 2026 17:18:18 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d79c62fab1a2be40dbfa3de25ba5c5cf3b07d8cbe085baf5bee1d73cc25b28`  
		Last Modified: Thu, 07 May 2026 17:18:19 GMT  
		Size: 645.4 KB (645387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4c40fb3cdc4d72e8965ce9f5e4f4a54e519b7caf8b0df8b27ddcd928d54779`  
		Last Modified: Thu, 07 May 2026 17:18:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:2b316ecfa89ac242b3634c79de8e008a8045151d6d3ecf708ac70231bff1dfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3f73bccdaca834772272d442d3f46990a145940958b2a5a861403f63b6a85b`

```dockerfile
```

-	Layers:
	-	`sha256:a05ede44aea7f8fef3030c81097908356365357e73672efbdcedd8226bea4acf`  
		Last Modified: Thu, 07 May 2026 17:18:18 GMT  
		Size: 36.0 KB (36007 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:da3766c379c40edc2d3c218ac257f1d67983b71ce61c774d5ebac453dd75042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320b2130169d11538c20b6380375dc56231f8d3e76e4f57c26d0a1f32d9491bf`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:39:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:39:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:39:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:39:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:39:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:39:56 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:40:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:42:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:42:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:42:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:42:56 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 17:16:47 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 17:16:47 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 17:16:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 17:16:47 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:17:17 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:17:17 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 17:17:17 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 17:17:17 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 17:17:17 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 17:17:17 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 17:17:17 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:17:17 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 17:17:17 GMT
USER adminer
# Thu, 07 May 2026 17:17:17 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 17:17:17 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0e3bcdd80e637fd71393c9ee48b5cf290fffecf4186b9251f6c62401ee8341`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 3.6 MB (3625732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306f125d990e591b2af03bfe264b76722f88dbaa0f2ad4a7edde57fb089ffe6`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fa2cfd2c623c6e10cb3c623a86e9524ea7b9fae4aa0c1821b7bc4d1e5f5358`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8726322ad664e2b12e52d06cb0c5be9579b2999652ad4ba4cd804dfa7e77640f`  
		Last Modified: Thu, 07 May 2026 16:43:04 GMT  
		Size: 13.7 MB (13742463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424d421bb68bfb837bf677484de54443cd0d99a6b91327fe269644ed9a42eef6`  
		Last Modified: Thu, 07 May 2026 16:43:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1633ecc160cfe80f5e34b901e080d321492b4f19b9c4572ab88b1bb6b8b65e`  
		Last Modified: Thu, 07 May 2026 16:43:05 GMT  
		Size: 20.8 MB (20760818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dc2091c90cfb03070867d42d3f93bcda6e5a8ea51bc0ce7fbb020d115f0fff`  
		Last Modified: Thu, 07 May 2026 16:43:05 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa692d2dab3a5a5169f3edb8215613db199629ce798804b7e8469e94998d17d`  
		Last Modified: Thu, 07 May 2026 16:43:05 GMT  
		Size: 23.4 KB (23390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3d940f50cd035e441038cf172fabc0ec98acd33996ea6176bace9f45e4902b`  
		Last Modified: Thu, 07 May 2026 16:43:06 GMT  
		Size: 23.4 KB (23401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d333d9af9b533b7bffee3036f4a78114bae1fc91197c8b347317aa928739c3`  
		Last Modified: Thu, 07 May 2026 17:17:22 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a164aceda95c1e8fa33ddf5cbdc05b2f2acfcea908a48a0c91cd38e65a1708`  
		Last Modified: Thu, 07 May 2026 17:17:22 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db01cade4800baa26b45788637978675a72bfac8ead2c8335024c406fff5cf`  
		Last Modified: Thu, 07 May 2026 17:17:22 GMT  
		Size: 4.2 MB (4202023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04857244e955fe09e4bb5bf396f22ab211ed4542294f3f3f8eac10b965d7f2e1`  
		Last Modified: Thu, 07 May 2026 17:17:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c3c101a29d3e5c2481b1ab6dcfcf670db1fbd1a164dc95078a155160f15940`  
		Last Modified: Thu, 07 May 2026 17:17:23 GMT  
		Size: 645.4 KB (645386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912f8305982b070e1463246346dda3adce47e7d0c830b1f6d407b9b19f896d5f`  
		Last Modified: Thu, 07 May 2026 17:17:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:7a488c0aa91624e46e172c2db256e350cb9a368f82abc61f9d7c6f71918bcd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32ed655e8f2385f5be73a40116b217413a50d59fec80b36edc5b84022db6e67`

```dockerfile
```

-	Layers:
	-	`sha256:ce100802f002bd8c6fba2a30d8bd12d6ad9181218d9e154c969f34de58c43b77`  
		Last Modified: Thu, 07 May 2026 17:17:22 GMT  
		Size: 35.8 KB (35785 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:e8ff6c6f5e607c308fa6e7d4d78daa84a71ea8228d82e93a42579ca1b3de9f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47970299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e2fb049335719702a1d03757aa92841dd72c94d3590a1caf09a2dc70351ac`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.21
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:57:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:57:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:01:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:01:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:01:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:01:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:01:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:01:49 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 18:52:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 18:52:04 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 18:52:04 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 18:52:04 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 18:53:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 18:53:00 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 18:53:00 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 18:53:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 18:53:00 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 18:53:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 18:53:02 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 18:53:02 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 18:53:02 GMT
USER adminer
# Thu, 07 May 2026 18:53:02 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 18:53:02 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeea5ff32ee1dba0a06a0daa8843c7c1d2a9bbbf75f94c37b124895ff17e31a`  
		Last Modified: Thu, 07 May 2026 17:02:05 GMT  
		Size: 13.7 MB (13742478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967ef38decddd7e18a61734284395c26dcba1c04f411079db3a41fd22f2de46`  
		Last Modified: Thu, 07 May 2026 17:02:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a26116418b1afff0ac9839bd38dc26bc1a00ac01f41ddc34614ec1ba9886`  
		Last Modified: Thu, 07 May 2026 17:02:05 GMT  
		Size: 21.7 MB (21651094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee0b2a0c635c416ca30b3abef5eeb6eae7ecdd9f1f0b1d3d2c451d9b22749b`  
		Last Modified: Thu, 07 May 2026 17:02:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4b13e7c20d1e71238dae2c38a1f79910a9539c3555f3e7a8ebfb6c128b0793`  
		Last Modified: Thu, 07 May 2026 17:02:05 GMT  
		Size: 23.3 KB (23275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318808986435163e82581eae5b8976ac5a6584f59a410c415c8f154282d80606`  
		Last Modified: Thu, 07 May 2026 17:02:05 GMT  
		Size: 23.3 KB (23299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd425a906164a073666c44d593637d602d2f1a17ff203012a404989e8b33c3e5`  
		Last Modified: Thu, 07 May 2026 18:53:08 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f83db5765c755eb19e48aa23e3bb422b46c50b5089336ae336f80c249b224`  
		Last Modified: Thu, 07 May 2026 18:53:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08dc2aa77aa06179f5e11983d1b59c4c80be2e45594aa90c31b760f6c08a19a`  
		Last Modified: Thu, 07 May 2026 18:53:09 GMT  
		Size: 4.3 MB (4279002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8524c6bdc2fb5c12e03d27eb7f2bd9cb1ca19401f14f79a7508576d9bcf468f`  
		Last Modified: Thu, 07 May 2026 18:53:09 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d878a137403b184426629cccebe0ef9cae0f5619e24f1ce100b62ac98459bba`  
		Last Modified: Thu, 07 May 2026 18:53:10 GMT  
		Size: 645.4 KB (645394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d1e07052087e35b1e4b8887de8994fde7c2bcc541d49f0cf81ffa0b100d3ed`  
		Last Modified: Thu, 07 May 2026 18:53:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:b6e27e2ff5de8b15b47ed766c3861ee0af2ecef115b01ab0f4c9b94846f66f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee47f59ad0cddc670084481222f1d57021ac99ef964d2803fb4cf5005dde2fbb`

```dockerfile
```

-	Layers:
	-	`sha256:55a7d534d4aca653bac3f9e0ac83ec3eea0c9ea457a463237b839768ceccf137`  
		Last Modified: Thu, 07 May 2026 18:53:08 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; riscv64

```console
$ docker pull adminer@sha256:df922b64dee11a66bea72b5784a27e5164fc5ce832f26368f66fd9934ff8cb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ae7abd97ad588ce7b4cb26cfaf52bcc1ff1c368a39b5e45ecb2b1b2a5e6d3e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.4.20
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 16 Apr 2026 03:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 16 Apr 2026 03:22:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 04:20:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Apr 2026 04:20:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 04:20:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 16 Apr 2026 04:20:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Apr 2026 04:20:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2026 04:20:22 GMT
CMD ["php" "-a"]
# Fri, 17 Apr 2026 15:01:57 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Fri, 17 Apr 2026 15:01:58 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 15:01:58 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Fri, 17 Apr 2026 15:01:58 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2026 15:07:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 15:07:36 GMT
COPY *.php /var/www/html/ # buildkit
# Fri, 17 Apr 2026 15:07:36 GMT
ENV ADMINER_VERSION=5.4.2
# Fri, 17 Apr 2026 15:07:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Fri, 17 Apr 2026 15:07:36 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Fri, 17 Apr 2026 15:07:38 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Fri, 17 Apr 2026 15:07:38 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 15:07:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 17 Apr 2026 15:07:38 GMT
USER adminer
# Fri, 17 Apr 2026 15:07:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 17 Apr 2026 15:07:38 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4fa4e03a41893883792ee4048e5be20691de7211e35a2a172723216fa8a57`  
		Last Modified: Thu, 16 Apr 2026 04:21:29 GMT  
		Size: 13.7 MB (13709907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476302825d394ab9e227dbc6c9b962133bd1e7955ae20467d45109b6fcf1a7b1`  
		Last Modified: Thu, 16 Apr 2026 04:21:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae93fe850ce2d47d2ee35f5176182923589520ead281d2204695138780e440ca`  
		Last Modified: Thu, 16 Apr 2026 04:21:30 GMT  
		Size: 19.4 MB (19402167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b2ae1ce1d3db4f69133c09d447ad3c342e61000e60a7e96a98f63b06f9f128`  
		Last Modified: Thu, 16 Apr 2026 04:21:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdef2f6a8bd5d08dba71a3e4d91001ad67c862f62a41be6ed5b6ee806795469`  
		Last Modified: Thu, 16 Apr 2026 04:21:27 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7d7d89fec661e0ac7ca030594a0402d2930b68b5f619177186f8b994a43f60`  
		Last Modified: Thu, 16 Apr 2026 04:21:27 GMT  
		Size: 23.3 KB (23256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b16b2fef6338c638a3a1675e83530c8b5f8b6bec2d6dc893c0ad070be5bb08f`  
		Last Modified: Fri, 17 Apr 2026 15:07:55 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bf93ee236ca1623f5b5c6d14c711977e40eb0b63d7bb179a631bb64016d686`  
		Last Modified: Fri, 17 Apr 2026 15:07:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f942b53f3b85357d4e7a26f687f7cc0fca0847c78145f9ec37ba2cef38a1e0bf`  
		Last Modified: Fri, 17 Apr 2026 15:07:56 GMT  
		Size: 3.9 MB (3938180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337d3d5cda4f62041284c040051da32d1403f63860b7aa0fab8f77ac3dac7f1`  
		Last Modified: Fri, 17 Apr 2026 15:07:55 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc80bad11e300815ba674eac78b329a25101178fc80103d7426406f98ab01053`  
		Last Modified: Fri, 17 Apr 2026 15:07:56 GMT  
		Size: 645.4 KB (645389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452433466fb47b1382556265d855525579c05eb0ab77c54f56f3ba8cd200b5a`  
		Last Modified: Fri, 17 Apr 2026 15:07:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:b8e4bf8af1f13c3090ff147141fbd303de048143929f270f61067871e5843a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d2bcb346382709a60121035c8b0d36b28089575e91a464c31dd8c7dd2d77ee`

```dockerfile
```

-	Layers:
	-	`sha256:d0655cc5d86824426d1077287c32e32adfc3077ce2c2fd18924cf7c7e08fc301`  
		Last Modified: Fri, 17 Apr 2026 15:07:55 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:4ea897dd455739e4b6c5bb9660f45ca1229bb487594240fb1f9a9a6108fcd4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46316217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b908b5959b6d1d5a960cc244c648cc06bbe48cd840a125787bbe893e7c6cf`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.4.21
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 17:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:20:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:31:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:31:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:31:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:31:56 GMT
CMD ["php" "-a"]
# Thu, 07 May 2026 19:31:06 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Thu, 07 May 2026 19:31:07 GMT
STOPSIGNAL SIGINT
# Thu, 07 May 2026 19:31:07 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Thu, 07 May 2026 19:31:08 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 19:32:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 19:32:00 GMT
COPY *.php /var/www/html/ # buildkit
# Thu, 07 May 2026 19:32:00 GMT
ENV ADMINER_VERSION=5.4.2
# Thu, 07 May 2026 19:32:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=5b761efe7049bf586119256324fd417b49e5bb9243b40d9734fe86655e4402fd
# Thu, 07 May 2026 19:32:00 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=a4106d61bc81575d0b45c762105eead064384643418cad197a3257677625bd10
# Thu, 07 May 2026 19:32:02 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Thu, 07 May 2026 19:32:02 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 19:32:02 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 07 May 2026 19:32:02 GMT
USER adminer
# Thu, 07 May 2026 19:32:02 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 May 2026 19:32:02 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ea2d0cf7c8d85c56d1b5761b310f3a4f7a802c7a2676a20632c92e0ff9bc2`  
		Last Modified: Thu, 07 May 2026 17:33:00 GMT  
		Size: 13.7 MB (13742500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5761d591d0c4db8737496043ce4fdb6ee5603571bfc0f0479e8349e74a3942`  
		Last Modified: Thu, 07 May 2026 17:32:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd5bf04c1b54035fcdc9fd0e6e8493699b9b6fae11b04ff8ef90936f0053b6a`  
		Last Modified: Thu, 07 May 2026 17:33:00 GMT  
		Size: 20.2 MB (20205503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fd9207bb77991da5b679aa716c5307fa3fcab7fa74067effd27b1fd44255b6`  
		Last Modified: Thu, 07 May 2026 17:32:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20575b7c277d43e024d03afbd6829b098c0619a9cd95dcb38cae9d9038dbdb8`  
		Last Modified: Thu, 07 May 2026 17:32:59 GMT  
		Size: 23.2 KB (23232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356509c9cdbddf24d5c96cc13da20d82e329ec875da5973bda0c3b7ba5be986d`  
		Last Modified: Thu, 07 May 2026 17:32:59 GMT  
		Size: 23.3 KB (23252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea695bfdb607ce860ab061526bcbbc23a7511718158910462537c9589e6060`  
		Last Modified: Thu, 07 May 2026 19:32:11 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38443362441828606a6120b6c6c945357d9042b255356d4eb39e6a16390e062`  
		Last Modified: Thu, 07 May 2026 19:32:11 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c04d891fbcba65b4e27f7efb9634c6bba99abe5221ba1792fe2d64bedcda15`  
		Last Modified: Thu, 07 May 2026 19:32:11 GMT  
		Size: 4.2 MB (4154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb16acf9043080cc9ecc17111825467661de249c3edb5b4ca816b75aaf638a05`  
		Last Modified: Thu, 07 May 2026 19:32:11 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f225f95407ab9a5b086acd5a7b551486f16fb742dbd98e245d6fa8d4f5be6a69`  
		Last Modified: Thu, 07 May 2026 19:32:12 GMT  
		Size: 645.4 KB (645390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840954c053b52d4ba68ab138416145c21a303315766c29b7f69fc1812e3419a`  
		Last Modified: Thu, 07 May 2026 19:32:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:77b11fdeef40bdd626f3a42c69b2eb6e1c42e6825162e0f4bf4abeaf2d3633d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf0a8ead7704205813679eeb46f57988affbd2feb6913315cebf5f425e8935e`

```dockerfile
```

-	Layers:
	-	`sha256:a90a27214457d205bd61485f5deb49f1160173d67b129a11c0667c16f659dc94`  
		Last Modified: Thu, 07 May 2026 19:32:11 GMT  
		Size: 35.8 KB (35833 bytes)  
		MIME: application/vnd.in-toto+json
