## `php:fpm-alpine3.22`

```console
$ docker pull php@sha256:f5fe925e21cd893f0d8b35698620f258d694aabae2bd2b80add16f5375facfc0
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

### `php:fpm-alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:f68484ce47910df79197ffcbbd6210ecf37a3c45f606859faf50783974e02487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38110231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00633196f81cdca76062d1070e7fe78b22846c2cea04a9d6765c897c5081d99`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:21:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:21:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:21:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:21:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:21:31 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:21:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:21:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:24:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:24:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:24:54 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:24:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:24:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:24:54 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:24:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5050f93a50f9c626d242a76d72784cf345f26044388db228358e737bcc8c6f88`  
		Last Modified: Wed, 28 Jan 2026 02:25:02 GMT  
		Size: 3.5 MB (3464773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f2318a9d8596a00b1b6f0fe845d072802fa4ec543401dfe4005ec2274d3ebb`  
		Last Modified: Wed, 28 Jan 2026 02:25:01 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ec4fe35c93964e07d3838bbc1c37b216085b8718508c21d072c23df960789`  
		Last Modified: Wed, 28 Jan 2026 02:25:01 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2514933ca6ed6e935d98eee3d0cd711ce0bfee471aafc603fc705f5445aab3`  
		Last Modified: Wed, 28 Jan 2026 02:25:02 GMT  
		Size: 14.4 MB (14353028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4563ac8bacb976461433ff103a9ed6bb379f3e73112f3de0655e859f9f56ac3`  
		Last Modified: Wed, 28 Jan 2026 02:25:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bce185cdd7f84812f8f0993b2196d68c463f890fad767ef62ea21915a7ddc`  
		Last Modified: Wed, 28 Jan 2026 02:25:03 GMT  
		Size: 16.5 MB (16454108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfbd0b3bfda9828fea612566b7b72c8aa1e4bf58e1fb4f11c2e9e8039c90bd9`  
		Last Modified: Wed, 28 Jan 2026 02:25:03 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caa0fd688971a1160ccffbe8f04d9e8fc2bedddd681e59d85c7a717e4700631`  
		Last Modified: Wed, 28 Jan 2026 02:25:03 GMT  
		Size: 20.1 KB (20069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26be62b9bbbe7e5d3d2701db98b2763bac004282cb334f0afe17c9caf6eb89dd`  
		Last Modified: Wed, 28 Jan 2026 02:25:03 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:081227b969eac1ddd645ae4c0eee6a8441c1efaecbe7a36c81f72bbfee0d1f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 KB (327069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c181f28961fda4b49d427247068fca1aaff825eaf9fd630e94db82633491af3`

```dockerfile
```

-	Layers:
	-	`sha256:9511987236b5c614fe70401145043826339289eaa4e2cb0088108329989fb285`  
		Last Modified: Wed, 28 Jan 2026 02:25:01 GMT  
		Size: 279.3 KB (279291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e727137e70be530641e1aa77942be2b87273297da0369bc4506dc7a9b85078`  
		Last Modified: Wed, 28 Jan 2026 02:25:02 GMT  
		Size: 47.8 KB (47778 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:4f03c37100fcd4fd5e6ca4ef647ae837e1663ef0eb3d81879ee2fc8264764397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35747942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524e8fceaf5ece42c1bb381a668be7283538db1f7e088edfc7e9b94f0c260415`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:29:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:29:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:29:53 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:29:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:29:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:29:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:29:54 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:29:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:29:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:33:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:33:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:33:11 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:33:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:33:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:33:11 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:33:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c0db52ebabcfb437b95f9156dafeafba243675ceb3be2f183c8ec41cdbe0e`  
		Last Modified: Wed, 28 Jan 2026 02:33:16 GMT  
		Size: 3.4 MB (3428953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63c1b532b2c33e04dc174e2adbe26559f81b646310183b0832bc99aaf97703d`  
		Last Modified: Wed, 28 Jan 2026 02:33:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c45472214248ad7bc08dc14082d12e2faaf7966d4e1bc506ea4991b81893a1`  
		Last Modified: Wed, 28 Jan 2026 02:33:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c0755af4f20ae78451f707c9d80dae3fdc8451bbc6f8c4860976980113afef`  
		Last Modified: Wed, 28 Jan 2026 02:33:16 GMT  
		Size: 14.4 MB (14353032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6dd4efb34e3220262789d6522cdec95563310f2d90c18fae45037f4666b0cf`  
		Last Modified: Wed, 28 Jan 2026 02:33:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66ae57913d82fae35d756cbe339045ca6f6f6d6975dd21fd069718c571e0485`  
		Last Modified: Wed, 28 Jan 2026 02:33:18 GMT  
		Size: 14.4 MB (14427666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78d1c20b60d32c1078194d4b274bfa4195e3a8aa0dd63563d8aedeecb9df7c`  
		Last Modified: Wed, 28 Jan 2026 02:33:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77e9a5cd122221e271755ae6f1d37c7288c91041c8d415052c399174b0b5968`  
		Last Modified: Wed, 28 Jan 2026 02:33:18 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba933c89584d43c1871ff149d426b3b435f55b085cf31725419ff25a05ea718`  
		Last Modified: Wed, 28 Jan 2026 02:33:18 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:cb44b889a35a91347ffe7af5a29a52650b1331d74825b2ffed528255108314e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b83985257713c23d312c569e05adfc6b8a68ca49f06eed00c3b1655c8592d25`

```dockerfile
```

-	Layers:
	-	`sha256:edffb013a7a204455983b71dfd86e105ae4f83522381562e06bb1c41fd00f19a`  
		Last Modified: Wed, 28 Jan 2026 02:33:16 GMT  
		Size: 47.7 KB (47721 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:8b9cc737e7b12a1b90ebf974928f0fddd09199183196050ec4ad2b396e804f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34495703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c660e3dc22644bd871b465b1880a83a3b95a958fe219f8d3cf62df53c4289`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:25:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:25:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:25:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:25:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:25:58 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:26:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:29:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:29:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:29:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:29:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:29:15 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:29:15 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:29:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:29:15 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:29:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ae90fb78fed230912b7cdffcd14c752af01fd4c9a06338bfe0c5e268cc75d5`  
		Last Modified: Wed, 28 Jan 2026 02:29:22 GMT  
		Size: 3.2 MB (3244518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba0a53754cde7fea33437453291d9b2b0af0b6763f125852808d7dcb933196c`  
		Last Modified: Wed, 28 Jan 2026 02:29:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363023f10f3325353079ce3f4542137049066074ebb7249c9ee4d2c0d3de4d71`  
		Last Modified: Wed, 28 Jan 2026 02:29:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d78c20ec3c10f0e2493b3f22c966765171efe3a9e9b37c24b1dc4d57a29903d`  
		Last Modified: Wed, 28 Jan 2026 02:29:23 GMT  
		Size: 14.4 MB (14353030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75962d5cfd7a9ac802af822fd1ca963bbe067bd6fe49e3533030b13597dd7436`  
		Last Modified: Wed, 28 Jan 2026 02:29:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ea1f281b8e8906708332a9b5696591f6f36fb05ab1022b336b20693bc53668`  
		Last Modified: Wed, 28 Jan 2026 02:29:24 GMT  
		Size: 13.6 MB (13641287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad1cc0e2e5c8ab49b0364aa61551e376a7676b1363f3522c2d9dd103b3c48bf`  
		Last Modified: Wed, 28 Jan 2026 02:29:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1cc665ca1f7e9c091007927414075df6e58e90ace6a35dd7e70a80a59ff06d`  
		Last Modified: Wed, 28 Jan 2026 02:29:24 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea761c662eca71ae1ba21246851927ceffdcabebc534f691855bebe5b4f5403`  
		Last Modified: Wed, 28 Jan 2026 02:29:24 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:0ce7ca7a16554089616c0451ee41c2dee95e6d91c0b061c85933f801c96a61ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 KB (324273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb2fa7922b55267ef09967d842978292de77b2496acd5692ed8065def4c2389`

```dockerfile
```

-	Layers:
	-	`sha256:f9f50c9a33c6fcb55715db10a996a314989c1f81f0dec03bb83f87aa15724176`  
		Last Modified: Wed, 28 Jan 2026 02:29:22 GMT  
		Size: 276.3 KB (276337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52d157e415854b0ba779148d7a229c7286165d6ccf3d56e052e0456eccfd3f3`  
		Last Modified: Wed, 28 Jan 2026 02:29:22 GMT  
		Size: 47.9 KB (47936 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:a8db288363b90dc4b7ae2b8cdfaf267cca9f3c1c78b117a08de40c8ad16784e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37991053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df38e2063fa7037de39e99fc4520b16aab5406b540b7ee96ddf286d306ef045`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:20:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:20:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:20:58 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:24:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:24:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:24:46 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:24:46 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:24:46 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:24:46 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:24:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722e0cc6b8c1ca4b255dae0c19c474c1d6d5d42f2537be9a2dc18d084a30e097`  
		Last Modified: Wed, 28 Jan 2026 02:24:53 GMT  
		Size: 3.5 MB (3467264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f372eb223cbe5e1d66330160fbab4a2c4d3c56a7c64021b31d2370fd93014a4`  
		Last Modified: Wed, 28 Jan 2026 02:24:53 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935aa8ca21cdc3fe423d1b237b92819b64c8239afb065df9a21b0c844f9da284`  
		Last Modified: Wed, 28 Jan 2026 02:24:53 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbe56f273dd09f8ffcd8bea7593dff06e91b9c1498112affa04fded3b61ca47`  
		Last Modified: Wed, 28 Jan 2026 02:24:54 GMT  
		Size: 14.4 MB (14353015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635fb9d146da3819dfafef177bbebe01acecd22916fc28023331632adc269641`  
		Last Modified: Wed, 28 Jan 2026 02:24:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1cc6d0b61e774113791bdf24105f70e5e40fdd5c63d164718b96de1af5a51`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 16.0 MB (15998014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9f56c8e8bdecf296f9b8d5174a0cb8abe23b4648954438e1e2a4204a1dc1cf`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cee6087e096f2bfe2821168c67ace0b3f69a6c4aaed249f839c9a0ddd4c106`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e24ec020566af4e7d6916cd86aa273300dc5a71ebf18f8b772083a97192f76`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:cd65eb7ce038298ee7a9a5e9efc75c9e090ad0051129233eb8864e66b19ceb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 KB (324329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4adc32a085c0d2b1f5d2f402a04d7bfda0ee40c0ecb6570a44028836beb1b`

```dockerfile
```

-	Layers:
	-	`sha256:26d25c1b1f9f07017cc8c201cbe499d4980ca255cd79e2a630727716a8615b15`  
		Last Modified: Wed, 28 Jan 2026 02:24:53 GMT  
		Size: 276.4 KB (276357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4ca53df5b8515a659a1bb5638ef54f54ed2493a095b76b29a16bcf1a38a8d`  
		Last Modified: Wed, 28 Jan 2026 02:24:53 GMT  
		Size: 48.0 KB (47972 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:ba2106a7d5292e6e8f0654de59832fe03651a5da405dfa00993f920c236abbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38429471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09e2fc7a5d13714db4b8221f9b37edefc025371e4deb3e7b0e2c8f244036f1e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:17:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:17:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:17:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:17:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:17:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:17:57 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:18:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:21:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:21:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:21:06 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:21:06 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:21:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:21:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:21:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300eaf5fbe9735c552e7a97c052cb092a075b51fca21d7c56b29b5a246c4ed1`  
		Last Modified: Wed, 28 Jan 2026 02:21:13 GMT  
		Size: 3.5 MB (3523580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffdff8209e17f94ef6ca3d4c9500d002c47d9bd6e804209278d0b05dba953e`  
		Last Modified: Wed, 28 Jan 2026 02:21:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f3ffcdbc2aacc68c551a4401184267aa78c5a0daf8676cdb8aa0edc9d530f`  
		Last Modified: Wed, 28 Jan 2026 02:21:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035a512dc1797aff73a48ff049bd9ce25ac1871e9b9125296ec32cfbca3cc37`  
		Last Modified: Wed, 28 Jan 2026 02:21:14 GMT  
		Size: 14.4 MB (14352954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765c9d5e882379bcd099dce9a13b3db1f59daf0820285069ae592d7e29a9ff71`  
		Last Modified: Wed, 28 Jan 2026 02:21:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc13504cea0831cfbf561a35a5ba7fd703554f1aeadaa96052bc0b192fd2d09`  
		Last Modified: Wed, 28 Jan 2026 02:21:15 GMT  
		Size: 16.9 MB (16898778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88233b3755fc796e3d44e2b346987c3366ec1b1868b00cdf5a50b6319602d19`  
		Last Modified: Wed, 28 Jan 2026 02:21:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad7111fc5ee289c1afd79faf2542552d0b386a865d35db39fe5cb84abcc7f`  
		Last Modified: Wed, 28 Jan 2026 02:21:15 GMT  
		Size: 20.0 KB (20042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143a07fcbb25fd6e42d948b495a2192c102488d91aaa673d4c81aa7b7767933`  
		Last Modified: Wed, 28 Jan 2026 02:21:16 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:b916d7b34eb75e0efbbb95387e583a5d5653a5c40f6e1e1f7dd42bc5d886aeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 KB (327000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a24e2fb564325cafc703dc6ba2ffa22e41054da3fcba7b67c8366cc012fea68`

```dockerfile
```

-	Layers:
	-	`sha256:b257abb38aa880ceb70bc319f6eeaa48af9decfbcb5668ca9847332a93f96f5b`  
		Last Modified: Wed, 28 Jan 2026 02:21:13 GMT  
		Size: 279.3 KB (279266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc89bce578aaeab82e9cca3b4f40d5023e6d8407f9d6f0b55d3a0fef92f6b154`  
		Last Modified: Wed, 28 Jan 2026 02:21:13 GMT  
		Size: 47.7 KB (47734 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:3a278f9387693bd4fb6b29cc48a8a19992039ebbd9c63019105d13872d508a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38251606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fd0cdd760f6fe84a671c4125322ed88d62a35e03b708f0e29c23583958f4ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:44:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:44:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:44:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:44:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:44:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:44:50 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:44:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:44:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:53:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:53:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:53:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:53:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:53:03 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:53:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:53:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:53:04 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:53:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea6e4649541347528986aab541f88342858858b6aa327d35179393fabb01485`  
		Last Modified: Wed, 28 Jan 2026 02:49:18 GMT  
		Size: 3.6 MB (3615312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9adce4985f2f10739654ad6d9d7b01ab001ce943991d309b785ffe0bb05c7ac`  
		Last Modified: Wed, 28 Jan 2026 02:49:18 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f956b83e26834c13344894cb32b9114fdc8bccc12ae27687e4555e621e947727`  
		Last Modified: Wed, 28 Jan 2026 02:49:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9bde96e866d9de46c0642dfa07aa3bbbb28d89e7b5fad235ab75af90f8a3cd`  
		Last Modified: Wed, 28 Jan 2026 02:49:18 GMT  
		Size: 14.4 MB (14353038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb1036a6bf20fc3ad12b4769f5129084387f4b087dba15609fbbce2a1e1d16f`  
		Last Modified: Wed, 28 Jan 2026 02:49:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296d9352c82403b69f513770e41d35f5ceb59379647508bcaa5d15166e60572f`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 16.5 MB (16515695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9934b50d94d3ec4b811b608144aef5ad8481f27d299fdb378f69407ed452dda`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0230921a9fab8d44c6f8ae26d1194c2a566036d705e95d8c143aa705d0de6098`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e5ee2bf655b1f06b8abcb9baccdee38c128503ef0c919d69263aed9fd29bad`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:1f830db3c4d201f4e31f9e1c00489e92e795065885f8f919c5c9b8e4afc8933a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 KB (322218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1801df5e1e1b5d067354a36a2640faded94cd84e58413086b4384d195fd02f49`

```dockerfile
```

-	Layers:
	-	`sha256:918f8df4de48bee64ade36015eae9c7e459e830bcc497f4eb8a48205e2825f91`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 274.4 KB (274384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64985d1443aee59b50d5aa68a77448b92c10374fe8c4eff6fcb2c8600ecceda`  
		Last Modified: Wed, 28 Jan 2026 02:53:24 GMT  
		Size: 47.8 KB (47834 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:52bd58f03e2496df735bb21909d9208a865b027e940c0ed8f5300ff8d3ce091b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36981967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d26ef959366454199b6754bb02334e3c78aef741569549068fcffdf7f1e4c9f`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.5.2
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Sat, 17 Jan 2026 21:45:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 17 Jan 2026 21:45:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 23:47:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 23:47:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 23:47:13 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 23:47:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 Jan 2026 23:47:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 Jan 2026 23:47:14 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 Jan 2026 23:47:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b3d0a6fe3ceca0faed35542ba991569716c5a80793014ce7d9059463ed06ba`  
		Last Modified: Sat, 17 Jan 2026 22:46:48 GMT  
		Size: 14.4 MB (14353017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1290816e69231a185a65b9b92e23e2f3af788d8ce9b593e0e7a93a8b59c5d1bf`  
		Last Modified: Sat, 17 Jan 2026 22:46:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8060f6301767a24dbb47cae4a1d4f6fb1ccbb3ca00492a31db989d1adf5ed31f`  
		Last Modified: Sat, 17 Jan 2026 23:48:11 GMT  
		Size: 15.5 MB (15480182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e868b993a05b7267b54087bb6e4f77f0d7f4c458faf8ffcf97e7d32b546762b`  
		Last Modified: Sat, 17 Jan 2026 23:48:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90aeaddb197ceda7b4726aa7c232056559fc977ce5350ce2a52b2ee1cebb5699`  
		Last Modified: Sat, 17 Jan 2026 23:48:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70477cfb6376ecdaea0c45108f3eded38b2d72f6539ae723097f6cd790cbc6e0`  
		Last Modified: Sat, 17 Jan 2026 23:48:09 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:78d4d6b6a36c28529e693ebad7fb6b4dc83591f88a9fbca957882bc1212a4b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 KB (322214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7236655b260608785e8f030ea47fcbcd6b6504162d558ff6607e1afc67d07346`

```dockerfile
```

-	Layers:
	-	`sha256:99d4e82fb6f346aae3e31b6ee5fbaa1d24f9a3f131eae89cec72b1018f5f73f8`  
		Last Modified: Sat, 17 Jan 2026 23:48:09 GMT  
		Size: 274.4 KB (274380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9786c69437037e6a77f13dd512a02e57c9ab29bf2dbd6db1de70f7e9f331710`  
		Last Modified: Sat, 17 Jan 2026 23:48:09 GMT  
		Size: 47.8 KB (47834 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:a24937f4a6d33f0a83da79b37d31695014abe9d38cf0fb9423eefb89483c9039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37591772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1154b574ebac48869811e99258bde5b2c38934136ad1af2202e130943c44a16`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:28:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:28:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:28:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:28:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_VERSION=8.5.2
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.2.tar.xz.asc
# Wed, 28 Jan 2026 02:28:11 GMT
ENV PHP_SHA256=cb75a9b00a2806f7390dd64858ef42a47b443b3475769c8af6af33a18b1381f1
# Wed, 28 Jan 2026 02:28:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:28:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:32:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 02:32:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:32:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 02:32:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 02:32:44 GMT
WORKDIR /var/www/html
# Wed, 28 Jan 2026 02:32:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 28 Jan 2026 02:32:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 28 Jan 2026 02:32:44 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 28 Jan 2026 02:32:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d024b80d0e9878804800228ebce9d42dc9ee9a81dbe8974af5688588ace05`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 3.7 MB (3693198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7f0b58cca09ec22f7800620f70ecd9dee1d6d8ec1f9b12ab18e456859fd1ef`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90b8c978e1c7310f30f5ec39cb20c5aa76e560c802278a13a0c82ec02a6fa27`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2afd1b62b313205c58643d24430ad79510462a2e18c9b193b88ddd469c1b29`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 14.4 MB (14353036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3850a43df42ad6463ab6b2a3592c057e2089c1d55f38834fd8785f78800a1de`  
		Last Modified: Wed, 28 Jan 2026 02:32:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6963a5ff45ef899db244f6b7e6bf44bc4e61ef82ed43f770286af9ac75f30bf9`  
		Last Modified: Wed, 28 Jan 2026 02:32:57 GMT  
		Size: 15.9 MB (15861868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d39bca5de0f17e14c5fd24dbaddee4c81fa4e31dccf19fb7a0fc246675a802`  
		Last Modified: Wed, 28 Jan 2026 02:32:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5663743f51e8bf489ce94c348511ca16768e9c7cab14a0b2b94646a472fa4720`  
		Last Modified: Wed, 28 Jan 2026 02:32:58 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a59da8a69cd4b516398e3094e4a03d9f8e4b7c2bbfdd7031731a991bd3e7a96`  
		Last Modified: Wed, 28 Jan 2026 02:32:58 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:ec5bf15502d21b6f2e4f7fcbb179b0460ed58ae8bbf4b15b6de8e827533c0103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 KB (322128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd5fa6193b3aab3ea6f3768c7f5441a13b0c8ac9d5d20403cfd08e6c446070`

```dockerfile
```

-	Layers:
	-	`sha256:4938df2657ac506d0392ca9b832beb74ee7762a2d3a8eae4d13aebf5036a3cfb`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 274.4 KB (274350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd46d050b59365f03168a0d4409f5674d0041987b22a8621ad5ede54d69e7362`  
		Last Modified: Wed, 28 Jan 2026 02:32:56 GMT  
		Size: 47.8 KB (47778 bytes)  
		MIME: application/vnd.in-toto+json
