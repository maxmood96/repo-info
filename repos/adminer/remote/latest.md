## `adminer:latest`

```console
$ docker pull adminer@sha256:f1a433dce87897f4c34a38d491fd3593fa141473b03904a863ca4288726d7804
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
$ docker pull adminer@sha256:1e9f8e38b2df2f3327b406d9ca10d8c163f34ac0863cec8f8fa5819d7dae3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46141440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2f4e20fd3ceb208aa3d3a950dc093bfc9c2a084dc442ce20e81f19cc87565a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1220d176a8dc4ff5bc1c09d81c91223d1db607237a519d56119410deee673cd`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 3.3 MB (3339341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c7a04f6c00070d91613ceaf576994307c0b84a90f0b1a088bbf9776a4c43b`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55cff53123d85a9177c4f1c8be768cdc148f4e75add12c2b2dac3b767c836e`  
		Last Modified: Fri, 11 Apr 2025 17:04:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d591373a1942f2bef00fa93d9a78e9ee85117617f7d4bd07858e863f6b81ff`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 13.6 MB (13634005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d32971fca8bf54c40f3af5a57e10e6c18f4586e18be60b8fd802d0b5c6167`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeef6b41a5682ccf70b716a775cc8e6f5dbf548ddec432240ec0f9bf7fb5026`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 21.0 MB (20959672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d95abe48138673ff509234f4be1d0a54c2ddcd056348417b10517a3eefcb485`  
		Last Modified: Fri, 11 Apr 2025 17:04:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d3af78a9d898a9b670384f9b1cf9632c2b68d324bd8a03779a70e8fbfd4ed`  
		Last Modified: Fri, 11 Apr 2025 17:04:15 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da433590bcdb1f51dee8267753f793224b9261aa60cab3d12d5d716c84d30da2`  
		Last Modified: Mon, 14 Apr 2025 19:07:46 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681a4eaa8c3e89e10f638fcac66c5c3b6b6b22095a42d55fc71c9eba18619752`  
		Last Modified: Mon, 14 Apr 2025 19:07:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b7dcf9097c1741c4815608c7faa0667fe08b67354426c011fbdfe6afe80da4`  
		Last Modified: Mon, 14 Apr 2025 19:07:47 GMT  
		Size: 3.9 MB (3916880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71b64d3fa1a5a8064c6fbbec536d2c1a6911ced4753d59bba253c5d2885f212`  
		Last Modified: Mon, 14 Apr 2025 19:07:46 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4048b89eff5448dd986d0bbfd5dda925768426f02f86bd33a1848ec1996ce50f`  
		Last Modified: Mon, 14 Apr 2025 19:07:47 GMT  
		Size: 621.6 KB (621616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b1fd0db08a9c10e5ec70c47821c672652fd0418d5a1caa39a0ddedeb03e4d8`  
		Last Modified: Mon, 14 Apr 2025 19:07:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:e3b002450160870765211ec43fe048e5da998d18b8476a359ea6162ab8ae3570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64653032f6e2a1bcacab36188bab186e13e25ab7244c29fb9edf17c5ddd4b93e`

```dockerfile
```

-	Layers:
	-	`sha256:83279ca05de58e65a0f51997df4d78d261e2230b44b0e1982ad2a1ba5eb5a611`  
		Last Modified: Mon, 14 Apr 2025 19:07:46 GMT  
		Size: 34.6 KB (34617 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:e49536fa1476c97b1c80e4c2b0e77269e69eafac72e9182751a1d7a618d5dc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44307478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe4385e2f6128f9027116eaa70023f471e432eb59de3272320150a7c6734f36`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99721caeced5447f0e5afae5f5f8e76005987b2b190cd4dddc22a580dfd0514`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 13.6 MB (13634008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ababb234d29b8f731d40c161eed8e52acac75254dd16fa03f85bf2beb52b5f34`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79afcfebd5eaf31b4d1c424b4505ec7745e291e9fd2b39ec55cda1ec8c511648`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 MB (19829287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac21336ef516c4563ea730b5398b5b1d7c49cf513f0387b277dc23823efc98`  
		Last Modified: Fri, 11 Apr 2025 17:03:04 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8877cd5e84c67dd2fb911e2d5ecf5a29aaac9d3fb00a134ad71f7a511402f`  
		Last Modified: Fri, 11 Apr 2025 17:03:05 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc93549631e50e7499b7efaae9003cc32884cefca27af2584eab5cb860ccd63`  
		Last Modified: Fri, 11 Apr 2025 18:08:16 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0526df450f9afce406ae161b76654f333520e0bb27ab4fb73debfff84c89661`  
		Last Modified: Fri, 11 Apr 2025 18:08:16 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069b71ba5d0b2f9c9d3e7e687b448326980daeeda192620b65e7a17865c38e2`  
		Last Modified: Fri, 11 Apr 2025 18:08:16 GMT  
		Size: 3.5 MB (3521281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e75cdf2649548a65eebe938fa083de3e8bb8de4b61043bb16e4f6fda7ea85b`  
		Last Modified: Mon, 14 Apr 2025 19:06:57 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55e18057fbf23a2b8204588f7301fbf338e26ed3536adc3fea15a47d1dc9c4`  
		Last Modified: Mon, 14 Apr 2025 19:06:58 GMT  
		Size: 621.6 KB (621624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02f7a25e585c514b065c4ef1de5ed619a6e2709264c690b6c606214ab029781`  
		Last Modified: Mon, 14 Apr 2025 19:06:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:f41bbefb75a992b43658338696e9cea26ef36c60082d9d9ba226bf392843fe75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bce0292c74892fa29dbaf14e13a61d37bc0c05de77f4578111bd7dc4fea278`

```dockerfile
```

-	Layers:
	-	`sha256:6fc5924b5b0dd42a7d1cccea1926d4f001f0ab0a51453b59b431386db2cff8a8`  
		Last Modified: Mon, 14 Apr 2025 19:06:57 GMT  
		Size: 34.7 KB (34748 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:09da00a13b3cf759c9878780b98047ec924c8103268112a2305d6625781fd1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42832667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4693b9a33f745e22e59fdecab8483dc5207813ca610c187e0d763a6ffc20f27`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1dd0d977bcb89dc169bd09934ab44550fcd7fa84e4c1a764504338b64dc02`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 13.6 MB (13634016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d041d9fc32e068941229ecca755921cb7bf3dca41459078370b44bc0e1716b`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c983ce618383841eef895256fe1429a2d6246352f469c73bc987c245f3fe6`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 18.8 MB (18750946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b81e508c642abc47048514b7828c1728c896f7e23d617c739c6ba2b340788f`  
		Last Modified: Fri, 11 Apr 2025 17:46:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032a03dd9d86c50fc7e8c67a780cfa359b696a75d57989eb073054e1649ca4f`  
		Last Modified: Fri, 11 Apr 2025 17:46:22 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d1f159553864f5804f7fec2a88c6b2840fd71861835a3de2cb8549fbca267`  
		Last Modified: Mon, 14 Apr 2025 20:14:04 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc5512279009ff14d10dc9dce6c76fdc2073a2735e47e994357720e219ff76`  
		Last Modified: Mon, 14 Apr 2025 20:14:03 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06354d91c235cdffc84754d43d283b6c5eed1563fe3ec5c253506ae56d9b4a11`  
		Last Modified: Mon, 14 Apr 2025 20:14:04 GMT  
		Size: 3.6 MB (3580054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61d2ef690366c8a6f5fcfd1209d2b9dfbdcba831ccd7b8e15d8732c3a7d037`  
		Last Modified: Mon, 14 Apr 2025 20:14:03 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ea52c56b5f014078a14997620556578ab0c20fafd94595c80effda98be9366`  
		Last Modified: Mon, 14 Apr 2025 20:14:05 GMT  
		Size: 621.6 KB (621621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798bf14d81638e28b4d10c26dd821b15994f874bb3111e2f6e8d26dd1f1b04d`  
		Last Modified: Mon, 14 Apr 2025 20:14:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:126c95a78c402a9c93a38c6f35687a87902a39140ff64d8b92b1e9c654688017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f52f6d2f24d80ebc0027357942d55bf31621142b317d2ced7d7a7747ad2eb`

```dockerfile
```

-	Layers:
	-	`sha256:0caf660a1b71bdccb63281a482b46dff602248198d3b27d3414fd6e04c5c4919`  
		Last Modified: Mon, 14 Apr 2025 20:14:03 GMT  
		Size: 34.7 KB (34748 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:0f6ecc168344bf3d330e4a0a9e53ec76701c61667173787f521f7fe86ac518d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46801812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7c8a62c220b96d0952f71c15339369a8545d1c2d43520302ba33639eec1049`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eeb5b6ce9478bd6c574eb74b77f0d1b395a57ce5b3c1301f9be9922f5b8709`  
		Last Modified: Fri, 14 Feb 2025 19:55:10 GMT  
		Size: 3.3 MB (3330757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26966b371bd90aa880696c07e5efe82fae85afb1dbbdc01200a938f225097a2f`  
		Last Modified: Fri, 14 Feb 2025 19:55:09 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8ec9c416f52d757beb3b934ea2fba8bda54f1a415fee89e3c4d7160ce5971`  
		Last Modified: Fri, 14 Feb 2025 19:55:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888604a1b9394bb976269325deda07c4d8169c4cee14278818bd445ca6ace6d8`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 13.6 MB (13634025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8095d66e8713db05b04fb8f754744cdc779ee671ef4eafa9088f937e0deaa2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cca1592d323aa0f6cb5ec07a6876179f91b2c3ce0c796933c04b6f10103855`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 21.3 MB (21279970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a8bc8a0cd49acc4449fe9f0acc592057ae29975a29d62a6d4b9afe1c096a2`  
		Last Modified: Fri, 11 Apr 2025 17:26:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d48f4eacb6f2a17df2c6b3e3bd6975606482fd0fb4085fc97fd820721682b`  
		Last Modified: Fri, 11 Apr 2025 17:26:46 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf914404d2930a7390e5ed68f353a08f25ee9078bb2df45a99ad5bf552b5aa87`  
		Last Modified: Mon, 14 Apr 2025 19:43:34 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89133d4a020cb7d339d33cd03f85a4b5386e531004da17c5afedd42c3930879c`  
		Last Modified: Mon, 14 Apr 2025 19:43:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb0929ad61943ba9428d956779b8a5a0975b5f58d8a9a49f6aab61fe95a69e7`  
		Last Modified: Mon, 14 Apr 2025 19:43:34 GMT  
		Size: 3.9 MB (3914922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68f12507580c4c235a24ab7a5f302488ab34e8dcad038ee7e0bab35e116627d`  
		Last Modified: Mon, 14 Apr 2025 19:43:34 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a1e5322b41816fa71011849295c0f43a2d3f54429579b1426d3185be537c3`  
		Last Modified: Mon, 14 Apr 2025 19:43:35 GMT  
		Size: 621.6 KB (621619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b657b18f7cccc24ec98bd265bf0b4c6096524f5a1c178a36dc9659da91b3b7`  
		Last Modified: Mon, 14 Apr 2025 19:43:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:4a34cadd4644d743e67c8c6a459109409e84b129c006b0b2bdd3d2c4c32a64a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885b8fc026ed5783c7704ae62c23939dd8e7354aca400cc5b5c528d9f9e91815`

```dockerfile
```

-	Layers:
	-	`sha256:73bb8bcc6dc744cdc9982c013fbbe58e6d359089b188f32b9b6d3dc0b5a7d69b`  
		Last Modified: Mon, 14 Apr 2025 19:43:33 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:8ce9a0da6a74141aef3b5b2c84091745b6059422f944d0382504371600048e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46386530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e491ab23c144f810e98fe7d54185e2903bc99697766f52414464c8690f091646`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb74e4e7481ac74704c80700e3c4ddbe3bba6754c002d67212ee6b4beb385`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 3.4 MB (3379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a5753b2d58bb8fc68ec945886fe7de494b5ee261438bcea8d88b2937900f34`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aacfeb7e836bafd68a68e693e0c4850fb8b6c9d73cd7122cf96cc97a7fa98e`  
		Last Modified: Fri, 11 Apr 2025 17:04:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d560359295c53bb0650cc517ca958fc15de86b2a8c983419ac2a98c51348`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 13.6 MB (13634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cae1e8a90ca6168765b32366e40a77dfa1a9f093d525668481c49b54a5219`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd190eaec27800990bf0e06d95bcfd7b1e67350f8149b0cc522ad689a26cd26a`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 21.5 MB (21478232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8a21cc6ec932ed65a9702e8a8f7f9ef56a89d9548e0c14451fba8fd364b87`  
		Last Modified: Fri, 11 Apr 2025 17:04:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5fbc1c23187c4341fbf6bb05c975aa484338eba9dee1e0d4580e88af34baf`  
		Last Modified: Fri, 11 Apr 2025 17:04:48 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0175137cd22beea0a07259e3208f155e0032afa19708c6e89213d6ea23c36f4`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb7308076d8a559f2098c14999cf7eb95efed1684fa0c9f88b3c847a22ad5a3`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df72c5c82c9a77bddf7e9310c21e4cc72c712a20c48adeb8c50ab1c9f554fbba`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 3.8 MB (3781508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629533742a772a86cf39af96b547f0b26a0d8739fbcc11fae39d09b3c66b930d`  
		Last Modified: Mon, 14 Apr 2025 19:07:51 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9980b7e69bbd355cb5acdd5a48c80e01eb2465dee63e43685728953db0630485`  
		Last Modified: Mon, 14 Apr 2025 19:07:51 GMT  
		Size: 621.6 KB (621619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c40bc77a4e0a2297c49bffe27d322d1bec045d482fa6c9307c6ed9f9def02fb`  
		Last Modified: Mon, 14 Apr 2025 19:07:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:53156603bb25f761a54e300e91bfb7ccab08bca85e59bc5ad7623796693a2bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4162894366c7101fdfca2312d30c930d1b2b1c55bd90047e1095d7700dee1a0`

```dockerfile
```

-	Layers:
	-	`sha256:388394e6a4260762c71f36a5ec81733fbfb4d7fddfc14da3c4777a6a69b51531`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 34.6 KB (34569 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddfda962b94e1d820e36074adcdc7b01988d67b0d17ced42a904a9ea584cbfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c21e9b02f24fa034aa7741396a395c94d6875534d65b188614313bb0cd0ebaa`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d560ffba9f9be51f581e9871fc30dcf9172500f0ab642bf3db44cad9005ba`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 13.6 MB (13634021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f992d633689cfd581ee2285b1814cf7241f57ab8b1e6b81ec099f7db10cddd31`  
		Last Modified: Fri, 11 Apr 2025 17:18:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc7583b344d15349ef4c186f3c70c912ed5f268328bac31fb222463f5f49efd`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 22.7 MB (22696149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e7c80238bcc2aaf108d8103d5e9a4f61f58730b25bd5e8628342c9883904f3`  
		Last Modified: Fri, 11 Apr 2025 17:18:31 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eeebd892d0ec453694a95efac3fffbf4ad8496c497175c61607f2ecac7fb1`  
		Last Modified: Fri, 11 Apr 2025 17:18:32 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d65f3aea4f11a08f294594ec244fed9e8586a8f65f1b94ed7199515c312b45`  
		Last Modified: Mon, 14 Apr 2025 19:08:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956c93bf4dd51ec709f099fd0b831dc0da0f65cd625c4c25053c1748cd0cd824`  
		Last Modified: Mon, 14 Apr 2025 19:08:28 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e83545344b1c0186966f09fe808134caac227be21c205bb4fb9d539b4b50997`  
		Last Modified: Mon, 14 Apr 2025 19:08:28 GMT  
		Size: 3.8 MB (3767573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59032e1342250b7b4bc8a18ccc7a51554c3c4fdf46475ca50dc4cab83d98848a`  
		Last Modified: Mon, 14 Apr 2025 19:08:28 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c5fd85caa3ce1cd4686786a91e5e4ce428e83be95f2167ab70f5634f8bde3f`  
		Last Modified: Mon, 14 Apr 2025 19:08:29 GMT  
		Size: 621.6 KB (621620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d63c96e785e621584d41dbe6b3b9449c27039b38f10d8910d18945b2c44ee`  
		Last Modified: Mon, 14 Apr 2025 19:08:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:b7fa2f1b11206f6aba9003470c20f782958c2e1232e4dbfd399ef10c085077db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f700c4fd8156cde86d36d35cf766ae1afe27975f10528b05f5461871393c66`

```dockerfile
```

-	Layers:
	-	`sha256:df88f2bffdc20e9bc5ea82a942bca7472dad0689ce2a899eec4a83dbe392a38d`  
		Last Modified: Mon, 14 Apr 2025 19:08:28 GMT  
		Size: 34.7 KB (34679 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; riscv64

```console
$ docker pull adminer@sha256:8e8e3e4a1af1d04edf9ae2d7bb0a8a5b8459e0e3048b453e90582fe806453771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45930249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23df82fc125d4732d44c419f52f79a4023f8c494b56ecc712d1d81df82fc891`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662ca344e9d88de4933f43573f5bd92302683f9e23ba289fa15adc11c5570561`  
		Last Modified: Fri, 11 Apr 2025 18:00:32 GMT  
		Size: 13.6 MB (13634011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf51eb817ad732be4c07beac2e2bd24ab0f70a4885ee9f0d2c8ab48de9fcce4`  
		Last Modified: Fri, 11 Apr 2025 18:00:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ebd503eda0ee80e853d7b7f7f2ab57db14d132193101730988ee556a3b803e`  
		Last Modified: Fri, 11 Apr 2025 18:00:33 GMT  
		Size: 21.2 MB (21159972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b210ca2d5b42afa75b3376214b91aca4e24abc786daf4ce705483c3a44977`  
		Last Modified: Fri, 11 Apr 2025 18:00:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4248d385c3cc30c430fb52ba6565c2400471b293f7bedf1ba5203d21b51034c9`  
		Last Modified: Fri, 11 Apr 2025 18:00:31 GMT  
		Size: 19.8 KB (19835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05207dfb5ca734eba3a29345be972515aee010f7302bd5498ab899ddeed7efdd`  
		Last Modified: Sat, 12 Apr 2025 07:32:56 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b633968f6dd4048dbb9b6d7804bfc707670d2f6586f33b4898260ab94560e71f`  
		Last Modified: Sat, 12 Apr 2025 07:32:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446e9d3beddc96bd799a08b7eace268c5254f9d2bb54dbccae533ba340f4a088`  
		Last Modified: Sat, 12 Apr 2025 07:32:57 GMT  
		Size: 3.7 MB (3672781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1bdda092211ea43760b79d3711935a3c7bece0380313d25efbf08b092a86af`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1719de9d29861bce79f6d5b031575ac82afb4d89cde70e79be121fca2486ae3`  
		Last Modified: Mon, 14 Apr 2025 19:07:51 GMT  
		Size: 621.6 KB (621623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530a6502371b61ab0c5260d5ee33e0cce3a430a429926616ea3e5745b94ccc5f`  
		Last Modified: Mon, 14 Apr 2025 19:07:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:2bbc454c015aaf6739fb4b8ff1de56c80631c30a836ffa3b6e80cb3824fda9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067863d27fc0ef03effcc9c12f9568a460bfd1707ff530230a95ee0ad8f5a4e`

```dockerfile
```

-	Layers:
	-	`sha256:cddda6e447765b09649e7e7d6eeb8e42428cd51573c89673f0ea987ceb2cbf49`  
		Last Modified: Mon, 14 Apr 2025 19:07:50 GMT  
		Size: 34.7 KB (34678 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:f456416000b7359f17b495b29a055dfd3f6897f159954ba66be00013c7d25515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad009b9512113bfa957fcb37ae7d21210e2231ea75679bd5668703018b39386`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 21:29:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 21:29:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_VERSION=8.4.6
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 10 Apr 2025 21:29:12 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 21:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 21:29:12 GMT
CMD ["php" "-a"]
# Sun, 13 Apr 2025 17:14:08 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
STOPSIGNAL SIGINT
# Sun, 13 Apr 2025 17:14:08 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
WORKDIR /var/www/html
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	mysqli 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del --no-network .build-deps # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY *.php /var/www/html/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_VERSION=5.2.1
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=572118dff2305f136a4b8d59404d01c3d8450e99e3abd506081ffdddd8816573
# Sun, 13 Apr 2025 17:14:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=64e6b6c9e049ddab694cc8793485f1f1888abaf70ab5a389544c0a1b2926bed6
# Sun, 13 Apr 2025 17:14:08 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
COPY entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 13 Apr 2025 17:14:08 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Sun, 13 Apr 2025 17:14:08 GMT
USER adminer
# Sun, 13 Apr 2025 17:14:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sun, 13 Apr 2025 17:14:08 GMT
EXPOSE map[8080/tcp:{}]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253288de5d5858d726a01e6fb54a8ce6491ee7ad88813406dc682b718a6163b`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 13.6 MB (13634013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846313eea72572bda46ef3194365448f1a2fdab2a7deb8841505aab296e073b`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d736c19ef542a7d956977a6db29f925772110f918ded10ffb8282b3f50f8be2`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 22.2 MB (22245742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fa64006fe97a6510fae87802b4557cb08e694bd5a35f57ffe86329d91b09c`  
		Last Modified: Fri, 11 Apr 2025 17:18:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439851fb90b80ae0219c17f42cacc625081cc820846b5e2cf91af178f478a1d4`  
		Last Modified: Fri, 11 Apr 2025 17:18:49 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5073f60454bd2f4c31b4918374142ffd50e717cfa6ec661cf408b52b06e58626`  
		Last Modified: Mon, 14 Apr 2025 20:04:52 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f42f0256dac8afa5cc37ddefe9de2b2f6846f69a28f17a660456ac75ceb6d5c`  
		Last Modified: Mon, 14 Apr 2025 20:04:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fba46727a7b484f66855fbe8d7a4999361704c341ee236b6a5bfe6b295fc7b`  
		Last Modified: Mon, 14 Apr 2025 20:04:52 GMT  
		Size: 3.6 MB (3598909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f5d5ab9e0642363ded4e174b79f347366ebf9a24e5ea43631ab16394332ff`  
		Last Modified: Mon, 14 Apr 2025 20:04:52 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12259247bde3aab0b423783cb51271f5f72f7e7f3a6dee50a384a57149bb84f9`  
		Last Modified: Mon, 14 Apr 2025 20:04:53 GMT  
		Size: 621.6 KB (621625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e405d27ae50f629047dcc212151b76ecac4c876932cb2a1515b7d1db48fc6441`  
		Last Modified: Mon, 14 Apr 2025 20:04:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:latest` - unknown; unknown

```console
$ docker pull adminer@sha256:c24499bb8c1911f72248c2fc8d45d61b6fc77c77245beeb5b196e10f1522cb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d40072e3c8dd5b252128b2f60d4de4055d51c122780e1ae9ec9bcf2b311aef`

```dockerfile
```

-	Layers:
	-	`sha256:0ff41ce579b3411e3d3d2803388948b4084baccf15d617a0c1e51465e356bc3f`  
		Last Modified: Mon, 14 Apr 2025 20:04:51 GMT  
		Size: 34.6 KB (34617 bytes)  
		MIME: application/vnd.in-toto+json
