## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:d5adc7cdd65ebb51c73a66cffeecac0a8d24ecd77504aa549ac3efe74edd795e
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:a739c31d5b084b20df48b632971366a0e4142d3f4c11e177a8a05690cb6d1a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43290827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c61ee03bd3184108cbba8b438fc733f953f58f5c1ef7165ea06ca40112f711f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:65e6d6a02ae1f9fa5d716a0094e6a21aa3bf2073bda447d0c2c5c7b90a028132`  
		Last Modified: Fri, 06 Jun 2025 18:01:34 GMT  
		Size: 686.6 KB (686568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99174df432557187d68fa593b48390971afd706261c57e8a2ea615403f569ef`  
		Last Modified: Fri, 06 Jun 2025 18:01:35 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6bce0e6c216b2802d1fea50740f49860abd98ee088f06fbff0e72e054aeddf`  
		Last Modified: Fri, 06 Jun 2025 18:01:36 GMT  
		Size: 481.8 KB (481762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31560fbab86f7d1314d5cb74d70511632ec462d45e8851fcfcd4e808aba63fe0`  
		Last Modified: Fri, 06 Jun 2025 18:01:36 GMT  
		Size: 5.8 MB (5767631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622157913b4e73f5e4df7ff7c7cc1483a8a79cc42059612f0bd4957221ab52b8`  
		Last Modified: Fri, 06 Jun 2025 18:01:36 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccd9b57aa8b6466b93968b2207ccc253fe89280dfb42337880e5a302d0ff516`  
		Last Modified: Fri, 06 Jun 2025 19:10:03 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:f25a4dff4f30cfdb1f4936cbf49a8f896d4c8d5aaea4abaa35b63bc8a3606231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7994ac1bd1c12f1eadf124ba4c60244b45877b8e1feb1f77bc9cd1b3fd5983b0`

```dockerfile
```

-	Layers:
	-	`sha256:8ef148a1a02f6e0875b3be11f6df622446fa5fbde7d948082eaade14b4e0b662`  
		Last Modified: Fri, 06 Jun 2025 19:43:12 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:87d732576c0c6a2d59f7baf1a13f93ce1d26d4c160559ac9beb96ba177c047e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41750933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3015fa405542cebde56eb8dd567d49bf311a7d20ba2aae624ee27cfc32d383`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:c66aca777857a43e1cc0d379a2b96ec1a3a7c4ba83d1636ddc7c8084f8b9212c`  
		Last Modified: Fri, 06 Jun 2025 18:38:40 GMT  
		Size: 191.6 KB (191604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec168f712cb3d2820618d084b46795ad5cb09dda88e730e7f0b52244f1898b`  
		Last Modified: Fri, 06 Jun 2025 18:38:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ed6eeafc25aaa338dff16ac08e2cd5017640772f1d8d45430f2c9170f586ee`  
		Last Modified: Fri, 06 Jun 2025 18:38:42 GMT  
		Size: 481.3 KB (481285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1440eddf91f67d9708b2c47ea70badd5742b15ca403d2b35d8aea4b28a6078`  
		Last Modified: Fri, 06 Jun 2025 18:38:42 GMT  
		Size: 5.8 MB (5767631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4063b23f1944b29da5c3b2110be78b3adfca193d2c31d47af48954afd59f52ef`  
		Last Modified: Fri, 06 Jun 2025 18:38:44 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a006bbe4c175d5c872f530fd8bc235641451edd4c281fcdd19bf8c4a395e7`  
		Last Modified: Fri, 06 Jun 2025 18:38:44 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:7a8262de5f46fb6b72faa09d5cf189482d6ef6ea0402b7fd38aafcf096de52d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8eb48384a611a8fef4039a211a234656bf33566fc31ba8e6441412ff12d618`

```dockerfile
```

-	Layers:
	-	`sha256:f58139e2d3c4ca27f79831c59e9d49178ec3afc9af2ae1093fa268a4fd7ab6f0`  
		Last Modified: Fri, 06 Jun 2025 19:43:16 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:c2cfdcd3a48315491cdc090e56bc1fe6a8deb60eedb2ca01acf751a28a4b777f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40427939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d055c586a5e2e9f913af3e93c6c9bf073a15d07e67c6201045a16d0360a928`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:29 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:27 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328e4e294a9cef787f8e4cd232dd727c5fe0dee8d4222317f06135fddadaa697`  
		Last Modified: Thu, 08 May 2025 23:27:26 GMT  
		Size: 14.1 MB (14145812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d36f2080f1795f8b3996710c7f5cb266b8791138e1502c4445a71f8965c071d`  
		Last Modified: Thu, 08 May 2025 23:27:24 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55be4da6eaa6604da0c2c6fbc11aecb6e1a50f1f9fbdd90f6e10b73998fbd0fc`  
		Last Modified: Thu, 08 May 2025 23:27:25 GMT  
		Size: 19.9 KB (19875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2d11a24430dc562699cfaaae85a1363fda3d0a0b6ef5b516bcc2679b3df0c`  
		Last Modified: Thu, 08 May 2025 23:27:24 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576e376ef3e3a159cd955f470537a535985b3c201569384ea7b85d0ce5dbe7fa`  
		Last Modified: Fri, 09 May 2025 02:53:43 GMT  
		Size: 178.3 KB (178330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d9fff01542d792d5e7332f3e5be30f2caace0911220c36eaefd6fa6ce7dbc3`  
		Last Modified: Fri, 09 May 2025 02:53:44 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e43cae8c8597b024e0c9b4f3df2b5fcded2a90ebd17cd1ba33eb98bb13834`  
		Last Modified: Fri, 09 May 2025 02:53:44 GMT  
		Size: 442.0 KB (441984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54db8161a130d4de616e6edc68edf84ed72fcd5147a9c020bfd6250af34436c8`  
		Last Modified: Fri, 09 May 2025 02:53:48 GMT  
		Size: 5.8 MB (5767632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0216177cc5ee0c5b1c9b7d00e15ccb5de9c5a3091501dc199acff2ce1680d7`  
		Last Modified: Fri, 09 May 2025 02:53:45 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26acaa28e5ef7b92011137f5cc75d66b82bc23328d26e3f71341f44582dd8d3b`  
		Last Modified: Fri, 09 May 2025 02:53:46 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:874c705558dcceec84c8efb41fc22a365a58ec7e0f84131d5733e2bd4f1b9d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5821d0c0d6b21c2e49a3f9ed315ca49341aec6f6120acde90985824ff8498c`

```dockerfile
```

-	Layers:
	-	`sha256:333099d6e654d0bcca371915c0153acdd5b4aef3b479c866a938022d209f9e34`  
		Last Modified: Fri, 09 May 2025 04:43:01 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:d6e397efd911e290b6279444cafa7c0b115cfe2110f272ec0d567d31ceeebb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43228597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63d9d4a536fcac80912370a78a873c58749c8b01f77bb2651c48599e917aba`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Fri, 09 May 2025 01:18:21 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Fri, 09 May 2025 01:22:39 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Fri, 09 May 2025 01:19:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Fri, 09 May 2025 01:22:52 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Fri, 09 May 2025 01:22:40 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40c0bc0fd5b2771529a50e28ebe4feded1dd5ae944da5d3122ee5a9f9c13cd`  
		Last Modified: Thu, 08 May 2025 22:38:25 GMT  
		Size: 15.3 MB (15321565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8650836d4602da09e4677007d7fd4c349a6766139491480c5e51cafc5e496238`  
		Last Modified: Thu, 08 May 2025 22:38:23 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ead3cdbca48011bbc30a39ec617df6b01a7c2ab848b1a5abce94c5d2a63cf3`  
		Last Modified: Thu, 08 May 2025 22:38:23 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a0e022bc84c3434b0f68d16a0ae9982163ed03c5c2b9a1f9fe9d3b7c259a84`  
		Last Modified: Thu, 08 May 2025 22:38:24 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f228c1e0a04b1a327385fd233c9e7f3740328a830f460de446265952b966c6e`  
		Last Modified: Fri, 09 May 2025 01:43:23 GMT  
		Size: 601.9 KB (601857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839883a3498ef455f0dbb8d88baa1f198db571125c821cb9abf5d534469d9490`  
		Last Modified: Fri, 09 May 2025 01:43:23 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661fdc698c284497ecebc1ef274edf9b38387bf87911f0f4b96e55f91b98711`  
		Last Modified: Fri, 09 May 2025 01:43:23 GMT  
		Size: 536.6 KB (536580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb562d1b6954a1d82fef971c905d4767540b9ebeb63c36d308c40ca53fd0e9`  
		Last Modified: Fri, 09 May 2025 01:43:24 GMT  
		Size: 5.8 MB (5767631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663d5f392d43733209d085835f61ca6bc16ad3855a64a10c75183c0c525af7c0`  
		Last Modified: Fri, 09 May 2025 01:43:23 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052def6bb726c60b95252e471268c6594bd6bd00935e68fa5039662b1cad1926`  
		Last Modified: Fri, 09 May 2025 01:43:23 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:b947fe94b2a40ad378359764e3dc8d096e67bd021f0f0d0351dc8603f385582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de98c5115e394f6efff6fc8cb43d025a4c67c057331df68f854e5ba6ec618ec9`

```dockerfile
```

-	Layers:
	-	`sha256:102bfe33ae14390dd81f79f18311161bcdf520f741c2a8236470abc5a7780acb`  
		Last Modified: Fri, 09 May 2025 01:43:05 GMT  
		Size: 30.6 KB (30642 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:9f188b33d055c340fee8e78c8bcbd123f7d22049f7455dac492f9b8e2a28c975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43581290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24a23b001079b933866da0da3004678c3782a410d4bfe9997e030e09b3d8dac`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043c21843e9e1a3c7f6e5e28cefb67d3fd3ff42f5cb542be868abb0bf055a945`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 3.4 MB (3379877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e0f5ad9273d70072d4bd2cfcf54366d7c5885dd4aae8cd4ecef26e17065401`  
		Last Modified: Thu, 08 May 2025 21:30:38 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28613618b700b5300d59c41e347bd3b1c1449940c21ba9589b8c07555fba4144`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838b1f9048edc7c78d0c3fb1b32660f69e17c8b5394bb808cc1c5242042f9305`  
		Last Modified: Thu, 08 May 2025 21:30:41 GMT  
		Size: 13.6 MB (13638338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66b2d566a29ceeea503bde1e2b45bd11cfa5cb3ee7a2ebd42701005e59b64a3`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff11237d8258872a5fef2b6b4ae70c2b50734ca568f5ab2e95d8d8656bb74ce`  
		Last Modified: Thu, 08 May 2025 21:30:42 GMT  
		Size: 16.1 MB (16093218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045615f459cec001a2123ab95865811e7feccfd21590a35ce27eb4830775e18`  
		Last Modified: Thu, 08 May 2025 21:30:40 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ba649a29c8160dfa80de0c634a050b436de6f08a5f31d65e01d9c85f802e36`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 20.0 KB (20048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4bf21e48c9b5eedfadc8bf99d6326daf7416ec2ab181683c59666e56de5d02`  
		Last Modified: Thu, 08 May 2025 21:30:40 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0c833476691b49d54553f69e08d6f8b42b0f38d557ae693aa87814c1e79a1`  
		Last Modified: Thu, 08 May 2025 21:50:09 GMT  
		Size: 711.7 KB (711677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a54a6a2e9dc7dae7459bcaa408d8627530e81a3b35de669d684162948b20bf`  
		Last Modified: Thu, 08 May 2025 21:50:09 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5082c31538df57d3a007f51d754ede7d9c76f045c12a2d331b5ab423e7261dca`  
		Last Modified: Thu, 08 May 2025 21:50:10 GMT  
		Size: 489.5 KB (489463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f171eca452a2897eae68d92e35cd3838bbda4c397c49fdb87da9ec7b5ab06be`  
		Last Modified: Thu, 08 May 2025 22:43:44 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea19c18052a34a335a973c088486f1b31e3f6ae833f1bc5d57806bd6ee18df`  
		Last Modified: Thu, 08 May 2025 22:43:44 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92064eaa5737d01b207acdf09b8b97c961c9ad7a32e8bd25ed4a3911a415fe44`  
		Last Modified: Thu, 08 May 2025 22:43:44 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:5a69b68a20243d7c2cb084e06990873858508de353eace93176ebf4382154b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c2a1d5f8a5f4360ee4cba73743a36aed28fbabc6cdf1eb11e1ffeacd91cefc`

```dockerfile
```

-	Layers:
	-	`sha256:3940a30dac8d8699d33886bce62165c7787a590536a5b99d7ddf43863620785f`  
		Last Modified: Thu, 08 May 2025 22:43:06 GMT  
		Size: 30.5 KB (30455 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:4a9b82d302c1cc7822ecbbd6c9cb1f2efe289c4199f5b1143cfed043177325d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44276992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1a98e23dbff676e00dbb3f331b80287f55644b64d57f1d32fd0e0fbec4947f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:58 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf329a18f84f173e0b474c180d6aecc4d7ba1fb09bb861cb9ce9e95c9f5296d`  
		Last Modified: Fri, 09 May 2025 00:49:20 GMT  
		Size: 17.0 MB (17002354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bac31bd3a5cee2a231c5b58f2a15312933055aeb5ba79086019db6d6c2da6a`  
		Last Modified: Fri, 09 May 2025 00:49:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0326b4dbe0b94fd4441a2d51f1ae20b94d15fd51432f99fb273a35d6fffa55a9`  
		Last Modified: Fri, 09 May 2025 00:49:19 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9d54d9fbf1e4c64a527b08d66666af49fc115ab4dbe9f14243e4661a7924f2`  
		Last Modified: Fri, 09 May 2025 00:49:20 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b22795dbc7a8a98434de1c32c4301ed6b74fa4833acffe6a409391d3934056`  
		Last Modified: Thu, 08 May 2025 23:14:03 GMT  
		Size: 228.3 KB (228305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a08009b38e94e8ea65bab8284fbecc779cc05632e722dd29aa8fb9c5e7ae8c`  
		Last Modified: Thu, 08 May 2025 23:14:03 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef9367fbd4a460ec7617780f77ae28bbe9e6b4f59a3b2d8e6cff04e5d107e2f`  
		Last Modified: Thu, 08 May 2025 23:14:04 GMT  
		Size: 547.6 KB (547611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6caa8339de5771c37f1aa840df539c909f3f5b4e9d3e36c0e61bfd41b66e82d`  
		Last Modified: Thu, 08 May 2025 23:14:05 GMT  
		Size: 5.8 MB (5767631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b176d71c7153c68fd189a36b7c589693f928dd71be46e06ddd884ec1aef03b64`  
		Last Modified: Thu, 08 May 2025 23:14:04 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ac4c8cb5be752764b60615bcf130757cbecc8a60300a89688c918d3ef9f27b`  
		Last Modified: Thu, 08 May 2025 23:14:04 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:2e9959aa3aedfd5c8aa6f8b7cce7346d4deecf1a160cb38944cce547c85a4bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d842285b9c189438dd908dbd852b116dd8b2750c3015a4edeca2b9cf5763b888`

```dockerfile
```

-	Layers:
	-	`sha256:613ae30ba8aeffaad3e7d8c33f94ce2a108f6241c4579f7b493337de152b1101`  
		Last Modified: Fri, 09 May 2025 01:43:09 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; riscv64

```console
$ docker pull yourls@sha256:8c76b3f57f7526a1705e0d5232abaa4a4de5cbc2c4697b365cf267d2007f28fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42841058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e564afcdadfc1be9467e8394dc4970f57bd0bbfb143cc0dc1c63624bd98e6d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:f5ad654d59e95a55261ea11a8c6a7d032c526b03efd3c2139364244216013fe3`  
		Last Modified: Fri, 09 May 2025 15:45:00 GMT  
		Size: 203.8 KB (203849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3da8ef55b38c4d380b94793c1f041bb13820e0c6855c046d58be9e723c2c45`  
		Last Modified: Fri, 09 May 2025 15:45:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff845d9d3201c43704fbdfae30209460845d8340daafb507c4346b530390caa9`  
		Last Modified: Fri, 09 May 2025 15:45:01 GMT  
		Size: 493.7 KB (493700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2585cafc1e81746c5d90dc89fba3b4d17cdb17982818f0cc8a39d7121a59b2`  
		Last Modified: Fri, 09 May 2025 15:45:02 GMT  
		Size: 5.8 MB (5767628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6bf751bc31344c41e5233de2b7564f2d03e0db5dd97119e390ce637d2a6c27`  
		Last Modified: Fri, 09 May 2025 15:45:01 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b1a58e0787b8ac50e00e0d953dd06f2fafce85411e8919d7f1e63066092270`  
		Last Modified: Fri, 09 May 2025 15:45:02 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:78dcbc4fd8aaed8195a7e0b390f922da6dde06ae96f0f443f623018ddd822e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc21b27382fb2b1bc75451fd00d03606fbe3ca882c2a3db657fb13dabe9e79`

```dockerfile
```

-	Layers:
	-	`sha256:ec25781a111ae541493e1c25a2de213816cc9353fb96bd81b8f230009fc2b211`  
		Last Modified: Fri, 09 May 2025 16:42:40 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:6eabd27c2dfeb9852bd6bedf243f7642ce74c2216cf173e1229709cb84fefc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43900635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292c4f0651aac77610e24ecf5f517e57f47843874206c790604e21c9d6f611d1`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
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
	-	`sha256:e25eb099f75f954aa9b258ced4032cafe9aa5138d9409b0b1f9d71a18c9cfb64`  
		Last Modified: Fri, 06 Jun 2025 18:52:55 GMT  
		Size: 219.9 KB (219938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b99eae31568575c32ad3d329cc7c7f087d3fd0140592f50e813a63323bd60`  
		Last Modified: Fri, 06 Jun 2025 18:52:57 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489634fb04689e9697873637d09e2629e3acba78480ea61608e5e6dd1c8501d`  
		Last Modified: Fri, 06 Jun 2025 18:52:57 GMT  
		Size: 510.6 KB (510574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5f949fcc31b08d14316fa19af8c137799a6087d8e43e5f7574356ffb211e8f`  
		Last Modified: Fri, 06 Jun 2025 18:52:58 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2566647764cae702e25ba97cae1d8ec6c53bab1999f18b4167f63de70e480c`  
		Last Modified: Fri, 06 Jun 2025 18:52:58 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137bd645a44c8b5381f5eaa9d25a332f60c954b17b1fd3c7522b2032e34b450b`  
		Last Modified: Fri, 06 Jun 2025 18:53:02 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:935195b010e55860469c630c9b2a17d0562bd1d502186f23c14af4ba46b18da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d476dfb8ca5fd9ac562264545a01e72b9a410f2307a8bf4d55b6185933b08d`

```dockerfile
```

-	Layers:
	-	`sha256:587f8826682ace3115dfa1719e0507dd9e48524549b5cedeeccae08370e3a396`  
		Last Modified: Fri, 06 Jun 2025 19:43:42 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json
