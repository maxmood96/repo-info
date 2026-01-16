## `drupal:10-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:aaeef991574db0c322ae0236a1373ffa6a187daa89df15ce3bffc1e0ffcaf1ae
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

### `drupal:10-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:55bfca936187b164b1683c0d927e866014be969c0185d0156c1d8bf9c456400b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60168617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff72fec675134ee5512e00c283057cd416189fc0b698639db1d162af9e1c77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 23:04:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 23:04:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 23:04:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 23:04:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 23:04:57 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:05:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 23:05:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 23:07:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:07:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 23:07:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 23:07:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:07:58 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:07:58 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 23:07:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 23:07:58 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 23:07:58 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:56:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:56:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 15 Jan 2026 23:56:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:56:33 GMT
ENV DRUPAL_VERSION=10.6.2
# Thu, 15 Jan 2026 23:56:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 Jan 2026 23:56:33 GMT
WORKDIR /opt/drupal
# Thu, 15 Jan 2026 23:56:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 15 Jan 2026 23:56:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeffab483b15f68f82bab4d4d572a5c3531a33cff9d680aab73a14db2efbdf16`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 3.5 MB (3464380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01c6dbdf43725adf0a89ffc2e637c3c98291df9f8a2b320f1f922a9c8be1922`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57caf36b884b3910375cb3d40a9cad0bd0348190bbfdfac77dc843c60b40e86`  
		Last Modified: Thu, 15 Jan 2026 23:08:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479a55e10fbb0707c9d7b11a353a7dcfec3ded5355345a60da94d5997c087e1`  
		Last Modified: Thu, 15 Jan 2026 23:08:16 GMT  
		Size: 13.7 MB (13691850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7224cbaadbf92c4cf14db4db06f2e09df75bdf8692f6773f9aa123db366bea31`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7eb72306506ca043e834841128f64aa44d583343ee2b316e77c207a0d08ce3`  
		Last Modified: Thu, 15 Jan 2026 23:08:17 GMT  
		Size: 15.0 MB (15043871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d08a3c6be9c774f7a046400020c4d230c1c886c4f5364cd4a0ccde6e6141d`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5ae3b01945de5ea43e48ad84d63c6574c510705c08fea802beb2af48aa4e48`  
		Last Modified: Thu, 15 Jan 2026 23:56:11 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34875e311283cb4eac5186085f18062a8b9cf4ffb312bc1c0fa2ecea7bf87357`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb679f37f413e08af2cdf203560be447159a127b3a0f22c20678de3d4b96c2a`  
		Last Modified: Thu, 15 Jan 2026 23:08:15 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a142252365b88deede0aaed8191e645f6a53d274a48ad9a77f1a3bc9d32a5ee`  
		Last Modified: Thu, 15 Jan 2026 23:56:57 GMT  
		Size: 1.5 MB (1493530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d969e4d2cdf1d4b63721441d3738709d8223a060c72d6126ca5cf294caabdd6`  
		Last Modified: Thu, 15 Jan 2026 23:56:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63557021541487a140b62bbf88606801e1c24aa796fc83536e886bc7ca16e262`  
		Last Modified: Thu, 15 Jan 2026 23:56:57 GMT  
		Size: 776.4 KB (776355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ad0b3ffb55d095707c1683bd739f91e1f43ca1f1f5b3f5797e8bb135e2eb04`  
		Last Modified: Thu, 15 Jan 2026 23:56:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed4eabd5b844f3b555ee245b14a220bbae5dce16c39d1725d011e712f2b3af`  
		Last Modified: Thu, 15 Jan 2026 23:56:59 GMT  
		Size: 21.8 MB (21842268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:a5469704065f7035c8719c37ce59bd56b242be75501407f7161848f04782ab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 KB (402361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1931a4e244c80cabf525018ad8615fb36344595add2250db60fb8bd9b50bc67a`

```dockerfile
```

-	Layers:
	-	`sha256:a56d53baecb89565ee86994dd1039d26f6412d26eda44ab8e5fdd8a9d2eec67a`  
		Last Modified: Fri, 16 Jan 2026 02:57:28 GMT  
		Size: 368.5 KB (368503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276f309420ca8f1a69fdd1e0f626e592cbd64bedf7ecaabbd5f484eb19ad1d6e`  
		Last Modified: Fri, 16 Jan 2026 02:57:29 GMT  
		Size: 33.9 KB (33858 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:afb23b711c63c993458a61026bbf421e19d6e81484a1be21112b8b115092f123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58178517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d499cd9ae3e197be08eedd0ec6dcd749aaa177e8f42cc55f9769de0b766ece`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:26:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:26:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:26:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:26:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:26:15 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:26:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:29:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:29:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:29:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:29:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:29:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:29:22 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:29:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:29:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:29:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:29:22 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:23:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:23:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 15 Jan 2026 23:23:43 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:23:43 GMT
ENV DRUPAL_VERSION=10.6.2
# Thu, 15 Jan 2026 23:23:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 Jan 2026 23:23:43 GMT
WORKDIR /opt/drupal
# Thu, 15 Jan 2026 23:23:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 15 Jan 2026 23:23:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336c435dfe3145bc7ae85a2c2822f5172dd73b6a3af2d6858be101bebd13f95c`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 3.4 MB (3428671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb40a772685fde0a3f638cdfbb106ef505ccb8b97970edffdeb7f2e1cdac25`  
		Last Modified: Thu, 15 Jan 2026 22:29:34 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e7954a46982323eed1f26229e894ad4d4fd2fb3b4d4594f63824665fdd75e3`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f925cf9f30f63caf22897dd783619e4f5ea46a9b7658568c5275eda805d011`  
		Last Modified: Thu, 15 Jan 2026 22:29:38 GMT  
		Size: 13.7 MB (13691856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2a4e58c03278ec4dc48e7fc54ea07047d1c8b0f63fca2781b894659c28faf`  
		Last Modified: Thu, 15 Jan 2026 22:29:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1789b4e1adebd43bb1ec3efde48d253ddf89ab37c35b462d706d27317845ab`  
		Last Modified: Thu, 15 Jan 2026 23:21:46 GMT  
		Size: 13.5 MB (13545907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c5db3024a8872ca14880e1ce4130803ff2ba1bff5227481dd3fd6ddcc4056`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5190e461bfd63b6f2423af1d5ea994651de6c5f915b5e0341c75fb297680090`  
		Last Modified: Thu, 15 Jan 2026 22:29:34 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddddc2931f1133f3c1e9d9dfd628ffe1970d4e5c389a44fbd3e080295b888ea8`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 19.9 KB (19868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32692ad2afe115469287ef6407a7d47cd915019ada53c942fd6ef1b659bd6c`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 9.2 KB (9223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df639c2b1eb950fcaea46dcf023280e6e871c48a5026fd1a173234153f5133e4`  
		Last Modified: Thu, 15 Jan 2026 23:24:07 GMT  
		Size: 1.3 MB (1335853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cf45f5ac18e62d4283ad8c8fbabd4a574e54fc1138b344bff4c3f7d87b5899`  
		Last Modified: Thu, 15 Jan 2026 23:24:07 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b373363e5bd390fcd9ee16f646aaa15635c691753ff6dadea2d1139087addb7`  
		Last Modified: Thu, 15 Jan 2026 23:24:07 GMT  
		Size: 776.4 KB (776358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093016c9aa1f5ceb0d4163aeddfa90cbf557ecc8dc21c59af46abcd810bbdee9`  
		Last Modified: Thu, 15 Jan 2026 23:24:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1500b3261be9707900c4989b784964fb2ddf25d43da0411ad7a9db00d25f533b`  
		Last Modified: Thu, 15 Jan 2026 23:24:08 GMT  
		Size: 21.8 MB (21842277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:f45cf1d74ebaf36806079e2c56393a6bd0e93c2e57f72a4cdc8869c518a96b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 KB (33786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a4d31ea8bd213153563a0936f4aa8d64f833a9d6993d9f78a396f1b53cee47`

```dockerfile
```

-	Layers:
	-	`sha256:97508e0c1b28d11a5aa58c7616569359ff85eb18f2ccbabff7e3864f58e29eff`  
		Last Modified: Fri, 16 Jan 2026 02:57:32 GMT  
		Size: 33.8 KB (33786 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4649dd4bb664f82231b96153de0eb6675704db1feffd63dd4a5c690359e195b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56851826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86121b943ba152aab073007bad2a7275823a9b8296d275c2ff37454206a2f74f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:33:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:33:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:33:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:33:54 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:33:54 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:33:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:33:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:37:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:37:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:37:02 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:37:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:37:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:37:02 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:37:02 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:30:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:30:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 15 Jan 2026 23:30:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:30:18 GMT
ENV DRUPAL_VERSION=10.6.2
# Thu, 15 Jan 2026 23:30:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 Jan 2026 23:30:18 GMT
WORKDIR /opt/drupal
# Thu, 15 Jan 2026 23:30:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 15 Jan 2026 23:30:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d723b9ddff74e43544baa9d4b5709f4aaab5982351bc285061609ebd9ff953b`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 3.2 MB (3244498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bdd915960929426d88cc8d151b9288e071cb558e47d25d708b46647c91a50f`  
		Last Modified: Thu, 15 Jan 2026 22:37:16 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9c360cf9b5ac664697447f3e87d4889f5aa51cdd55cd0f64a774c6ce0ef551`  
		Last Modified: Thu, 15 Jan 2026 22:37:16 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d995a8a252393a35dfc54550ff230e8db8a628b6effb8dc5dbe7bceea8b40`  
		Last Modified: Thu, 15 Jan 2026 22:37:19 GMT  
		Size: 13.7 MB (13691842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2db5003017cd98e0a1061adf152bf6b7d5de74e2d7db35c25565b07c54c27a`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9148aebfbb6375806a94e71ff82a7777e58610027bd0194d70d52b3143df389`  
		Last Modified: Thu, 15 Jan 2026 22:37:18 GMT  
		Size: 12.8 MB (12787689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9de1d9926ff5e388d710acff5457f4deac178542b7c51fc05201203f27e9a0`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a263fd6f7de059c869206b12f094a36b838392be63b89bf4b4c45fe5c215eda7`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79434505c51b11068cdf1b1ca5d6207c89e4a7905d77e701ae0076b538914406`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4742edc61a011d1aa37c7aba0800d2a235c365b248214e0c6cbb597189ebcb1c`  
		Last Modified: Thu, 15 Jan 2026 22:37:17 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b857150b214f784cf62f03bd06bd36e4ba92892acb1390a5b50a069d1e1091`  
		Last Modified: Thu, 15 Jan 2026 23:30:44 GMT  
		Size: 1.2 MB (1234029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7b5a6aea26fdd93970f888cc7ba3dfa5492db7d5c7a9199e27208a4e7af74`  
		Last Modified: Thu, 15 Jan 2026 23:30:44 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0432a2ec3fc4a7624a0f1fcf7953c0fafd3d3f0628559cf2fbb31edb98f3a060`  
		Last Modified: Thu, 15 Jan 2026 23:30:44 GMT  
		Size: 776.4 KB (776356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e159dcfe93f89c22768d76e00bad7d43f3c6b6e9a8eb28c686424424220b7d17`  
		Last Modified: Thu, 15 Jan 2026 23:30:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12e638de232b35b4c6bee98988ff59ef7d1f69ff718925307a3c13f7b79cdf`  
		Last Modified: Thu, 15 Jan 2026 23:30:49 GMT  
		Size: 21.8 MB (21842387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:4b975f1dcd8933db51f989eaeb1d81cd8f5aa5d5e9e02d8c85992c05d8ebc1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.6 KB (399566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4352b3cd7e9e8e5d53b9b19852b4c37d0295fcc17966be12c8015a6f05dcd6`

```dockerfile
```

-	Layers:
	-	`sha256:f3b73a2922ecd9bb6ab6386d22ce25aa2d4d87a95ab2c7719ff56f05259d6835`  
		Last Modified: Fri, 16 Jan 2026 02:57:35 GMT  
		Size: 365.6 KB (365565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff82310fdd92a538089ee440cf23c2fe155ee805021c32647056d9e0aaa2a0e`  
		Last Modified: Fri, 16 Jan 2026 02:57:36 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:1f9cbcfa995fc4bc1286a7f075938fd22482bec042928b0aa76766385fe7f8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60124516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0ad1e18a01b27ec1191cd69659a2e9767bf0dc353b6eeab62e25dbd5e716bd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 23:11:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 23:11:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 23:11:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 23:11:36 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 23:11:36 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:11:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 23:11:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:15:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 23:15:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:15:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 23:15:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 23:15:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:15:15 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:15:15 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 23:15:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 23:15:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 23:15:15 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 02:37:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 02:37:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 16 Jan 2026 02:37:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 02:37:18 GMT
ENV DRUPAL_VERSION=10.6.2
# Fri, 16 Jan 2026 02:37:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 16 Jan 2026 02:37:18 GMT
WORKDIR /opt/drupal
# Fri, 16 Jan 2026 02:37:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 16 Jan 2026 02:37:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056a5f4247be8b2120a775bbcd5eec21da4d05838db4d72aa7a5700470c8ca1b`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 3.5 MB (3467138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1085f1ef8f07068f174a645ca44a043c276857d35f4dc708e245df6c6da36808`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7043262e2f0f9339f33933445d2b0b3a8984a5221aa8c7ddb5916a5f7bf3c3f`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f5ea084bac50ee437f8efba6ecc93362938d4aa54a9bef52d7540dcd0c4a26`  
		Last Modified: Thu, 15 Jan 2026 23:15:32 GMT  
		Size: 13.7 MB (13691841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa476a7b07311a9acf51169e61029af5eee46aecea53501b6053c453fee919bc`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582391d4c1997c76088237b6d18bb5ce6a298bd7ba324bd5d0d0f5e688eb501b`  
		Last Modified: Thu, 15 Jan 2026 23:15:31 GMT  
		Size: 14.7 MB (14674435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25027d34a8cf9b7312908da9b9cec9f4ed12d84f10140287cd80789a72dcc908`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7248a17758e671423e32d1a38079dcc7030db47eb4397011c18d78389e2308a2`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5b0bea35d6339cd671d3688fded5f78feba70e15f0e490a5e1299e872c41a5`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b6ce09c0ce00bfa33471dc7e4054bf3cb074b4d75b769a7c3783ecbb12a02`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 9.2 KB (9223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e4d7704958b11fe6c5dc1ea0d33e14fecaf908f460c4e5a2bf2ab63f482d1`  
		Last Modified: Fri, 16 Jan 2026 02:37:45 GMT  
		Size: 1.5 MB (1480911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b324b88da26ea668da919ab31e866240a7bb92236abca97911b64d51506acba8`  
		Last Modified: Fri, 16 Jan 2026 02:37:45 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e7bf22328b8ded256c1cb06c9463bd18c7e044d5407cb827973856b178501`  
		Last Modified: Fri, 16 Jan 2026 02:37:45 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394839f1841eaac9311bde05bb4984c8e5c9931f0b3108ee77e887ef3412cc04`  
		Last Modified: Fri, 16 Jan 2026 02:37:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ebca83fce4de9f79ba0167e2426d7dcfdc258f95752938bc132e93adde578c`  
		Last Modified: Fri, 16 Jan 2026 02:37:47 GMT  
		Size: 21.8 MB (21842263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:de9d37a5015ebe758b87dbd744ae9200e9fd5bc2e84f6c19ae14eb638505cafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.6 KB (399635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3de8d894537e81517723ae5121d54d7c89d2c103728e5412077a291a5ea9cb`

```dockerfile
```

-	Layers:
	-	`sha256:4fa9e4fc8a64ee96383760bc116dac1ea5cc62687aa96ef38a61bf6cdd7dba37`  
		Last Modified: Fri, 16 Jan 2026 05:54:20 GMT  
		Size: 365.6 KB (365593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7615ef2cf7fe38ea990ef3160cc703008010d6524de7c935de618ca48498bb9b`  
		Last Modified: Fri, 16 Jan 2026 05:54:20 GMT  
		Size: 34.0 KB (34042 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:01474c41324257dd9b536bf2402123a6b6daeda8fac8e012f7a57d020bc989cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d9a020b257073c3f951fe64c129970948767e68a266907eb2783c82759990`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:26:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:26:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:26:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:26:37 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:26:37 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:26:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:26:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:29:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:29:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:29:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:29:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:29:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:29:45 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:29:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:29:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:29:45 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:29:45 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:22:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:22:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 15 Jan 2026 23:22:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:22:24 GMT
ENV DRUPAL_VERSION=10.6.2
# Thu, 15 Jan 2026 23:22:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 Jan 2026 23:22:24 GMT
WORKDIR /opt/drupal
# Thu, 15 Jan 2026 23:22:32 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 15 Jan 2026 23:22:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08142c9d5a2cdb5de24d61ec22ef3c43561b5c5fc9700cdadbfc1453c93fc4d0`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 3.5 MB (3523247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da083e600a16736ab4f9764a0a9bf0581f353a6d8b1f7305d3eaf9082eb5e0a1`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7d552af267059d5912932d686a3e401d6fb7d5389110bac673d241318736de`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d368bd50300ca199741a6041ea4db8556e5ab3946bee9d11d228e09c57b00aac`  
		Last Modified: Thu, 15 Jan 2026 22:30:02 GMT  
		Size: 13.7 MB (13691827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f9741b1678f7494260d3c71ca20b70714ebf209b484948762dadec16757906`  
		Last Modified: Thu, 15 Jan 2026 23:16:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6bc98a6252a6263cef4e6b7b827b2eedb3cb51ddf5db88c043271fc24a7ab9`  
		Last Modified: Thu, 15 Jan 2026 22:30:01 GMT  
		Size: 15.4 MB (15441516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d708e68f9a624cc4584091eb2540e45122ae0939062e4effd7df482ab89e2baa`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85291caa29a28aa1db20eec7b120123b63bd8338ff86ebfba75bb47eafe23d91`  
		Last Modified: Thu, 15 Jan 2026 22:30:10 GMT  
		Size: 20.1 KB (20056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051ee22b5ffcf0e5e09f80000d3c8e13aefbce78bf5608f46feb3e4b12c558f0`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 20.1 KB (20055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950720a586ea5cdcbfc61ac8bb1ca220d331bbf0a8aca52cddbf78fe287f6f7`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f570aa65d6dd2a641f1ab9257beba0efa5e128fbfaf1d1432d95913eb7bbbd`  
		Last Modified: Thu, 15 Jan 2026 23:22:50 GMT  
		Size: 1.6 MB (1579031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8115f272e6a4b76be2bd3e2cf5b622fb3a194fb478ad24522c281419c1222351`  
		Last Modified: Thu, 15 Jan 2026 23:22:42 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c4436849f5c98d8eb2db688cc789b41ec393abd2b3458396b91c64ee92baef`  
		Last Modified: Thu, 15 Jan 2026 23:22:50 GMT  
		Size: 776.4 KB (776355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23667410147623a6726945a5f9bf61abc514a5601f79df5a5c1e154c2ef7be11`  
		Last Modified: Thu, 15 Jan 2026 23:22:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c67d4b8dc741bffad10d5c2be5eb6f528a4f1a6131198f7bd66bc16d7369c0`  
		Last Modified: Thu, 15 Jan 2026 23:22:52 GMT  
		Size: 21.8 MB (21842258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:e8bc8a0b094dce6d73a943bf377576f2ff9f6fb9ed35bd8c5af672a22c0d48c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 KB (402272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4195d6cad287ff16206185bef7dccc5978e8535f15cddc6574972a4443cacf93`

```dockerfile
```

-	Layers:
	-	`sha256:3367db81e287a108a737ef693e12d8cb0eabe852d38c6bd747e1b38fd0dc77f4`  
		Last Modified: Fri, 16 Jan 2026 02:57:42 GMT  
		Size: 368.5 KB (368468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc51c28fa437bc0ce09aed6bbc3f05a7a79597e1a09a7caa4d86b79e453b06b`  
		Last Modified: Thu, 15 Jan 2026 23:22:42 GMT  
		Size: 33.8 KB (33804 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:f3ea40b0bdc9de5390b8fd7471214f5af6aef6dbe62b95aec6945c640f54a6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60834554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181bff68dbdb5472c10a9a075f9d0f7c418f56861c4adb915df2f34c479d0187`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 03 Jan 2026 02:18:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 03 Jan 2026 02:18:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 03 Jan 2026 02:18:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 03 Jan 2026 02:18:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 03 Jan 2026 02:18:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 03 Jan 2026 02:18:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_VERSION=8.4.17
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Sat, 03 Jan 2026 02:18:46 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 00:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 00:18:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:24:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 00:24:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:24:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 00:24:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 00:24:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 00:24:19 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 00:24:20 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 00:24:20 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 00:24:20 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 00:24:20 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 04:31:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 16 Jan 2026 04:31:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 16 Jan 2026 04:31:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 04:31:51 GMT
ENV DRUPAL_VERSION=10.6.2
# Fri, 16 Jan 2026 04:31:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 16 Jan 2026 04:31:51 GMT
WORKDIR /opt/drupal
# Fri, 16 Jan 2026 04:40:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 16 Jan 2026 04:40:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b6394af72fe3bce8ca5637424420c20414926c7c8816d76948244c39456b43`  
		Last Modified: Sat, 03 Jan 2026 02:22:51 GMT  
		Size: 3.6 MB (3615199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9e64228e9f9d06c520c3269eace8a5a63ac3f2440bf106ba44b2fd771ad626`  
		Last Modified: Sat, 03 Jan 2026 02:22:51 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb669fcba61516b54db2698bd1f6bc6d5c26e71f1862fd0b419d41eccab618d5`  
		Last Modified: Sat, 03 Jan 2026 02:22:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dcb1cb98f239ab6cf2624c3bb385436a6da5cf829b93313830b10f8451866c`  
		Last Modified: Fri, 16 Jan 2026 00:22:07 GMT  
		Size: 13.7 MB (13691844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd17bb4151159330d23ef4b898a1d551f5ae9919119dd652d7eb1ff91eb7c2`  
		Last Modified: Fri, 16 Jan 2026 00:22:06 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b8d1d8b81862dda8291d4a424078cc44b02130130056330c65b2527d6871a2`  
		Last Modified: Fri, 16 Jan 2026 00:24:42 GMT  
		Size: 15.5 MB (15507416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8ddfe8ac0fd7868a5b66bb016bb317d4b8969804fc8a4bc3fb29089e7aeef2`  
		Last Modified: Fri, 16 Jan 2026 00:24:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec107a043db683f1608bd6de07338d2ba90636e633ae9eac298f5869db877dc`  
		Last Modified: Fri, 16 Jan 2026 00:24:41 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8da0052318d4d293ecac896498d7a2f9f0434e68bc41288cb6092e98474b7f`  
		Last Modified: Fri, 16 Jan 2026 00:24:43 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21703d820dc10d9046cf16556cce77f203cfad0f9e75bc944d48e666b18b3c`  
		Last Modified: Fri, 16 Jan 2026 00:24:41 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c50ec21b08fed092d37e7ae809907cddac9b49f5c4322efcb5b79e52dd207d`  
		Last Modified: Fri, 16 Jan 2026 04:32:49 GMT  
		Size: 1.6 MB (1615684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595df2df2e946110e9adc6669e521a83142e715e9d52354d7da0ba7a64ae746d`  
		Last Modified: Fri, 16 Jan 2026 04:32:49 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c5d521f20808c2da590e0eaa3f1608679cf9c5a456db2194ed66b06dfb4eb9`  
		Last Modified: Fri, 16 Jan 2026 04:32:49 GMT  
		Size: 776.4 KB (776360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f846a2a16632a754d464c457da9c71ba6d2d9c80dc800723f1da4a2d83884025`  
		Last Modified: Fri, 16 Jan 2026 05:16:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff251e81ef240931ab3f5aebf61113379082f244a3d0629c2a76b08e9f0ba32`  
		Last Modified: Fri, 16 Jan 2026 04:41:02 GMT  
		Size: 21.8 MB (21842279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:45a79d6a7d60fdc05e6895583c05ac493af7ff5cddb408cfd00f27f0d5f10289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 KB (395337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d032b420d9ac4bc47594ef614fd2b633afcc5b7b08bb4bc7e06f53012b2722c1`

```dockerfile
```

-	Layers:
	-	`sha256:0b31c7ea3de10c78aa2c1dc5b03ca144441a66382fdd6c785dd896e4084c1fc6`  
		Last Modified: Fri, 16 Jan 2026 05:54:26 GMT  
		Size: 363.6 KB (363608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ec5d906bb026a39bfa9f3ee8e9f0af22c014964cc080d443c8d1fe22967dc6`  
		Last Modified: Fri, 16 Jan 2026 05:54:27 GMT  
		Size: 31.7 KB (31729 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:73a706b183ef363a31d3aa489568d1a1c4941fd2701df1e11f384a4b93598b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59432079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf501a0991fc4fbe23ce001d8d9d34e35b69ff928c5926ce1a95489f42ebc7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 05:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 05:22:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 05:22:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.4.16
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Sat, 20 Dec 2025 16:02:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 16:02:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 18:17:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 18:17:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 18:17:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 20 Dec 2025 18:18:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 18:18:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 18:18:01 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 18:18:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 20 Dec 2025 18:18:02 GMT
STOPSIGNAL SIGQUIT
# Sat, 20 Dec 2025 18:18:02 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 20 Dec 2025 18:18:02 GMT
CMD ["php-fpm"]
# Tue, 23 Dec 2025 16:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Dec 2025 16:03:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 05 Jan 2026 10:03:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 05 Jan 2026 10:03:04 GMT
ENV DRUPAL_VERSION=10.6.2
# Mon, 05 Jan 2026 10:03:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 05 Jan 2026 10:03:04 GMT
WORKDIR /opt/drupal
# Thu, 08 Jan 2026 21:54:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Jan 2026 21:54:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Tue, 09 Dec 2025 02:08:24 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5ba105ee87a39f4dab9b61a0482c7c6c7039d05e277a0060f20a8a0a83579d`  
		Last Modified: Sat, 20 Dec 2025 17:11:01 GMT  
		Size: 13.7 MB (13682586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601ee1f25efcefb5b2ef49dc592b5ee85777aa906728de216be973c28ae92bc`  
		Last Modified: Sat, 20 Dec 2025 17:10:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135fae163d9624003566e349d65d0af18dff8ed33a245f30a148fe3b1270161d`  
		Last Modified: Sat, 20 Dec 2025 18:19:07 GMT  
		Size: 14.5 MB (14546691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27cb2fd991daf07662969595c6273ca9486370b85c464dff4f3840d01aed3f3`  
		Last Modified: Sat, 20 Dec 2025 18:19:05 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225ad9664e5da6365d2a1e501e368bba9d56ef130ff559801773d8afff6b6adb`  
		Last Modified: Sat, 20 Dec 2025 18:19:05 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec7bdb7eee2363137445ddf96e24e2b825ce0e57293cf65eab670a0e5dc7b8`  
		Last Modified: Sat, 20 Dec 2025 18:19:05 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc10a3ed1845f8deea6719ff00983b8229c9bb3850d2fc13767e8137120c3dd`  
		Last Modified: Sat, 20 Dec 2025 18:19:05 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc717616d87a9bf5d646f9f663b38c46db1671db983e800ed95fcc77c6daf00a`  
		Last Modified: Tue, 23 Dec 2025 22:51:38 GMT  
		Size: 1.4 MB (1415105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f69e8fa4ec768594c49c43cbcb77fde3a93a221e2b6e8b9102e78a2a726a8`  
		Last Modified: Tue, 23 Dec 2025 22:51:37 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0376a5a338b8988c217e1e60fb7d623a5bb43f5cb25b64f7863aad356e01da93`  
		Last Modified: Mon, 05 Jan 2026 10:06:44 GMT  
		Size: 776.4 KB (776366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3e00911e0c0e72cef30f5e31dc21881cb59e0207c2701e328823b70d3ebb6f`  
		Last Modified: Mon, 05 Jan 2026 10:06:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb97cfdab1d08ae63065f17dabb60a309b02e01b3b654348ea6cbba3ccce76b0`  
		Last Modified: Thu, 08 Jan 2026 21:56:55 GMT  
		Size: 21.8 MB (21842327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:0319074ecf6f80d15fa1742e6e3677a303593832575c6b798716be8cb2731eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 KB (397532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27b242c2017c045783b42d6e904d45bb3bc5d85925fcc42ca4067e31cd25240`

```dockerfile
```

-	Layers:
	-	`sha256:e087b4cd1d8ad474298cefd493da6b6dc6eb8cb50ad247f55fa7eb3b20e90265`  
		Last Modified: Thu, 08 Jan 2026 23:56:21 GMT  
		Size: 363.6 KB (363604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c257f45ce966d45c982a9d372515a04947777390561b2123f76f23ae07f0664`  
		Last Modified: Thu, 08 Jan 2026 23:56:22 GMT  
		Size: 33.9 KB (33928 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:9dbb72acd94462137e05ea775c69f621e2e6dd3f462ffdc5d9094ccf45495322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60270714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c224b97a6560408f307b69c2ac8db9b7bf6b449cce843fa142df46722e5925`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:07:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:07:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:25:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:43:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:43:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:47:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:47:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:47:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:47:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:47:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:47:46 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:47:47 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:47:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:47:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:47:47 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:38:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 15 Jan 2026 23:38:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 15 Jan 2026 23:38:53 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:38:53 GMT
ENV DRUPAL_VERSION=10.6.2
# Thu, 15 Jan 2026 23:38:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 Jan 2026 23:38:53 GMT
WORKDIR /opt/drupal
# Thu, 15 Jan 2026 23:40:07 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 15 Jan 2026 23:40:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b2ff0842c178e1087be78ce7fd9398e218ab3073b14df552c39751910aff3`  
		Last Modified: Thu, 20 Nov 2025 20:25:24 GMT  
		Size: 3.7 MB (3692751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98970dae6ec226fa5b2211ea3ccd1469feab0f7fe3b6e39ee7636d46eda3ec13`  
		Last Modified: Thu, 18 Dec 2025 21:31:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce81fd762306676d63e4ae5519fafe546496c1de85dfad336d2b374a174305`  
		Last Modified: Thu, 18 Dec 2025 21:31:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cf24fb38250394bf3bd2c890aeb366285e89ac794fdb642a0f1af093388c62`  
		Last Modified: Thu, 15 Jan 2026 22:48:08 GMT  
		Size: 13.7 MB (13691865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a851497f663dadb420eeaf4ab47cd1bf0e0d095e4f3f2a29a74a49c8fa841ae`  
		Last Modified: Thu, 15 Jan 2026 22:48:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4eb36cedc42c41e573ca9c2ec035835dad8b25a2e0955b5464be26b3729977`  
		Last Modified: Thu, 15 Jan 2026 22:48:05 GMT  
		Size: 15.0 MB (15024870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4e4730ac5f580b29b12e16ff00cbeeed3f6461bbac3b4e4dddc369b74be95`  
		Last Modified: Thu, 15 Jan 2026 22:48:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3addd654dfe37e2cb8074071c65d1158aca8f30d4fe485e069723a9820948bb`  
		Last Modified: Thu, 15 Jan 2026 22:48:04 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127e5621dd133961cb88510578f403d6f3b388eb480635c979c5761a3b8def9`  
		Last Modified: Thu, 15 Jan 2026 22:48:03 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed8c0b6062bc1babc0a79a7643db46851a2b62fb84c238ab0ae53e4332cd3df`  
		Last Modified: Thu, 15 Jan 2026 22:48:04 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ae392c09526e4df32afadf4abe5f1ab25baf4421b43f88f2d9fb37d59d7a9`  
		Last Modified: Thu, 15 Jan 2026 23:39:30 GMT  
		Size: 1.5 MB (1539800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd97ba8b7b535cda74b3f355a824f230d434011769495656ce2cc6dc73b9eb28`  
		Last Modified: Thu, 15 Jan 2026 23:39:30 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e86eef0e6461d4c0e2362f9f2bbb0d3cb20cbd8cf0e45e5516894cd093da33d`  
		Last Modified: Thu, 15 Jan 2026 23:39:30 GMT  
		Size: 776.4 KB (776356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466ce4e3ddd40c0305ab0bddf00c9f8400a9a1b272236ff4d7615a86d302d9e2`  
		Last Modified: Thu, 15 Jan 2026 23:39:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76d897c5f6a7071dbf25de315291d789220665ab7f452e5570110eb2a79ac8`  
		Last Modified: Thu, 15 Jan 2026 23:40:36 GMT  
		Size: 21.8 MB (21842284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:9e8782502041cea81b617c31a92e7a6cf469e0022a6227e61205e863afe69b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 KB (395221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dccfe581707c893473d92b43ee99721b093601b5cba60c48dbce15b6d3a8e64`

```dockerfile
```

-	Layers:
	-	`sha256:10f7d0128f705c969a88e3de16ee3130bdcc51ae3463850f22de08110806ead5`  
		Last Modified: Fri, 16 Jan 2026 02:57:52 GMT  
		Size: 363.6 KB (363562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4c21e1872b4e1d7097d9d07f05b6e798301c8cb779ffb731e189126b6a4abc`  
		Last Modified: Fri, 16 Jan 2026 02:57:53 GMT  
		Size: 31.7 KB (31659 bytes)  
		MIME: application/vnd.in-toto+json
