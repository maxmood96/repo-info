## `matomo:fpm-alpine`

```console
$ docker pull matomo@sha256:d2dad785df9df45d16ee09f1e86daf78f3e5675e3d3bc23c3c9a2f5f13294078
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
$ docker pull matomo@sha256:19496d7c56633994397d2d4b4b30df8c816d5c1af80c0d1edc39ce601f1697c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61117406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d6e75f344f62321a56a403d30c696217d87b520adf3a4f74715c4777a391a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.23
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef952cbf360f9accebc7c2beaa1888046fd2decdb103e9cb37ca7fe8901e8448`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 5.9 MB (5944405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb247df7bed499a5b20b7a8f5275f005942ae29ff269444f08485852b0a82ba`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896673d396d677374e76584f6148d05009f4bf9cb800ff16ece4e2b1cf7f785`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b045c0c09a16557279905f885315501ebc707dad24429e3f76c4ba889eaea8`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 12.6 MB (12599155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c8125335db3c68c8f6abc01bbf84258e57476bb185eff879d4c1a3466b8eb`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d7dbac9207c1e11b7b23ce6aad0740e3ba427719588e966776cc44421a861`  
		Last Modified: Thu, 03 Jul 2025 23:05:44 GMT  
		Size: 13.3 MB (13261724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac6221624b83e2f407497538d9cda65f3c6bb6028088b26532eb138997df78`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80922a9956d152b4e0a3bc8fd473151f805337d5823f8bd37b68e79cdb206f7e`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26906d4e70978b9475681f326ed2a302b23ae885e81ae8770bb41a1c51135f3c`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4226ad16511c854708eeb106b22f950a04e5db658db5aee0703cfdc687c5a9dd`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adaaa886a64c1e75fd8812c5455d463ce03a2d495271480d8dc801fa2ebacaf`  
		Last Modified: Thu, 03 Jul 2025 23:16:45 GMT  
		Size: 3.4 MB (3447156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b9b4043f9cd038180e0cc5063e41c2b66c5429a3bb3212584717d2b55e0239`  
		Last Modified: Thu, 03 Jul 2025 23:16:44 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5119b0de129efd7317b67efe7160d5ad9fec9d5641803254c852b16db574fe`  
		Last Modified: Thu, 03 Jul 2025 23:16:52 GMT  
		Size: 22.0 MB (22012932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb905f9e012f8b36b5061e608bf0774feb4e5a2376bb64ca36876e615781e022`  
		Last Modified: Thu, 03 Jul 2025 23:16:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c42b71238131c809170a62acd3b0a8e69fea4c267d2ccfd1330fa3d8122079c`  
		Last Modified: Thu, 03 Jul 2025 23:16:47 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:fa0e82376e9759414c544e23886835aa803d951499a7d2927b9885832b58f987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54851007a2e44a0cb5cabd2ae123cfcf57f49c7e4f8ffac7fb6f6a480c41f88`

```dockerfile
```

-	Layers:
	-	`sha256:40c239fca12e930f6c305619968cc19023786ce6dda13c43282d6efadd6465b5`  
		Last Modified: Fri, 04 Jul 2025 03:12:05 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:5d2006bd645cf8bbf5feb2a95ef3d9ed42f52f55727e4b1c5892e303a55c62b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59649244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2a3b91ec52cb265251498e4936aa114d363d32f0a9515453581136045922c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.23
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146672ba2c374cbf86842c858594d7c0b44ab2080ad5e2ec35b1d430d956546`  
		Last Modified: Thu, 03 Jul 2025 23:34:21 GMT  
		Size: 12.6 MB (12599121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb5f1af16a6958fa9af152ac28632aff56dd315585de1020a729fb999c3dee`  
		Last Modified: Thu, 03 Jul 2025 23:34:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d236cf740ccc769ceb4ead8aa9d45e86ed16335a52d930c4fe0a9c0557f9f`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 15.1 MB (15107434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14679d7fe0b4602f2402b4899b623f618df96d2ba33280d5cf4a4afc825bb7`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7a906289e5476e4a4fbca6e72f2a28c1274a886810de274c3d9d075537bdba`  
		Last Modified: Thu, 03 Jul 2025 23:39:43 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab072a5208326c03096cd254e9205b7fd25f2fe20d9e8723ba9f85b55faab72`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a3d59f66b3f5f865439aa342092b634c80b67cc2b0976838e9806ffba9bd8`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e71dfd63076134c38f2e85f4bd037f1017e5ffa56024d652ec572b5ebddf87d`  
		Last Modified: Fri, 04 Jul 2025 01:19:36 GMT  
		Size: 2.9 MB (2942098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b21db52706ab73abdf02dd40b1d67defe9384e5a3d6c9d0911923eaa9c555ab`  
		Last Modified: Fri, 04 Jul 2025 01:19:35 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d7f73dc54893b2cb56b31c7d80c4c889817b4d49a078c2ec5a2bc6fad0213`  
		Last Modified: Fri, 04 Jul 2025 01:19:39 GMT  
		Size: 22.0 MB (22012408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b153a4b044855ff5e9467ace0fba3fb9a53f72ddf5f3cd027df968f8e0c29f58`  
		Last Modified: Fri, 04 Jul 2025 01:19:35 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08a4861489e196e43269658f3e0f616d164c72c154d536db60ea8ece515ec9f`  
		Last Modified: Thu, 26 Jun 2025 00:12:31 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:73759678fd1a8abca0325a72fc05421d836cfd30a31565c73e2bdceca3714a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238c78fe636d9d88d3ec6e80d12f9fb00074ad102fb6e0d51902090b43c1696a`

```dockerfile
```

-	Layers:
	-	`sha256:471aec6277b13eeb3a4b0a236a59bd650c5bf586ef2a332b592932b3987c1ad8`  
		Last Modified: Fri, 04 Jul 2025 03:12:08 GMT  
		Size: 31.7 KB (31717 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:808708178b65214ff7b617d42d9d6b1692bee4d04ad7120fa7a3a565b310c434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55178051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d170be013323cc6161b16079fbbe86831454fd94d3f1c7da7d4656cfffc6df4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.22
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4283ac42685038a3ed46bf05fa54ab4bfdaa975c17e26e357143c8c0323ea7`  
		Last Modified: Wed, 11 Jun 2025 11:58:48 GMT  
		Size: 12.6 MB (12576225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741687b0c9e57be621e022c7972e29e049714b0076fb944fa8713a06d0bb1bab`  
		Last Modified: Wed, 11 Jun 2025 11:58:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08a3c676bee3ca3ea309b1b4da6db64f4e2308209926dbbd58055cba3c9cbcc`  
		Last Modified: Wed, 11 Jun 2025 14:30:57 GMT  
		Size: 11.3 MB (11284618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750dcf648e107457b9a560f1e14bacdb7a2959046bd0799322aa97386f1dc9ef`  
		Last Modified: Wed, 25 Jun 2025 19:56:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c267638649633cbfe708a73684e4a36ae94f702cb8ad8948ff80276c8a4b572`  
		Last Modified: Wed, 25 Jun 2025 19:56:07 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442abdebdef4ffbb9c008461435cf8f0e2f881a6e839a6024f9bc7e5b3cd249`  
		Last Modified: Wed, 25 Jun 2025 19:56:08 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3debdf6b7e87b559834fec59c59a828abaf3f466c64207241acce9e1b3213ef9`  
		Last Modified: Wed, 25 Jun 2025 19:56:08 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb966334cee4fe83887a7432ca1e023150b34fb1bd151e50e76c127dcc15ccf`  
		Last Modified: Wed, 25 Jun 2025 22:55:16 GMT  
		Size: 2.8 MB (2783356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637a013bafa813b159c712cf69b7d7ecca012135cfb8dc481afe8facaa49858`  
		Last Modified: Wed, 25 Jun 2025 22:55:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4f305160d1b95a5876930a97721c95b52952ff7419b2cc4fb720017eeaf0ab`  
		Last Modified: Wed, 25 Jun 2025 22:55:11 GMT  
		Size: 22.0 MB (22012415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877159093ced9d98704948a911f0fac38eacdca22ef9dac738f5b85ac943dcc6`  
		Last Modified: Wed, 25 Jun 2025 22:55:09 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922f8bc1249db5cec2f73e7bc17940fb0b6f6d63f21f576af26adcf3d3aed663`  
		Last Modified: Wed, 25 Jun 2025 22:55:08 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:35df29edfdd45db8e5a7ddf93a45aedd7820cdcf7a289e8ba3a1ecd9866b2bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7cc10b2d974d3569ab56ee8c1bcb8cacdc5f9f99f58c0c34393add4f63170f`

```dockerfile
```

-	Layers:
	-	`sha256:69bbee4f082a50757351724569edf1f2fa11b4f1a9e86d6b5c2a32130b5fff49`  
		Last Modified: Thu, 26 Jun 2025 00:12:13 GMT  
		Size: 31.7 KB (31717 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:534e53de1529ce8520b0eaa4b8fa3280dbb08a641bab7260fc5224ef717f8fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9982e5edb15a65b6f4f1f772a0a6cfe6cfb08f31725c4d036deb7b2cb6120b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.22
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f789f409ce4125f1a91d782d4ba7029d14c9bc9e8a763ce540561e0c590d1c`  
		Last Modified: Wed, 25 Jun 2025 23:20:03 GMT  
		Size: 12.6 MB (12576225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953f352e5d9d7dc9addebe83956293c660d06b117a627847bb29b0e86a8efd7`  
		Last Modified: Wed, 25 Jun 2025 21:12:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca589e404c8267c7247c67d85ef9409eae1da10206a097f95e3228eb95cd6c`  
		Last Modified: Wed, 25 Jun 2025 23:20:06 GMT  
		Size: 13.2 MB (13247766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff6b6a65e4ea826c69c5319edf00ba8f04caeac7112de7ea7de6338edf89a20`  
		Last Modified: Wed, 25 Jun 2025 23:20:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d1410c5df8e205023ebca7317b27565ef46a8ccf8de1b4021e6f49cb70005`  
		Last Modified: Wed, 25 Jun 2025 23:20:06 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14f20c0cb1d31e3d9f398b8e607d6894ab6b39ba5fee62d7339ec4e6a3f837`  
		Last Modified: Wed, 25 Jun 2025 23:20:02 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d77859ca8607d5824115711e5dac51e877fd2d576e9f152803d4b6f2ff9a604`  
		Last Modified: Wed, 25 Jun 2025 23:20:02 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128301204bf5d68d0b9a4e79ac08424e0718a8d70a00f4fcf27e406b43656049`  
		Last Modified: Thu, 26 Jun 2025 02:14:24 GMT  
		Size: 3.8 MB (3758275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100a634091e800cbad7f0aa0c34af09a7fb3e7418cee4e420a7ed4917b30a4e`  
		Last Modified: Thu, 26 Jun 2025 02:14:24 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641111c9d56557d4410b0c8997efc8912089e77e208276c5d510fdb79c0ad33b`  
		Last Modified: Thu, 26 Jun 2025 02:14:31 GMT  
		Size: 22.0 MB (22012403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c39b4d6339bb411ce215636e284d1d46b6aae3be6532679ac5cede18eb055`  
		Last Modified: Thu, 26 Jun 2025 02:14:23 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c11e4f1df94cb9101ec021c7991ce428fd395d72bf5a874e7d246cbd2b33954`  
		Last Modified: Thu, 26 Jun 2025 02:14:24 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:9e99561ad0caa2f5b6b20372deda9699a92954672b9414c49c13bf5c491ba18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baf45fe2ddd14750e4f7f0d3abc2f2b11793402cd082122f6af258f78e23b2c`

```dockerfile
```

-	Layers:
	-	`sha256:56f7f49e898882175e5b83b9a8491774ce69658fac21219814202ab89a1e1aae`  
		Last Modified: Thu, 26 Jun 2025 03:12:03 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:edf875efd036b1c7df0e81b79abd0876ca85113293e060813aca2ae7733db767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b601297cd17baf79e5557b6af84029516d517b67ac47417c13cf8f7817a1c586`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.23
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807332f552a5d43d50bf321942aaff6f62a51ea718c4bc5c92889c7da5518cc`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5952ed3b34bc2bb95e5d92041b0d1e2f1102370e20445fde4e6ae170753fd54f`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26cd4edff9c58bc8c1207c850646d9dfdfc9668c692e2b02ccedbcd463e458`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b172088b57748f502c5aa1cb684e21421b0497fea01813cd1a37fc90acd2`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 12.6 MB (12599126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0cd325f2b5b783c7b8a674f750116f3312bd602ddc978c5b9f679705430ed`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a1d58746e581f9623e1af350bf3217a46d1bf2421a049c667ce7611ed9234`  
		Last Modified: Thu, 03 Jul 2025 23:05:47 GMT  
		Size: 13.6 MB (13572591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86069b8c031ffbd54f99dcbf2ae53e9e0957fc9842ceeaa4a5c8036b2f82643`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef072b2e721a30c9933cc7e4efd20c954bbd7be2cf4635995276b751a09425`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b7b0119a26af8eff640f542e3e4ca243bddb6c7bffcb62f9018e53e27a28d`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bce8958e293647dbc8485a223c57de84e18b7d627799a89f7217e466b8dc86`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c74ea3f078e504a119df6d1a7b20e279c0ffd3b3ffbc0ff95b7d214591ecd`  
		Last Modified: Thu, 03 Jul 2025 23:16:13 GMT  
		Size: 3.4 MB (3408543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177562b8f0c1b3d1ddd731a5a2f78a3642b89f09660362010b9661b1396b72f`  
		Last Modified: Thu, 03 Jul 2025 23:16:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa7bf06d0104a02b0907c1ecf94ee21bc960d86b7a68010c09fb6dfd9ede926`  
		Last Modified: Thu, 03 Jul 2025 23:16:15 GMT  
		Size: 22.0 MB (22012914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e3eb3630291afac005a7e8cc1eef6213de5190daeca0b3d74f72b0f14015e`  
		Last Modified: Thu, 03 Jul 2025 23:16:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00eaee3e8527c6ba69cf8496621c730ecc3be4a1423f284ea305000da1fb7ac`  
		Last Modified: Thu, 03 Jul 2025 23:15:42 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:8ce3b4d26f29e74328bcdc446319d77ba8521c57fa33f27272bf17d787971b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8a65a30e74d94a92cac477fd361843fce46560c09b422dc36ce25e4127469e`

```dockerfile
```

-	Layers:
	-	`sha256:aaa418f0c9c3aa9ba0d400b19e9f15bac1e3de015173ceda9652918a754eaa31`  
		Last Modified: Fri, 04 Jul 2025 03:12:17 GMT  
		Size: 31.6 KB (31579 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:27bd8726243db100c29e49f7626c7d510e25a375303eee32277933ffaade4b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59025521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde0426f382b9b7a2a47ee0e066c2a34d840b977ed9a59896bf70d22a1ffd9a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.22
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e98527d27dfe373bb05fe4a32feae4e983c3ea61c6e75a47cd18dbaa9f06e4c`  
		Last Modified: Wed, 11 Jun 2025 09:28:04 GMT  
		Size: 12.6 MB (12576214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb3390ac49f9efbf6d20912051491cbccf67620aecd18d32594e6dd87b74ba`  
		Last Modified: Wed, 11 Jun 2025 09:28:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce87323c305e4286779fea7b441f7613b7dc467b41fd24af74fcdd8fc2c824b4`  
		Last Modified: Wed, 25 Jun 2025 20:09:53 GMT  
		Size: 13.7 MB (13731605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2bcb039af49f83cbbf32234fa782035fc17cda0d0402978c1de0233a84ca5e`  
		Last Modified: Wed, 25 Jun 2025 20:09:52 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff9616b48bf54f4e15be8bdf26f6943f649ea6d28440743755e25e0ec10a56e`  
		Last Modified: Wed, 25 Jun 2025 20:09:52 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4734876393bf36e9b859764ea4a55edb5371fd61a9ea8126199bc8ffdd7ee58f`  
		Last Modified: Wed, 25 Jun 2025 20:09:52 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc3ce8761b0f5f26e4e0bc848516c37129654f6be8fef9707e93e794aef6a24`  
		Last Modified: Wed, 25 Jun 2025 20:09:52 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5b52e17392e5e8abb6c73b4cf1d121c5cdd5d0bee9607db870fb962adfc356`  
		Last Modified: Thu, 26 Jun 2025 00:55:03 GMT  
		Size: 3.3 MB (3301150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3dc1596158d9fefc16b8420a285fcc6c1b11b5831c52a69692d49828a2f712`  
		Last Modified: Thu, 26 Jun 2025 00:55:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5374aff965882eab8179ffb6a16aabad3ebf827dd25053dc360117393b3f604`  
		Last Modified: Thu, 26 Jun 2025 03:12:25 GMT  
		Size: 22.0 MB (22012422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9e6fc0ac6b9e7f82408386ca9898532c3a52ba2742b9b64df391ed54481b46`  
		Last Modified: Thu, 26 Jun 2025 00:55:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da918cbbd5bd378dcff5f60760db73668defccca3757ff7158f627de65bcf8e`  
		Last Modified: Thu, 26 Jun 2025 00:55:16 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:9ee084a420e257eb09909c7d594b8169fdfc26b760822a820bf4828329a97971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24121ede58d826d85d3d740d0ebde1de71f303e39b1d22c2ded8a799cc67e669`

```dockerfile
```

-	Layers:
	-	`sha256:6b8700572adb1348653283e7aa8ead300b13e63727dd32cb442448bff21e6383`  
		Last Modified: Thu, 26 Jun 2025 03:12:09 GMT  
		Size: 31.7 KB (31663 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:df1894b2d8511fb204eafa3306653ce5553427bc8d7d23196a3bc39a9160a09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57473960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5a2ac8c81b1ff0e4286e860ae0abc70e13a2ea0290da2fa4bcb145320ba55c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.22
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5cafa4d9818b0979221ee32a634774fa7f630af34e28dcd203e49994f474f`  
		Last Modified: Wed, 11 Jun 2025 08:15:56 GMT  
		Size: 12.6 MB (12576232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27333500b47fd459f2d6ae7fe8c9965e6a2e171e3413cd3721da70944d32400f`  
		Last Modified: Wed, 11 Jun 2025 05:27:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94ea32cb34db450a708bccf88f34888f12a69e81197c5e562becd545f55c0e`  
		Last Modified: Wed, 11 Jun 2025 08:16:04 GMT  
		Size: 12.8 MB (12758742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5d92b246a6d60b990cacf09bb2fcc12451ac7c1b17f7396ba16c682667c7f`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91e11dba2e3d8f6f7071f2936da54d2416010d1a7ee5417246d3253bf6623e1`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8195a02efbcbc128ec081a88ee47bec8eef940c0795b5cbc4df768899a7937`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a159d59982da6923f201118958fe2300484b8b87fc234f3931bd53e5ada97eb`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a66ec172a8718a830d4ead70501c00ee1c2f296c3880e0aa170edaa155a9ba5`  
		Last Modified: Thu, 26 Jun 2025 11:53:36 GMT  
		Size: 3.0 MB (2954601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507a1dc5a212e66e442e376a80c57a4dee4ed45b1880949e17e9cda958eae281`  
		Last Modified: Thu, 26 Jun 2025 11:53:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d8c35318eb301a5519b3dd07c19232063a3ed5accb4b6db8b093680444ef16`  
		Last Modified: Thu, 26 Jun 2025 11:53:39 GMT  
		Size: 22.0 MB (22012404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4dfa61b750b241777c450e799b9212c786815e749b91da258fa8125a3048b`  
		Last Modified: Thu, 26 Jun 2025 11:53:37 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4991cd16d834622ea49340ba80be1193844cdfc275153b16cb96dc2f545b3`  
		Last Modified: Thu, 26 Jun 2025 11:53:37 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:5d551354513932bcb943f9515baf96768e3cfe03ffb3e6af89cb96eaacad5cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a83152dba3e959a18fe94dcef1cacfee1ddb39834165a6dca0a6e16b6ab8d1`

```dockerfile
```

-	Layers:
	-	`sha256:30e8c14da5f14d46a27089b26eafd05c893b655b22ad29ac0734064679e40be8`  
		Last Modified: Thu, 26 Jun 2025 12:11:36 GMT  
		Size: 31.7 KB (31662 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:14a89e1031ca0b4682f3e9ed54f81e2bf770ba7b06aafeb54512c8002000a466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58366210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77626b4ee929be950e253caeee163839e2840f47195aa98facbd278182c0fd11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 02 May 2025 14:44:13 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.3.22
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 02 May 2025 14:44:13 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 02 May 2025 14:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c50b23d2f6267cb43b11b038938247a74fe9e643b50e59fdbb4b5a4b6fe7861`  
		Last Modified: Fri, 20 Jun 2025 19:20:52 GMT  
		Size: 3.7 MB (3699029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d657aded1e5f64f14aeb2f0fb46bb5042326900e94f375c02676e1df16f2c0`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773155ae64957d9bd56f77026e1934533d4df47e0e44a57e52cc2ecc33f78584`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86366961de2d70cd0757b39be313f008b2e111be75086aa5010426cd572913`  
		Last Modified: Thu, 26 Jun 2025 00:35:38 GMT  
		Size: 12.6 MB (12576231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96083f5aaa96c40fdb9af86bdf965d677e33ee4358affb81bea7831776a2507`  
		Last Modified: Thu, 26 Jun 2025 00:35:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4fa3d7b3999ac0d1a763c3e6183bc1f48ac0c808ca3102797cbe63694aac5f`  
		Last Modified: Thu, 26 Jun 2025 02:27:24 GMT  
		Size: 13.2 MB (13209705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7212d6b1c568f79c31527c5d00f96c0752fcbf0bd9b13fb825c8f9ccfc667e`  
		Last Modified: Thu, 26 Jun 2025 02:27:19 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76747318c532a1f3e7e70630500d792c58ce6d5b49d21bac1e77d89589b57e19`  
		Last Modified: Thu, 26 Jun 2025 02:27:18 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa6f0b5f33c5d44c293bd0d777d4a791d9b7efe9d73889f585a47b9d0c4316`  
		Last Modified: Thu, 26 Jun 2025 02:27:18 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659b635aa513fa85af2cf20be51f5f5caa16ee5f2d935645be5268918c25f036`  
		Last Modified: Thu, 26 Jun 2025 02:27:16 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6bae4395cf1a9315200ff405469fd8d24a799faeb43c83e63ed8e9c374a513`  
		Last Modified: Thu, 26 Jun 2025 04:30:09 GMT  
		Size: 3.2 MB (3166502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8022772f690e954d4857910ff926ba90f948a977c788666ca322cbdbca74ad6`  
		Last Modified: Thu, 26 Jun 2025 04:30:09 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6881ed812878d334797b56f4ed9041627edf7f82064f39ef9a89af35ecdbadc4`  
		Last Modified: Thu, 26 Jun 2025 04:30:11 GMT  
		Size: 22.0 MB (22012423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb165f38107471660b14fc8c9761151029638cc0343ec2be169491481f4a906d`  
		Last Modified: Thu, 26 Jun 2025 04:30:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bca01c4c27a669decd6fae7fb03cce0e711e3a2b0241a475f2d4f0eaf6cb346`  
		Last Modified: Thu, 26 Jun 2025 04:30:09 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:ba56cca5fd4010926290c0ef77cd1bea34e82a82c83c5aea358378bb908b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbad071df8277c03b86d86ed4a1f62db67ac681ed9e6f58ab4768c7400db8d20`

```dockerfile
```

-	Layers:
	-	`sha256:75f5ae5d3f88152941afc4993087265d190ac048c54992a2366f2abc8ad0c65b`  
		Last Modified: Thu, 26 Jun 2025 06:11:51 GMT  
		Size: 31.6 KB (31615 bytes)  
		MIME: application/vnd.in-toto+json
