## `yourls:fpm-alpine`

```console
$ docker pull yourls@sha256:f0d0035ce18292b3046d6e6322f871ceb6aea791e04c8d0b4fab73350308242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `yourls:fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:7d8b04a3bf6a05421428ea06350baaca0e40a13a926d356ffe723d7909a4effb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35911909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a35323682cf80afb6a685813dea9ab7cd9467d77fe96829fe329fd40ae28cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:11:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 20:11:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 20:11:53 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 20:11:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 20:11:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 20:11:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 20:11:54 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 20:12:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 20:12:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 20:19:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 20:19:11 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 20:19:12 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 20:19:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 20:19:12 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 20:19:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 20:19:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 20:19:13 GMT
EXPOSE 9000
# Thu, 11 May 2023 20:19:13 GMT
CMD ["php-fpm"]
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 11 May 2023 21:25:39 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 11 May 2023 21:25:40 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 11 May 2023 21:25:40 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Thu, 11 May 2023 21:26:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 11 May 2023 21:26:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 11 May 2023 21:26:26 GMT
RUN apk add --no-cache bash
# Thu, 11 May 2023 21:26:26 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 21:26:26 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 21:26:26 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 11 May 2023 21:26:26 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 21:26:26 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 21:26:28 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 11 May 2023 21:26:28 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 11 May 2023 21:26:28 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 11 May 2023 21:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 21:26:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482c13708aabf63e831cec9a7a7c482e06954909130a8378bc2ea0555b092729`  
		Last Modified: Thu, 11 May 2023 21:01:47 GMT  
		Size: 2.6 MB (2646551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4231935b557bcd8db7765211fa8740725f28e3126a7afa24ee1203806f31d6d9`  
		Last Modified: Thu, 11 May 2023 21:01:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889ac5addf84973ce7a59ca03e0e8eee13d74b802798524b45eee73915efb46`  
		Last Modified: Thu, 11 May 2023 21:01:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25d4ad06cd8c3f1c5a18d63095de1f776752109274b2e26a78e01dc14e25aa0`  
		Last Modified: Thu, 11 May 2023 21:01:45 GMT  
		Size: 12.0 MB (12035901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca73195221b888e4e8df9ea81a1041c1285f094a4acb8f7377040235fc8624`  
		Last Modified: Thu, 11 May 2023 21:01:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e628002557a8f9a8dea3d3c22f6f3c707ae5f7cf8d45df3fdf97069eb9d3750`  
		Last Modified: Thu, 11 May 2023 21:02:27 GMT  
		Size: 12.7 MB (12690874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8fc8b0fe10d2d8ecb0cf1c9d39fd2ab214717a568c2b7a97c849c1545bfb1a`  
		Last Modified: Thu, 11 May 2023 21:02:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e9a4038156610fa168a6f0bbca008dc7aad0a77f73adcf234c41ed5527b753`  
		Last Modified: Thu, 11 May 2023 21:02:25 GMT  
		Size: 18.9 KB (18888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfca8a49f8fddd40b65927c533b47becf5b86b2fde0b0c50a2281465cde8bcf`  
		Last Modified: Thu, 11 May 2023 21:02:25 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687133cd9c824d2dff466e681f56730e3ae79ae70b67f4a861744694353d5f6c`  
		Last Modified: Thu, 11 May 2023 21:27:30 GMT  
		Size: 541.1 KB (541115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148150219ffc3fc6d842e0200798df7fcf35e77dd7d5955f993ef9eeec80182b`  
		Last Modified: Thu, 11 May 2023 21:27:28 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6d30ce952546cbd1ac9985670b1b733cd3882859b1563416cfe633e86eb55a`  
		Last Modified: Thu, 11 May 2023 21:27:28 GMT  
		Size: 490.1 KB (490055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5023f97aa63c0c3fa87f6379bd89d43a80d8fce0f329540aa973865e3b683c6b`  
		Last Modified: Thu, 11 May 2023 21:27:29 GMT  
		Size: 4.1 MB (4073469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e2511c45ced20e64be58783259bd6b21e1734deea07145854848b98493a1f6`  
		Last Modified: Thu, 11 May 2023 21:27:28 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24175277f5329a7400d740b29069d98af7ade1cff143bd1348c165124974e59`  
		Last Modified: Thu, 11 May 2023 21:27:28 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:8806146c759674b8973d480c2fe38f51a071e4aea6bcedf45b9281990b685976
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34259738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c638dac3ec432ad37eba3652ab5ae61af0dda50210dcf1ea5a4a8653630c197d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:58:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 19:58:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 19:58:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 19:58:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 19:58:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 19:58:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 19:58:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 19:58:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 19:58:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 19:58:37 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 19:58:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 19:58:37 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 19:58:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 19:58:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 20:05:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 20:05:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 20:05:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 20:05:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 20:05:57 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 20:05:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 20:05:57 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 20:05:57 GMT
EXPOSE 9000
# Thu, 11 May 2023 20:05:58 GMT
CMD ["php-fpm"]
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 11 May 2023 21:11:39 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 11 May 2023 21:11:39 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Thu, 11 May 2023 21:11:59 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 11 May 2023 21:11:59 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 11 May 2023 21:12:01 GMT
RUN apk add --no-cache bash
# Thu, 11 May 2023 21:12:01 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 21:12:01 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 21:12:01 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 11 May 2023 21:12:01 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 21:12:01 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 21:12:04 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 11 May 2023 21:12:04 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 11 May 2023 21:12:04 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 11 May 2023 21:12:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 21:12:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e20819b1d0cece68aa8af3f83552465afc12b03814a9b22a9432540697046c`  
		Last Modified: Thu, 11 May 2023 20:34:25 GMT  
		Size: 2.6 MB (2648438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b6751aa5f52fd6dc7693dd8054d32b4b2b13f34f8279ae1dccc42be19fd39c`  
		Last Modified: Thu, 11 May 2023 20:34:25 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08e83bce071be5127a0c0b997f13aaa3d7c8ce2489c41b326fe8e1f859873ac`  
		Last Modified: Thu, 11 May 2023 20:34:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b83899e04563181159d91efd8c11c990e34c7fe55fd5c45413e69df4746b67`  
		Last Modified: Thu, 11 May 2023 20:34:24 GMT  
		Size: 12.0 MB (12035879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d467d08dc3ea4aa15f5226b4a725c40ad127ac67080038d570159392ca62df`  
		Last Modified: Thu, 11 May 2023 20:34:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded3c0121a506a45e941fe20adb40542e995e66f322bda146cabe456f077e9c8`  
		Last Modified: Thu, 11 May 2023 20:35:06 GMT  
		Size: 11.6 MB (11605763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56023012e51db1c2639a3d3305269b1871058277046b0658699d77f22eee1d81`  
		Last Modified: Thu, 11 May 2023 20:35:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9ffd3e9e861aa48fc2778bce8fde3d4791fb5bd0ef0b6cc34286f076a7d86`  
		Last Modified: Thu, 11 May 2023 20:35:04 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3090608c3fd9a2795a15d8559bb6597cf538f358e2bdd6a55aa719863ff0a68`  
		Last Modified: Thu, 11 May 2023 20:35:04 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15726ad281e75e3974e3f4c4ab63cf7e70eea9521d782c5e827a00a8bb75c942`  
		Last Modified: Thu, 11 May 2023 21:12:13 GMT  
		Size: 170.2 KB (170204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e87fab404c1b8afa4f3ed2093709f0ba87edae2ef5e41850962e9d79063165`  
		Last Modified: Thu, 11 May 2023 21:12:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daa2c6ae0f46224394ee4c05de5f847e27058dd516623e20022331d604212c0`  
		Last Modified: Thu, 11 May 2023 21:12:12 GMT  
		Size: 534.1 KB (534074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d068aee98c14f58f54976d3c960351b77096e0e87aa044b07f00fa982798c6`  
		Last Modified: Thu, 11 May 2023 21:12:12 GMT  
		Size: 4.1 MB (4073467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e242265f80198b2145aee73599b06fe1e2404b83b72bca79c3ff38045d2355`  
		Last Modified: Thu, 11 May 2023 21:12:11 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591e624a4ed2a32f137d0b7d38dcfdd3de345fae1ebf5f1496905a1119e2712`  
		Last Modified: Thu, 11 May 2023 21:12:11 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:1da4d8d679039f1e7c302eef566381ce726cadfffb059976e7b8189b4037e877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32996902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f878adc7d285ec01d6f4f190563e46405395701151fb82788587a39060a8bbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:56:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 20:56:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 20:56:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 20:56:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 20:56:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 20:56:52 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 20:56:52 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 20:56:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 20:57:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 21:02:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 21:02:36 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 21:02:37 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 21:02:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 21:02:37 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 21:02:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 21:02:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 21:02:38 GMT
EXPOSE 9000
# Thu, 11 May 2023 21:02:38 GMT
CMD ["php-fpm"]
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 12 May 2023 00:05:27 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 12 May 2023 00:05:27 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 12 May 2023 00:05:46 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 12 May 2023 00:05:46 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 12 May 2023 00:05:48 GMT
RUN apk add --no-cache bash
# Fri, 12 May 2023 00:05:48 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 12 May 2023 00:05:48 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 12 May 2023 00:05:48 GMT
LABEL org.opencontainers.image.version=1.9.2
# Fri, 12 May 2023 00:05:48 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 12 May 2023 00:05:48 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 12 May 2023 00:05:50 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 12 May 2023 00:05:50 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 12 May 2023 00:05:50 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 12 May 2023 00:05:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 May 2023 00:05:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f49e4305a7c675983bc091c81a380a03985c5b735d445214ed99b6dd981040`  
		Last Modified: Thu, 11 May 2023 21:39:35 GMT  
		Size: 2.5 MB (2492006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c87bf657029d5aefcd9b77b6d7791fce55302cdb6e3f5198ba3907855a440ce`  
		Last Modified: Thu, 11 May 2023 21:39:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65fadb61c8fb4cbd3e372a3dc64bcc4857821f5ba868f79e8ca211e2c8fbe53`  
		Last Modified: Thu, 11 May 2023 21:39:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793e0bdb6949c5cf1e37c1b687aba46bb2b0c9fb78335e6a90a885094899be73`  
		Last Modified: Thu, 11 May 2023 21:39:34 GMT  
		Size: 12.0 MB (12035890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46ad384c9ba4384d86580d319e7b4984d06f0376433e91212f5a908e0528572`  
		Last Modified: Thu, 11 May 2023 21:39:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595e7b1ad577cc1123310f69c7213964f922ed2c2970817ce0f8de31351621b2`  
		Last Modified: Thu, 11 May 2023 21:40:21 GMT  
		Size: 10.8 MB (10844974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5258fedaaba5c4c472beb9fd9fe37e34c7b657a00004d2407882f1955143fd`  
		Last Modified: Thu, 11 May 2023 21:40:18 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f747c4fc9aec70f36a162e9a1ca87be074bbc10639d67a39c533eee37db6c8e`  
		Last Modified: Thu, 11 May 2023 21:40:18 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185721503a82e79307b253974e65f8df29aa5bf87566e5096f9c67e9e2802350`  
		Last Modified: Thu, 11 May 2023 21:40:19 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9422cfc012c2f3c48acd8616d825b7d302ea5574f2fb43b7124d81a65147f9`  
		Last Modified: Fri, 12 May 2023 00:06:48 GMT  
		Size: 158.7 KB (158715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc1222a6c64bdda399e660d3866bbed38d653636088492ba86ecb6ac623115f`  
		Last Modified: Fri, 12 May 2023 00:06:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa74c61bb04df5ca5300e18f99ce946c56f0ecf6c795cd900154b8348ae590ad`  
		Last Modified: Fri, 12 May 2023 00:06:46 GMT  
		Size: 444.5 KB (444483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b775e8527a3787c56db29f2fda8d2de652b2c72e7e8de4026a3bc9031a0e286`  
		Last Modified: Fri, 12 May 2023 00:06:47 GMT  
		Size: 4.1 MB (4073468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1049bf6eccf6cfecc5c1245498ec9dba5a98aea19427129c6e2ffd1421364b`  
		Last Modified: Fri, 12 May 2023 00:06:46 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e5005f66cf83f7b29838e48c37700edb9028b99ac644fb4364d7fd0d73c4bb`  
		Last Modified: Fri, 12 May 2023 00:06:46 GMT  
		Size: 1.6 KB (1553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:699a5e6ee77f3f840c4eb608103cec7d189a54f3a45c454269bd853c69611953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36298074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37121602b89ecea292ebb148d2241e2f8e212d214c5f92a36a15131408d9a3ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:25:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 20:25:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 20:25:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 20:25:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 20:25:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 20:25:57 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 20:25:57 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 20:26:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 20:26:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 20:33:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 20:33:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 20:33:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 20:33:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 20:33:18 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 20:33:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 20:33:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 20:33:19 GMT
EXPOSE 9000
# Thu, 11 May 2023 20:33:19 GMT
CMD ["php-fpm"]
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 11 May 2023 22:04:06 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 11 May 2023 22:04:06 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Thu, 11 May 2023 22:05:14 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 11 May 2023 22:05:15 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 11 May 2023 22:05:16 GMT
RUN apk add --no-cache bash
# Thu, 11 May 2023 22:05:16 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 22:05:16 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 22:05:16 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 11 May 2023 22:05:16 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 22:05:16 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 22:05:18 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 11 May 2023 22:05:18 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 11 May 2023 22:05:18 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 11 May 2023 22:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 22:05:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214874b3c3bf1db5999ce9284cf3c82ab6a5044d860b3803c16cdfb064835b46`  
		Last Modified: Thu, 11 May 2023 21:16:13 GMT  
		Size: 2.7 MB (2682835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c76bae672668a7fb47a803618be8da7f052c69db16eb096ad628b453ceb307e`  
		Last Modified: Thu, 11 May 2023 21:16:13 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fb2ed5003bc498c9f970d971ef8796d2b73c13dbb8533083bcfb6b3aeb6ea8`  
		Last Modified: Thu, 11 May 2023 21:16:14 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d81bf2b537e5ab98e0fe33f90af1bbffc0b4a734f88fa3ae3565a6349df0faf`  
		Last Modified: Thu, 11 May 2023 21:16:12 GMT  
		Size: 12.0 MB (12035861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658c5919ed2262088600f33ce05e33d83fc71248ec393a2cee6f69c38c3cfaaa`  
		Last Modified: Thu, 11 May 2023 21:16:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea49f6a422b147f6445746b074da1e92ed8856358dd3cf96b73d02cc44a62407`  
		Last Modified: Thu, 11 May 2023 21:16:57 GMT  
		Size: 12.8 MB (12768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d7fffa87c4f5e4f33f4c26a08a5cf81eec8ef7e41359928aadde6a09af582c`  
		Last Modified: Thu, 11 May 2023 21:16:55 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd30ff7d08c3d6c356312c980212ffbd4bef34bb7c6668fe9da54f30e2bc2002`  
		Last Modified: Thu, 11 May 2023 21:16:55 GMT  
		Size: 18.6 KB (18623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a841328d305e34c984b9cf695b43d9c5d26924ce6b2fd0aceac6f25886b56a`  
		Last Modified: Thu, 11 May 2023 21:16:55 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abdbeb7b0dd71d2016c50e14112c55164e77de880daf4bf7f96e070fa437561`  
		Last Modified: Thu, 11 May 2023 22:06:20 GMT  
		Size: 805.2 KB (805193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c725a7868c9918ae0baf059ed60625171d99c25010452fd8387acb706d66be23`  
		Last Modified: Thu, 11 May 2023 22:06:18 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d224af0d47a82224afaf529e515abd66a778262fde81af6b912d7bf627c6b7`  
		Last Modified: Thu, 11 May 2023 22:06:19 GMT  
		Size: 552.9 KB (552912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74096f6190d0474e2521060a05f14fd66c851d6e6977fd96ebaa6e25d5aa2ee2`  
		Last Modified: Thu, 11 May 2023 22:06:19 GMT  
		Size: 4.1 MB (4073464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92af0802d1d77049d20bac7387ddc8eab43b76c02c8a7bb0e0ea8d39f605019f`  
		Last Modified: Thu, 11 May 2023 22:06:18 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb7f236f986d47dbbe7a179edc99b973d9968405e2d2f12f9941c14314dcaaa`  
		Last Modified: Thu, 11 May 2023 22:06:18 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:038d8cbfbed73ae9587559108c0eb62aeaaa113adbfc058187f2b9113d08d08d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36003738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5bc77cd6f4025af75786a7b15aca36edda9599375e66b3a3890ee6fad0f538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:43:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 20:43:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 20:43:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 20:43:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 20:43:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 20:43:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 20:43:22 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 20:43:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 20:43:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 20:55:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 20:55:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 20:55:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 20:55:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 20:55:45 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 20:55:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 20:55:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 20:55:45 GMT
EXPOSE 9000
# Thu, 11 May 2023 20:55:45 GMT
CMD ["php-fpm"]
# Thu, 11 May 2023 23:15:37 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 11 May 2023 23:15:37 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 11 May 2023 23:15:38 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 11 May 2023 23:15:38 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 11 May 2023 23:15:38 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 11 May 2023 23:15:38 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 11 May 2023 23:15:38 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 11 May 2023 23:15:38 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Thu, 11 May 2023 23:16:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 11 May 2023 23:16:30 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 11 May 2023 23:16:31 GMT
RUN apk add --no-cache bash
# Thu, 11 May 2023 23:16:32 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 23:16:32 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 23:16:32 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 11 May 2023 23:16:32 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 23:16:32 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 23:16:34 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 11 May 2023 23:16:34 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 11 May 2023 23:16:34 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 11 May 2023 23:16:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 23:16:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40710bc3fb9bc5ad7e3c434ed80c5779b850fcb32c45f0e8a675b32e23c5e1e`  
		Last Modified: Thu, 11 May 2023 22:04:06 GMT  
		Size: 2.7 MB (2684981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7494169f84aa7d9ddf422873e7db65413b6862b123151963fa32fa05907d25ee`  
		Last Modified: Thu, 11 May 2023 22:04:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e2ace06331713fddaca2119a604c67787f1e2d05963efbab6c09774a14bfe`  
		Last Modified: Thu, 11 May 2023 22:04:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829bceb76e6c181d71c4f54d989241aaba850140b8de2aad51669fd1dc42befd`  
		Last Modified: Thu, 11 May 2023 22:04:05 GMT  
		Size: 12.0 MB (12035878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1455d2d7d6ad8a76c751a0d40426573810e7fdd04ab60244d0a4fd8c253bfbcd`  
		Last Modified: Thu, 11 May 2023 22:04:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ae67a8e6dfee90fc96cd6d96ec19a9ecc35680c8d1dfaa876ae83ca5f788ff`  
		Last Modified: Thu, 11 May 2023 22:04:51 GMT  
		Size: 12.9 MB (12891757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217186230bf70fccdadbda1f789b0fffcf9b1f93dee2654c1dc3dcb156cd1d54`  
		Last Modified: Thu, 11 May 2023 22:04:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a4384341beaba7e0037513e2295b23eb5af0b59cbaba775c3a4eaf08c70b4`  
		Last Modified: Thu, 11 May 2023 22:04:48 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3d9f85f686b61f57f1f16361bb34122c2aec0d0e511394b53e333f3c17ff95`  
		Last Modified: Thu, 11 May 2023 22:04:48 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93968b0ca592076cc604dd608917d1dff112400cbd3c0da682f2595cb2034a`  
		Last Modified: Thu, 11 May 2023 23:17:40 GMT  
		Size: 522.0 KB (521958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574369ba29a1ef960ace2a1e767a1bfd8be2a94de7b635caa999ad138d979fca`  
		Last Modified: Thu, 11 May 2023 23:17:38 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d93c486720a1bf619bc79332c5c2c2911bb65c1a6c27a63691cb48660ac338`  
		Last Modified: Thu, 11 May 2023 23:17:39 GMT  
		Size: 494.4 KB (494408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a415316f0f650cd6a165a927a23dbfaa6b8ff811bdf518f64fbc3113a8b766`  
		Last Modified: Thu, 11 May 2023 23:17:40 GMT  
		Size: 4.1 MB (4073467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57270a0d35ba14dfe6a5b9edd672cb2942ac591ad8f2185ef5fadacd74db9a40`  
		Last Modified: Thu, 11 May 2023 23:17:38 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8ffe30e9f8df806efec8661aa498ce9a698bbfaf11960d6241ee5321f4a76`  
		Last Modified: Thu, 11 May 2023 23:17:38 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:63b159da668e7061e3fabb021ed8bb4d13a5f4bb9042f5e069ea3f56b1acd49c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36127348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c594fe8a6431b498ecd8411117011c9bd7b7c3036160594d9d642fed7c9bcc33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 21:29:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 21:29:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 21:29:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 21:29:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 21:29:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 21:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 21:29:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 21:29:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 21:29:15 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 21:29:15 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 21:29:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 21:29:16 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 21:29:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 21:29:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 21:37:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 21:37:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 21:37:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 21:37:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 21:37:59 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 21:38:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 21:38:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 21:38:01 GMT
EXPOSE 9000
# Thu, 11 May 2023 21:38:01 GMT
CMD ["php-fpm"]
# Fri, 12 May 2023 00:05:15 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 12 May 2023 00:05:15 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 12 May 2023 00:05:18 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 12 May 2023 00:05:19 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 12 May 2023 00:05:20 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 12 May 2023 00:05:21 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 12 May 2023 00:05:23 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 12 May 2023 00:05:25 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Fri, 12 May 2023 00:06:15 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 12 May 2023 00:06:19 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 12 May 2023 00:06:22 GMT
RUN apk add --no-cache bash
# Fri, 12 May 2023 00:06:23 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 12 May 2023 00:06:23 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 12 May 2023 00:06:23 GMT
LABEL org.opencontainers.image.version=1.9.2
# Fri, 12 May 2023 00:06:24 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 12 May 2023 00:06:24 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 12 May 2023 00:06:28 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 12 May 2023 00:06:28 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 12 May 2023 00:06:29 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 12 May 2023 00:06:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 May 2023 00:06:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7ab64acf5d7892690b10023745d6938fb8b74120c8c60235a21cace67fff33`  
		Last Modified: Thu, 11 May 2023 22:28:19 GMT  
		Size: 2.7 MB (2728145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12ef25af3414555b87ae448bb8e85e3f3805ec3dc4ad68bde083f1e61ca3423`  
		Last Modified: Thu, 11 May 2023 22:28:18 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b6a996eabeeaa6829fb842ecc5a98a81553b1a9bba417dbcb837eca423720`  
		Last Modified: Thu, 11 May 2023 22:28:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0945098d2a1ab63f1fac48cb6acb7979b0d3371dded2b25be282fe672551d07`  
		Last Modified: Thu, 11 May 2023 22:28:17 GMT  
		Size: 12.0 MB (12035892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df57dc8ec0a685b4238d0c8cd88ba24ac76ae50e1f443d4676ac50ba2031a8`  
		Last Modified: Thu, 11 May 2023 22:28:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7c81e9008dc5042e8454746dd4ee17c2b27d48f7a8494d63919e42382edb4`  
		Last Modified: Thu, 11 May 2023 22:29:10 GMT  
		Size: 13.1 MB (13105307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a8172c2c219811ecc94b318a6203f831517cc94913eecd823c73902a66f344`  
		Last Modified: Thu, 11 May 2023 22:29:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d083bb654eae97beb3de616cc3c55ee0852648c1a36ffe1006da0dbda095a23a`  
		Last Modified: Thu, 11 May 2023 22:29:06 GMT  
		Size: 18.7 KB (18674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa9e005aa27384a73997faf8bc1967c04797d93f843e0b963eb98034cdef407`  
		Last Modified: Thu, 11 May 2023 22:29:06 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea34c5c58816820318d0804b0ac6b9c5d041ee5215d5a87c603b328abb00ed9`  
		Last Modified: Fri, 12 May 2023 00:07:44 GMT  
		Size: 207.2 KB (207162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9281df009f9f8737ee8bf57b5b110d313a727ea082c167eef6c738d1650282`  
		Last Modified: Fri, 12 May 2023 00:07:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b37761ce995f4821f25129d19039fe41ae9526c3c6aab96b5cd1523a7661b4`  
		Last Modified: Fri, 12 May 2023 00:07:42 GMT  
		Size: 555.5 KB (555492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb591277bef0da5530f3fbb6b8c8fa14499151e5e56e0046a1ba3968631b3b13`  
		Last Modified: Fri, 12 May 2023 00:07:43 GMT  
		Size: 4.1 MB (4073470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45709f63a13e58d49eaadba493fe88821730766045c5e5a21a25a1532f4833a1`  
		Last Modified: Fri, 12 May 2023 00:07:42 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67927cf2cfdbc986fb8fd68b8d243f41604b1e2b42fa436c95e1db8dda915222`  
		Last Modified: Fri, 12 May 2023 00:07:42 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:db5b0e865c34f7173df592b49f5d6b1e1c7bc48d93f69b51fb20d0af9e664776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34676676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a629f55d5a50f126b60845dec43c02b3bdaacb705224776cbea722b997178e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:10:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 May 2023 20:10:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 May 2023 20:10:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 May 2023 20:10:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 May 2023 20:10:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 May 2023 20:10:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:10:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 May 2023 20:10:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 May 2023 20:10:58 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 May 2023 20:10:59 GMT
ENV PHP_VERSION=8.2.6
# Thu, 11 May 2023 20:10:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.6.tar.xz.asc
# Thu, 11 May 2023 20:10:59 GMT
ENV PHP_SHA256=10b796f0ed45574229851212b30a596a76e70ae365322bcaaaf9c00fa7d58cca
# Thu, 11 May 2023 20:11:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 May 2023 20:11:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 May 2023 20:16:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 May 2023 20:16:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 May 2023 20:16:40 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 May 2023 20:16:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 May 2023 20:16:41 GMT
WORKDIR /var/www/html
# Thu, 11 May 2023 20:16:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 May 2023 20:16:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 May 2023 20:16:42 GMT
EXPOSE 9000
# Thu, 11 May 2023 20:16:42 GMT
CMD ["php-fpm"]
# Thu, 11 May 2023 22:01:42 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 11 May 2023 22:01:43 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 11 May 2023 22:01:43 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 11 May 2023 22:01:43 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 11 May 2023 22:01:44 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 11 May 2023 22:01:44 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 11 May 2023 22:01:44 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 11 May 2023 22:01:44 GMT
LABEL io.artifacthub.package.readme-url=https://raw.githubusercontent.com/YOURLS/YOURLS/master/README.md
# Thu, 11 May 2023 22:02:09 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 11 May 2023 22:02:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 11 May 2023 22:02:10 GMT
RUN apk add --no-cache bash
# Thu, 11 May 2023 22:02:11 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 22:02:11 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 22:02:11 GMT
LABEL org.opencontainers.image.version=1.9.2
# Thu, 11 May 2023 22:02:12 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 11 May 2023 22:02:12 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 11 May 2023 22:02:14 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 11 May 2023 22:02:15 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 11 May 2023 22:02:15 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 11 May 2023 22:02:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 22:02:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1229cbf44dd4d93ce3b40fc629fa6700457195d0080eb6e6d28096372f526093`  
		Last Modified: Thu, 11 May 2023 20:57:02 GMT  
		Size: 2.8 MB (2753025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997be929bbab1ac7c5ea596b8d8336fdc045fe9ced4c15b05bb8173b1f9b79a8`  
		Last Modified: Thu, 11 May 2023 20:57:02 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e9ef3515d879c1d5a2806852a344a3349ab8399604e5cdd2ca621b69cc8e4a`  
		Last Modified: Thu, 11 May 2023 20:57:02 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cee375cb295b17191b66516520860e68b93950fef0186dbd300c08e661a95b7`  
		Last Modified: Thu, 11 May 2023 20:57:01 GMT  
		Size: 12.0 MB (12035897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02663d2397cedd44d5a7bfe2f500fcbd0904a7cd1caaad634dc33a99cb9a3d55`  
		Last Modified: Thu, 11 May 2023 20:57:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0620825df3e55d639d590a09bb64d6a0a4c2d58cdcc1ec9f305fc40616817af2`  
		Last Modified: Thu, 11 May 2023 20:57:30 GMT  
		Size: 11.9 MB (11853928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ffdc5b892940f51b558efce67f6b6ccb4ac1cea10adb356810456bbd5bd5b`  
		Last Modified: Thu, 11 May 2023 20:57:28 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ec117b7a25e815a2d75b8d9a22078503c84e3916858fd2aaabc4747ea4b940`  
		Last Modified: Thu, 11 May 2023 20:57:28 GMT  
		Size: 18.7 KB (18696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950c8ae8d5fb297a739192baf2b59f02bd6c64c19a00bee2486799a92ce1863`  
		Last Modified: Thu, 11 May 2023 20:57:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da4e4a459c455d2ddc1e35fb47872385f458d934d69253744f69acf94a77ce`  
		Last Modified: Thu, 11 May 2023 22:02:57 GMT  
		Size: 180.3 KB (180257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbe0e256dfead5b13a18c64f755f9986e1800d053b4e41aa05ece9d07221f58`  
		Last Modified: Thu, 11 May 2023 22:02:56 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0018df17cd48bb8ebe297260033efff14e0f4954a690fdd1ec781ee5ffd7fb5`  
		Last Modified: Thu, 11 May 2023 22:02:56 GMT  
		Size: 517.5 KB (517527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023371e50fd9d9110024d75fe245832926f1dadabb5dec9267870edf2387fe9c`  
		Last Modified: Thu, 11 May 2023 22:02:57 GMT  
		Size: 4.1 MB (4073474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff20134a7434fe0e73f762d18d918748bfb4e2b564f8c937fc1badc5bc83d5ac`  
		Last Modified: Thu, 11 May 2023 22:02:56 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba22234d4b1ca57ed7b2873d697aebca54151f572989d305b8371eb63137ff0e`  
		Last Modified: Thu, 11 May 2023 22:02:56 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
