## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:8c19c6765fb532b91a9d0e169fe30d5f28c7ebf0440d04cb5606f97fe55cc3fd
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

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:a01656b015544e5f7e59f5d98e4381154b1fd84100867616b6e59677ad707cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40689344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be609740e08f54942af459b510263be9ba31911758fab8e4148c941da668c0f`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 21:09:19 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e6590c00a6efae6a3818cdcdbdc07de42c8f3cfe66436e090e1288afd7a2c5`  
		Last Modified: Wed, 08 Oct 2025 22:43:27 GMT  
		Size: 3.5 MB (3463759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1399ace04dbbd0ab0a9210ae417a50d2f41f3a63bc81b9bbc2d240d5c5f1d2f`  
		Last Modified: Wed, 08 Oct 2025 22:43:26 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe403392f1ee6380631b8c01269b35592b867d70a7ee1802914246935d05b8`  
		Last Modified: Wed, 08 Oct 2025 22:43:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7b4b38e816a1e4872dd9a8431b2c03704dc23dd29eade03f27dbd2e1d01e80`  
		Last Modified: Wed, 08 Oct 2025 22:47:05 GMT  
		Size: 13.7 MB (13667317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95ac84397d632d475b25e746efabc8798b55392e9750a02ed9542bac26e8bd`  
		Last Modified: Wed, 08 Oct 2025 22:47:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b655922521e702487d1134941ea3f10f0adfb3ca5619efe1c2c77459133fd`  
		Last Modified: Wed, 08 Oct 2025 22:47:05 GMT  
		Size: 15.0 MB (15027201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58f640ef5868a2d939d32a84617abbec3cc2a2845094bd09f77dccae36460de`  
		Last Modified: Wed, 08 Oct 2025 22:47:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c191bcad7c7de466886debdeed072168d3048b01a6aea5a5539f9c488ab6f`  
		Last Modified: Wed, 08 Oct 2025 22:47:03 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca2feef647585078301af6d9caafbb67c1ae12081d6bf95569670d333e5ebd`  
		Last Modified: Wed, 08 Oct 2025 22:47:03 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27201e4a7baa8f397eab63397a9eb5ccc9b601b4ff63f64f0cecbcaf31a4b852`  
		Last Modified: Wed, 08 Oct 2025 22:47:03 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132a5bf02c97b3d318a0ead4a1ba46380769f4c10d7da92c7ce24ddabc9117f6`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c041bb1da65e255e95b0e65d5bbe079f3206be0cb475d9a37e4aab33955661`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304d85968f02c5d0ae43d8a7cf8949a27c3abe2a0a5b4586e0a28990c4f4ead`  
		Last Modified: Wed, 08 Oct 2025 23:38:04 GMT  
		Size: 4.0 MB (4030707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac3f95bd3708cb1d785e21f67e8deb4f29017e300040073002590a414606ee4`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc82ac24ebe9f2f3d3c0a6b7a8d93ab31d5fb642a5a008706ab1c2c256e03bef`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f57e708a19f01f3365e6a390c8bc07b549aa20e92598269303ea8a661b32c7`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:2cfd4155886fffa22f8bf92318f8419ad99714f7630901c6cd7d173b2be4a729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bf910ad754ccfded45023f9ea967eeea2b7c9db3c33aefd18ff0c89b538420`

```dockerfile
```

-	Layers:
	-	`sha256:947b082b2db0b8a02c54823c38326421decc915c7dd745150b50ee351832d3be`  
		Last Modified: Thu, 09 Oct 2025 00:50:03 GMT  
		Size: 34.0 KB (34027 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7be869507205de6662dd2deb5c6fc23d894f9efda8f14f6ce7c211114f6c2e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38438422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fd5f4ce68954749f75d9c92e12d7f022b3b28c3d42efa4b162d07b1e8babac`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 21:09:19 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8096ad85a1b46a9b85f71fc6b71136ab4aacbc5dd3dbedfe16ccce6670b4d854`  
		Last Modified: Wed, 08 Oct 2025 21:50:04 GMT  
		Size: 3.4 MB (3428329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff4647a815892b5cad95e2085d4f8749e66e17b97d0f39273b36e13986fc18`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507824fa53ea4d449c9be4f807898ae15579bfab9e0c16ea165516239860478d`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c2891b626e82b4becc53181b7c57a31d8fa303d662a5a2ee7d4027e327882`  
		Last Modified: Wed, 08 Oct 2025 21:50:11 GMT  
		Size: 13.7 MB (13667311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ad5966c23735e254d643a1c82ae2289ee87d8c996c71e567862866d35554e`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8abdd5f7de9be19dfa5bae3ec88c092f147234f9394b4af50bab15a72790d91`  
		Last Modified: Wed, 08 Oct 2025 21:50:12 GMT  
		Size: 13.5 MB (13536156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf37b826d6a01db8c4182a0a2f3203c6f855ae91123295c790f12ac349b4946`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6870f4e9ced6af1c7667532c65a035528f51a0bfe8a73c538d06136f6d870e`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c145fb1ffa97182569ce8f0fd2809a8514a5b29ab6b4e5894bcc60db1fac8199`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3f6136ff57fb8404d527e2a6346c6cc6a71312de24280f5444235652f67964`  
		Last Modified: Wed, 08 Oct 2025 21:50:03 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e18ad6cabfd2a2a5b3ab4f542156bf19b0ab0545ff8deeed2bbeecee3958f`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6848bac90ef3def7be88731a77b328d1641f2a6f3d030d68e53466f736d8f3`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df37c0a6e0ae2f1d5e05464f45c27f1be1f553bbfb8529121206fbd3594c77`  
		Last Modified: Wed, 08 Oct 2025 23:01:20 GMT  
		Size: 3.6 MB (3605064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1128f7fc0aa1aac25ae46065780aa40adb6abe403ecc085f474dae6050d4c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663744cd9bea7a7e6030a3c7f5c2659e6d8f7ef7a3fa775c7b9073c762ce971b`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 640.9 KB (640903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6406394b56824702417878965bea211e02d0e1d562ac56dd5215309e657f992`  
		Last Modified: Wed, 08 Oct 2025 23:01:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:8fa266f2d6a1cbd1ce8b226cc3c4b428ff4ef326022cd91fed5e7bfe1f72ed97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1e19b24edde5c933b52e0a142969163699b38771761cb9cefb39f6e1560cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc206fc7616992debf4ba3daac9ec613781f07b47a1be64bfaed81822fe1bcda`  
		Last Modified: Thu, 09 Oct 2025 00:50:06 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:e47505ffde5819e2fa26d3f98b64811219781acb1d4d5922b1cab54c0da071d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37291734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b261e4a0afa5a62c500d3992a4d1c585730d1d1e14d8c2236302601875d9f59a`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 21:09:19 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a542e87a7c661204e86eb09c5d76f8df3b7dbbff78cf0a911e63fdb95b9daf6`  
		Last Modified: Wed, 08 Oct 2025 21:48:17 GMT  
		Size: 3.2 MB (3244394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e12c98013d08d84660cd3c28830dfdeab2739af850ffa337a1290f9c6e7d585`  
		Last Modified: Wed, 08 Oct 2025 21:48:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c81e532edcb873dc2e2cc6260019fb0981398832302d5494d527d90e56e8f`  
		Last Modified: Wed, 08 Oct 2025 21:48:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efbf8b4035136783431c8f65c111b152a54eec2ad2dd83f2a33f1bb1b85952e`  
		Last Modified: Wed, 08 Oct 2025 23:16:03 GMT  
		Size: 13.7 MB (13667305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e547371539b44e06044c1c74e38143b52f470f649d2e7084e7e4c335f53a3`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ac8ef7f2e810a3e3b48063c4d50d9b2d1892e861c0a2337c6c93cf15c93f66`  
		Last Modified: Wed, 08 Oct 2025 23:16:03 GMT  
		Size: 12.8 MB (12782712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c4c7a4d1ffbb2f3722634735c9b2c2d5b47cad00211f8e7df37bf82451eff4`  
		Last Modified: Wed, 08 Oct 2025 22:42:18 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0fd86f5c953a36d8434d60ae260ade8dc87f0527d24805298ca81ad529d8c`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0394e0309a7f73e61af1d2412b3779d978667c4bd25bfc032aa170d205ceb1f`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b83ca2c1c93b9eaa4aca5029df8cc913ff70c50112e599275c16565666be81`  
		Last Modified: Wed, 08 Oct 2025 22:42:17 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e774ff46b02b7a194cdedd87192fee8ad0a44018afc408bf25a5d3d39102239`  
		Last Modified: Wed, 08 Oct 2025 23:18:08 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdd90850280f3032a7cf805dd54f34a93c630598a09c3c3d4a7778de2d882fa`  
		Last Modified: Wed, 08 Oct 2025 23:18:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb1df7872b9f553338acceaff70cb9ab4f2459a1a1e7090c12b6e13150504b4`  
		Last Modified: Wed, 08 Oct 2025 23:18:07 GMT  
		Size: 3.7 MB (3678316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f23e95fc51bb78b6b78b583535d4d6ea8f28547e57857ec6c6d3394e52c623`  
		Last Modified: Wed, 08 Oct 2025 23:18:07 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a536dcda0aa28d1e0ebddf8e20d6b8d3bda776a584962028a90b620363b923f4`  
		Last Modified: Wed, 08 Oct 2025 23:18:07 GMT  
		Size: 640.9 KB (640899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49633091657df733a1751431c9c0a9aec0e19a58ad81895e5480504654e0f99c`  
		Last Modified: Wed, 08 Oct 2025 23:18:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:cf75dd607602ad1eb3224d20c9843fe7cc050516fe88a05ffa12748883ade522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159342f4ba0c29dac97ec0d5281f9a904bbe75df393ac063ed4c72d4dc980b7`

```dockerfile
```

-	Layers:
	-	`sha256:be626dbbc75a11c455d3951164bbca324b4ae7c2b5b51a32e1276266c5a874db`  
		Last Modified: Thu, 09 Oct 2025 00:50:09 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:fd440778a3590f5ded09e4a8ddeb0afadf2b87e1ad7afd14928bd2946859310f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40655622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3821a6154c67b831e00d0aae815ced23e7a8249918de5449cbf8e22afa357f0c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 21:09:19 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ebec91d5e3bf4e32730e408e0d3d7d67b64b4f916d210a55ad102fa97e08a2`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 3.5 MB (3466801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f52d1dbb7f7fbfc95e099c5650807b88916220f5a5cd4ba59cad5a0a6d2bc0c`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8789e309aa9c45d4e867dc44d5e25723a71fc6b95f6fec153bdefdb22101a43`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041ec1ed023269548f8fe8d32715031eb2c80d251f775efa44027414933f2f6`  
		Last Modified: Wed, 08 Oct 2025 21:33:14 GMT  
		Size: 13.7 MB (13667306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a1aa3ec692400fd6057c9b216b251a10850474657a5f6db3919694de83855`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3678c235066d6c6ee70879fd40e31798ff829cb592fe67396acca429d9561d26`  
		Last Modified: Wed, 08 Oct 2025 21:33:10 GMT  
		Size: 14.7 MB (14658207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4fcbf9a168bb300314c3f55e9457f6407319b51c142d1cc38d1dc5b9b97a1d`  
		Last Modified: Wed, 08 Oct 2025 21:33:10 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a3f707841d6e78b913849c34d6b048cc90df23b7a9174634a7b277646b080`  
		Last Modified: Wed, 08 Oct 2025 21:33:10 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf3401c51cd7b30879cd4737319e1edb82b8597bba76dd27122f24ce9d4521c`  
		Last Modified: Wed, 08 Oct 2025 21:33:10 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79930f48261a960a34f35d7f92a089b5d6d062823c500b134fed9614c501b7`  
		Last Modified: Wed, 08 Oct 2025 21:33:10 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83958cbeb6afbb827646582337f4470b3650938f5ad99a256120311331d955e5`  
		Last Modified: Wed, 08 Oct 2025 22:57:32 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f0fda54b82cbfb91ee5958ececb3c238ac0dfdc5ceaaad4b64ce3cb2bcb87e`  
		Last Modified: Wed, 08 Oct 2025 22:57:32 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544e53f5c3bda185795fc01ea699488ae75c9d6713aba3402ad57ef844010a8`  
		Last Modified: Wed, 08 Oct 2025 22:57:32 GMT  
		Size: 4.0 MB (4027764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58502399a09412a655f29f47ba4bdbaf30190ad47c9ef847b577a389a80ae387`  
		Last Modified: Wed, 08 Oct 2025 22:57:32 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda6564605e9a39a8ece610aaa85be4135f2b54ce4890c3c6888b430fb0c63e`  
		Last Modified: Wed, 08 Oct 2025 22:57:33 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211536a799e3f82fbd4a1c865503058d2b878d96874b3cea6925c994c7fbeff1`  
		Last Modified: Wed, 08 Oct 2025 22:57:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:ea0e764b38abc1d06576e813f70601efe37bbfbb14e9442ea27b3166f49f33fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9f71b6aea4b6adba3da66d302db7600985a7562df2796354bb7e3d61865771`

```dockerfile
```

-	Layers:
	-	`sha256:39e3743d0e7e0e70f29c521dff5bebd7c929bfd27ea9acb9fb0a418e0a661ab3`  
		Last Modified: Thu, 09 Oct 2025 00:50:12 GMT  
		Size: 34.2 KB (34164 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:f5673edd2268bc25c67028cdda6727d831131ef5e5cd18b2892ccdb26d63e23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40822959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eae95546ede60bd252c648dd4a825a90a9982e93c173ad2565d66dd8ceb8054`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 21:09:19 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Mon, 08 Sep 2025 21:09:19 GMT
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b1c8f28dcc9eea59bc468507a822f9cee5923019a234682b17fffc0e0399e`  
		Last Modified: Wed, 08 Oct 2025 21:29:25 GMT  
		Size: 3.5 MB (3522947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c8476eb364d29e72f440167fb044ac72dfa85ef77b1c2bc1cfa03c4d8793b9`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7115926f8e2adaddbca9f8b1778fc2142df7ec3fdad63b6c6e1c8399109e3b71`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eaf5c5fa7e4fae1e5ce91a8aa7a311895c774277dae69bf3b4395bb7e4b344`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 13.7 MB (13667288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741bf9292a6bf0fd75328cac116ab9a15c37b4cd92a34c0964795f4c66197b5`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11189242010cb867cbcecd3502a7985368afeda128cc73419725dad71001db06`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 15.4 MB (15426681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b68bdbae9ced3decd4cee6efcab71157186bc4547f45eb1a9260bb568d846`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeef9f239767fd37ee59bdd0c3b25b7d735e1c8346a5a0361c7054bc6c19888`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 20.1 KB (20052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba566a1e9b316fabc4534724f1166d20e2d9ac961956832b0e6fc29cc2da25`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 20.1 KB (20050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60800b2cc2a5800de8152cf69fc39817b8ccda398608111c29365655f269068b`  
		Last Modified: Wed, 08 Oct 2025 21:29:24 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe5b3c63c4967fe46d801c2ce451bc633bec5b9243f9b3c215a2bfbc6caf805`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 303.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19d9d72cc617c4803b99254cc3655b5a8fcbd065c68badd31168e46667ae9ec`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7651f6acfb8a3040f9c3661d4814f4d23ad706751a5b9e1c915f166cfe8909`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 3.9 MB (3889263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515f2ee9497ae92fbf3ca2d4f1d3d87a822998bb8070f70c395e91963c4484d`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9878d71b47e61a6fb4b4b0ab19ef9364665f73a51019beb2a91109dbd315ce15`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 640.9 KB (640900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2151db12d4aa1fc1eae2ed37d3135e3a784234bd8b4afe4072e8ac65b6058ce`  
		Last Modified: Wed, 08 Oct 2025 22:20:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `adminer:fastcgi` - unknown; unknown

```console
$ docker pull adminer@sha256:92466099097b573c312c27395897b950db01bead9d945b9bcba80806ea37bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (33994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1323bcd7757ba8b9485648ac8e09df190e0eaa3189e73ca25edf506f8ac5b84`

```dockerfile
```

-	Layers:
	-	`sha256:e6a7eb7b68d4c2c023b0e3608fc1a26aa3cf96d166e4c8b5d5eccf25e4a2982d`  
		Last Modified: Thu, 09 Oct 2025 00:50:15 GMT  
		Size: 34.0 KB (33994 bytes)  
		MIME: application/vnd.in-toto+json

### `adminer:fastcgi` - linux; ppc64le

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

### `adminer:fastcgi` - unknown; unknown

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

### `adminer:fastcgi` - linux; riscv64

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

### `adminer:fastcgi` - unknown; unknown

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

### `adminer:fastcgi` - linux; s390x

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

### `adminer:fastcgi` - unknown; unknown

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
