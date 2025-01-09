## `php:8-fpm-alpine3.20`

```console
$ docker pull php@sha256:06eea6f8d11f74a301ecd0d3fadc03ad6c36e875cb99785f68c4add512e7c2da
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

### `php:8-fpm-alpine3.20` - linux; amd64

```console
$ docker pull php@sha256:b806f6c06c195cc32c540abbea8679af3104bafce00f7fcd3f1685d1e710b5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36080995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a0beb139a238ef61eaae488c7c919c0070cb1dac5d957dd8cab440c10b32f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a276f6e0f035d95bc24b644ee212b72c9ecbf2f5ff987da48d1e4c9ebce85d`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 3.3 MB (3308792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e62ed146db2c9fdb7011af8421508bae9ccbf0728a5e5f1d94dfa04860705e`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f452fbeebf435f89b02a40f34e8c2a68baab28e8ed64ece907c633484ecadb9`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99944c98f6196ea54eb65982c9cccbeb67d4510eac54b55ace1b0e57a63484b`  
		Last Modified: Wed, 08 Jan 2025 18:06:27 GMT  
		Size: 13.6 MB (13580219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f934b29408380ca1e416db3b849f02f4739161aade57fab66102af2cb3e4b`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6792111dfc765110937a2a5a468faee9a668931e506fee896b368aaf660aaf95`  
		Last Modified: Wed, 08 Jan 2025 18:06:27 GMT  
		Size: 15.5 MB (15532691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84863370d645a1aa8ca13c085886b209ffb8f07f9c2000403a772faf21fe0af1`  
		Last Modified: Wed, 08 Jan 2025 18:06:27 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed7cbcf45ea05c43af725e9439694723b16c03e441332f923932d5259ab4d6`  
		Last Modified: Wed, 08 Jan 2025 18:06:27 GMT  
		Size: 19.7 KB (19713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba92ddb9691b2fc89b2fa193878cd27a3dcb532876c3c75e7c0dc41b720b30e8`  
		Last Modified: Wed, 08 Jan 2025 18:06:27 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:4e381b26c69f4a00e93a316ab2901a4a44e42e6a4f80c2c20d33c53852aa804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf90d9b0f9f9dc0df0471fceb4ca3d0d7825711b013d450ad7dec97f9574257`

```dockerfile
```

-	Layers:
	-	`sha256:499c81bb41744035888d3d3f1e98bfae6d91fcd11dbc32911dc4279b1415b4a8`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 263.0 KB (262999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb57406df450c7f0998e220efcdbe5340775805797c228b439868999df7f629`  
		Last Modified: Wed, 08 Jan 2025 18:06:26 GMT  
		Size: 47.6 KB (47636 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull php@sha256:329f08982496818f05a3e33139e1e4352025d8972eab9a335dbaa70c04347dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34419803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c310647b2abecd7ed693027b82c9039ef7ee787144addb8834018655b15725`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6e5e4c2e68718d1f73ada486908f719d13b227a11f78fc8876bdae65936e`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 3.3 MB (3277802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da5effe2170797797df1994313aee89dcd1884282164d0f8a7b2b6624090726`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e18edcb50238487ec3d15c28791318639104f7da84baac7d0aee6de4f24e5`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ca57ef1a9c35f92a0e03ee65bde6b009258b73b0b1abf7728ff589207f22b2`  
		Last Modified: Tue, 07 Jan 2025 04:42:09 GMT  
		Size: 13.6 MB (13580074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f346cb3df097f5e674b3426e54c2a4c2c9e5a47b98629cf5831a6664be85393f`  
		Last Modified: Tue, 07 Jan 2025 04:42:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec77867c0a8f36a6623ec59a3d29c3b7436c6e7b8e4a777449a5e47597a2ca8b`  
		Last Modified: Tue, 07 Jan 2025 04:45:59 GMT  
		Size: 14.2 MB (14165432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dcac42e0296dc07b6106d4389d6756a0b1866a0cf21cc780ffd3ece4e1a37d`  
		Last Modified: Tue, 07 Jan 2025 04:45:58 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36242705b5b61d30e3db859f8a8d11b50cb43e700297b5380ecb90634f51179`  
		Last Modified: Tue, 07 Jan 2025 04:45:58 GMT  
		Size: 19.2 KB (19220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae697de33cbe0f9edce13895474adcd0b7e405bd4295778413eb0983e9cf2402`  
		Last Modified: Tue, 07 Jan 2025 04:45:59 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:109f203cd93e27a7db13da8d738eac2825c0c5c88bece1c3cb7b11c8c55b2acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39623ec3c82109338c775d14f1aa0e83b42597437c5b09200c34363d971f3751`

```dockerfile
```

-	Layers:
	-	`sha256:7f040e2e4b539cc87f13532f1f0e626fe6371028553f932023d3a7291b517672`  
		Last Modified: Tue, 07 Jan 2025 04:45:58 GMT  
		Size: 47.6 KB (47575 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull php@sha256:27a85e6e08f945db0ae500936db929e85e4734b45b5e2d81600606fbcfe934ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33147878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2677be6956d78aff6c44f707ff1c77c0c106824d9ae1ca581c2b229de966d9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666fe9f2778fc13085387269ec8e5a9a92fe5a5cd43a1c04d0550044cef029e5`  
		Last Modified: Tue, 07 Jan 2025 04:03:10 GMT  
		Size: 3.1 MB (3086378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33e8f07354fb119b701cf115f1a2dc9d9e81c9a1d4e577cc25369377d26496`  
		Last Modified: Tue, 07 Jan 2025 04:03:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7628e2f49a6657703e1bf3b16f926b733c3fcfdc62265ce69d5a5b75d985504d`  
		Last Modified: Tue, 07 Jan 2025 04:03:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b283b1258b7b2ff179416f77b05865783c1a10b6d8eafadbd25cb25f367744c`  
		Last Modified: Tue, 07 Jan 2025 04:28:27 GMT  
		Size: 13.6 MB (13580072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12036f56693f898ba13296a999176a96f9ec2557715bfb31090f976bf5f8d9a1`  
		Last Modified: Tue, 07 Jan 2025 04:28:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be44ef4eaa252096ca84b32746afbf57fc92c942ae80c62af55064f444b379a4`  
		Last Modified: Tue, 07 Jan 2025 04:32:29 GMT  
		Size: 13.4 MB (13357589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e09f998298ba074d41d5033ee9546d48860f76c9f48097e3bfba43310a2bb5`  
		Last Modified: Tue, 07 Jan 2025 04:32:28 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a67289909699f693ceb809271bca861ba093d27b6cdec21dc04781a54201a26`  
		Last Modified: Tue, 07 Jan 2025 04:32:28 GMT  
		Size: 19.2 KB (19226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b57702f81af777c89fb45fbf3597e65eaa682f9c1c021563c9c2156605fb9b`  
		Last Modified: Tue, 07 Jan 2025 04:32:29 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:853483fa8e321a6009fefca05aed97a1d67766457206adc6b75ac6531946916c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 KB (302086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c2293fbbf3431b5d0da6a6b4627c382fbef1b3bfdc3e3883745c2274e46978`

```dockerfile
```

-	Layers:
	-	`sha256:2adbf1b89cd046fb2f42140330c403d50ee1f79df682ef33500e73c9983e7fd9`  
		Last Modified: Tue, 07 Jan 2025 04:32:28 GMT  
		Size: 254.3 KB (254296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38439b808ad5a5feef8f00b389903cf56e47a1650a0b88d0e1dde4aa64c89c75`  
		Last Modified: Tue, 07 Jan 2025 04:32:28 GMT  
		Size: 47.8 KB (47790 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull php@sha256:584ba6903a508ea9ce330a77707a1687884076c026fda1cfa0e9594c117389fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36266830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da03f1fe38e500dceb64f8efa8ebb48220426bfd2107cccc24b444455833dd77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12651a1164be1c0ff5ff6b5888077c5a5ce96f08fe1a1eea4c3c70cec19c59`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 3.3 MB (3341946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29137c219172cc292e8d59680364cf3eee1a1e71b5507c0237d302305c00ec3`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c134198c2af672fa5dd2e3639c0be7847f521d9b05277485eaa64a00c4c20fb`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de7e03f1dbf94e96481cb45a626a418d9c5d3e7703b67aef0ca26705d46f0`  
		Last Modified: Tue, 07 Jan 2025 05:00:07 GMT  
		Size: 13.6 MB (13580060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2573daf9a0212bbc6984fa2a85897a7c1c015575228e41e283db0fbd4a92f7d0`  
		Last Modified: Tue, 07 Jan 2025 05:00:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d82b1c33bee8adaf3d1e5d416f8c9cf40eca46e40deb9ffa82352c6143b0c1`  
		Last Modified: Tue, 07 Jan 2025 05:03:49 GMT  
		Size: 15.2 MB (15225618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcfa904aa51f747d567dad5d1da45a26dc62dc47c702cf9a8f6c5f84c79da59`  
		Last Modified: Tue, 07 Jan 2025 05:03:48 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e003050eac7bbe0d68c382c4d2d22a3d8a732a69caece7aff8efd221d154aaa0`  
		Last Modified: Tue, 07 Jan 2025 05:03:49 GMT  
		Size: 19.2 KB (19198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059feacb845e77616256aa7ace1cfbe53ae5f2be232dc8fe6119dc6ce17073a4`  
		Last Modified: Tue, 07 Jan 2025 05:03:49 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:ede22daab9d7697026d7f2d92fadc967671fbc9138df051629b7c4cce809c521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 KB (302146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d276a23a55072e5e00f14b6273d22820ce0ced4d5b12238edf2a64c4e42f6812`

```dockerfile
```

-	Layers:
	-	`sha256:4f21754725cfe28ad13a46fe1edd3319d746a1044cc81f0d7536ad6e66558684`  
		Last Modified: Tue, 07 Jan 2025 05:03:48 GMT  
		Size: 254.3 KB (254316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524eab3eed54369fe8d3c30ab7e2a6b86b242d8ee6677f7d12afd4982adfce83`  
		Last Modified: Tue, 07 Jan 2025 05:03:48 GMT  
		Size: 47.8 KB (47830 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; 386

```console
$ docker pull php@sha256:e760aedc6811a08456f58a308254528026958a7b735f7c6b61d94b7451304580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36387613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59148bec9fd6217e8f32e9898b73eaf5c391bb92ec8d92e1b5d0b51bdb995065`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b208fd3aafc3f54387c084a5f1b41950210670eac6dd4e01488adec355887`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 3.4 MB (3359957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922c19db5e609d84fe57f570c32ebba8ce812158cf6b3bbe430e0aa853b33506`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7dc01e9920f7cbc939523531482d8a8a9c52e5de6f9f58adb727ecbbcc564`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a537d5a2bbd41650d1e86605e9ba797860e415df0a91204d40b0759e6d900b90`  
		Last Modified: Wed, 08 Jan 2025 18:06:03 GMT  
		Size: 13.6 MB (13580217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288bcdc7bc3f16bee701d5c644bd1d750d8462849d16808154945a5f5c39536a`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762f85eb53716655f95103f1328e06f679ee0d76155ff600e47ed295eb857f5`  
		Last Modified: Wed, 08 Jan 2025 18:06:04 GMT  
		Size: 15.9 MB (15943442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2574e87aac641980ba10d86b3f56e08a96ac8819d2a3629a6d0b9c004b2a34c5`  
		Last Modified: Wed, 08 Jan 2025 18:06:03 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcc6504128864cbd637f498f6ae0b994bbf3f1db49645273b8c76c67cdcd63c`  
		Last Modified: Wed, 08 Jan 2025 18:06:04 GMT  
		Size: 19.7 KB (19713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94823e93269aaf5d813d961fce7cfed2b9719032cbfc6e8cb6d9389b82ead89`  
		Last Modified: Wed, 08 Jan 2025 18:06:04 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:8d4c4b9dc2dd9269f05cb9e3bf47ed132cacf6f92824ad801df617863b7c00d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2c46afa9340099114d1d92ef78954d50a29483fd88e1f3982f6430a86f0f71`

```dockerfile
```

-	Layers:
	-	`sha256:487d4e653b72c9efa28e46469009b1a88aaacec37b48a214af6ed9a2fc85e3ed`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 263.0 KB (262974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f988b73ba19b66ac483593f3a2934a1b8fac835f09fd6d3dfe991c46b132dae`  
		Last Modified: Wed, 08 Jan 2025 18:06:02 GMT  
		Size: 47.6 KB (47592 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull php@sha256:941fe6688c1b116e8ed9c716c84e3a35d1b4bb93abf51e54a1c2c7df5dd185b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36651437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe0b01aa4c69333e066cfb967dc3c5f60fa0f7f03d5f53de794da2d5278d65`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c1c7ca97bd5883ed3428282fc1d95b690329961e07598c989d7cc3e28ab72`  
		Last Modified: Tue, 07 Jan 2025 04:08:03 GMT  
		Size: 3.4 MB (3419545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9082a14288e52e96ed72a73b7cb744d6f4a60665586a1301c8a7d13caadf8`  
		Last Modified: Tue, 07 Jan 2025 04:08:02 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e6835799395b61d043101026bec9208c8d02d4ab267305b04621b87ef4aff2`  
		Last Modified: Tue, 07 Jan 2025 04:08:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d22b35b604838e23ed08ea7e0260bc716f0a039abeb185ddc5d7e85073fbc3`  
		Last Modified: Tue, 07 Jan 2025 04:29:53 GMT  
		Size: 13.6 MB (13580054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db6e05db39bfad5da4bb51e73320ce99f139d09a7cfd1a3ea29b74ccb1039f4`  
		Last Modified: Tue, 07 Jan 2025 04:29:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4b4e17c3a3f39efb5963474aca7f3d99332d03325084ac1afc4f82de91b8b9`  
		Last Modified: Tue, 07 Jan 2025 04:33:24 GMT  
		Size: 16.1 MB (16050579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3389c62ca5fd11b96f08ad905c6f55c6d68c79ad8650e4f32b5d653fcaa8916`  
		Last Modified: Tue, 07 Jan 2025 04:33:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4367041d5f23f415ba2ece7a94ab4245714f8bfa683207ec02433263cb460bd0`  
		Last Modified: Tue, 07 Jan 2025 04:33:23 GMT  
		Size: 19.2 KB (19204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea44a33a7319c08fad4a2a7b29fad482155c21577ec761fbbc84e5bfbf1a7eba`  
		Last Modified: Tue, 07 Jan 2025 04:33:24 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:d7c6d71ce38e7d626e3a4b40833f282f945c671037843e5c21db347aca289013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 KB (300035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29a1b6772e5d94b6ca6633b3464401839843f97fc80b409320594d30cfbd110`

```dockerfile
```

-	Layers:
	-	`sha256:c95e810b54384deb0fda952565b315f5892df68eb1e6279293d37220184638ef`  
		Last Modified: Tue, 07 Jan 2025 04:33:23 GMT  
		Size: 252.3 KB (252343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df22874d2817674faf087b7f7af9b22a363dfaa3c4ccf44babfe1a31c5123a76`  
		Last Modified: Tue, 07 Jan 2025 04:33:23 GMT  
		Size: 47.7 KB (47692 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull php@sha256:92eb829ab27eae4ba56d456fc6476fb2826a864c06970dfe68cedc44e9bdde9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35385512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd0603f9dd08a69aa44e11cab8bd3e94dbcaf3f17ed11df39a651c6e22cbd4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-riscv64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb004d8f7711d1f01f66ee3b1754326effc166c60f63ee7f0748d2ea817676c4`  
		Last Modified: Tue, 07 Jan 2025 02:33:45 GMT  
		Size: 3.4 MB (3361534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3163fe4049ddb9629b902ed2bd216ace8f06eeba58f3d2458b61c40d1a18e70a`  
		Last Modified: Tue, 07 Jan 2025 11:30:53 GMT  
		Size: 3.4 MB (3412443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db75dce836b2d57bbf95c8369e668b597d3a4b7c2135dcc7c3c9d8b2992d869`  
		Last Modified: Tue, 07 Jan 2025 11:30:53 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a8609d87a1cb88aa761172dfc58283ebb6a2b85a1bd675bbcd713c2ea7a32`  
		Last Modified: Tue, 07 Jan 2025 11:30:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1817f890c58b3bc1721ebbbcce9a39d5a6adbcd50007119b08bbdac5f45ed38`  
		Last Modified: Tue, 07 Jan 2025 17:12:00 GMT  
		Size: 13.6 MB (13580062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3124067eefdc9a32a1eb1b9853d946c4ac7937f7a7bbcb3a87084c246a238f6`  
		Last Modified: Tue, 07 Jan 2025 17:11:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f11579c9d734f50b1b52338403ba3e8fbbbe6cc4490694a78b0d2b3c07db9b`  
		Last Modified: Tue, 07 Jan 2025 18:06:09 GMT  
		Size: 15.0 MB (14998927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deafb3aeb757e2c4de0991ad97d07a2f25a5ebd029149cacbb87ad40fa5e1865`  
		Last Modified: Tue, 07 Jan 2025 18:06:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f051f2a367801bf7f0d908dc6e73530279d71c0da5f1dd639ec10b5278b2d6bf`  
		Last Modified: Tue, 07 Jan 2025 18:06:07 GMT  
		Size: 19.2 KB (19215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9c08654fe39689757ace95934371f3e11972901d6d19bb3a236bc96e0d0c63`  
		Last Modified: Tue, 07 Jan 2025 18:06:08 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:5f5f39059f4d632b4678227b9e458264aa633f4ef0b7bcc47401bd08bf1889e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 KB (300031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d82dd8712521cfc351a9e382dcd4a71303639788b70b94deaa5084fa6cab9`

```dockerfile
```

-	Layers:
	-	`sha256:2c1564cc1147d761bb9773765d5253b9046ca35c0ddb4f883fb3cd1a477e44f8`  
		Last Modified: Tue, 07 Jan 2025 18:06:07 GMT  
		Size: 252.3 KB (252339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e048c8f28dbafe88b3f3ebf20664fc7da7f7977a82d00722a129565dcc20b10b`  
		Last Modified: Tue, 07 Jan 2025 18:06:07 GMT  
		Size: 47.7 KB (47692 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-alpine3.20` - linux; s390x

```console
$ docker pull php@sha256:006a01ed13abac7c6d5e2ccd690c575fd884d908fe14e1eab104fb89ec31afdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36287636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56abc822ec23e2f42cff16eae8b952952109722707687916ce1b8dabc97ee705`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcacb882a5db1e743c34cc92815e2f3aab3e188ee2522e3208a1ed1657316319`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 3.5 MB (3485610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c95db3928cf5b057875d0344bcbb766164738b63d3ec9f076fd1b10abd46e`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17161d12eebb02d227b9e5af0a2feca4cb2817d393db01e188518657f245ce3`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c06b3a2a47bad8633f7b11f1cb73becd849299d752ab1f58140c365f2d19f59`  
		Last Modified: Tue, 07 Jan 2025 04:27:31 GMT  
		Size: 13.6 MB (13580056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767617ae06e30e91a6c1aaaeb100ebb603fe0deb233d4219ce4180f394a82411`  
		Last Modified: Tue, 07 Jan 2025 04:27:31 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6684e509a1c5bb43026a3bc7c9da51f558a9f24b7d80ba62094dea2bd25a12`  
		Last Modified: Tue, 07 Jan 2025 04:33:13 GMT  
		Size: 15.7 MB (15730243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccf4c3c781c03c14875f143ade5491dd64ea083f4d43b03b91ab81288a99d9`  
		Last Modified: Tue, 07 Jan 2025 04:33:13 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9510ea7d9d41d932a1bb7d36bc813d1422724228157f2fa80b360b1b4cb318a7`  
		Last Modified: Tue, 07 Jan 2025 04:33:13 GMT  
		Size: 19.2 KB (19216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3c393ddf656a48788605247308af3496f99020429dd3ff4942ce4312371e13`  
		Last Modified: Tue, 07 Jan 2025 04:33:13 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull php@sha256:6d01e99ab9c508862394ac0313e04cb4515fda361673d0423e86bd7bfb990d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 KB (299945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dabef6a9b65104e0e6b77a5ff9b5f4c889ca660aca76002a6a5b8a78a3ec97`

```dockerfile
```

-	Layers:
	-	`sha256:75d7e7e25a7777e058f2a92a803e6cccdc69c62127bdf49802982178fca725f6`  
		Last Modified: Tue, 07 Jan 2025 04:33:12 GMT  
		Size: 252.3 KB (252309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecada3ee6e13c3f89f515d1664f35b81b8042acbbb717420cc6a8ef26bc09c06`  
		Last Modified: Tue, 07 Jan 2025 04:33:12 GMT  
		Size: 47.6 KB (47636 bytes)  
		MIME: application/vnd.in-toto+json
