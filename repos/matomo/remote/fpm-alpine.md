## `matomo:fpm-alpine`

```console
$ docker pull matomo@sha256:05525b59382a383ac6a4e197186f81c08f1e0108042192436edcf4dc3d7556f3
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

### `matomo:fpm-alpine` - linux; amd64

```console
$ docker pull matomo@sha256:dacfabe09462dc25dbf1a269d1293b26a1dc3b6d951f046f3961d028402e0bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61344895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bae9904d1e65fe3b49f9828067df38eb846dd9b6d2188ebb31267ae14d642f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:04:18 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:04:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:07:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:07:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:07:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:07:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:07:37 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:07:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:07:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:07:37 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:07:37 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:38:38 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:38:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:38:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:38:38 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:38:42 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:38:42 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:38:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:38:42 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:38:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:38:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc381c22afc093b02701ea7d26801e5f8bc363e734bd1329d32f7d7e43ff1df9`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 3.6 MB (3591357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c740ff8b99fd46790bb6390b290de42ce7099d84fbac7504b27a3588714ccf5`  
		Last Modified: Thu, 04 Dec 2025 01:07:54 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054dacb7cedcbcc68afdd2c8a9ab1ee0e35a9ceb5a0840295ad4fd0d2d944af7`  
		Last Modified: Thu, 04 Dec 2025 01:07:54 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edd268a5e867e6244318c34082637d873da4a4d8a4c2bdb4ef1ae302d08b81`  
		Last Modified: Thu, 04 Dec 2025 01:07:56 GMT  
		Size: 13.7 MB (13676351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51b7a6e2771a892024bc3cfa97a4f83864ca7b74618eb4fc92e2664e335929a`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869b10c053eb7477436bceb903eaf223528f45077ee35a6dab6ee94c9272c68`  
		Last Modified: Thu, 04 Dec 2025 01:07:56 GMT  
		Size: 15.2 MB (15174638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f993fa5ab3f7cc2d01c503df819c9420e8ec632cc7ae84add75ee1ff66dcdf5`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca4b9fc8208da9338ae20690d77d3eb73c6985f4c93d049d6d3fca56bcef98b`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 23.5 KB (23487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d092dbf8d7ccda9a3c07fbc692d30434705d85fed14dfb2c6f6b4bca9432ee`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 23.5 KB (23508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a63374b4f48f197771338016f8bdf8efe04e099963e866ba5b556d913d3b3e`  
		Last Modified: Thu, 04 Dec 2025 01:07:55 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9b9d3e782eee9ac71603b215253bed648715be9a32f1c890c9f0b22308505c`  
		Last Modified: Thu, 11 Dec 2025 00:38:56 GMT  
		Size: 2.8 MB (2830344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b12d70f4aa0bccf622ab9ce76ec59f76a8b8a45f5dd56847f0b05e5f369067`  
		Last Modified: Thu, 11 Dec 2025 00:38:56 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc5efdb85cbbd4c64736b7387784b9c3fef92f632de4e614048ba86650a2344`  
		Last Modified: Thu, 11 Dec 2025 00:38:59 GMT  
		Size: 22.2 MB (22151103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792587a9c66600a390993b76677b34822a24c4e2769bc714793fd77ce48d5c25`  
		Last Modified: Thu, 11 Dec 2025 00:38:56 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201e5414e050df5e2070265e94e3024b7c9a076a81c61091c752b746c4c25b2`  
		Last Modified: Thu, 11 Dec 2025 00:48:43 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:d2f225d1f35892baa2c093f3137c24dc9b7c015dfa90ede49825b02d853039f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a78b490987c7c18a8b417be6d9fc0d5cdb298ff72cc05801a138178ff2dc564`

```dockerfile
```

-	Layers:
	-	`sha256:a36efa54c97bc90f385c817c15f68d606b10c054c22f0126c25cab848922152b`  
		Last Modified: Thu, 11 Dec 2025 01:12:55 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:260ca1a2627f6a101257fc1f0002b03e528497a8646356da4694008016b77d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59359063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50a8ad2d6571a049d8a222970bd69ac7638a2a09ba93e4fafc6822042e4201e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:03:23 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:10:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:10:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:13:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:13:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:13:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:13:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:13:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:13:50 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:13:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:13:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:13:50 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:13:50 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:39:41 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:39:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:39:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:39:41 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:39:47 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:39:47 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:39:47 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:39:47 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:39:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282ab84442e5667da6ab76755d677f2c138618e5b0017a60d63a818618ed74b3`  
		Last Modified: Thu, 04 Dec 2025 01:06:58 GMT  
		Size: 3.5 MB (3547625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73582f6b7d2492e7c93ffb23e5878769a782317485b2ac5ac238b60dfc377367`  
		Last Modified: Thu, 04 Dec 2025 01:06:58 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb66864cd68154387ebc22f9d9623f22d3d77a445f6fcd3e4ca8e011bafe39c`  
		Last Modified: Thu, 04 Dec 2025 01:06:58 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe71e1476088e03d5e5de4b045877aa44c1827923ae7bd0bece6b331640baf3`  
		Last Modified: Thu, 04 Dec 2025 01:14:04 GMT  
		Size: 13.7 MB (13676399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fd6ae9e0ed34dd07593ea5d3a45bd9c88b53a7872d148f88256eac9c623dd0`  
		Last Modified: Thu, 04 Dec 2025 01:14:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972fce26c06d50aaafdd40816f26aee787e6f5dba2b03a091349dd08488cae0c`  
		Last Modified: Thu, 04 Dec 2025 01:14:04 GMT  
		Size: 13.7 MB (13667783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243296c3b1687861e7d9e578cac3f25d58b18eed39f084d88bde175bbc793298`  
		Last Modified: Thu, 04 Dec 2025 01:14:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd887ec93be8d760fdd9fad3ea2705674fe4ce7cf248ce72757e9bfd5f3c53e`  
		Last Modified: Thu, 04 Dec 2025 01:14:04 GMT  
		Size: 23.3 KB (23333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd127b364805d092e50c01c5772ffe4319aeee24526867648f0136131150f0e`  
		Last Modified: Thu, 04 Dec 2025 01:14:04 GMT  
		Size: 23.3 KB (23347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1e012cf4b899dd1dbd8088e1bc5c9c2f021ecf484ec13f1e802a762696dcd2`  
		Last Modified: Thu, 04 Dec 2025 01:14:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0abef2c404810a1078f8aa326e19c18cdc6ddd64659047ddde93bd2101e5`  
		Last Modified: Thu, 11 Dec 2025 00:40:06 GMT  
		Size: 2.7 MB (2686555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1299bd45eb3551ba7ab4c231fcd283ee2466766d6fa69c2beee5a13b08cfb0d2`  
		Last Modified: Thu, 11 Dec 2025 00:40:06 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989b1b3d2789c7c60139f5827492870a4893a6cbdd497977cc1978cc8ec31cd5`  
		Last Modified: Thu, 11 Dec 2025 00:40:10 GMT  
		Size: 22.2 MB (22151331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f54e1996b528a1125f4710e3472998bce84b1e8de05ae7ede7736b7192ae1ce`  
		Last Modified: Thu, 11 Dec 2025 00:40:06 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7558b7c42da5c05b16a1c47f05311882c61d942ace5a0a6d2e9666eee840b7`  
		Last Modified: Thu, 11 Dec 2025 00:40:06 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:fb32a8c6815d6313622d1389a98f551a3c4ec5da933d3802cbcdb0f671618754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4cf9b9f29c9e8dbd6dff734416044f70cca5bdd95243c38dbfd1bfb5ace342`

```dockerfile
```

-	Layers:
	-	`sha256:07fa6a77bb0cfb9adbfec20dae3c8067fbcd3b05579da4490d9079c569c15d2c`  
		Last Modified: Thu, 11 Dec 2025 01:12:58 GMT  
		Size: 31.6 KB (31610 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:62b1c2e577cd7925c0e89f662744042f3b4ecbde06c5a3a438a5fa77fd9d2711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57968050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b24036020f01de15337f1c8db027a543598bd8d26f850a8647b8defd59d360`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:03:22 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:07:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:07:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:10:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:10:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:10:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:10:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:10:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:10:11 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:10:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:10:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:10:11 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:10:11 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:39:23 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:39:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:39:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:39:23 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:39:27 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:39:28 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:39:28 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:39:28 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:39:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd894f51e3764736bb05301b970f25645c1cf3e4f8c635b1c60a852a93f7ac8`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 3.3 MB (3346525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9259ca1939c2345efa94c49afa3bb7114bd93157c3c12c9d71e12b61fb659030`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe771a7bc75ff2477d17a4e1e5f8a78571610720921b5a8e6b761dd954c99c`  
		Last Modified: Thu, 04 Dec 2025 01:06:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721a295816b865b9072f65802d34d9904fe939654b367bcd434b59973e994cae`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 13.7 MB (13676364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590389d88b30bcacdb597cd70702395962e08e3b8f5f2469b82fa6f77ba301f`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1578098c266a015ffbb817415e4551197024d094ea098635a78f02c9b1dbfaac`  
		Last Modified: Thu, 04 Dec 2025 01:10:27 GMT  
		Size: 12.9 MB (12905781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7ed1dd8e10a8310b2591cae448b8526d7cc0927ec73e848840245c0760a8f`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b8e31d695cca008dc4758a98461b22f9b9a2f5cb4baaa7378e80672e38966`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d42732065277b79cd0ac41d5a2d9933c840610251e1d8b07e8651ae854c41fc`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 23.3 KB (23347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6a5f7f80d131611662fabccd3822ed9e251bd2e1aa9af0287fd64f2ed7b097`  
		Last Modified: Thu, 04 Dec 2025 01:10:26 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87a3d76e6c8e3af2729eda940eeb1f521bd522d67def6b7bda3955000c5c0e`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 2.5 MB (2548127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45439946fb2d17509b4253021954404601dd51a92edb147ace2bab32fc9345`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a999c49760b2909a099879c4b17146e3624be864c447d3aa028445886541e7`  
		Last Modified: Thu, 11 Dec 2025 00:39:48 GMT  
		Size: 22.2 MB (22151324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c73bbad9fc55a56c9e4d1c37c6f14f7d408a329722a872027cecbc0e144f21f`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f879dab28b7527cc48eea6bbcee171b4ac6cac6f9f16a5cbe12f3605c63886`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:c55504a34c17747991edcf2695dbfdd7d7ca850746d8c994c7a845a90d794445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4758f1e6054b643c010122d5ec0b0d3c57a4eb3a14b6f68dc61666e1ab887`

```dockerfile
```

-	Layers:
	-	`sha256:c51a153b5de9bb34eb55e54f1f4470ff737ac36213e8704fda720b58d951f4f0`  
		Last Modified: Thu, 11 Dec 2025 01:13:01 GMT  
		Size: 31.6 KB (31610 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:152051e5e0f5ecec8a6a0f3db0c20d81715099a3a8fa1f3b04c9ea2d471e5531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61204494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a152c3b5d721886027174d37c5031a5e49aebaa8c7a7d3da2d710dc9cdcc7605`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:05:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:05:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:05:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:05:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:05:46 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:05:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:05:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:09:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:09:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:09:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:09:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:09:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:09:10 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:09:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:09:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:09:10 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:09:10 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:39:19 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:39:19 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:39:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:39:19 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:39:24 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:39:24 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:39:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:39:24 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:39:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8f6818f2b4c8063bb18759e2c7020abede0da990a04ac78231557e2251d5f7`  
		Last Modified: Thu, 04 Dec 2025 01:09:29 GMT  
		Size: 3.6 MB (3600609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fa82dc6805c7b8c66c152a9808394315bfcc0cff5690ddc4a3c2d5ea0b48d5`  
		Last Modified: Thu, 04 Dec 2025 01:09:29 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6f187c586428770f6e8ab0f7df259d4e638fe97735b150d47ba796ecf46c69`  
		Last Modified: Thu, 04 Dec 2025 01:09:29 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d887a51e02d6cfd2c5e030f622450a1f7f1b376bef576e3a0f419f6354c380c`  
		Last Modified: Thu, 04 Dec 2025 01:09:30 GMT  
		Size: 13.7 MB (13676351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6039c19b05c6dabc703a14a2d773a473d4e0e1e22879d9d6cd7870575bbfe0b1`  
		Last Modified: Thu, 04 Dec 2025 01:09:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4a3e7e05aa44443f5ae3e4271ca949d6e214f01714c7ed54af17c56d3f21a`  
		Last Modified: Thu, 04 Dec 2025 01:09:32 GMT  
		Size: 14.7 MB (14683884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b67105a9144a6e398227703915785f934cc83fba7dea08208ea95eca963bde`  
		Last Modified: Thu, 04 Dec 2025 01:09:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee24e75cd58c648160be3c4a395cdb3394546fad4f69491f382b6ed5bf885a7`  
		Last Modified: Thu, 04 Dec 2025 01:09:30 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426a9ad64d069ac6cfe8fcef5b0a91bb62ee3293ad0e869e4e1487159a2566aa`  
		Last Modified: Thu, 04 Dec 2025 01:09:31 GMT  
		Size: 23.3 KB (23342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd665a2eb61f764194db661b4e331df88406223a13a2b76225c746d129965ff7`  
		Last Modified: Thu, 04 Dec 2025 01:09:31 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416eb5db3e0ade4d82ef2d5354c15b253a5edac8f88096bfc3f48c858afa5c36`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 2.8 MB (2835741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adddb092356696af49443b6c9287a29e5726505355a7ae7cc3f3998e1307171a`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965588e6c539906d4cd8491164d25bed138dee4c72250fe6f0592e305b7acb3c`  
		Last Modified: Thu, 11 Dec 2025 00:39:44 GMT  
		Size: 22.2 MB (22151251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b8763902528a01c3447658833722aef7a06e47f0df4c343e0c4b636731ca75`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ccecf6585f9eb2a849f69224596d6984373f78ce96963e9f999a6db8aaf313`  
		Last Modified: Thu, 11 Dec 2025 00:39:43 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:4ac550cc00f463bc52c8d2b0d8738056f0cd6a03ee61a6e1888e9523655beaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3112f8a8421033243790a33dd45dac294eb7a33dfbf38c0aad0510d053c908`

```dockerfile
```

-	Layers:
	-	`sha256:f44ac5b72cfd467a46511734ee8170b4316f48b30c55b2424e3ea924e5de937d`  
		Last Modified: Thu, 11 Dec 2025 01:13:04 GMT  
		Size: 31.6 KB (31638 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:db0cf04c5bfc2970551865b1cd952f71c912fe6dbc7d692086bd69bdf32472e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1bd207f673eeab7e841140dece2705eef7c2abddf675b27e127509a09c1227`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:04:49 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:08:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:08:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:11:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:11:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:11:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:11:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:11:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:11:39 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:11:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:11:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:11:39 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:11:39 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:38:45 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:38:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:38:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:38:45 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:38:50 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:38:50 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:38:50 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:38:50 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:38:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:38:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40f3c13450f02007e17bc20fb8f9181bcf7b37b2b54c84a50f34c48644f01dc`  
		Last Modified: Thu, 04 Dec 2025 01:08:13 GMT  
		Size: 3.6 MB (3628341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9155a3e54b80d1c7e22085266af719e9ac8732911fdc3a88099d3807a9752a80`  
		Last Modified: Thu, 04 Dec 2025 01:08:12 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927d906183c357c72a3ab3419979c42e1a0fbd64bea0e115031573c3d916158`  
		Last Modified: Thu, 04 Dec 2025 01:08:13 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf1cc81cbd25c7e6a20b3d0e3d925b7c475bcb0f2321d82d213191a931cb550`  
		Last Modified: Thu, 04 Dec 2025 01:11:55 GMT  
		Size: 13.7 MB (13676352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec43c7158f2d20491f559d806f730a022d16d01f21a06aa88a5260552785a5d`  
		Last Modified: Thu, 04 Dec 2025 01:11:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fad202167e178e6ef1a5a5b2b3a0a4241594cbc9a7750b3f17c915e6cf4e2bd`  
		Last Modified: Thu, 04 Dec 2025 01:11:55 GMT  
		Size: 15.5 MB (15485408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef7e560e47210d2bc86a9aaa0307c3a02715b85211ff548296840fb95554bf3`  
		Last Modified: Thu, 04 Dec 2025 01:11:54 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f228f750f69a8394be033d4735b9c3befb83d2135bd95216ac15aba8bee40ce`  
		Last Modified: Thu, 04 Dec 2025 01:11:54 GMT  
		Size: 23.5 KB (23497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9cc8ac37d108737f595f63df986ab4b00e073b44f2161908688c37ce46e9e8`  
		Last Modified: Thu, 04 Dec 2025 01:11:54 GMT  
		Size: 23.5 KB (23512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4923bfe5f49324fbda7f3d56664d1c96432566d33263d075d42ad5fff83c0126`  
		Last Modified: Thu, 04 Dec 2025 01:11:54 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ca55feb61c8dc4fd40dcd9cd483f7bae5ae2a22809571155c4abb10f472db`  
		Last Modified: Thu, 11 Dec 2025 00:39:09 GMT  
		Size: 2.8 MB (2834257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9a2892c7bde2e51b82078381c92821b565ee8409d1ddd752c8184c04acd822`  
		Last Modified: Thu, 11 Dec 2025 00:39:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5de0f3b425b526ecedb403c7a5a3d77cbb0b1bdd76d6619449fde717a3a1241`  
		Last Modified: Thu, 11 Dec 2025 00:39:11 GMT  
		Size: 22.2 MB (22151061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e95009da512725b3d2e69b523d07098972428b87c7fc6ac0d3da311ba8579c0`  
		Last Modified: Thu, 11 Dec 2025 00:39:09 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a5b5105af04cdf28a76b4e0bdf09e6e595db30795430bf8e3db164f6697e9`  
		Last Modified: Thu, 11 Dec 2025 00:39:09 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:eccb8bf61833fb3d163e25522ac99af2534608ec7faac13cecd41fe014b5883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cfa5bac35874c674207da3e99e927a689bf6c8d77a237eff0cfd60868c4840`

```dockerfile
```

-	Layers:
	-	`sha256:12da712b4e08f9bb9208005d54d0aa2ac2656d33ffcc4be10071844808783983`  
		Last Modified: Thu, 11 Dec 2025 01:13:07 GMT  
		Size: 31.5 KB (31468 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:686de0c8d47a34541281340b93874a9f3e9c3d7005b9762593154baf0a2710da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62257112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b6a85b3c93fc6d9ca92e43f1fb68b5f6ff58070601ad9124a9fead1e59bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:04:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:04:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:04:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:04:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:04:39 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:04:39 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:10:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:10:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:20:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:20:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:20:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:20:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:20:26 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:20:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:20:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:20:27 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:20:27 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:40:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:40:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:40:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:40:14 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:40:23 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:40:24 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:40:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:40:24 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:40:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:40:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0a7d1a3b5b7008c71c24d3d5a87883f4c3804bbe6f605d645eca31542c453c`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 3.8 MB (3768890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4195a5efebe02f479fe9c6976a2651e23f862d3990e7d601648b7bd1f929850`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79239a134bbad0459d3e57c5cc7de1311cda2607ee4f1b08432fc54de839a4e5`  
		Last Modified: Thu, 04 Dec 2025 01:09:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fb50256cf5cfef74e3383d7fa4ca3e5c53e437ebd969bc0fb6829868faccb6`  
		Last Modified: Thu, 04 Dec 2025 01:15:30 GMT  
		Size: 13.7 MB (13676360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a844a2b3b9af21a2e476cbbc2808c5fd83d1ba1ca7f029f11da4cb630ce8b19`  
		Last Modified: Thu, 04 Dec 2025 01:15:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58edcb7addd3a3306a7dafb48950a9f4fdc01310c86eddba6b64ffaefb45ea6`  
		Last Modified: Thu, 04 Dec 2025 01:21:05 GMT  
		Size: 15.7 MB (15716504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b31f558c52d39e060a61155e22d222ce5ca97bf5b98c92fb16800e4613c0152`  
		Last Modified: Thu, 04 Dec 2025 01:21:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4cb022e8ef9565628ace41c252c90d6851707201f489a5e386ab7f8e5175`  
		Last Modified: Thu, 04 Dec 2025 01:21:04 GMT  
		Size: 23.3 KB (23339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235f2960210453009b9c31adcf5dbc9a2363e74edcd7b4f539b233145a39f74`  
		Last Modified: Thu, 04 Dec 2025 01:21:05 GMT  
		Size: 23.4 KB (23360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d486d352329a5e6e75fab05368b786fe620610f9de3c6b083a91e1b56fea205`  
		Last Modified: Thu, 04 Dec 2025 01:21:05 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10275d18448ba844ff3cc191cb59fd651082ee575abeff93e56fbf548c1e3be`  
		Last Modified: Thu, 11 Dec 2025 00:40:47 GMT  
		Size: 3.1 MB (3055606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2932e2807e6e9fba980a012c8c1a7894b42071591d2d9255a79e30219cbd4a2a`  
		Last Modified: Thu, 11 Dec 2025 00:40:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a041d9ef5aca0b7245e1cf74454c709dd7c3366db4d32e6a442c3bacb9d417d`  
		Last Modified: Thu, 11 Dec 2025 00:40:48 GMT  
		Size: 22.2 MB (22151232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523caaeb43274496957aa3049bc8e78af0f60af0e0b21e1499401e49fccdbf51`  
		Last Modified: Thu, 11 Dec 2025 00:40:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419913762d0e4336ff61035f84844920441b6d75c5317efebbc573872251d2d`  
		Last Modified: Thu, 11 Dec 2025 00:40:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:3b757a8c1c882810fe1bc70d9ddcb8e92c57cc81b3726abdeb5f268897356fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f5ef025b22cb992b83ebf19c3492ac9cf03132dcadffdd079479366e42553`

```dockerfile
```

-	Layers:
	-	`sha256:662c70437df961968fef15def6741c244c9e6b924a04f8b3b81240889483ce84`  
		Last Modified: Thu, 11 Dec 2025 01:13:10 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:fc7b8a49e66459c3153ea570cc2d81715632eafd12c61ee002f5552958d74c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae780e95b39d9639e29584ae448acdc7a71163abcff1c4e6d803a87f46d8c5af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 04:20:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 04:20:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 04:20:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 04:20:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 04:20:59 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 07:28:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 07:28:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 09:25:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 09:25:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 09:25:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 09:25:23 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 09:25:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 09:25:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 09:25:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 09:25:23 GMT
CMD ["php-fpm"]
# Thu, 04 Dec 2025 20:01:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 04 Dec 2025 20:01:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.27; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Dec 2025 20:01:50 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Dec 2025 20:01:50 GMT
ENV MATOMO_VERSION=5.6.1
# Thu, 04 Dec 2025 20:02:08 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 04 Dec 2025 20:02:09 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 04 Dec 2025 20:02:09 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Dec 2025 20:02:09 GMT
VOLUME [/var/www/html]
# Thu, 04 Dec 2025 20:02:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 20:02:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2559d37315299ac2974df718491e68e75407bd4024398180bf2e31452dba7291`  
		Last Modified: Thu, 04 Dec 2025 05:22:56 GMT  
		Size: 3.7 MB (3739982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3bd8574cb0921dcd93805f3fca6feedf60a33fb9c08e52f2eb9827989b0a`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8090aa9a6be2d187aa1322d22eee1829c9afdeb8a4c68df173418fa6face7`  
		Last Modified: Thu, 04 Dec 2025 05:22:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b6f1d80a56f12660d5596d9ccb80af5ab2555709531ec9536283065ba2b7c`  
		Last Modified: Thu, 04 Dec 2025 08:27:14 GMT  
		Size: 13.7 MB (13676356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4cd5b409854fe4a455aee413aea8743702d3c39940d594e8a1d5df3b733c7`  
		Last Modified: Thu, 04 Dec 2025 08:27:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc5f3cd1bc938589d3af8bee2a0a760eac5593351c8cfbf7daa966d79bd79a`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 14.5 MB (14451333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dea69d8712081a20f50702211ef8728c137aef12d913a49d7b3b2210aa82298`  
		Last Modified: Thu, 04 Dec 2025 09:26:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce5c9a07f0e52fb87d03303a9f5405bb267fc835bc6e3c87635f0f0732cebf`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 23.3 KB (23308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f45b2944ae118a8ba724c516eb2a8946f88256c5d31706a46d89fb1ad4b979e`  
		Last Modified: Thu, 04 Dec 2025 09:26:30 GMT  
		Size: 23.3 KB (23336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deefbbba63184595d7d47d0b71530760ce003b267843b476a5c4b464abb797ab`  
		Last Modified: Thu, 04 Dec 2025 09:26:31 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5328f1bf5411412c34d666bc92c67b67fd859619e3c748e870eee05a38ef00`  
		Last Modified: Thu, 04 Dec 2025 20:03:08 GMT  
		Size: 2.9 MB (2884526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a73a9f3e3666ac09fa883d8ea95ced360f0fd323f7ece322dc169516b2a8e5`  
		Last Modified: Thu, 04 Dec 2025 20:03:08 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127e730d03f6c5d3a4717a72c126e8027a8e5e44463e2dc21fb1be835bb6325`  
		Last Modified: Thu, 04 Dec 2025 20:03:10 GMT  
		Size: 22.2 MB (22151231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98a9fe9eaa3d08f2a0ab1421e75274747a020ccea5f7dc74f331c79fbe72ff8`  
		Last Modified: Thu, 04 Dec 2025 20:03:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5cc8c7fa9ba8aeacf0c4f69f17082c80d38dfbbd41ad8589941d448c411c79`  
		Last Modified: Thu, 04 Dec 2025 20:03:08 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:ed93d8d35aa1402dba98db059165f9733a57722863994482d33c55688856f026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba31e284d1e724627cfa18b5caf9bd39ce65671dcf1bd8aba0a6353f3a4eaf9`

```dockerfile
```

-	Layers:
	-	`sha256:f68d417dd6e24f76fa75911f82093bfcf0863d880f9442e8af0c392c53412749`  
		Last Modified: Thu, 04 Dec 2025 22:11:41 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:075ef752fcf80c3bd8d71c4f3b36ba5541b5f69270f3d6f131dbdef8580e9894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61247009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cb8a70b59b08dd845f200d9875353049e30f6fb83c87fc323e37a766a85ba7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:03:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Dec 2025 01:03:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Dec 2025 01:03:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Dec 2025 01:03:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Dec 2025 01:03:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Dec 2025 01:03:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_VERSION=8.4.15
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 04 Dec 2025 01:03:55 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 04 Dec 2025 01:04:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Dec 2025 01:04:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Dec 2025 01:18:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Dec 2025 01:18:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Dec 2025 01:18:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Dec 2025 01:18:14 GMT
WORKDIR /var/www/html
# Thu, 04 Dec 2025 01:18:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Dec 2025 01:18:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Dec 2025 01:18:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Dec 2025 01:18:16 GMT
CMD ["php-fpm"]
# Thu, 11 Dec 2025 00:36:35 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 11 Dec 2025 00:36:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Dec 2025 00:36:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 11 Dec 2025 00:36:35 GMT
ENV MATOMO_VERSION=5.6.2
# Thu, 11 Dec 2025 00:36:40 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 11 Dec 2025 00:36:40 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 11 Dec 2025 00:36:40 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 00:36:40 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 00:36:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 00:36:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57875495d370cfefa264d828344954d60baa21cfed9c624ccc8c3f7017d281f`  
		Last Modified: Thu, 04 Dec 2025 01:11:43 GMT  
		Size: 3.8 MB (3793991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a484672f7cc3379a76694729bfaa2a2fc1eed11bf2448fd84a78a6c0e5cbf8`  
		Last Modified: Thu, 04 Dec 2025 01:11:42 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e20e4686724e9dce787d50b8e7300dbca70dabe54a633b4e671c04ac36e27`  
		Last Modified: Thu, 04 Dec 2025 01:11:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237aa36c44796eb102ff0717bb1e63f78aaac5d6bb8b6edde4cfecd653ac5d44`  
		Last Modified: Thu, 04 Dec 2025 01:12:07 GMT  
		Size: 13.7 MB (13676362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961f2d0ceb7670e7e99fd9c2a3a2e010a9fdca3aeddce7138f3f348ccad7c24`  
		Last Modified: Thu, 04 Dec 2025 01:12:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81987196c07e62c0a120ffade2285400d8033516352fdce4c64f38902cbf42c5`  
		Last Modified: Thu, 04 Dec 2025 01:18:49 GMT  
		Size: 14.9 MB (14930109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e9656a162e2c1ffdd25cf650ccb65d7724e2556fed6ff04226283bbad506d6`  
		Last Modified: Thu, 04 Dec 2025 01:18:47 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed158a0da4993508c7f621c3b055a252ab549bb6819f5a74d2b795b5fefc29c`  
		Last Modified: Thu, 04 Dec 2025 01:18:47 GMT  
		Size: 23.3 KB (23335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873f4caa6c65cb8f9c00db6333dab888b64c1bc5c4f4440506987c3ded0a9388`  
		Last Modified: Thu, 04 Dec 2025 01:18:47 GMT  
		Size: 23.4 KB (23357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce21b0b318274894904c8a1ba421608c1a756ea703a8de88c8eb6b0557cfc66`  
		Last Modified: Thu, 04 Dec 2025 01:18:47 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc20866c5babbf75bffccc87d5958a139da9897e0014df23e4879488e2be50ca`  
		Last Modified: Thu, 11 Dec 2025 00:37:14 GMT  
		Size: 2.9 MB (2909960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c84b60f292da64a243097b1fc6e1a0f03a7c632efd3ac02a9039ed2a44247f3`  
		Last Modified: Thu, 11 Dec 2025 00:37:14 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e341c459d5840c09fb0b108d8d35094de598e231f6f74212b818629506653fd6`  
		Last Modified: Thu, 11 Dec 2025 00:37:15 GMT  
		Size: 22.2 MB (22151284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed776652d76c5b845df6ec24be6f496fbda614cb2f57d5f1df92eea441fc53b`  
		Last Modified: Thu, 11 Dec 2025 00:37:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef3393a6519e3a6a915961f6ab026665411561a369ccdfcde7d26a78d0c31a5`  
		Last Modified: Thu, 11 Dec 2025 00:37:14 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:9926523e8960efd8eb0d49c1907ff4eb1ab1efc86678fefeb59c14c09648dd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dea6524f112be24addc2142beae0122bf384a50c96d01ad65b83014f47ef4f`

```dockerfile
```

-	Layers:
	-	`sha256:cea0c76224e8488c721a803a023c24fe0040afe8ea16153fc92431db3caf0116`  
		Last Modified: Thu, 11 Dec 2025 01:13:16 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json
