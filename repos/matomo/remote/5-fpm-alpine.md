## `matomo:5-fpm-alpine`

```console
$ docker pull matomo@sha256:ba0e216b73dc3c1a351179b29b47a73d7a79d19c057f8da579f5364c2247bc34
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

### `matomo:5-fpm-alpine` - linux; amd64

```console
$ docker pull matomo@sha256:5946aa2baa50fc53de65a42bf8b4b37d63e2e72612df892af856e01efc5bbaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61111448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd5d178aec34cea225bd3d2f83891fdc26d54c90c65cc92a2984ba7b3761ec2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.25
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10ac87811a7151f2d455ecd66e1f24914759aa556bf865115e9b5451c34c6`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 5.9 MB (5927523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fc0402d547809980039811ae9b42dfcded62490cdfd22f86eeae02a5401c4f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118a89a65a7879c4cdee30e47c63bad49e3b3db33a51de3fe326c3d569fc205`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd1735270d6e1518aaee894fef4efe6676e548396eb6350a2823bd039d45d65`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 12.6 MB (12604759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b287e8c3fc7e356d999ffd59f3ff23eaeafabb55d3e982709ea8418d30caa7`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8c7c6fddb40b2fb483e7c0cdb28a715ad094759babae305cc3ee8b3324cad`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 13.3 MB (13265060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca0b473638630b0d5752cba198cb4c45e865cc6f571d15a657778b8c9573f7c`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadbc3591c836d34e9c40cf1dbc676c2da1c2c323afd6e29624fe20bf6143a7f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 20.0 KB (19959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff2d0bf89e370e10b4bdf5193157afcda7091db8c80f48573111444634e51a`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 19.9 KB (19950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a961078f85baeb62fad90d7f53e5a386185ce08cde9f06f1cbaa0c3d91b7e81`  
		Last Modified: Thu, 28 Aug 2025 18:54:14 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f68e5656fed869d527dce7ed6a375e7c183d0cdfe613f26972b3a3bee907cdd`  
		Last Modified: Thu, 28 Aug 2025 19:21:44 GMT  
		Size: 3.4 MB (3447388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3ca91f38490783e1a9e245809a900df79d1c2c7fc3e3ed57a4b1fc5958d24`  
		Last Modified: Thu, 28 Aug 2025 19:21:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c398724f12aa0ce79cc86cff913261028c14d9c600ffa435a46d884d5f3ec0e1`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 22.0 MB (22012340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062fc3b6fa4574b918eb440749ed4ff3870fe06b19672bfcb00b1c3a489ed740`  
		Last Modified: Thu, 28 Aug 2025 19:21:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20efeaeebf3b56c852ce38987fa4b18c4c7bb1feb07c03f33bf8952cb05a16d4`  
		Last Modified: Thu, 28 Aug 2025 19:22:04 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:dc1cf92047509333b930730546f01d87accccf88174a9799df172439fe1e4f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf8e172326a2402704dda69044276c7401d095fc23f9afda81b7b537573fd48`

```dockerfile
```

-	Layers:
	-	`sha256:2d9fb1aa0027958ac5974694fa3a3216564500282bf5507edea3ab072d5158e5`  
		Last Modified: Thu, 28 Aug 2025 21:12:08 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:a0f83df51f819084a870e90237e04661636ee4f85fb1eafe2f33d1bad73d5c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59128238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0823e304c9a0a6388e7aea211c8ebcced960bd768f736c497572b2d936497fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.25
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ffb49c82cf16fea2b2658c93683845111cd140ee61f49d53a82c3343d66eec`  
		Last Modified: Thu, 28 Aug 2025 18:50:06 GMT  
		Size: 12.6 MB (12604744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dede99cf30270dcfe20bbea8569fb35edb90a7f2526cf016a454258c5bd825`  
		Last Modified: Thu, 28 Aug 2025 18:50:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d46d83cb43634c3a9d6d3ae51bc364e0a22f932446846a5076f8f853c5b633d`  
		Last Modified: Thu, 28 Aug 2025 18:54:48 GMT  
		Size: 14.6 MB (14591980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720229cca20b0fac0004477dea0d6345a3bb1f6cfa25abecc961966d9b0fc077`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94728b4b4e6e7e475cf1d5bc67e2be88a5b5f9280e3041dd6233847e30fcfcc6`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47051b49d7293aeec1bb0d509def29db4e079b0d9b723e3b05d57fc971e003d`  
		Last Modified: Thu, 28 Aug 2025 18:54:41 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a2f3a97e3f7a9b96a80c2275a22d9dcb266c7d0ac5725c9c782dec1d4fbe1f`  
		Last Modified: Thu, 28 Aug 2025 18:54:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda05f0def475d5e6c7c59a7aa29e1dd221b121765513d053da82031f1abcd77`  
		Last Modified: Thu, 28 Aug 2025 19:48:50 GMT  
		Size: 2.9 MB (2942107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01f23f2a3f92fe780aedec9f03a2351f1de7e2388b60f66e7acff955ed8287f`  
		Last Modified: Thu, 28 Aug 2025 19:48:50 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7379f9ac5ca9ccace5f23603b926d8327943b7167bd569578aba8b7af991236`  
		Last Modified: Thu, 28 Aug 2025 19:48:54 GMT  
		Size: 22.0 MB (22012221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438bf70ab855b7558e1175189e797228cad1f73548b2bd699323d40a61d97c25`  
		Last Modified: Thu, 28 Aug 2025 19:48:50 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080775d4309be282772b223337e6ce1c37b2f1011f6db626234de61dda2a613`  
		Last Modified: Thu, 28 Aug 2025 19:48:51 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:d4333951b9a3df08335116a71572513bf0723e8f3d08c65ab2dfd49b23194575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eddf29da4735d84d8066b8e207934521838246c171199798812de88d41868a`

```dockerfile
```

-	Layers:
	-	`sha256:47ef941d5209857d4f0bd805f996f854b3aa56792f6e4c90863b14c9835ed676`  
		Last Modified: Thu, 28 Aug 2025 21:12:12 GMT  
		Size: 31.7 KB (31717 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:e168e36df377c4a230cdb116af20721f252fd75893f7769eb61aed90922d5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55196947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea48505b06d817cdd56e31d2ccaf70b0a54fee5ae9b036baa6b807eebdf88523`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.24
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba00dd2d5d8f6a44bf0a20885871d1853fc7167d84fb6ec957e7ac660ed1f49`  
		Last Modified: Tue, 05 Aug 2025 00:07:34 GMT  
		Size: 12.6 MB (12599855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db466338552dbc3e51fab25cfb4c0a29f8cba308945ce14c23b2f3cc32a569`  
		Last Modified: Tue, 05 Aug 2025 00:07:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5e1050777a14bb79aae042037d3142cdf0379a6fa13e1bbd464536acaab1c4`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 11.3 MB (11287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3533ff91d2cbf4b64276ed59a40895b09a8dcd8196b65d19578e2c5fb49878e1`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b0618cc8e7a0c9625469ed1f03151d3a30be85350383e190f2611267e11ce7`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c93fa35098206749c593cfd31020dd3187b539cb278056d4b68f8a7abd3312`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c160173b8f73a178b3ac82cfd72acbd558dba08c5a7ed38426a8a9e6eb839f`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c01e0ab3f371db223d3086f87265e6c14324628e1b21353f0aa0c1dae6c5b14`  
		Last Modified: Tue, 05 Aug 2025 04:19:12 GMT  
		Size: 2.8 MB (2783528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8001b35767bef6930ff4dd160945d5040894102622173ccb697835d5648c4b29`  
		Last Modified: Tue, 05 Aug 2025 04:19:11 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1870eed09be42e136db3f8b6a526d7649aedc463b94febcab1f812fec51b53`  
		Last Modified: Tue, 05 Aug 2025 04:19:13 GMT  
		Size: 22.0 MB (22012162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331320ccb9b136f9ca3c3c854812270365c9d26ae030553e30e052662bda02d`  
		Last Modified: Tue, 05 Aug 2025 04:19:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f548f8014b46123b0df70e762e063c33e6ebc721018a9f44e9f26eace05751b1`  
		Last Modified: Tue, 05 Aug 2025 04:19:12 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:668d1a72d3ae07c1c3e86582553adc56889a585ef34baabb391b54b03092b222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9835f16c209c0a82b968b75b44de9779c737c6119d0beac3c48ad8ffa6eccd`

```dockerfile
```

-	Layers:
	-	`sha256:2793fe00f3e70e4fa8d06ac1adb57bd6d13127fa345116ea9813067480362b46`  
		Last Modified: Tue, 05 Aug 2025 06:12:02 GMT  
		Size: 31.7 KB (31717 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:d47e82dd533df92e75036cc736c5e59c3a703984afc4e0d28f1c7476e737d619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59259934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6920d67cf37516d18bcafafb7701d78a451cf1d3b85439bca1a5d9daa9ce91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.24
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c312f75964337f4db7770ce494c065e1775810a79a6ad25cc8846d1924eb8`  
		Last Modified: Tue, 05 Aug 2025 02:40:12 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3179efae18545d01b9663211a16a1cae37ca72749953364336d472c4e81e2f`  
		Last Modified: Tue, 05 Aug 2025 02:40:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e3af117145aa9db60dbdb547182b06888346793df58c20cf6ed3d58f79499`  
		Last Modified: Tue, 05 Aug 2025 02:45:31 GMT  
		Size: 13.2 MB (13249851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71127f1e5a0d78107b15f785398d341b771fdb0179d1132baacf28602dbaafd6`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024bb4e36e07326dda259a05227cadf8e5e26b6fc8e6ff2c756423e75f55a5f2`  
		Last Modified: Tue, 05 Aug 2025 02:45:30 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110b4929c8b1443c6afd235ecbc59b4a2d6797414a06ba0cc2a541b0e7be8ba`  
		Last Modified: Tue, 05 Aug 2025 02:45:39 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaddacb01d48656b98dbc057e2387016c89d834cabaf74099ed0fdaa5ef89dc7`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc4b1d932bef165f211070fd5f8a3fe63e97fbf50ccf66e43d32c4e4baa058`  
		Last Modified: Tue, 05 Aug 2025 10:20:32 GMT  
		Size: 3.8 MB (3758253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ad79e4faaf571fc80bc7b0d05faa08cee11ab8b5431b40bfc0b7f8266504e`  
		Last Modified: Tue, 05 Aug 2025 10:20:32 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66481a96f39550722b5764e3645e6795cad2917d33e797398bca93817214b334`  
		Last Modified: Tue, 05 Aug 2025 10:20:34 GMT  
		Size: 22.0 MB (22012178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c9300d5ae3e60c97b630787e80890eec6eca63ec46d3693f7d7db3a2583e2f`  
		Last Modified: Tue, 05 Aug 2025 10:20:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28079e1d65d2bb930ab45594fc036eaff85a55eb20cc249e8f1c87f6859f856a`  
		Last Modified: Tue, 05 Aug 2025 10:20:32 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:685deaae19699f331ca31a7cceecc1e0f44e4c81155b25e31c9b6b7e735febe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298a47f3b95f9d71459794c586132ca76a009380814c530d75da938e9bcf25ce`

```dockerfile
```

-	Layers:
	-	`sha256:9f7cfd403cb89233bbb09ef302c894d197bd8f7b86d89962316de4cba11b0f86`  
		Last Modified: Tue, 05 Aug 2025 12:11:43 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:605379ae9337e83c50ccd112455741f1d734d30617ed4bd79d5744684e625078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61065951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb94952fa8bc09c40e14dd554c7283905e70ac65dfa68cbe50883c4270a6115`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.25
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a59919ff7785468d660110ee9507b13705f5565f639b7d7bca52a140856b5`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 5.8 MB (5794083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33e8e8baf1e334700853edab49903aab1f8ea7b65bc8ea9036cad309a3b7118`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76198f21a38b8e65970b7af97c8146cceaaec7b8de4cf4fce2e437c8d7c1ded2`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0592096578de3942e0d1a4c0f06e422ce9b189222d19d93f037d9a2a7cd776dd`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 12.6 MB (12604751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ff3610c46e30d8afb952ca77229101670ff07b031f0081af9be71a61f790d9`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f9edc9ac84dc15c4aeb3c15f82244bce0018deaef4c21466f4176f60271d3`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 13.6 MB (13576202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a6a5ffb0b2a909ed36d16b6d5edb06ad2441db4e65f12a3e54b31a4257f002`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c4b3d6bd1e1a984ffcff35fb9de7fde05ffe9612a5162b6623b81891a7738f`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 19.9 KB (19939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860d1b0c44da61c8fcd2da1c6fc38bb05b9af25db92a95654b50e27c114639d`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264286dd6fb0223c2ba34bbb87fdf4e5aa440f4c3d17067731cb9bca46215247`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62278aa49d44686bc19ac57addb7051408b3f8f96a9c0bac6bfd453323962cba`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 3.4 MB (3408928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1f917e564db82d84dc745eae0500e384f7f9c2d45fd12f60e16ee3d46d1839`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02acb2c968dfb8ac52ce7b8662cbb28268a0fd96e4ef50caff9043ca0b2cf9ae`  
		Last Modified: Thu, 28 Aug 2025 18:58:36 GMT  
		Size: 22.0 MB (22012326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc505c4e30f42e3b5beac2880e40ba8d7b8b944a4dbc75776337249202cf66d`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55476e0a748ec2c5405f87f0d245c4d4001500fc3fd65fd2f30f09d11655116`  
		Last Modified: Thu, 28 Aug 2025 18:58:33 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:be4c5682ebe74c8b10d574e408b3180efc1b49a0f5ef73c5a8bf324c270e4d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009b9ac99100217e546d5ca08c16d765c0681cd79ad36a45c9b0b271760ee87e`

```dockerfile
```

-	Layers:
	-	`sha256:6a19c9f068b6bbc32b20552384fe0abfba21dd468ddd4063c67dd20f8d98c1aa`  
		Last Modified: Thu, 28 Aug 2025 21:12:20 GMT  
		Size: 31.6 KB (31579 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:b3187bcbc459356f4dfdba9f1d2fc57587a542f0493838fc2ba46dae5fb691a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59039044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196fe0f58ca04de2639c2baa98e93885fcb1a6b3ecf2d73e9dd6d81d2df26ede`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.24
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
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
	-	`sha256:d7afea3ff1a55cd1792a8e64481f14518dfcb576dfa3d19bf97e598dc725a314`  
		Last Modified: Tue, 05 Aug 2025 01:24:26 GMT  
		Size: 12.6 MB (12599881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce8edbb87bbd2dae7350f982fef8786dab63c95b1cdcaa6447b211ea5dd6d6`  
		Last Modified: Tue, 05 Aug 2025 01:24:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345e094929378315708a186dd96aec526fcce0b74800d7da428c1fc526a69f7c`  
		Last Modified: Tue, 05 Aug 2025 01:27:58 GMT  
		Size: 13.7 MB (13733436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67a689b009152557ab3f5e3109a568cd2181e27a9a8880e5f8424106b5647af`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e438da494fff08dd7155b6f3c5929f50cfe9230d3084485a2d94bfbb89b11ec2`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965b1a291960272c429bc9fd3e8ad7ffeda0dbceea98e9de56c1679d92ab972f`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad038c628b170712953ffd695fd9e7205f2b61a0cd789750a5a06c2f96ba4e`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bf9c8c4af43bf021ab4f388cd7d58a99b8f20d90759815ea7e8d01bb1f9c97`  
		Last Modified: Tue, 05 Aug 2025 08:11:13 GMT  
		Size: 3.3 MB (3300957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd15fbace187762e35305687e10a777933fcff9734b29d556db4d11ae1188bff`  
		Last Modified: Tue, 05 Aug 2025 08:11:27 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed6a2024642ad848af4c6a6e72d09628a62b66b21207effab8d30a8c81b363d`  
		Last Modified: Tue, 05 Aug 2025 09:12:24 GMT  
		Size: 22.0 MB (22012236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462806b34954604d94b78d5880c601ac0cd645b4ad51e1cd9ccfb2553d1755a`  
		Last Modified: Tue, 05 Aug 2025 08:11:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55929db8eb4a7a032511091e389689b8fae18de7bd2be884bf08c9abdac137b`  
		Last Modified: Tue, 05 Aug 2025 08:11:31 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:358bb9ac2fc4806795226f5208e56bc64a34fddfae42065a647a22ef936792d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1433de8a831e5e53696e781b88f528b1774e1f5612e9f5748d4bb058f26bae`

```dockerfile
```

-	Layers:
	-	`sha256:577c061970d5292083946433bc7e38604ce5c947651e09c5aab1c7a9af8f212a`  
		Last Modified: Tue, 05 Aug 2025 09:12:06 GMT  
		Size: 31.7 KB (31663 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:842cd7354957480020e167f366469a795f7240be9e7497945b931d8097119956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57488702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00198d449a58a37adc72592a6d9354e43ba4fbf830b9050e53c49d3b56c7f002`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.24
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
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
	-	`sha256:5a201b0a16aadc2a7c27ca0b373c85630463930fde99bd3c73f103ab676945d2`  
		Last Modified: Tue, 05 Aug 2025 12:57:01 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24220ce5963ab886efe9c3b3f66ba547029509a02a6800ed1f96dd054b509f70`  
		Last Modified: Tue, 05 Aug 2025 12:57:00 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f524b7a4013d49f1672e3def14da703786da1c7f1e3bfd8287705fa4b7f7d9`  
		Last Modified: Tue, 05 Aug 2025 13:51:36 GMT  
		Size: 12.8 MB (12760936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19de0d3435de422114fee898a6b066f70ee28ecfd5f589638e2dd921f1b9e2`  
		Last Modified: Tue, 05 Aug 2025 13:51:38 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e96cf40ae551ebddd54c87ea502aef0be1094aafd9756757f0938d43bc2d6`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fe0ec7d18971f49b97f267bc624a19192d37ac9a1a0211e5465c4fad6d585d`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f97d9049337329d8dd279f3212dfcc82651729e891bcffe27adcdcbebd199c`  
		Last Modified: Tue, 05 Aug 2025 13:51:37 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c27da639fe8df57b8f9dfc9f83ce270814c2b2b6a68d9af243ff3e161a0a9`  
		Last Modified: Wed, 06 Aug 2025 12:02:12 GMT  
		Size: 3.0 MB (2954471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc4d439a7a80c1b73cbeda8296283a33089042bee94eafb654f4c5ecad4939`  
		Last Modified: Wed, 06 Aug 2025 12:02:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb95b62836eefba4b42ac2203d8ef2b9d391b0b6e4603c5aa1788e22061ed9`  
		Last Modified: Wed, 06 Aug 2025 12:02:14 GMT  
		Size: 22.0 MB (22012174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4edbdd4cf12a229642030a2dd49f8e5c1e42cdb941490f927a3c835aeff3a2`  
		Last Modified: Wed, 06 Aug 2025 12:02:15 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9127dcba78ebba3635ce4ef0bfbb1b9d1b28963c452253ac8da40c1e5f01b575`  
		Last Modified: Wed, 06 Aug 2025 12:02:15 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:daa1650f2d7383c2d8488e15a5355be07ba9f67b2690a37b0bcc89f02270faa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3748678ec16ebd2b997bb41a8e18367202f2e407819180c0296196615148eeef`

```dockerfile
```

-	Layers:
	-	`sha256:c833e8669a496b1d841b856a845ea08a66a5c8f4f5513b6ab8a62d38b4650567`  
		Last Modified: Wed, 06 Aug 2025 12:11:36 GMT  
		Size: 31.7 KB (31663 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:2dd88258777ed118929449f6fcbe779689dcd384264e40b2908c50592d90bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58368135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd3b67536ae55e5411dd105c560fba3a18d8d5af5cb586f49187cbb7c6d008b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Fri, 02 May 2025 14:44:13 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 02 May 2025 14:44:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 02 May 2025 14:44:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_VERSION=8.3.24
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 02 May 2025 14:44:13 GMT
WORKDIR /var/www/html
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 02 May 2025 14:44:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 May 2025 14:44:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 02 May 2025 14:44:13 GMT
CMD ["php-fpm"]
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
ENV MATOMO_VERSION=5.3.2
# Fri, 02 May 2025 14:44:13 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 02 May 2025 14:44:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:44:13 GMT
VOLUME [/var/www/html]
# Fri, 02 May 2025 14:44:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:44:13 GMT
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
	-	`sha256:2523afe7bac87b158b525d19c04b257f3c07e08691519ce8330dd437653643c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:17 GMT  
		Size: 12.6 MB (12599878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78df3cd97ddbf126a4a6dfd5bf63960fc6ccf9adfdb9aa202edcc51b19c13c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851854bea31942fe2c53199a441ecdcdab06a3e076fe408512317e67f5b4a771`  
		Last Modified: Mon, 04 Aug 2025 23:41:14 GMT  
		Size: 13.2 MB (13210677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b8257fc0b983043ce66078653ca13abb7f9a5fc1ab5a2c0c153f5a15001dd3`  
		Last Modified: Mon, 04 Aug 2025 23:41:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3938a4241c29aafc2b6a7e97e8b4850970dd6104375af53a1e3ed200d5eec5a`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78755911dfc20b138109d2303255ac2c16fb7ded0a53fe627fc8a508dbe07e8e`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0c15c5819db3959fbf66a1cba899ae66e9869e1113c660149c00934a42fbe`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9bc5f575bfb9dc1ebec07d1f40ca57a46a704377f4e20325fbf3a5b200a93`  
		Last Modified: Tue, 05 Aug 2025 04:53:13 GMT  
		Size: 3.2 MB (3166262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886f837300b8cfc11c90fba175e5595f3783eacce7a41926daf25729f36546c`  
		Last Modified: Tue, 05 Aug 2025 04:53:14 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacbffad8286519db03e38ff21f45f4b097ea26aebf64a330dfa42334f66fbf7`  
		Last Modified: Tue, 05 Aug 2025 04:53:18 GMT  
		Size: 22.0 MB (22012217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf3802db54fa821ae7d3b1163044011c8aeae0b5ce0126b0049a48f4283d7a`  
		Last Modified: Tue, 05 Aug 2025 04:53:13 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074a134851eb4cbb16e286d508ec6e1f74ec365ffbe1cef0dd9e449b06c64fd5`  
		Last Modified: Tue, 05 Aug 2025 04:53:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:5531cd051b8cea29b4a7f98abab59bc8baf3745565484053879c38f8743631c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9fa26936dca607f586dc3f98a710e893304de7990dbd5b56e90f514033dfb7`

```dockerfile
```

-	Layers:
	-	`sha256:597f31aed6cc0f38e081302b99ef0faa002afb32f4e9dcb6df94b2c1477e8dae`  
		Last Modified: Tue, 05 Aug 2025 06:12:13 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json
