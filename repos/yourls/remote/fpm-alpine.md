## `yourls:fpm-alpine`

```console
$ docker pull yourls@sha256:1a06e2439584618c615bb7a2e381d3dd67f40bbb4e159c87432ed748e98bd282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `yourls:fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:94e87553a8d3f49ffeb213ae5bedc27c847fc3d80fbd7ee804ddeab5928725a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40644106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2dbb163f0e7ab742ba7fc35f902191ae05944d9bf013d4bf0ff6b4035fb204`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.17
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207bc05a08b8daacc010304596f4555c7dd7e512b07f0e8712ada4bfe812dd5d`  
		Last Modified: Fri, 14 Feb 2025 04:09:18 GMT  
		Size: 5.6 MB (5629163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477d1fe83bf94e1a24745e1da620b1e5dff6e9b9487d5387fd639cc44415f460`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c856e5b5022081d97a2bf6756bbbdd762f86e95f01f318666c06a8ccc34728b`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c0720d0e317abfde2b6515ec4bea9f6ab51e839ce55bd642f85bdf38eb991b`  
		Last Modified: Fri, 14 Feb 2025 04:09:18 GMT  
		Size: 12.6 MB (12562516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a127c2fcd663cb8eca722691ac7b44e2703caaa57de8c4398053b6facfd1a6`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff89a2b054fdb11435f0a56e735ae74f7e2a33f23e2f0907e91dc8efe87e33ca`  
		Last Modified: Fri, 14 Feb 2025 04:09:18 GMT  
		Size: 13.7 MB (13664864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327aaa073171c0ae0456f06b31d7d55647c3f254ffc3da55c218c1824753b4f`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c9905f4dab912dcc7c8cf86c1e42cf084be61e0af2e1a8ae9c1b63715f07ca`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 20.1 KB (20057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5733cb80c37001c01e13c6c34201cd6116f1db64119ccf40bbfa0a80f6a81258`  
		Last Modified: Fri, 14 Feb 2025 04:09:17 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec793973462702fdfabd6424dd67720169709ce007000e90c4bf250c739a129`  
		Last Modified: Fri, 14 Feb 2025 05:43:36 GMT  
		Size: 553.3 KB (553285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8db4522a2f04bc4d74f840088904f8225a38a2bf1b77040806cdcedc8b89f5`  
		Last Modified: Fri, 14 Feb 2025 05:43:35 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b714a032c63fb04e2694d2ff5fcb094c6fcd63f3e1c694e79deda67879106f`  
		Last Modified: Fri, 14 Feb 2025 05:43:35 GMT  
		Size: 481.8 KB (481782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe54ee03523d0509134750717afa9c1606565d69611fa3f8cab8739eafc6ae69`  
		Last Modified: Fri, 14 Feb 2025 05:43:36 GMT  
		Size: 4.1 MB (4073361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea896d1d022ff881c580f33a3e32470211bf210d984da7d508e3a559c1c478e3`  
		Last Modified: Fri, 14 Feb 2025 05:43:35 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08003f814b48a9c4a32f0ab0a42ae26787f2c543a303feb8b691b8247935aa63`  
		Last Modified: Fri, 14 Feb 2025 05:43:35 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:e3f233730d57b786e2aff1553bc03ee5b2bb1aaa3028537afef02e997c89a8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03932aef1f8e5c65a9b0355d28e6e9aa5591125cf73d022aa44b1ea3c37bc278`

```dockerfile
```

-	Layers:
	-	`sha256:f5c15aff6a011514283afc9bf6cfb99a7ae1344b547fca462e454cd3365b16e1`  
		Last Modified: Fri, 14 Feb 2025 05:43:14 GMT  
		Size: 30.5 KB (30500 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:a2b9d0911743bb4d965cf808082f3301929771f5d7280c7a1d8695239ea42e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39290792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c243b4771855204ef0e8fef8527153f8ee753fc2f952035bc3134b839cba6d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.17
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36ffd5d56565f408fead8730ad00c88d09d80e13a91f0f16f2665e72b8adcf`  
		Last Modified: Fri, 14 Feb 2025 05:14:06 GMT  
		Size: 12.6 MB (12562547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc7ebdcd6ae994284a7b614c330571e0b52ebc1268f23a7afc6e8e19a39fcbb`  
		Last Modified: Fri, 14 Feb 2025 03:43:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e129beb7133bfa10f86502b0d147f55fe4a5b52ab56a10f41d3b9b992f3bf`  
		Last Modified: Fri, 14 Feb 2025 05:14:06 GMT  
		Size: 15.3 MB (15299214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5654536bb52da87a969b1ac07d476a7faa9942549c64f2e45bc37e59f53d65e`  
		Last Modified: Fri, 14 Feb 2025 05:09:29 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788579a25dcb477a3029c4666c21510f435575bacbbba414240f33505d63e0e`  
		Last Modified: Fri, 14 Feb 2025 05:14:06 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e05375deda5b2443638979962a7e8549cf98087687590305f1e3f95228576c`  
		Last Modified: Fri, 14 Feb 2025 05:14:06 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c4573c12a53980ae7ad90150599ac0f9ee97fe2b0badfa48dcd443f4f21249`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 172.7 KB (172748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169419d223324920c198b202997320b6dc6359ac7e0e651a044f8881fdae80a6`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330210d3e6de997df2e0ed2eadd2b8e1b1c2fdb4822b5fd6d2a69705f30e743b`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 481.3 KB (481314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8473db087f7ad7f53d8a17304a69d5fce1b8f27dbc33922eac014f3efa539559`  
		Last Modified: Fri, 14 Feb 2025 05:43:32 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69653565c14cdbc4f2bce5108836c912f041f49a13c7bcda63ffd589262d339b`  
		Last Modified: Fri, 14 Feb 2025 05:09:30 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6134bbbb3f3062b7191c43b1f4edf86fc932b496fe81aaa41404fd129761e0`  
		Last Modified: Fri, 14 Feb 2025 05:09:33 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:7a38df980a09a18da2970896a3f693b40cef3ade21f1bde4565e63a99e72f93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12081af9b611d940259ff37ec51be02543e4c9eeaf732c59f00c5f7a6cae8a79`

```dockerfile
```

-	Layers:
	-	`sha256:78db658ab048b49ba2dad7c6e32fd12e41699695087109a4506b5f5f96c7ce0f`  
		Last Modified: Fri, 14 Feb 2025 05:43:15 GMT  
		Size: 30.6 KB (30615 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:7f40575a8bfc5940b6d193ceec1499a3c3cf9032dc8d5ef467e9d689ca991203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34741150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee86ed24ec6386828faf0c688d4166954f49a859a54e4e3ae72f651c3e5882e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.16
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0204e80c0296cdae0cbaa8fe8c132f49b9c6f8c1700e5c9d1b71849266b1c96`  
		Last Modified: Fri, 17 Jan 2025 21:23:15 GMT  
		Size: 12.6 MB (12565935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b976bccfd388504dcb1ae8991cef4eb2890a7d4f843ed9d26528f97837f9da`  
		Last Modified: Fri, 17 Jan 2025 21:23:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06915eca9877d9be2e06530e8c442b3a0bea045c98d533126fc6ff2bceee37d4`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 11.2 MB (11249099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c86c92b496bccd4526be3879519d53e5daa8819acd1e44b18e710d8ac090ca`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1ced4a77966f8850c5fb7d6bfc943c4888012a4921f49b3a3dacc4bc627f7`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ec4d14ce3d25d025ee7927a6c0d15093dfff4d08c3c458131c6cd56b57bfb`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da52eb0b8862cfd30fc5f19fc7815683ab3f89dc1fd604cc0441ede601193041`  
		Last Modified: Fri, 17 Jan 2025 03:14:13 GMT  
		Size: 161.1 KB (161099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac00002c517a1a0ac5a46ffdbb9ace523e6e2c307b870c968b9b3f73519ee9`  
		Last Modified: Fri, 17 Jan 2025 03:14:13 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf23c77ce433bce42dfd2f44b562cc7aa5dca26f090d2395a9a49ee5ded5758a`  
		Last Modified: Fri, 17 Jan 2025 03:14:13 GMT  
		Size: 442.0 KB (441972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db3b3339e97d10a9a2291a9e6eaf4006388c7a56210f4b5e1ffe1b530c231a0`  
		Last Modified: Fri, 17 Jan 2025 03:14:13 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac38334c6dc18430e1a88f06763d2442507d2399839aa064614c2e10df80d1`  
		Last Modified: Fri, 17 Jan 2025 03:14:14 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7bac9c2c01fcdafe9a7245039efd239733523076b9383b69cdfa1a457a4740`  
		Last Modified: Fri, 17 Jan 2025 03:14:14 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:12429dd175c709d47a35417328a8282e102ca5c5d6e0ff92f8a6306dc62f8f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d84f8627d9f4b641d9fc23f62fd4c2e9fedecc97bff73abd49eb5271042a1ae`

```dockerfile
```

-	Layers:
	-	`sha256:162618ef5baabbd120dfbaf4e9482cc9664ad53278181219160cabab4716d9de`  
		Last Modified: Fri, 14 Feb 2025 05:43:16 GMT  
		Size: 30.6 KB (30615 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:49016cd1d8500d7553a681025ad18a392c33e0c1b2fb5bd81db14651a7892420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42548415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bc17aa19f323c1ed03c6592771dcab07119c2e02520a723d5cc72379139a4a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.17
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af101dced5bbfaf8db0f7a341e07a2bbcf3ca04ee7fdeaa370569ee26a2dd3`  
		Last Modified: Fri, 14 Feb 2025 05:15:24 GMT  
		Size: 12.6 MB (12562573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4be92213c02d53e83c0fb7e8726a03cfea142959fb42136fa3583d97d92900d`  
		Last Modified: Fri, 14 Feb 2025 04:07:14 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef51b5683fb7be49ff599614da24b1b33fc62a90377973d09c64c61aee8b8209`  
		Last Modified: Fri, 14 Feb 2025 05:16:20 GMT  
		Size: 17.2 MB (17194493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613782ac90e254b369cba885d635f48faeefb7d80ea93679db904d55a1ac0a29`  
		Last Modified: Fri, 14 Feb 2025 05:07:12 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ff754287f92e7add46ec8e16ce098f761b6102bb64ef798e4a23b53d872819`  
		Last Modified: Fri, 14 Feb 2025 05:16:18 GMT  
		Size: 19.9 KB (19895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efdcb3e09eaf6e6945d7682c7be10fb1fef1f195b94fb24096338ff94c7df57`  
		Last Modified: Fri, 14 Feb 2025 05:16:19 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156f4ee2977eb371c0abe31ab50c3ddb40e83f2f957c58bd5b6664471d40bc6e`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 824.1 KB (824070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706bff6224dcdb704d250bee3659bafc2c66fe5a30452291397e4be6d8c29c0b`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4888e8650b62bdcf90b9096607b2f52e41d2aaf3cd884c70e88503e5c9796081`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 536.6 KB (536621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769aeb0b428baa4d54023d5adc7c942d4e733269ee7c18635bceffeb8bcb31da`  
		Last Modified: Fri, 14 Feb 2025 05:43:32 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa1886e3750d9f7f2050ae2850102b6e5a5a48cbcd045e33f937e77b9653d75`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4499c1b9750d1e5813db3eb6fe3f7bdcf37cbb432f58e006fb7d2c0c7ff25bf`  
		Last Modified: Fri, 14 Feb 2025 05:43:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:4ef595406dd786ea24f405ed9fbdd86606875bec82c5955bca41c1a18820e2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d562624892de056618b41f48b4e89cb3eddc4c2af4b3c4a80c77c94f200bfb4`

```dockerfile
```

-	Layers:
	-	`sha256:1894544acab857eb62759d0978ce4c07fdf3262d59e8a82cdde55bfcaff181f0`  
		Last Modified: Fri, 14 Feb 2025 05:43:17 GMT  
		Size: 30.6 KB (30649 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:bde38cc9517dbe6e1a002c6e067d8d803703552310139f7081d0bffaed5df261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40615783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c500b7b244494bcc704f4cfebd02fe29f8c55711d3e284a0aacaf6dde241e139`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.17
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7a589dac8a3b0ee1c78d0061d1dfb467fff00c19b5f1915498cc20097f0962`  
		Last Modified: Fri, 14 Feb 2025 04:08:59 GMT  
		Size: 5.5 MB (5479165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c54e161362085ad35ef1b732a7c39eb44105242169135628a79a775292c5a0c`  
		Last Modified: Fri, 14 Feb 2025 04:08:58 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0c0da825ac23007330f86c31c36fb1696d82e90dc9882a3bea76f77a292e43`  
		Last Modified: Fri, 14 Feb 2025 04:08:58 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e639ee2047223f2e74e52d15e36305acc073595dfcfff6a0496115829f48f`  
		Last Modified: Fri, 14 Feb 2025 04:08:59 GMT  
		Size: 12.6 MB (12562535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2bfb8bef0808252365804938750493762e8cc5cb5f7a4d1f20dfb935bf6e44`  
		Last Modified: Fri, 14 Feb 2025 04:08:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcf8874c5b0113d689db8364cef98e1a636a8092b5d36bdbd9a05086aace76d`  
		Last Modified: Fri, 14 Feb 2025 04:08:58 GMT  
		Size: 14.0 MB (13974968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cee044ffdee230cdacfd4be637c5be07463e95d201a70eb78fe519a3a7fb11f`  
		Last Modified: Fri, 14 Feb 2025 04:08:57 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c94cc523262107139f82ced791c106eab65168e798a692a8af377bec898446`  
		Last Modified: Fri, 14 Feb 2025 04:08:57 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6544d4f14343ebf41c6b94f3fd21ba9a5938a1eb8543a9f8860ff3681598d9aa`  
		Last Modified: Fri, 14 Feb 2025 04:08:57 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f64a9dcd0cadb3f143f42676d02ea03add68f00ba1382fc27200b9bff676cc4`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 535.7 KB (535693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1cc8ed47edbbcde6d0c7b08d872d003a2daad1cf61bccf442fcca23de8cb08`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f540d5c7ec7d6a8247d49288d5a53b8b73ab2dafac1025a01fd8bda3c202a`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 489.5 KB (489497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50632da99db9939e74789de5c00acec3cbb661f7d2de49f0da1f14463f28f023`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 4.1 MB (4073355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaf01d860adcc9ea7fcabd40bad87fc321a0db915a9fd388135a8c31c42bbf9`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55a32db071ef0e6af17e252f0e7e0b9c86b1a499f99b3940291371fd96d2785`  
		Last Modified: Fri, 14 Feb 2025 05:43:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:d8362797993457b1f565c96f956ec383f6d41d325d562b7888ecc5a9f10b4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e650aa4519f8c4a1ca7ec933e3a0a9864fa136bd76eb73816925835f0e241757`

```dockerfile
```

-	Layers:
	-	`sha256:d1001e2bfbc00d2349400de64b3d7c7a650069781308bb56f729de9919a1a50e`  
		Last Modified: Fri, 14 Feb 2025 05:43:18 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:3684fd377a669c30fd98e2188fa310083c717e7641d742d0cc0231ca11f642cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41746426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8910f8c3d5187b1f2882a572af3d17ffcfa5504e828a7fdc1e4a711c4b13c09a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.17
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682579faac57494082443d2234da91b74fdd5f92e58049a301fd179a48dc9dc3`  
		Last Modified: Fri, 14 Feb 2025 05:14:18 GMT  
		Size: 12.6 MB (12562577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09186fbbb6cb1c6cb4d556b78caadf527fad4a47f1f8f518ed65b0a90029705`  
		Last Modified: Fri, 14 Feb 2025 04:08:56 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26420fe5192f7328e4a1bc994a684effae0e538fae509445e30db71718cecd`  
		Last Modified: Fri, 14 Feb 2025 05:14:18 GMT  
		Size: 17.3 MB (17267168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71766572486d8f3cecd6eb3ccef24c3f4a4599e6381e2863bea2483371f0fe62`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49210bc8f1a7d5507ac3aef16ca188d3359ac0c7a054243a2e3710e24ad2b192`  
		Last Modified: Fri, 14 Feb 2025 05:14:17 GMT  
		Size: 19.9 KB (19886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475203091eafb533697553387f1c157389ee7ab8cc78382c459ff8c1f893807e`  
		Last Modified: Fri, 14 Feb 2025 05:14:17 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f26c8c307a30af43c1f8924797c75fa4d4f5c187c0eaf7192b5ca1d64e8b0`  
		Last Modified: Fri, 14 Feb 2025 05:43:34 GMT  
		Size: 208.5 KB (208468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddcd9d4f20da38d26175158d45fe0490430eb296041d8ba65ada4d3aec36077`  
		Last Modified: Fri, 14 Feb 2025 05:43:34 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc7aa033714c47f87642542c08687e9904d3d55bbe4f5797a09a27ca4ff8415`  
		Last Modified: Fri, 14 Feb 2025 05:43:34 GMT  
		Size: 547.6 KB (547637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0b83833b48109aa117c53c8d2f3807ed7efe263882f82bc8c138a837f1b16`  
		Last Modified: Fri, 14 Feb 2025 05:43:34 GMT  
		Size: 4.1 MB (4073361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045e26e2a1de96fd33014f96745a0ea59ac4ca60615945c799d5ba1049162f2f`  
		Last Modified: Fri, 14 Feb 2025 05:10:03 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ace77446f72445316dad04347e48be6fed0f636bc8987778fbbf54b2ea3777`  
		Last Modified: Fri, 14 Feb 2025 05:10:09 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:5abe5120d54ed6b7ca9d7feaa8d103f8a8917f5682e8caf1773cda30c05beed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d2feb3eb0cd41607da8bbdc584a0a22003d4fec77f74eed2c3091b037d794`

```dockerfile
```

-	Layers:
	-	`sha256:d6bd2b9d5a535d7b813aa7ee001e9d12017b68059cb14e286ce6629028710fd9`  
		Last Modified: Fri, 14 Feb 2025 05:43:20 GMT  
		Size: 30.6 KB (30550 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:6f58f20a413d86843885cf4ea2045ce082ac1781f784480c5f2eecae95a1c3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37568194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc864dd601a48148439c1dc782417fed3f7069d83df470f9883d43be0d4dbbf`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.16
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e2199922fd8d7b8d2453ad72d0f34a391222745fd39879844966ec900938f5`  
		Last Modified: Fri, 17 Jan 2025 21:24:52 GMT  
		Size: 12.6 MB (12565955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adde8da54c2f0f411f50cf6a809c4a1af1aee5affd7cb940e862bfdca93c3518`  
		Last Modified: Fri, 17 Jan 2025 21:24:47 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7fb1fc245741323ebc4eb147da95dfcd8a2c6e0bb633d0061f597f51444c1`  
		Last Modified: Fri, 17 Jan 2025 21:27:08 GMT  
		Size: 13.2 MB (13152506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34851439a144f35dca37236ffcb0218a7ba02b3fc0d1b49db93660c3043c71b1`  
		Last Modified: Fri, 17 Jan 2025 21:27:05 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cddda9c549e9df5904213a2c37a90c34f6e4295fb9272bc5fcae0ab585797b5`  
		Last Modified: Fri, 17 Jan 2025 21:27:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbf5ae9a1ef4a2a5234e34dc0987fcc6e4c2424e71f5b50c5cb7d4b4725de4b`  
		Last Modified: Fri, 17 Jan 2025 21:27:06 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5ed024e75870c1c1d502ac3489e0223e25514da18a32226bd025709071259e`  
		Last Modified: Fri, 17 Jan 2025 02:33:56 GMT  
		Size: 200.4 KB (200446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6835ab26acecb23b56801474b26a50b5d24c0ba3c6459e2366f28f3e40338`  
		Last Modified: Fri, 17 Jan 2025 02:33:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9740fa0818889e03d200105e04ac082fbfe425238a6ef55a8ec261ca6b7b9096`  
		Last Modified: Fri, 17 Jan 2025 02:33:56 GMT  
		Size: 510.6 KB (510564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38788ee14e73454ff6a3f66bcdbabe143fff4e60c85a5dbb44a460672f3505fe`  
		Last Modified: Fri, 17 Jan 2025 02:33:56 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42f76c6350c6a7ddf701ea69d2c4e57f77016612c35e7f6795ccd91f8e576ac`  
		Last Modified: Fri, 17 Jan 2025 02:33:57 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e8e922632acd73449c1bbf904167acf7125cfced197378fb887d800945afc`  
		Last Modified: Fri, 17 Jan 2025 02:33:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:d6c598c05dd61fcbb6648313b902fda718c5c0934c6fb97653edbb85d4a7d083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6376525414841b775e6c3513abd10ee340e3669c0b3b398a94966dde52b092c9`

```dockerfile
```

-	Layers:
	-	`sha256:6d80b9f34bc20a05a4d2f6edac628adb45bb5dcb3c45b8ac053282c6ce652983`  
		Last Modified: Fri, 14 Feb 2025 05:43:21 GMT  
		Size: 30.5 KB (30500 bytes)  
		MIME: application/vnd.in-toto+json
