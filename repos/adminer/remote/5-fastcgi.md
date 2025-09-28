## `adminer:5-fastcgi`

```console
$ docker pull adminer@sha256:ddece06387f5dcec9f614abe7a1eb311b5eb698dd345bc8b8e278c2c9096b6b5
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
$ docker pull adminer@sha256:031e14bea176924cea5ae4655500921588d73511683496e50f417c7636e79589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43150527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf7d2c6028673c17d16fdc377d207f8c8e274b4854f75435610b08654924860`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ff51f2ea727a7043940cfc2fb2f68d58d10d5359a33071855155359a696d7`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 5.9 MB (5928421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6daa090ca97098274aa0ed6f7f64465168f8ca337b0f30c1857ef21f07fd7`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b84768904846715613a8f5e76a29acfae483f321bc82fddfa7a83b01b8433c`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd732135359065fba3dbf169e55d4c065122a69ef438a8bf6c5c3659e31de7`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 13.7 MB (13667228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd0b9cf1437dd9feafcc659c5af008e174d71acd7fefe9b71aaa96c30467a1`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced1fcbb1ef657a0b3898a127e963131a0099545af83077a1b2bcb5ed37d898`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 15.0 MB (15027081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415445076d113094d936a74399c4de54c2fb68d515a2d582984fdb9fd4c5a569`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1b29d39ef81a71d52ae54f98679eea8a543e664cc6d99459c1379e56c7772`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 20.0 KB (19960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f0f032c840a150ab2997e4d529b6df675086c1d128b5f5a07152558e26d31`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0912e70f8c7e6581863c92ecb8a53705ca16cd033ca9f05ac05b69adac4181`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dcd529b22b7b096af7e46d598d74f7e15d5b86b7b03b5fc427a42dd3e51a67`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d820c488890f269737fa002685b29d0d7b41846f3c74b0d12d9d9d8ef8aee1ee`  
		Last Modified: Thu, 25 Sep 2025 22:13:02 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2681b7ef42c825c241dd1ac4b1e95ee90c74b3ddabfbad81e5d31e4ea409b1f9`  
		Last Modified: Thu, 25 Sep 2025 22:13:03 GMT  
		Size: 4.0 MB (4030448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7208abe636b602cf9f6a0681c44ef6e0c7248c7ada56b9a572e3e0064392844`  
		Last Modified: Thu, 25 Sep 2025 22:13:02 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671105eb1bd4e58667468b70c6a4ae5c994df2d21215270ffdaf4e981a160f90`  
		Last Modified: Thu, 25 Sep 2025 22:13:02 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387b23e70b194fc39cb19e0f7961ce128c0c7a2d8f0c086653e2a9a0eb81fdc`  
		Last Modified: Thu, 25 Sep 2025 22:13:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:0bf4076b4c059338acd763ac4680c76e1758723be1036b467980dda508d65ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5eec5c0fb459eeb2552367099489004523b85febe6b200d71c535596fff63`

```dockerfile
```

-	Layers:
	-	`sha256:5e992bd652ccca364cfdd2b3a2c12fc34f38bd153c206ad2f400170f2b4734bc`  
		Last Modified: Fri, 26 Sep 2025 00:50:38 GMT  
		Size: 34.0 KB (34026 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:bf9e17c06b5d2c374abdb73adcdbf2988fafd6efb4ad6338e18c3ce2b3426291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40537726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120e61c23d881b91065f3292f8005e4f047f7c599cf88c99fd37456840007650`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a67790b167583e60e508f6d629f5d12e582a6660df9d0b1eeaf3f40d951d80`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 5.5 MB (5532141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff4e845b8d460a651554faa7fd3e340b0ee89de9f36dcac5ef8e4c8d2f2108`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b147fa84f71c751a59eecdc171fcbf8585b1a6cc0999bb778ce7437a7eeb9dc`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07cecaff067ecfebe81f2148d35179886b6eea43dab6621362d9c90f28345fa`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 13.7 MB (13667216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764709b356f09b5c5483ada2c6af7267987584736c6a097028b9329f8f5ecab2`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fb754ed6d5d711f9fe45af29b81435ac6d016c9f104a197e02ae38a8b6ec`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 13.5 MB (13535949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5dd25f3cef6b4a020c2164e5827c3e14045977a81fc65c25ba2d3747b77cc0`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213638172a84ca00b4daad0e22bbaa5a22b80472d4866a27791add5e689e10a1`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e15e130a9409610e44c3bba79fada57d94acf47d2f14e31ad32f4d6176e976`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caa106576197fa7708918ef456b7a91916c9d67e486d8b6cfb5b457a3303ecd`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2ade81f4f91236f8934e2644ea69d81831724f30a681d75676bfb6f870e8d`  
		Last Modified: Thu, 25 Sep 2025 22:16:57 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f31dad18f909404137b60fb9f5fbeadc157aa5b69a6a9b592271eb2482930`  
		Last Modified: Thu, 25 Sep 2025 22:16:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc856e3548c221a4313579ed22f373ecc628a5aa6524cb2ff3209f25124f5ce4`  
		Last Modified: Thu, 25 Sep 2025 22:16:58 GMT  
		Size: 3.6 MB (3604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd08d7d32fb02f60b2b3d7cc1e00fe9117e4e097179bad8d9a1fdef71e45869`  
		Last Modified: Thu, 25 Sep 2025 22:16:57 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37abaed19d5106f0b54c8b617597a5f15b0ec1dc49146eaeebd980fe42a173`  
		Last Modified: Thu, 25 Sep 2025 22:16:57 GMT  
		Size: 640.9 KB (640899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8c37bebfc1fca1cbee117212da55e086ffdc0d1464fc15d24bc34fb28d06f`  
		Last Modified: Thu, 25 Sep 2025 22:16:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:8375912ab1a9b849f38bb1964e8527689296e6f2bc1adf3427368874e2a00654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddb5388d637a5caa3c5d9d53b583bc3fe96c22cc7272b8c94004815207f0045`

```dockerfile
```

-	Layers:
	-	`sha256:76521422092cf882e859cfe529705019ecf5ad32bbd56c942e0ff0c49a06da72`  
		Last Modified: Fri, 26 Sep 2025 00:50:41 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:c71db1c0b27861b3a151664f5fd43f3c9b246addac8bf6ec6e3c71200d8dfd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39224128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0ec581420eaf9595d5b817fc51233a3163628cd847c5e8b61534b1010fd374`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa32fea9d18e0bb21aa5d036fefbf058ad92b637b4745b85cedb2e309f8c143`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 5.2 MB (5180910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fb35f74d20fb8549fc68209ec760e72c2c583bcff4fac189065d64b7aa383b`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a16a4e21aed64875cb326e0988ccb265d6db5eec435587012ba9ee5b634e8`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bbdca2e9a981657abd022c957bfc454eb758cdf37c2001c8d49e5b1f371eb1`  
		Last Modified: Thu, 25 Sep 2025 21:24:20 GMT  
		Size: 13.7 MB (13667207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b031fe9573eaa2ce66a637df5c3891656df759e88de025d1f110abdb0403737`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830af3ffe9544082402754722668d5862fc0e25372119c0d9dcd51e2cb775b11`  
		Last Modified: Thu, 25 Sep 2025 21:24:21 GMT  
		Size: 12.8 MB (12782275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8452452133ceb6d3804fa2b5df4420830ff13bca809abd4c7b8645f64aadab`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b731097d3f08cc776d90474f4d20964a8d77b0a2396e76d49494b8c6ddbd8`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcec5fac0bb0ed9143225112878db8b7ab8cbcd55f1f1fbfdd08f39a18d3fb5`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 19.7 KB (19725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cc70e10c7e338f96cd087abebe29b53bdfd6e988f6f7735e3703f943dbf4f`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5b4f6d05746cec9264c1e42979fe6473709254acea9f35c5740070e8565eb`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c36fb82c397e5ca7901f39c9fb93db666c94f14512a71bc1be808b41e337cf9`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d29c1af7f9b9b58a832480f72fe18262b55da262dd8a6a4f7eb47acba19f7f`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 3.7 MB (3677499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6f1f9baecf5ee5d3368b99a854def878bd59247e0448000c6937906cf93b6f`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e68a5dbf34862481463c78b726ad7016d0080b0dcc634e386322486526c884`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 640.9 KB (640899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f5c26097b43d6c194b67c8b3e6b00a5e65ccbf42bff89ed74da8edc444defe`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:630fb75275655fa4bd34f6195f3ab9735d424b604b1854d410369b198bdd550b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca4eda401b9ce15545a612581dda2b036fb26aa14a91814f6c3937af6614d61`

```dockerfile
```

-	Layers:
	-	`sha256:933d7580ea23ea76a1502a4941dba56d31869d9a5fb779bea2fa525d2f52c579`  
		Last Modified: Fri, 26 Sep 2025 00:50:52 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:de1c62d2349d1f86dd58df4f6ed89a95322b628a0537e35e69384d33ccc9c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43409309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62485508a70f2a89ce332d2553fc78944ac847108971abe0a9ce330bba547976`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42762833876b2891840162bb3f2b2dc8e337b6405e803877384d81f6d7f859ca`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 6.2 MB (6228304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7e50b72b234b509972818d92d08709e6c7c9f021cd8bc4734296b33e074985`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496881f94362cbc448851f854f7343b9f991445464c5064fa768ba1a5f6e9da4`  
		Last Modified: Thu, 25 Sep 2025 22:10:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf93b637fd1c3f389acc6e90f0d387d5c23d661d11d853624c023d9617fe14e`  
		Last Modified: Thu, 25 Sep 2025 21:19:58 GMT  
		Size: 13.7 MB (13667208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7f61d2a4e13b96e05bd135218b8010a10de187149881190f100746490e9dc1`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6736c2f6b95f249926307a489dd76d28c534dbed06ba64ef475e3d76b48aefcb`  
		Last Modified: Thu, 25 Sep 2025 21:20:08 GMT  
		Size: 14.7 MB (14658309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d423cf999628f922fe623e5eddf38a175f746cd4130e45df74da6850e16776`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce53955b4bd84116f9401c48f4b471f28d7afa1a4d9b994cc56bf78c07adec7`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c65a21eeaadfe7e7e4f930a073089dd938d24cac9b2b464f216c8b48fa3ccbb`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16ededdb9cf830ca8d46d9fd8ca6ea7b6af37668e16de43e313c681758552fc`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fafe3038939aeb7ec49a2cadb2449c6d111a46c8281b89d599775ad2fd0edf`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa667ab42ed9f2065e36dfa8d1beec5299ce0c799ba92619347c0b12d1d0cbfa`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e8a241a7f0933bf19b20a4415238caa32705e0301a6d4eef5a54cb7778710e`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 4.0 MB (4027485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c9cf9d79f752ae1f3ef79edd3150b6b39b08b401753be2551fee7d23da5006`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72910fcaf9817d84950910a4027b611401cf23d7d54d963ccfdc69b4751f17`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d605f834119d753dbba6892e7e5406237c48492c112254d0bdc40d72230267e9`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:cd37d210ac7d06d9b8dbcc232232467c57bff2504b912b94b88bfdc4a2121ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4152811da52c51641b42fc8c7549c7bb2bb65ec50ff28f14465477c371d7b73`

```dockerfile
```

-	Layers:
	-	`sha256:c0b3be082e2565df40682565907ae0d78e9fa8c63f8d4f7dc5cb35b0fb38ac07`  
		Last Modified: Fri, 26 Sep 2025 00:50:55 GMT  
		Size: 34.2 KB (34164 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:0e667ddc6a79684752c4df5200b3a157b255de279b9546c0579231bef5b9e77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43089018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c162e3a5df16ea60e2cc558ded795fd0cbd03674a87286e34d5ccc6a24de67`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5992baace3a2271f05ed2a94a020aaf7e05936e26e120dec169f46809566bdaf`  
		Last Modified: Thu, 25 Sep 2025 21:19:18 GMT  
		Size: 5.8 MB (5794064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea4bb153034cccdd78ae6b08206ff8960d8d3cf59b6f478405d1518224e28c3`  
		Last Modified: Thu, 25 Sep 2025 21:19:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9269a2570ff3e6d899fe152395b9db64f5756dd6c597c345742ba90637212476`  
		Last Modified: Thu, 25 Sep 2025 21:19:18 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be885cd77dac459ec23a86aaa280568be2eb0255ee171946cb89efdfc7dd1089`  
		Last Modified: Thu, 25 Sep 2025 21:19:25 GMT  
		Size: 13.7 MB (13667217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd218f1c89dce4e0b5544963d80e132403796afc41eb1ed4fa8805171bc6745a`  
		Last Modified: Thu, 25 Sep 2025 21:19:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e111e0ac52e8d2b90c086e7fad36365f4e0363fd0088059b3e3dceb06c46e9`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 15.4 MB (15426681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8048db63577e741e6f77898284e7d2d62fa4c423a085cc9d894339342f2b810`  
		Last Modified: Thu, 25 Sep 2025 21:19:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d91abb36b14d95bf6a6a07bf3ca58fb37531c4ad9ca98b2f199b5697a068fae`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a47c7b1dfd01ad18bf5dcfe3c4a3b79cc3eaf79678cb3b7e8782c8788a4d941`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 19.9 KB (19926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6077ebd6864105a246e69252003a68b05fd57f1613c9609c7efbf61916f43382`  
		Last Modified: Thu, 25 Sep 2025 21:19:21 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba1f502e2dfe7246e55434d98495091ec35bf4517ab76b5e42a5a8a1aa135cd`  
		Last Modified: Thu, 25 Sep 2025 22:13:01 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbe2cefe08426d6fa699474452df0fdc08215dbc798670e3f87d4f2a8afd0e4`  
		Last Modified: Thu, 25 Sep 2025 22:13:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a87537860746836f93264a824a89e63aaa62b9021de40da3d70b2780824b2c4`  
		Last Modified: Thu, 25 Sep 2025 22:13:02 GMT  
		Size: 3.9 MB (3888447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43766076c47ef2804577b563b20cb47f51ea2de3b4d0842c84b68d824bc86ae4`  
		Last Modified: Thu, 25 Sep 2025 22:13:01 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b90c624810692a87c7e2bb423ee2b9b5df2309a7e515aee195452445f255bbc`  
		Last Modified: Thu, 25 Sep 2025 22:13:01 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9f50df89fb1c8175f978b19d55f4d0c312e24b38b91dd8281b072fe2f0fe42`  
		Last Modified: Thu, 25 Sep 2025 22:13:01 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:aee9fdab3ff19dd20404782d1c25bd43ce28da6b47854645859644ba6e5fa80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e071c560d90e537ee66f3233de3d63371343add1611e1903a7e3f2927ad408`

```dockerfile
```

-	Layers:
	-	`sha256:0fe449afc3985561b7c189e2d85bdbf5defd2a55187fa03f269ec2691c279595`  
		Last Modified: Fri, 26 Sep 2025 00:50:58 GMT  
		Size: 34.0 KB (33994 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0572e3f605424af0d1e179574a003d0dc036b4433762ec2777f32b45e11703b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43881990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5772bff2dc771809293b176c0feff78f17449b2ccf39b92237d0f9739297d6`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
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
	-	`sha256:852a8582978935292b01078a8bf867fa366e4ae24fdd3a6b63289a97e9e36a9b`  
		Last Modified: Thu, 25 Sep 2025 21:54:19 GMT  
		Size: 18.3 MB (18302097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74a94a214cb2f71f482afa4faacf43be7ff3885ebe5681a2a2948dacf6bd38`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657f121eb8a9c561c1df8375d82ca583c0d2fef78c3fada98ea8bb02facc836`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e1cf882843f2a8c239ed219c88fff5529cf3ebaa3d261c34d572fdeb471ea2`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810f4a524095951e7a04f5fac55938c485ab06b36becbb1da240b347bae343f9`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b845f509eb41911026ac2d4a737baaf8c08ea65c21f6cae4ba3b5c4cba42f0b`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668049a9ce33a93d47875a7d7281d4ada1b09eb5f90d19ed11e6d99f9255ca75`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a96adb232576435755f7a2f6c276520d0219f22040a5f58a00d6785078b2b7`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 3.9 MB (3877110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90325d7b454665745c6fb21a9557cf96a27f419341e5d45ec56c9ea387b460d0`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185163da354e929d7e8e28e45ab5e7d1a7c8fd2c600ae09d0a9a5420c3fc2be7`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 640.9 KB (640905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6af863e05fb955213639321a40b530937ecb4bd051310bb483898b956104d2`  
		Last Modified: Thu, 25 Sep 2025 22:29:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:10172ac4d7539fc4f58b3d19b943d41cdc6901aa73008ef1e3b479ce273013bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba300a2a648eaebe472330095d9bba7e5c25ec903bdb9ac696e2f008c360b88d`

```dockerfile
```

-	Layers:
	-	`sha256:cffd9421c4cd3f9259af9851495eb8df060bae2b70c6b73c281a63563621e90a`  
		Last Modified: Fri, 26 Sep 2025 00:51:01 GMT  
		Size: 34.1 KB (34071 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; riscv64

```console
$ docker pull adminer@sha256:0a1576ee8fa558d21478c78fb8af86ae322dee7d5dc7b06f4b53e1089a5f1585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42325115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e330b580acee0d1fb69e27a9a052cea5356eeb118de64e814f227c29fb98cbe6`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
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
	-	`sha256:410e2dcf97d734b0c6aa57f526a2f6790249dc29a3db1b8d560391854969845a`  
		Last Modified: Sun, 28 Sep 2025 03:53:22 GMT  
		Size: 17.0 MB (17049187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07818f4ff36efa1ca4dd2b14c543ff6486b20831e6367e4ae3115f78b17913c7`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12efdb41f2b3b1d5745bb1b2f116cd955caac98ddfc6a5099a65804355ee9f8e`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c5e4d1b398c9c371a721bf982bd522681338b5af4b3afc2856ca84f04924ba`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61d787deb89cbb48a17297405231ffd0f4ba5c4ef059cc29a6225599872e80`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b3e0898a8089408f7fcea122d3a112c3903aa6a234e0e68fa968fa7a10688`  
		Last Modified: Sun, 28 Sep 2025 09:08:24 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69146fcb46f79ea32abc66ccd340178bb0e24aa0c80bc1b7737b393c09898176`  
		Last Modified: Sun, 28 Sep 2025 09:08:24 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4ff85b27e06b124724a33e15173af655fc01876a766719773ef778ce19d658`  
		Last Modified: Sun, 28 Sep 2025 09:08:25 GMT  
		Size: 3.8 MB (3804494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a21ab67510ebf858f0169f29a87f61b32b47981671608ed1be21bbb651abae`  
		Last Modified: Sun, 28 Sep 2025 09:08:24 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088fcfe25246a53577e910c42fe720005d259fd86b96b6afe1d80592de65134a`  
		Last Modified: Sun, 28 Sep 2025 09:08:24 GMT  
		Size: 640.9 KB (640907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231d3ba9ea36cc4c422fb5c53f322f4f8fdf003d25d217a6654845788b826890`  
		Last Modified: Sun, 28 Sep 2025 09:08:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:3fdcb08ff80ae599a4b0db11016542fcab00fdd1cc995f82fc344e164eaadfa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aca4434f74fb8ae2536cd88d1e89b01c8ad12e13db2382c2f8726f51202fe5`

```dockerfile
```

-	Layers:
	-	`sha256:5690a6a09a118530c14d257187e7e8f2d6a056c8d2e2d76032aebe14598291de`  
		Last Modified: Sun, 28 Sep 2025 12:48:53 GMT  
		Size: 34.1 KB (34071 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:5-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:2308fc8712e67fc71785a576572c7257491e93cd05381d285eda711bed93a9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43109245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb43c24e28a36a2a7fe546e36210e20c2e4608b7ef9daf059ec0abcb841bd924`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

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
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Sep 2025 21:09:19 GMT
WORKDIR /var/www/html
# Mon, 08 Sep 2025 21:09:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Sep 2025 21:09:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Sep 2025 21:09:19 GMT
CMD ["php-fpm"]
# Mon, 08 Sep 2025 21:09:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html # buildkit
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
CMD ["php-fpm"]
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
	-	`sha256:bb01789d2f734019e508a5d3ecdd9f51a0822d95e2d4b9ab5dd118731e4b244f`  
		Last Modified: Thu, 25 Sep 2025 21:52:55 GMT  
		Size: 17.7 MB (17671315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15f0850d24368c212cf078cdb77767416e9757af489ea505ecb9611bbbf0316`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3013684b773ccc2ab01f27c859679e86bfd68cbf6693b35ebcd1e1a75123e300`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1ecf3624fbc0d6d100154c4e3a79ec2874f74d8db894a62a7fd8f8505f3cf2`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ed9966c1b20ebbdec26707359e143a71a352650d3f56aa91db62ca653a9a7`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25c86d2977a776f8119e551015cf7d49408eee15cd457b3061a6f943cffeb88`  
		Last Modified: Thu, 25 Sep 2025 22:24:55 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66243665fd74d54556db2a1d7fe37bab43b6b464523ee6b6494e74648556520`  
		Last Modified: Thu, 25 Sep 2025 22:24:54 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec9cf066b631f837b3048d7721a9e5ddaed304410dbae76c11f700675de33e`  
		Last Modified: Thu, 25 Sep 2025 22:24:55 GMT  
		Size: 3.7 MB (3748628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0520b7284cb9e9253290458e4050e1f9a553d5d4851a5c607e45aceca0c13`  
		Last Modified: Thu, 25 Sep 2025 22:24:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ef1479019adc51ef43cfa3be43a0061f59f63890f5012c706343461df1f2ab`  
		Last Modified: Thu, 25 Sep 2025 22:24:54 GMT  
		Size: 640.9 KB (640906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532c5ba87008e29d93cc566bf8e272dcf478ff1c4f2e1e088d271a1fd7508d99`  
		Last Modified: Thu, 25 Sep 2025 22:24:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:5-fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:43b30c01b00d56500e5a7d5fc9820e9bea7cb684c3eaebbb7abf3cf7ff5f502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae7a10281a54babac1dcae66a5b56b1a4d6be2e86e0856c79a721d530d012cf`

```dockerfile
```

-	Layers:
	-	`sha256:f4bb90626bd01aefb2778c67808817e9579ed58ee9a43282c31f281c0aee2ee3`  
		Last Modified: Fri, 26 Sep 2025 00:51:07 GMT  
		Size: 34.0 KB (34027 bytes)  
		MIME: application/vnd.in-toto+json
