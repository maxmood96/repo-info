## `php:fpm-alpine3.22`

```console
$ docker pull php@sha256:95588bfaf1b890e3fc1f308a0a23539c4f03ce28a4fc770473ae3899d6669777
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
$ docker pull php@sha256:b44fa951a7e4833f2fe32db0a19b785c6b58aabe6c6e90b1263f55e00ae9927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38356529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752cb6192dab6fb2e0c8b9d29455a09f189ccc51e20fd90800fc217f117a0574`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:03 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:18:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:18:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:18:00 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:18:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:18:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:18:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:18:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f531a5764382442e625004130c25e537264c0ef5393088a3c51e03c7abc6e04`  
		Last Modified: Fri, 05 Jun 2026 01:18:07 GMT  
		Size: 3.5 MB (3464927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b82e5a893c0c3f891d66d3548e01431068b0351cfab4763a7c5983b66e142`  
		Last Modified: Fri, 05 Jun 2026 01:18:07 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208c408b71eff992cb46801ae6e11e2f95d655065ff29f7808504b884b7c954e`  
		Last Modified: Fri, 05 Jun 2026 01:18:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cecaeadc07c4a68281231087db7ba30c13b46a6332ab0c2d007a094463c0e9`  
		Last Modified: Fri, 05 Jun 2026 01:18:08 GMT  
		Size: 14.4 MB (14419449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4befe70e09c82aed8285dbc1701f93f7010a512f03a9c6f8be847a67d8f81aff`  
		Last Modified: Fri, 05 Jun 2026 01:18:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831bb33df4f14039c7d46537cf642e656909292b28370118031fbe5950c4f373`  
		Last Modified: Fri, 05 Jun 2026 01:18:09 GMT  
		Size: 16.6 MB (16630552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268bf0235546c4889b58f392dfc9573561f7320e4208bd17f91dc2180f460477`  
		Last Modified: Fri, 05 Jun 2026 01:18:09 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be67e38e68005cb89544be7295e9e8d69c12662e04cf1c975e5b940168e0a32e`  
		Last Modified: Fri, 05 Jun 2026 01:18:09 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9f6633e9994758e0c0d477feaf1790122f12702bce9270013ae25dbc145c3`  
		Last Modified: Fri, 05 Jun 2026 01:18:10 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:b127a7f3c776a29f89b362202f1f4e6f8279e1bc1db5dad480c6a32826842be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 KB (326380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350ab05511d7ff96cda5d035f43712c34c576df94f145b7ca3c48cd058b6a8d6`

```dockerfile
```

-	Layers:
	-	`sha256:cff8037b0b232ac05eb77db4e232294cfd564ac86e53d9286b0e8ea1104b1227`  
		Last Modified: Fri, 05 Jun 2026 01:18:07 GMT  
		Size: 278.6 KB (278604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541126765e935a77d380f46210620ef37022e824e13ecdd5a25bc17d9a094765`  
		Last Modified: Fri, 05 Jun 2026 01:18:07 GMT  
		Size: 47.8 KB (47776 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:de7e3964339b30701d79461a29aad731fade73dbef8810a24cac09fde6710add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35940751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df147b2533edacf13fb0b108ae9be2c8230f9be65fd26999a5c1cfbdd2250d0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:40 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:19:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:19:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:19:02 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:19:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:19:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:19:02 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:19:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a76163803625a81fbc1f2804448e8cc3d6cbfab5af704c4d164fb08bccb9f4`  
		Last Modified: Fri, 05 Jun 2026 01:19:07 GMT  
		Size: 3.4 MB (3428188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ab8c36ae1e55a9a86bf20866ab9d4f9c6ee08537ae486601fb3af8aadbf5f`  
		Last Modified: Fri, 05 Jun 2026 01:19:07 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be87cdf6b98c7996cc3723df606090a6b8297bf3a3f3c590170e2e71e55c93f`  
		Last Modified: Fri, 05 Jun 2026 01:19:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a589ade0a4dcf4bb69f54272bc6e87270100307713f199da097e4efd35fba0`  
		Last Modified: Fri, 05 Jun 2026 01:19:07 GMT  
		Size: 14.4 MB (14419494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f2ed7aa717fb91c200f7762e92bf959c465b547f55c1140c6ee18e17874e4b`  
		Last Modified: Fri, 05 Jun 2026 01:19:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50c3d569feb6d7354769c2500c5cf6c8d978b273481a4983255c16c6d7ef024`  
		Last Modified: Fri, 05 Jun 2026 01:19:08 GMT  
		Size: 14.6 MB (14552464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4a26708a64db4e1bb17bd1b3d764559694289e80fa948223c30d8a7c558fe7`  
		Last Modified: Fri, 05 Jun 2026 01:19:08 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be338f02115f510ea4ec50532372ce1202c0d99ebeac39798677b7203f5bd62`  
		Last Modified: Fri, 05 Jun 2026 01:19:09 GMT  
		Size: 19.8 KB (19835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b62ed6b9a895d7b6d0a9e7366a3008dcfe0290edb80f850f81b2a028d0b92b`  
		Last Modified: Fri, 05 Jun 2026 01:19:10 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:9dd80b2b4502e8bb5110ebdb4ee4f1ad11a83ae568edf7b37246840765fd8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ac4fd02d1a5cce7182569e246b4b08069776295173248e4e0f2c3c7b486ca`

```dockerfile
```

-	Layers:
	-	`sha256:884310035c37e49e633b7747cff26d45dd554561a2f128b29d680f9429ea3ac4`  
		Last Modified: Fri, 05 Jun 2026 01:19:07 GMT  
		Size: 47.7 KB (47720 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:fdbcbc7196eec8fc904b4772390099e069ab779bb270f939c5d7071cadee307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34684070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c578c834f5d2d0c096311965809bc689fb6dcf84448163d7efac11d41080d91`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:19:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:19:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:19:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:19:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:19:10 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:19:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:19:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:22:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:22:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:22:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:22:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:22:24 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:22:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:22:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:22:24 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c089af267ed11e3ee02e8633eaa304907ef8ac6eee31e48a9396d47ed2edb5a1`  
		Last Modified: Fri, 05 Jun 2026 01:22:31 GMT  
		Size: 3.2 MB (3244390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a58721fa5298078c6d07f7e2f4cdc7f19b8025302de1be20eeebb4136491ef`  
		Last Modified: Fri, 05 Jun 2026 01:22:30 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6fcaa2af485bc33512ee389ea45dd01a49f1a5d0e987e9e9ab1612ecef70fa`  
		Last Modified: Fri, 05 Jun 2026 01:22:30 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad132eac53467d4bb804bca7ebce23783c69adf24f235c339b0f9a359999cc4c`  
		Last Modified: Fri, 05 Jun 2026 01:22:31 GMT  
		Size: 14.4 MB (14419489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1208d15d63890219da18bd3d94bfbddad93e4484bc6b020fbae8e92f89e4ba4c`  
		Last Modified: Fri, 05 Jun 2026 01:22:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de02e0f782d6fe4cc356ff8a483992baec4e9a057fd2459de20c242d73bed7`  
		Last Modified: Fri, 05 Jun 2026 01:22:32 GMT  
		Size: 13.8 MB (13761167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8870d27afb20b803d6a4fc8c16ec534289b016bbf5148e25fe60838a434a489b`  
		Last Modified: Fri, 05 Jun 2026 01:22:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d8dd3c3c7c650ed75ebfca40a39a338e1c04954afab5e1b10288adcd629de3`  
		Last Modified: Fri, 05 Jun 2026 01:22:32 GMT  
		Size: 19.8 KB (19813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad33173126e52cfcaa1934d835ef6bc2f9e31f696e57d58e20da6e3cc5a28a6`  
		Last Modified: Fri, 05 Jun 2026 01:22:33 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:779ebf263754096867ad69525310603481404bcf0a3a09f80401fcb03773f72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 KB (323584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a33cc75d9ead53bf69288e333264ae789ec100a5001006c45fb7e2ef6401e`

```dockerfile
```

-	Layers:
	-	`sha256:f6a9bb8901b45678f00ac5119c3c5b2ff9547a9c8ae0c19502cdd28b8b74e1bc`  
		Last Modified: Fri, 05 Jun 2026 01:22:30 GMT  
		Size: 275.6 KB (275650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8dbb4195c674d8f4b087ffc4d3779295a1f46cbc159828932c81f45364ee7a`  
		Last Modified: Fri, 05 Jun 2026 01:22:30 GMT  
		Size: 47.9 KB (47934 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:2239f58d4c644285da192d281cebd9e356e25dae73bd3cb3bb76a4b6401831f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38231043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f3bd61f2b1e24114c858ffa35836ad5e8ea2fb8cb39fcf9221dc8f5e9a530d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:31 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:19:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:19:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:19:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:19:14 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:19:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:19:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:19:14 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:19:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ce31bdc765ccc71b393c5eeb4731d7e68d438e0af60f60ad1ed4223d63f538`  
		Last Modified: Fri, 05 Jun 2026 01:19:21 GMT  
		Size: 3.5 MB (3467680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b4e3276b27ff0d38c3b9e6b4809aa00ec16d509f5dbb3e0debae30c3ec6fb`  
		Last Modified: Fri, 05 Jun 2026 01:19:21 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6352b25e709752f08e1d05a6f283cd1aa4e28d79651c4ed27d332dba2e2a1f`  
		Last Modified: Fri, 05 Jun 2026 01:19:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede32edb5d94739d894afcd23104366305d6f28355307b082fa1c80c34a40cbb`  
		Last Modified: Fri, 05 Jun 2026 01:19:21 GMT  
		Size: 14.4 MB (14419486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a04c85cf91cf6b6b00febda7e1be7939c3436bba69a435ea4770cae1ab352`  
		Last Modified: Fri, 05 Jun 2026 01:19:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c0ab89ace7269d5a26a0f6a61333c8cf7ef0a8ae197689b5b878465f4d79e6`  
		Last Modified: Fri, 05 Jun 2026 01:19:22 GMT  
		Size: 16.2 MB (16168785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f4537d1a7b227a668dd923daac41717d90a590a899c1a3fd7ea676efaed7b`  
		Last Modified: Fri, 05 Jun 2026 01:19:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c89334d4ef2a8b112d545d9d3e2c5c7fe398e0482f885aee138a01cc1788`  
		Last Modified: Fri, 05 Jun 2026 01:19:22 GMT  
		Size: 19.8 KB (19822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ad5a7e753388165e43550bc49a7e2d38daff3fcdd1ef34e7659aebcc0b2dc1`  
		Last Modified: Fri, 05 Jun 2026 01:19:23 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:38b1a305e2998d914384dbf9299f24d9c080538c981442c8090267ca6332bffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 KB (323641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f34c24ca31ac6423b3382676d29960017fbfc3b5f15cbcd16abe021f1a4825`

```dockerfile
```

-	Layers:
	-	`sha256:db2e0146cc69c4c28687dfcce83fa010c7e165faec419fc6c1300fce47f0bcb1`  
		Last Modified: Fri, 05 Jun 2026 01:19:20 GMT  
		Size: 275.7 KB (275670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b502f0ea98ec732f3e4922d746c40febd67c71a7d767cebe37332e6bd245ae`  
		Last Modified: Fri, 05 Jun 2026 01:19:20 GMT  
		Size: 48.0 KB (47971 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:01b018b60c11e53532bc3811fa44b140982bc452dcac725a6b41cffdf09fe4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38679683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cf0f3c5accf0f61dca559bd3180b460a23c901049428283046e724e0efe00b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 01:15:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 01:15:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 01:15:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_VERSION=8.5.7
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 05 Jun 2026 01:15:16 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:15:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:15:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:18:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:18:23 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:18:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:18:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:18:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:18:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9752d9856a7d7415d6cb91decea93aded4a2b3d2d3a37273996497fb404d2f`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 3.5 MB (3522712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606b752fc791d0580b100232305b6e76f0963fbc32bc03fa19b4aee5eb7e4e8`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433a55922d57c1b620923ebc6c66edd7252525f6c6ecd017685e7368056efc7c`  
		Last Modified: Fri, 05 Jun 2026 01:18:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae04095b3ee9e588efdcf26b483f4c1e824e7de339b5fe819401942150ed263b`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 14.4 MB (14419460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111da8ed8b47c1af4528803232b7ebd36e5aa5c37860bb4f1f0994696390eded`  
		Last Modified: Fri, 05 Jun 2026 01:18:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae527ecafa4409212b066027ff3fa1e83412d8bcceebef66aa29949ea5fa5ece`  
		Last Modified: Fri, 05 Jun 2026 01:18:31 GMT  
		Size: 17.1 MB (17079390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fa21053ad27aec0047cf361ecccbc7e6cdebc38e40a25f1d7afea348a7f966`  
		Last Modified: Fri, 05 Jun 2026 01:18:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c84a3eda17148905bcf7ea9438caf58d088ab5d1dc3f0494ceb40c3ee4c6ad`  
		Last Modified: Fri, 05 Jun 2026 01:18:32 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba1c6e8d55c88aba2f728911275fe4abd7f9e36def2ee9e99f4cc2855e13e52`  
		Last Modified: Fri, 05 Jun 2026 01:18:32 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:efd5cf993adb72695bc85a9fd0b5c7e2e0c2944f11cd9da328f6e127fc7136aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 KB (326312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1623cae367267b37c43d90f791818446074bc911c20280ff051e54f1f461d`

```dockerfile
```

-	Layers:
	-	`sha256:f5d645020f7ba965f239717e656112a524d28a1ee1fb5d63af65c26cfc16355f`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 278.6 KB (278579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3a9829cb5021c4d46d49e6009fb1e953f3d03733b57fa2a10bf4751efd526`  
		Last Modified: Fri, 05 Jun 2026 01:18:30 GMT  
		Size: 47.7 KB (47733 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:6bcb0d810ef2c95f21edc3fbc12f071f1b5a38aacb808ce6117e23f742ced041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38775773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac42bcd7f754d86653437b690f14bd5aa0c806599dbb8335f0983ca8d5c488a5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.5.7
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:42:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:54:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:54:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:54:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:54:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:54:09 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:54:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:54:09 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:54:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af78c2b9be930d3bfca6d9c5d98914a3ca2676bb7b3951f252adfc0b6f4f24a`  
		Last Modified: Fri, 05 Jun 2026 01:48:40 GMT  
		Size: 14.4 MB (14419518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd934ad5eaf9340d82ba9aa021468563c91541fa549c823a5babdf4cea89a19d`  
		Last Modified: Fri, 05 Jun 2026 01:48:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047f3a10ec715d53cbd2b6d2cca78185b2f101b025043034e4f9754dd091f17`  
		Last Modified: Fri, 05 Jun 2026 01:54:23 GMT  
		Size: 17.0 MB (16971301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb383f6304ab6cc7ea48a1f0e2f95194992206505a0d6c9beecd0aec86cc675`  
		Last Modified: Fri, 05 Jun 2026 01:54:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ab84addeace4f815744b89a108eb35dbb5c18916e1dbfcd16b4d970bd596b`  
		Last Modified: Fri, 05 Jun 2026 01:54:22 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b517833c675b9729ebf98013826763458445b64ee26f87c1ba66d6d9e1988`  
		Last Modified: Fri, 05 Jun 2026 01:54:22 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:6ffa3238c5d4b3b42864232e3bbe7b75ed8d1cb19752db848333d879fac55b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 KB (320579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c838a4f0636e6300b5fc3d58707778e6650b88e1cc0ddfa87d2de8c8e7d64cc3`

```dockerfile
```

-	Layers:
	-	`sha256:4cf7b1904487714af4b5774d8ac791433b32bccfcf481794cc26410f55bdbaee`  
		Last Modified: Fri, 05 Jun 2026 01:54:22 GMT  
		Size: 273.7 KB (273697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133ec6c4a93a991464e24355092d9e172396a5f5647aa87d0e63e5ba716c0b09`  
		Last Modified: Fri, 05 Jun 2026 01:54:22 GMT  
		Size: 46.9 KB (46882 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:7c52110108bc795508b6d4b6b736a2ee3fda9b79b4d295153578f5579a296d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37334678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52fdbfce8e79d847a5cd3aa1fb348cdff0d3c60d02d9036c91cf7bde5b60f6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 11:02:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Apr 2026 11:02:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 18 Apr 2026 11:02:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_VERSION=8.5.7
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 07:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 07:43:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 09:43:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 09:43:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 09:43:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 09:43:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 09:43:34 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 09:43:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 09:43:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 09:43:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 09:43:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aba8e387b0f52a066bd16fc16548380bb5c1ba358c87f632f41bf0e1538804c`  
		Last Modified: Sat, 18 Apr 2026 12:03:48 GMT  
		Size: 3.6 MB (3600194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0aef12c28ba880017fb96a48e3e22f4b4e363ee1be8f9a85075a131d12b72`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a7d02aa931427745ea3ec5ed71cd22b97056886e6224d2e88e3226411519f`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2613ed4a3e869f6c55d87b3babbffcc862b86c10e7c4d15ec090cd5053e49`  
		Last Modified: Fri, 05 Jun 2026 08:43:32 GMT  
		Size: 14.4 MB (14419468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af80e7cb29dfe9b2e4aff888245a456ba3eafbcc0ab5c19a6c677cb0ca672fe`  
		Last Modified: Fri, 05 Jun 2026 08:43:28 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331c5343374330e1a8a02f4415d9104a49a7bf34edc7b251df9288f865f2469`  
		Last Modified: Fri, 05 Jun 2026 09:44:33 GMT  
		Size: 15.8 MB (15760896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3247a059ac7cfea760bbc60d586cffd7b89cd6ecf2060cc5f0f759d535f2c4fe`  
		Last Modified: Fri, 05 Jun 2026 09:44:30 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6606b43af01a2b7dd4d9b570cedb7c1e06f614748cb6c38e9e866bcbe9d459`  
		Last Modified: Fri, 05 Jun 2026 09:44:30 GMT  
		Size: 19.8 KB (19834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ab4ce7ae7f00d442c5e1d6ca00495a0cfe3dec8878a9e9cc6781f54ebe15e`  
		Last Modified: Fri, 05 Jun 2026 09:44:30 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:61c00e1d8eaaecc92e8569c864edd360d8d3ac010632f7940f850df1bbaa8089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 KB (321525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c4135558323f1b17e93a7da4062ae942f9fe82a08bb1da47db5daeed805769`

```dockerfile
```

-	Layers:
	-	`sha256:b57e4d769fe9492492d9b329aea6d036e287825626ac3ee1bfc0d34a3560ba53`  
		Last Modified: Fri, 05 Jun 2026 09:44:30 GMT  
		Size: 273.7 KB (273693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9730096d7fdd68ac1019ee08344db380c6360359410b0000e459507224dcb6e0`  
		Last Modified: Fri, 05 Jun 2026 09:44:30 GMT  
		Size: 47.8 KB (47832 bytes)  
		MIME: application/vnd.in-toto+json

### `php:fpm-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:a51251196f292297e483b9494cafe446c3b7934715e3c52eea3c78f4d59d9538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37817034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f125626ddcae653f8bef1058de50fb49f816d611af3a3e22ab23ad455f4893c3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 02 Jun 2026 06:10:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jun 2026 06:10:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_VERSION=8.5.7
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:27:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:27:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:33:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:33:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:33:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:33:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:33:04 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:33:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:33:04 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:33:04 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:33:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75735c7840576081d137f73c9e1d671fef683197275ebf98b3f89df2d6f047`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 3.7 MB (3691317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467f2db1ecdfa183e05296de22d16bef58101b59f959d209d6247d1f495d947`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17247e4c91d7dc91ceb5e0d3f79b6712c2173b99d17a3c9edfbf048e100777ee`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff11588a3caf58ad81c5155c6e1372335e0a2d6a86222b96cc84daef958ac8e3`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 14.4 MB (14419503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1fb8967fb08536e9d1df5ada307b6557c57eec7fa27fbf14a261c6e0ac7d76`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73418a892411b021b056cbac90d938f7592822ae97b048e3d52a05fef91ee09c`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 16.0 MB (16019120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c75744c4437cc3f46ec6c9ff6e7b10d152c81d66048b16d22af7018efed4ad`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee246b64f148f40ee3c217eb15a129c0145891fcf2a070e1d80d695f00608d18`  
		Last Modified: Fri, 05 Jun 2026 01:33:18 GMT  
		Size: 19.8 KB (19826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c91e97e9a24bf7cfef04f17b351e9e01e71b2de205fc0b593b5593da97e886`  
		Last Modified: Fri, 05 Jun 2026 01:33:18 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:9017e16c098e650560e308ba13079d8377695bba0c452fa73cd209877b5478c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 KB (320489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db795e0fa4c95c7f466bb79055debb39119bac2d2d9e2184105834deaa60b10a`

```dockerfile
```

-	Layers:
	-	`sha256:07b9661dc4a3481376846908671012c43a0dc4ddb95a37500a683eac1a13ce7e`  
		Last Modified: Fri, 05 Jun 2026 01:33:17 GMT  
		Size: 273.7 KB (273663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94741528eefeab56ac30e9f63831b11c0bf4184a8682b2a79f118c5c3556bf18`  
		Last Modified: Fri, 05 Jun 2026 01:33:16 GMT  
		Size: 46.8 KB (46826 bytes)  
		MIME: application/vnd.in-toto+json
