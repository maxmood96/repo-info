## `php:fpm-alpine3.24`

```console
$ docker pull php@sha256:972b47917a0e8de6d3c617660f16ab18d2283daeb0c6304e8b4c7f3106207b6d
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

### `php:fpm-alpine3.24` - linux; amd64

```console
$ docker pull php@sha256:87d0c9ef3ce02edaf5516e68fbc2746b400bfd8dfd0b98a8ba1a93f95eaf73d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38614368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8685f6ecfa3dc9692da8c11ce34cdd80847bc511ec52f3ae61cd99b1c857926`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:15:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:15:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:15:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:15:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:15:23 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:15:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:15:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:51 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5990c225d2f532cf9d2364edbfb31ebf2e51024be7489c6f67a9b6ac6c56b86d`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 3.5 MB (3466792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e3b9e1730b86e4b79755171bf4f5312045127202a683a7b5929afc4004996b`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac90667b19605f3d95cedd73a8c1f5affac41fa8a617f4d117ad1f7e5bbf37`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3efc0a61b91c50856db3d44569cb2b76d465c8f4bed6550d677129f55e7ef68`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 14.4 MB (14421108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84e4467e09c46965efa0de3e1be440ac7d905cdff3f9c19e7937d780a638840`  
		Last Modified: Tue, 16 Jun 2026 00:19:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2342275643330d3dce45541d55b160bbaa07dd8890a6d10eb6c4ba90189a7f3e`  
		Last Modified: Tue, 16 Jun 2026 00:19:01 GMT  
		Size: 16.8 MB (16844356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c028e8336453d742b721abe8848af4544619fb6f0a293f7169c9436296f9478`  
		Last Modified: Tue, 16 Jun 2026 00:19:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e322d0fe35cd20e6dc7e34f51543e154c251a93c1868f9bc8e1445266d1c164`  
		Last Modified: Tue, 16 Jun 2026 00:19:01 GMT  
		Size: 22.3 KB (22341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22d8ec232d5625ff16e349be29c9632121a5ffec2c711bbdcadb14e6d79c873`  
		Last Modified: Tue, 16 Jun 2026 00:19:02 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:5bf17423efc12def66b63fdbc8cbc77197407f2a156b90f86e5a2c0a0115e4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c552a1b2d469692fff4a4c408cb6d61f95cde9241dd9f2b2915fa8b066f96315`

```dockerfile
```

-	Layers:
	-	`sha256:d6028b066ed6aa53135b2c64b7669c5773cc7aa972b7508a6c0591d429ba0e72`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 261.6 KB (261616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96811c1de7be86dbd621824a682f1b2a6a26fb1ac2ef4eea35c09b50022e0b0b`  
		Last Modified: Tue, 16 Jun 2026 00:18:59 GMT  
		Size: 49.0 KB (49001 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; arm variant v6

```console
$ docker pull php@sha256:e734a5fa5643ec57592f64aaf834065c2f4abe5af7cc6c5becc71099f6c33132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36163655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff539ce9d77d17e9a332e5d42982e1022504598868bce5f1aa0f1b73ffc6df8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:16:33 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:16:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:16:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:19:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:19:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:19:44 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:19:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:19:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:19:44 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:19:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed2d912231da453d3f787a6b8cb17b78e25561f6e4e297b39b3ecb4d806ceb6`  
		Last Modified: Tue, 16 Jun 2026 00:19:50 GMT  
		Size: 3.4 MB (3416667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f84f93105c3f03f7836c9f6bace4e8324b1efddb660c6a54a410c7ed6fc145`  
		Last Modified: Tue, 16 Jun 2026 00:19:49 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce726178e3fc01e4147d059f5b70b4168de928aedc19a5d66f62ecfbc4116aa7`  
		Last Modified: Tue, 16 Jun 2026 00:19:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e9578908e23ed091dab011406880f30142ff53b21cd1c63556df22e5942f16`  
		Last Modified: Tue, 16 Jun 2026 00:19:50 GMT  
		Size: 14.4 MB (14421102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da18e5ccf9c9a298dedd48bea6295c68cafad7b8735d67bdc9586eae3d631b4`  
		Last Modified: Tue, 16 Jun 2026 00:19:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abffc3b0d46d9f6336d3d0faa0a7f6af31be38a11b7b095aeff68651d3d05955`  
		Last Modified: Tue, 16 Jun 2026 00:19:52 GMT  
		Size: 14.7 MB (14736929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809480cef5def3b4cec72cf7e886cbc69db54efd710d489bddd86f9c8f3fd402`  
		Last Modified: Tue, 16 Jun 2026 00:19:52 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e0031250d030f8e5b03f20f4e7d8a5043fd388f0137f853917b71d481df464`  
		Last Modified: Tue, 16 Jun 2026 00:19:52 GMT  
		Size: 22.1 KB (22126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c147da1fd3539795cead978a1cec2fff3af03e7b40d6f3c3517a3ef7a59dc6`  
		Last Modified: Tue, 16 Jun 2026 00:19:53 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:0f90f1b1baff5bec9cd771f03796a4c9e936c876f165598f4aa8b9e6b3ea7a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 KB (48975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64818a8153eb63a7e7e9c8ecac9d4c90db7eea27d9fd430cadf1eea436a8dd3a`

```dockerfile
```

-	Layers:
	-	`sha256:6d359a063fd5c7beb06381c9c1fca58251ace575eae88ad434af7361c5cbf674`  
		Last Modified: Tue, 16 Jun 2026 00:19:49 GMT  
		Size: 49.0 KB (48975 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; arm variant v7

```console
$ docker pull php@sha256:5d356d38447a6c08c86df390e2b96e4620ac57a6fb696bd584fad3405cd9a4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34877868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e869f3504b540b09cb1ac40d8b710e9ec0dcaf3858a34caa5fb0744b8786e00a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:17:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:17:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:17:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:17:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:17:19 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:17:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:17:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:20:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:20:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:20:27 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:20:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:20:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:20:27 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:20:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37f610a940412a12676ed0e83646330d0ade6205d48c176b96e6d8579c541e`  
		Last Modified: Tue, 16 Jun 2026 00:20:34 GMT  
		Size: 3.2 MB (3233749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e63acecdf1db8b0dc2dd007223259f0fecd3d7c8822350789247b9126d8cc8`  
		Last Modified: Tue, 16 Jun 2026 00:20:34 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf82c9b0b03e2d8b8ff70d142ff5c9a70ec607cbb923241c19f89c06d1c273c`  
		Last Modified: Tue, 16 Jun 2026 00:20:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c08ec7b59a253fcd2cd915bee649825ae42c5c4619cb66e2afee15ba43f1d31`  
		Last Modified: Tue, 16 Jun 2026 00:20:34 GMT  
		Size: 14.4 MB (14421116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4684af451b433e01a629af8fc36b0e1b0640a1b6b3f2056855e7cedae530d725`  
		Last Modified: Tue, 16 Jun 2026 00:20:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e511233abebcfa64589a6a58c8947c2c01c027ad056612f95f61b82183977c01`  
		Last Modified: Tue, 16 Jun 2026 00:20:35 GMT  
		Size: 13.9 MB (13926887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87f5f2e36448c404a8c533143baf76ab03ad79c7b0c1ecac8144ab45ccad067`  
		Last Modified: Tue, 16 Jun 2026 00:20:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2604172a03745e0dd3ef1945606d7165a4f004f1963cbd921d5885e27911c1`  
		Last Modified: Tue, 16 Jun 2026 00:20:36 GMT  
		Size: 22.1 KB (22128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c2bbea797f9fc4b7b8e36db8d1a352e5e848b8203fbb43bb17ba8d534930e`  
		Last Modified: Tue, 16 Jun 2026 00:20:36 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:d7ed2d183628719546be0b5cd777b3a4449f5966c1f7085723f1fbc661d2f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 KB (307235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeadeb8c53389893958048ccf208f2413eab53bf5a4809d370ff01d86618d6c`

```dockerfile
```

-	Layers:
	-	`sha256:86e707eb73237ae6c5beb7b85ba198b8d5757918eb48330b859d7897ba336d1f`  
		Last Modified: Tue, 16 Jun 2026 00:20:34 GMT  
		Size: 258.0 KB (258044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1fb10e480ef3a3dd0ca3cb9f8efb43bfaca1d73e16ca8233af49867f798f6d`  
		Last Modified: Tue, 16 Jun 2026 00:20:33 GMT  
		Size: 49.2 KB (49191 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull php@sha256:3f65354339bb8a8ec95106db2eef87760b00d654ad16b52d8e1bdc92af21f3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38370543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2148ffe1c22b01f71427b653df5c61d21a88f628538441f77039407ff20b08`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:13:57 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 01:08:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:08:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 01:11:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 01:11:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 01:11:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 01:11:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 01:11:25 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 01:11:25 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 01:11:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 01:11:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 01:11:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9581c8e84458f0efaa7a12aa817f6834fd89b206f011623ea5efb87e88659f5f`  
		Last Modified: Tue, 16 Jun 2026 00:17:55 GMT  
		Size: 3.5 MB (3475825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6513cd59f0eb209836cc832bcd8570db9120a455fa54e0a31be8ea8d0ae8d6`  
		Last Modified: Tue, 16 Jun 2026 00:17:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d3b667f434b1d46066b26a701da569751188ea0c0fef36f582c6848fd2515`  
		Last Modified: Tue, 16 Jun 2026 00:17:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b37a8b5df3bfaac19ee934f3dbef561048797647a80b24b303059fcb7ab07b4`  
		Last Modified: Tue, 16 Jun 2026 01:11:33 GMT  
		Size: 14.4 MB (14421109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27eba152bfb805df656f20c7e93b56bacd374d6c195d6bcfc1f4f4c90af97c9`  
		Last Modified: Tue, 16 Jun 2026 01:11:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3555f153512419341eefb837d097dd8d1f29f850b9821e56d4d37a97c4722ec`  
		Last Modified: Tue, 16 Jun 2026 01:11:33 GMT  
		Size: 16.3 MB (16255038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ccc9923bfeb0e3da235773dde1d1941896febc8ca77b8d56f59ec358cb0718`  
		Last Modified: Tue, 16 Jun 2026 01:11:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efd1a67b535878d8b84ab5f65f7cc5cb74cc79a929d2f29bd8d8fd93e22a287`  
		Last Modified: Tue, 16 Jun 2026 01:11:33 GMT  
		Size: 22.2 KB (22156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b69126b36a0465deda3a80b463375810fd3d03d4270f0d3dd46a778b0b460e`  
		Last Modified: Tue, 16 Jun 2026 01:11:33 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:355797776b54bf8c11e483c638839b56b92ff6d076285477aa8c4ad8998f0731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 KB (307323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c7bcb1ee3e688c665bd5d3d912cd0a008ac359c6941c5b5eafb12a57a9748`

```dockerfile
```

-	Layers:
	-	`sha256:3ea35d81384f4f744f0594ae63cb3b787802fab9d5096abfa44ab233c26028d2`  
		Last Modified: Tue, 16 Jun 2026 01:11:32 GMT  
		Size: 258.1 KB (258080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460affc676b826de50edad0e60808d4265788e5209435d97252ed0936ceac9d9`  
		Last Modified: Tue, 16 Jun 2026 01:11:32 GMT  
		Size: 49.2 KB (49243 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; 386

```console
$ docker pull php@sha256:9492c6b79439b690ab3a5c07345c1b145a65202ca32d9ed4ef4d04a4c7b7b87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38816669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed3acef344e3f48fee5863592faf6b7daac0f7fe7e3b6cacb171dfe3551eb77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:14:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:14:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:14:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:14:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:14:27 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:14:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:07 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:07 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28208592c162a9b98cdc81e6b1170ea3bb31271b652af9b475cb68aa68867855`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 3.5 MB (3497281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca3acdc2ece53dbf33c4230e77aebf03c5a0283c63ab3988c9f714fde8f198`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a79a1d834ba949f1cd0f934ed561e3c7d4559f390586dcfb3908c1bad2fe5`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38825cbd5040b55c1a2bd7a9b45b15a989447a19b1d1f80ceac6da52fdc4d1e4`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 14.4 MB (14421093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4045f21a7f850cb0bcb8e8aedcfac6eef7f7eca28e8c73751b3e0fd4f1102eb6`  
		Last Modified: Tue, 16 Jun 2026 00:18:15 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e36fad1a45f9e00e92545956309f8f703c2700797fd625ed1f614ae616823`  
		Last Modified: Tue, 16 Jun 2026 00:18:16 GMT  
		Size: 17.2 MB (17192413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31604e1fd3a7b2b90e812f7524dc51de7f816084dbb719bf976298d89815e680`  
		Last Modified: Tue, 16 Jun 2026 00:18:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d092c7f27633cde370a926911baf681d1d0d53d9230d0656510b2f862a058a`  
		Last Modified: Tue, 16 Jun 2026 00:18:16 GMT  
		Size: 22.4 KB (22360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91d7f2b7abb5548be1bcc93c5c73110ba7b1d278387768c8f7142b57e39b89`  
		Last Modified: Tue, 16 Jun 2026 00:18:17 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:bd2edbf2e2b77bf0d148bdc09d79ee1715b894ff5b28cfe2d3e7811c2ae4dccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 KB (310508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d486e6c69a8625db10088fd655f4313d16ef0be156f84441225de360f3ae4302`

```dockerfile
```

-	Layers:
	-	`sha256:e7653d8d250d6734dbe07837b4c0a15f0bc329fad85771bd2ddd48ac75eec65e`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 261.6 KB (261571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec9e6466bc2642146f22232f6c89cf686836cf31a4e9d8f4604a16fb4023bc4`  
		Last Modified: Tue, 16 Jun 2026 00:18:14 GMT  
		Size: 48.9 KB (48937 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; ppc64le

```console
$ docker pull php@sha256:006d827783f8ddc8f4665c86cd3a7ec3ada7a637c630c4a7a3d65fc9e3790f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38863595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115a49649d5ff22f9606f80d8108e370c2b41c2bd90ba93bcfb78c386673e01d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:17:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:17:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:22:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:22:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:22:52 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:22:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:22:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:22:53 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:22:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b9da4fa7a0b9d4db76eaa5e7475a9b26aebc92ecdbad7795d33e8c5862bfa`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 3.6 MB (3637828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72717bce2b969f044f4c03b530bca77062f0b0d4dfc1eb2f53b9a1459bcf77c`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecffaea7a9240f30a6d71b76e5cba5e41c27f6ab0409cce52536feeb7b55db`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38963ea696c0baa30897d72fa1c115b549abcd0ff8afabb7e64dff601dad030a`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 14.4 MB (14421124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdf993820811354bc778a92c8fe5650e39118fea0109698110c3a5470a1537a`  
		Last Modified: Tue, 16 Jun 2026 00:21:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9713c707c7dcf6f0800126982a3e62ba34dc078fcdec46d68015af375d394749`  
		Last Modified: Tue, 16 Jun 2026 00:23:07 GMT  
		Size: 17.0 MB (16955672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f3e3a0ea8f237bcbe6005f3a5632b67e9308699131d4d16c3d39c05ead409b`  
		Last Modified: Tue, 16 Jun 2026 00:23:07 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab2f169f55d363790e388665b977a573079721a04d9090a2adb82f30b1f1e45`  
		Last Modified: Tue, 16 Jun 2026 00:23:07 GMT  
		Size: 22.2 KB (22189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae95f947b28afef951ac41beedf7a72b77608adecbb955fb7feb0e87e029781`  
		Last Modified: Tue, 16 Jun 2026 00:23:07 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:8140d51a2c93d06a1e0ec7eb6ae17d0ec2b9a3fb71a8c1706ba4797ccc6eff4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 KB (306163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bca0fd886a539d63b26a955e47abbb84f912350ca07af08a624722f5fc6f8d`

```dockerfile
```

-	Layers:
	-	`sha256:7cae412160cbd0439c4b61128afded82ee6a3c43c4e32a9b96622f3da8e3680c`  
		Last Modified: Tue, 16 Jun 2026 00:23:07 GMT  
		Size: 258.0 KB (258033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ad0cb6bf914de5b5b08615d1a020bd1c867c36a10812f2ffe4bd5def0a596a`  
		Last Modified: Tue, 16 Jun 2026 00:23:06 GMT  
		Size: 48.1 KB (48130 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; riscv64

```console
$ docker pull php@sha256:9233e490dbad2b175b91a3481d4c823f3750cb16662580fbf2693c6685f0acfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39416814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f051cddb1154222bae7ff3cd35a69b739f26a43860742eff62d0eab2377cdd9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 04:52:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2026 04:52:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 04:52:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 04:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 11 Jun 2026 04:52:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 06:25:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 06:25:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 06:25:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 06:25:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 06:25:22 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 06:25:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 06:25:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 06:25:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 06:25:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1dc2b0247d9ffb9aa950846edb9cd66b4f53852a8a9879e3b90eab1e6b59a`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 5.8 MB (5791702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6ded20d49de2d129bbc9f97fb6b326363a5b54d9bd6c73e47dee306b314693`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f977f288e84989a2379a82f5f4195784dcdf513d90a9d1c0069a2c531162f0d`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c51303935734568446c07e9e6bb9eea9bf61706e0cde61759feda9703fded49`  
		Last Modified: Thu, 11 Jun 2026 06:26:29 GMT  
		Size: 14.4 MB (14421889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991c412cc8ffd7f1daa3164040df08522cce407cd4f6ca38b90f8487651e0d1`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2446f083136e11060fe87e4921e3523ab8618405949beb9627d35cd940e50d84`  
		Last Modified: Thu, 11 Jun 2026 06:26:29 GMT  
		Size: 15.6 MB (15574954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f41699f8fb2ed07fe31e87905ebce5f27f124c164c2712c350f390ca5acdec`  
		Last Modified: Thu, 11 Jun 2026 06:26:28 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0f3dc417a52f11027744eb5deafb8c6a8d810b486ddf1a17b38a2d210f3977`  
		Last Modified: Thu, 11 Jun 2026 06:26:28 GMT  
		Size: 23.0 KB (23030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf1810240ddfbfe6fd2d73d1c6031f1c9cc40cd77a0b4ce774f43f922dee219`  
		Last Modified: Thu, 11 Jun 2026 06:26:29 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:06d9c007d25080812c556971b22a22ed6a80d9ce76f76948d4aed72961f2958a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 KB (324001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2975d1ea23018167085120983c995937747c9120b96982063ce6928d054687f7`

```dockerfile
```

-	Layers:
	-	`sha256:f24ba2e9cc7d55b447e8ddd9e3565a021bdde7e4cfa2b627e56618bc290515b5`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 274.9 KB (274921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baafb5b86737d6dfeee2443ac9777f69ad1cd22486868cc373c43d94887f6ace`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 49.1 KB (49080 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.24` - linux; s390x

```console
$ docker pull php@sha256:138c20786e85a144829f2ff760bc979c4e73cf8b9f3a19e6682c7eab26b2626f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37910668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf8f8c6280fb8fd4dd39c60f0b31be64ef21cb5e9f3c6e68b1694696eddef1e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:14:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:14:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:14:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:14:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_VERSION=8.5.7
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 16 Jun 2026 00:14:40 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:14:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:20:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:20:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:20:27 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:20:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:20:28 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:20:28 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:20:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722e9c880ce7782bdfb9d99949ffad62bb5ffcc9c3fa11f6a8606ca88b776da9`  
		Last Modified: Tue, 16 Jun 2026 00:20:43 GMT  
		Size: 3.7 MB (3651073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb2138b3292979f0d1e784a2b9852582a1e8965cd081d47d8343705e4c2fd6f`  
		Last Modified: Tue, 16 Jun 2026 00:20:44 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503326c17b9bc4c7d97c1003fb9c754f92e72cd45525b5710e005d5c9359eaa0`  
		Last Modified: Tue, 16 Jun 2026 00:20:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3549188e2087b906ce9e1478bf30e71c3a07ef57fb8ae6431dd40db877e05c27`  
		Last Modified: Tue, 16 Jun 2026 00:20:44 GMT  
		Size: 14.4 MB (14421093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0975420e43a1e5ac383656725767d86586d93fbebcf63d0d872c26061674ecf`  
		Last Modified: Tue, 16 Jun 2026 00:20:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1120adea7df4d6dcf57ab5292776b3b8a4144cfb4d1ff2fb9da15490f7edec`  
		Last Modified: Tue, 16 Jun 2026 00:20:45 GMT  
		Size: 16.1 MB (16093660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879fcaa1f34fb0da8166e61defb89729051e328a4726b5b29f3aae198c7a34f`  
		Last Modified: Tue, 16 Jun 2026 00:20:45 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee7387441e27e04dafcfaa85a3b28c11b40a814fd391961aee21a09a0f561fe`  
		Last Modified: Tue, 16 Jun 2026 00:20:45 GMT  
		Size: 22.1 KB (22136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607dc23dfd260d6f6bbbddbf097ee85066fba3f46cfbef5def1b4bb496375faa`  
		Last Modified: Tue, 16 Jun 2026 00:20:46 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.24` - unknown; unknown

```console
$ docker pull php@sha256:fc77208a743f5aec287c21526ad1b1f8b9848c7ceffbabd899c400c39b174eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af023ccb3773d39cd67874e21298e4a27f69134673babc7c4fd08e039577f61`

```dockerfile
```

-	Layers:
	-	`sha256:30c016a7d85b45f2cc3719bd2f35e34f5a8c2616b0ceee1e888f87529458367f`  
		Last Modified: Tue, 16 Jun 2026 00:20:43 GMT  
		Size: 258.0 KB (257975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc7274bc702d63f21f576d6c78c12bafc314b0cc39eb4ef12e30b330feca566`  
		Last Modified: Tue, 16 Jun 2026 00:20:43 GMT  
		Size: 49.0 KB (49001 bytes)  
		MIME: application/vnd.in-toto+json
