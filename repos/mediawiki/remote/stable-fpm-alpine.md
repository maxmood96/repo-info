## `mediawiki:stable-fpm-alpine`

```console
$ docker pull mediawiki@sha256:f17a2af090b71ff4960e6e2d067f04d69608769fabf9b9b247109288909ec248
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `mediawiki:stable-fpm-alpine` - linux; amd64

```console
$ docker pull mediawiki@sha256:ac0f199ba21c6b81ffe905685a6375177a1f1c077cd2328112086442395245b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150268610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8281de8eb48522b20fc26d271127c122d2f702d39419b277c510e55e5282d06c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a73e68ff7768f6e915d93f497ff30d2304385bfbc45127635b8c6114a22`  
		Last Modified: Tue, 07 Jan 2025 03:33:41 GMT  
		Size: 3.3 MB (3319680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2799f6a8e8ac70de966998118844e393ec11b5df494626ff35160bb0e5969e6`  
		Last Modified: Tue, 07 Jan 2025 03:33:41 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9590f58dabbc32fc462d1292c7d4a09c535d6a7d5850f7d72bc15c108b35206`  
		Last Modified: Tue, 07 Jan 2025 03:33:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc882e91c7248b0ff0e68af3495b9127a73e83b81b10d2144bc873fc37a63fd7`  
		Last Modified: Tue, 07 Jan 2025 03:33:41 GMT  
		Size: 11.9 MB (11937928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e826e275b7320de036fe05a2558f925970ed1a397a28d00dbd715ab2aabcf2dd`  
		Last Modified: Tue, 07 Jan 2025 03:33:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f5a5b7f2f8986c981c73ee7f9fb9bd7c343ebbdc10988a35df1db2c687900`  
		Last Modified: Tue, 07 Jan 2025 03:33:42 GMT  
		Size: 12.7 MB (12699878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba32181e2bf0c363049cf31cd7fd14767cbd12b0a904d340523816ee834ebb3`  
		Last Modified: Tue, 07 Jan 2025 03:33:42 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cbc2ea7dafecf4adab6aa1fab33f58d97758bc860d02cc510305fd3558173b`  
		Size: 19.8 KB (19753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c56ceff4e77f193ff295197972cd84467d6bf8292c11493be0c859e00a61a4`  
		Last Modified: Tue, 07 Jan 2025 03:33:42 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9165390361b441f77871a5025196ff7e6b3838a13b89d3bd7db809f345a6eb4e`  
		Last Modified: Tue, 07 Jan 2025 04:21:44 GMT  
		Size: 23.4 MB (23387815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf69b9d25f19f807297857ddae4830a7161f5b001ce490b788ec610e0df012b`  
		Last Modified: Tue, 07 Jan 2025 04:21:43 GMT  
		Size: 4.8 MB (4840981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8657df389c223eeb26b7d529f78f86eb638867dec114259fb905c55efeaa1f`  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ce40a5a9a937bbaa7b178e6d79f12724c7b0ad268e446ae0ffb3e6e879eeff`  
		Last Modified: Tue, 07 Jan 2025 04:21:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c60572e75a48cd158afd6f5b9ee6573d2d7f411283eca86c5304ec6f1bf15`  
		Last Modified: Tue, 07 Jan 2025 04:21:46 GMT  
		Size: 90.4 MB (90412898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:70d89a96a007eebb09bcb6413316ff2d7eef4ec8cfc4a4784881eccab006478a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 KB (32076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a970426c81a91dd3412e4bbd15d4561866553b862d641f7d6d0388c243de0c5`

```dockerfile
```

-	Layers:
	-	`sha256:635b9b558092b401be27a93c9f98923c7fdd7c1969c74ffeb6f081dec536180f`  
		Last Modified: Tue, 07 Jan 2025 04:21:42 GMT  
		Size: 32.1 KB (32076 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm variant v6

```console
$ docker pull mediawiki@sha256:2c682a4d6680ffedbad66e13f07372107781d66b616cf1c2bd9946562d068a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147418050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e08385a49c06353bd01946b89c09a6449be53f39490e58b65f20fe421fda30`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bef010c611114840926e80cb28932ac752a42db1830688c08b53e3b0479b57`  
		Last Modified: Tue, 07 Jan 2025 04:04:46 GMT  
		Size: 3.3 MB (3288904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6270f8fc8d436fea30c28e682f01c03d0fc9e3ad4d478dd522e49204e509af1`  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d76c367f31c843767d908ec20d1f4689fd733c923fd9605738b522084ac5a`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e1913c1a3367199609013fc68d88296462607203a84bb86d7eba7ceea5995`  
		Last Modified: Tue, 07 Jan 2025 06:04:16 GMT  
		Size: 11.9 MB (11937927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636cedbb7e2965fd15eb9343b1ae3bb07fa68fee5ac45f64fb9f6975d506b2d`  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9502a1240c8acdcf452b7893141032b5a3f3bb3855860d2959ffce2fe42138f`  
		Last Modified: Tue, 07 Jan 2025 06:07:57 GMT  
		Size: 11.4 MB (11436427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5de3975e1f7746c1a65a6e867c5534a5ff50cf40e983a806bdc254718f6b82f`  
		Last Modified: Tue, 07 Jan 2025 06:07:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372efbf4cd25ba85b2af3d60087056f5e167e0a3e7c1b4b4a99ef4cd279da6ce`  
		Last Modified: Tue, 07 Jan 2025 06:07:57 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd176418bbd83cddd3a39c8176244f2a255ff4658a90f594391658ab2a76eb1a`  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe08cd86728ffba1f98a75bfede82ac780165301412622e290337c88e6c31a1`  
		Last Modified: Tue, 07 Jan 2025 19:03:04 GMT  
		Size: 22.6 MB (22646199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902bbb2068848eff623837bf0aa9e37243ee89113b84945c402cc6c0aa46d854`  
		Last Modified: Tue, 07 Jan 2025 19:03:04 GMT  
		Size: 4.3 MB (4301861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2d21ca5ff81c9d393b60093a5447b2b70ef4b4d3937ccdea388c32d1be337a`  
		Last Modified: Tue, 07 Jan 2025 19:03:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b547961b28ee06df1787410634e2e84cf7b4e3ef656b6b1a844c270886dd9033`  
		Last Modified: Tue, 07 Jan 2025 19:03:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a462ba1a821c11c1f411f56a579ca2c8764cf389e5436a20da4ecf9d121814e`  
		Last Modified: Tue, 07 Jan 2025 19:03:07 GMT  
		Size: 90.4 MB (90412679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:e5a7ccc17260d6dd3961c0795330f0223a999a2764cb9b51062e5be2089e0ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615aff71fdf5a7f539225ac7173596e03d47a5ba7e3fdffe2fb08e74df5964a3`

```dockerfile
```

-	Layers:
	-	`sha256:34ad465c1232fd291dc561dd81a0a07576b739bc02bcc5f93331a44cb411d4f7`  
		Last Modified: Tue, 07 Jan 2025 19:03:03 GMT  
		Size: 32.2 KB (32196 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:c390347668de192921c354db7d1eee7161f17b7752b40cfe1dfb5ab0fa0c9373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145328819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1421faa0813c7f30fc4bf7d88e75f6f3b7696a85237b1e720fa29d468d40ccc4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a46a05ef2f8f5dc8f91bb48ccb26f8769e182e5d38d1a1d557e82d060b4ec5`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 3.1 MB (3097878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0ae4122e18dac51504a788ad60f49ca9ac0b06ecc7c0df42385e05efeb7e30`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90539fb79bdae2b2ecda3212490766029854e00ebfa8dd5d8618634d5b8b789b`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34d49e7ed227b175af99a5de5a8c0ce0a96c8b35707880f240a7b51eaff332`  
		Size: 11.9 MB (11937926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182e3fdffc86e300815065acbf92bca4912c239a141f6191b950f65afccaf0c`  
		Last Modified: Tue, 07 Jan 2025 05:47:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c360b46f297176891a0519b25a10d42d06a5ca548b2008ece6d6c431cb0bde1e`  
		Last Modified: Tue, 07 Jan 2025 05:51:33 GMT  
		Size: 10.8 MB (10774453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9443ecb3ab8aa3641e5d8db98101d24205e680a6f7ce3314ee032f72a45d5d`  
		Last Modified: Tue, 07 Jan 2025 05:51:33 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aa1e476fa7b0c85051ccab7dc943825087bcd07e5d76310923021db6427ce8`  
		Last Modified: Tue, 07 Jan 2025 05:51:33 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13614f6576ef14198754f091ca4b0fa8f348fcc26909abbc41998db29f7c535e`  
		Last Modified: Tue, 07 Jan 2025 05:51:33 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5065f1485c5f6275d44c2a69df62a3a94eb0f8820ca00ccec1886dc0ab18e`  
		Last Modified: Tue, 07 Jan 2025 19:15:35 GMT  
		Size: 21.6 MB (21616965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b101ffd75bbd751c94435b3f48113323bcab50e7bba494130d8350232ea1b8`  
		Last Modified: Tue, 07 Jan 2025 19:15:35 GMT  
		Size: 4.4 MB (4361825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e07ff1067112a154190d23e15e378921a6956a5e63c5cf85a204bfd203e7d5`  
		Last Modified: Tue, 07 Jan 2025 19:15:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4780e543a7c870f1f184235845ddaf062a1b2fd843c112c1c425a6c5edaccf`  
		Last Modified: Tue, 07 Jan 2025 19:15:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11fb0454ca7a4e17aaa9bb918e2f70154021f23a40695394ec9c72d52580748`  
		Last Modified: Tue, 07 Jan 2025 19:15:38 GMT  
		Size: 90.4 MB (90413504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:7ecc018f27cb3db60c340a4d362f7debc6a97e40e5e1f4071a38f690ea5828bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6a04a0ff4a8cde7b4b11461fbd7c64494efa255044641906f478345332340f`

```dockerfile
```

-	Layers:
	-	`sha256:9ed4e78dc42c7aa0ddb5091054f7a3fdd703b729fa4456e610f3572f9fe9c587`  
		Last Modified: Tue, 07 Jan 2025 19:15:34 GMT  
		Size: 32.2 KB (32194 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:dbf71aeb8833ac2cac9bb46d48806f052be730212315288c7c63733788e60c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150650687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a69bdd09e1b43390107d98d93a9da46d2cb13991b5adcb3ccc2c16fff5dab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40162970ab5d274af508499ec972de793b17d5f14ffee01a11a8e5a5256724`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 3.3 MB (3315021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8949964140eb86d4055cf8d682a19190f4519a76a0135d9c0635b8e590a12`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc0ab84d61c5b652f4966a78d4064b20a3ee74b683b2fff8a31bfa6695fd46`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f4177f3aa12ce8283ea80c3cf2179210acd3ec15247cc5cf485e1dad3eee88`  
		Last Modified: Tue, 07 Jan 2025 06:35:33 GMT  
		Size: 11.9 MB (11937931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9440a0c20152419dbb0384eab44fa748d04520f6bf1d464a3584c5dbb7be8d6b`  
		Last Modified: Tue, 07 Jan 2025 06:35:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6999e333ebf87cced143819cc28b3d5636172cd026ec3453d5cf58100cbdb8c0`  
		Last Modified: Tue, 07 Jan 2025 06:40:19 GMT  
		Size: 12.7 MB (12689733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3797fdcdb5ebba90ec07d941f55012132afd36677a6ba862da60a7da0ca5c9b`  
		Last Modified: Tue, 07 Jan 2025 06:40:18 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be5f3edff73c8d90d06d9b07cdc65665f000e8f3a48c22e9d37665f5415ed9`  
		Last Modified: Tue, 07 Jan 2025 06:40:19 GMT  
		Size: 19.6 KB (19554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aaecb8ad30ad05e768bb3c4cf6f4da62144b4e328858de97ba523804276c7`  
		Last Modified: Tue, 07 Jan 2025 06:40:19 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cb04db8e5cbffb4644d761ef51a8a2099ea68b6780dd65ab29f1d7fb02f22b`  
		Last Modified: Tue, 07 Jan 2025 16:57:17 GMT  
		Size: 23.2 MB (23165995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997f30976760e9dac773f9ebcff52ff8e1818d63ba29c96c0b870e22665ef04`  
		Last Modified: Tue, 07 Jan 2025 16:57:16 GMT  
		Size: 5.1 MB (5113089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475fa046782aa050b0e79df50a4a01da22ca76f6b819d102d8c4b08053a61eaf`  
		Last Modified: Tue, 07 Jan 2025 16:57:16 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c274638957a15744fe1a8c0f8cdd7e9c8a37671540054d92cf3b4a36dd6aa759`  
		Last Modified: Tue, 07 Jan 2025 16:57:16 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954d45463fa7bd0ef6b7a123b49b6edd625ff22e6bf4d869a0ac88f18a9e20c`  
		Size: 90.4 MB (90412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:22260814814ebef2cf38fc06cef27b71e603353e4c5ba246f4de32551ab57db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149745b63a974e412d0ab095f85daa69bee6585965ca24b2e754f7e4fd0eb8ee`

```dockerfile
```

-	Layers:
	-	`sha256:b0c0bed7306a36e7a845f2d4eb210c21d4d305bf1371696f3e56970b955d08d2`  
		Last Modified: Tue, 07 Jan 2025 16:57:15 GMT  
		Size: 32.2 KB (32228 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; 386

```console
$ docker pull mediawiki@sha256:9441b193953671486bcf15d21f3cfda2ce143bba7c21af4abcab0f548922c518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150978902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4357abf8230e27a5d63fc1c9f2ead58ec0166fb7d8a14d422540613c16aeb6b8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7543ebf1e616e7cb03f0f1221404748fa56b97579416f6039f5f69cee92a4b`  
		Last Modified: Tue, 07 Jan 2025 03:30:22 GMT  
		Size: 3.4 MB (3357012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab81f820746395d31cf04b56f837bae07305f6e37ec13b752fa38786550a43`  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b3e87e456e672054eefe2fdecbb32ef3535161bd695680b9d05f6eb94e0498`  
		Last Modified: Tue, 07 Jan 2025 03:30:22 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f45dbc3d1f606b6861d36c6fb6c92c7551a0c644bee6b5314f24cfaf5d261a9`  
		Last Modified: Tue, 07 Jan 2025 03:30:22 GMT  
		Size: 11.9 MB (11937918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52d474f1e10acf7d765d8ad62edc8c2372c0b62d121be8d4697025e4503c11b`  
		Last Modified: Tue, 07 Jan 2025 03:30:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e20b426cd68d0d8a2234b038f14ec814b7f518ff25be5fef02d4f213dc701c`  
		Last Modified: Tue, 07 Jan 2025 03:30:23 GMT  
		Size: 13.0 MB (13009129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8260a7f74618ce3ab9b7e8d29f1d66b40910993240bbb8eb112a22efa2eaa`  
		Last Modified: Tue, 07 Jan 2025 03:30:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a986cc16b42c1d6f12f9821e1f4faee9e15a501dd1259a9ba62047a74c8fc32`  
		Last Modified: Tue, 07 Jan 2025 03:30:23 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19e9e327a150f468e6d6c40783d4067080c17e446514f7ac627b6ebe4d0fc25`  
		Last Modified: Tue, 07 Jan 2025 03:30:23 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237f751575f4abc304695f4dd20a35e296f987443ca54960d4813b9b19e7d1fc`  
		Last Modified: Tue, 07 Jan 2025 04:21:58 GMT  
		Size: 23.8 MB (23816713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885f227a4b88ef0e27cc85528a6f5de829b327083f0490c3b9f929d92a5abbf7`  
		Size: 5.0 MB (4953053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ae91fa8f49d8ef99d2803d5da145f72a8a7a4e015c011abc84732b19d19d6`  
		Last Modified: Tue, 07 Jan 2025 04:21:57 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e266c24c5ebdba1e0ab4ac4178878c9de7347d8d3a627112180743ae05045be`  
		Last Modified: Tue, 07 Jan 2025 04:21:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ec1757eb44bdaeddaa4b2e1f57863c84170e8d4315040f5fa2967b21163b38`  
		Last Modified: Tue, 07 Jan 2025 04:22:01 GMT  
		Size: 90.4 MB (90413606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:34fabb38d507487f7ed2cf7fa63a7bc355b6a836c1dcb3f7552f1dbbfe4dba62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (32040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fafe70af39cf66ff4a6f9a24f94fcd33d6fbaebbbfee29d65862798af0ba53`

```dockerfile
```

-	Layers:
	-	`sha256:0bde0ffff8dc14ea6aec5651ea4d33963471b9fee8224cc079d43955948adbd7`  
		Size: 32.0 KB (32040 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:e65addfe2e73fa507dacc665015fdf79c88d4c8286bc6bbf24cfbe0892c2ff19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151267979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b79cc0c2e0dad52f6b66cab3cc1d8fece2ecf162f71dc9b6304a50736bfdcc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Fri, 20 Dec 2024 23:07:36 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Fri, 20 Dec 2024 23:07:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Fri, 20 Dec 2024 23:07:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770cb477b1c68317bfb2860d023b4972e2abdce0461a24b5e3c5d2ff8eadff58`  
		Size: 3.5 MB (3462737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8249e7b9c0ca9f3f0f47f0fd9d16c7a924f96930522c42609a86570d36e0ce7`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91a0f9929fb530faadf31b21d97adcb1eb6d139b4a4d3b93c2e76f0c02b000`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddb064e7b13dc78008c480f9b50806ab38cd416489cee96649aa23811745db7`  
		Last Modified: Tue, 07 Jan 2025 05:39:33 GMT  
		Size: 11.9 MB (11937926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2492777819c8a43eee1179a3c308d736a95916a35f14c60099102cd2cae69b`  
		Last Modified: Wed, 08 Jan 2025 03:42:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b292a88221316377f0dfccbd731017ca5c6008a45dd2eca46c1d5d23778668`  
		Last Modified: Tue, 07 Jan 2025 05:43:02 GMT  
		Size: 13.1 MB (13099122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d3c208c8d65bc3f733b9e43a860eeeb4e40b0ff931844b853ff824a310f00`  
		Last Modified: Tue, 07 Jan 2025 05:43:01 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee591fcfdb981918b28e6664bc7c319e4a14b2386fedfc73cf11ac9f6d715f7`  
		Last Modified: Tue, 07 Jan 2025 05:43:01 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f61d701b5b8ed3e2e7e1cae5ca5eb949be519b6c4c86d4fe64818d6eb0cd82`  
		Last Modified: Tue, 07 Jan 2025 05:43:02 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d405c4aeebd5c0f8ebd1381d8b2c4108a664c1993518a7f0dbf0f49e77cde`  
		Last Modified: Tue, 07 Jan 2025 10:54:28 GMT  
		Size: 24.1 MB (24128159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c52bde1cbe6ad815c7083e589588527d5e5ec5f462c13ebbc5257a7e3fc56e`  
		Last Modified: Tue, 07 Jan 2025 10:54:28 GMT  
		Size: 4.6 MB (4626307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07803dc42cdd0c80fe5190fcaaf2855b988fbfcaa2081bbb5fef1a90bd89c7df`  
		Last Modified: Tue, 07 Jan 2025 10:54:27 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc86b3af166c39c9de8f090d3e50c35463b722840e677f935c1e5fe6401eeca`  
		Last Modified: Tue, 07 Jan 2025 10:54:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcf793f1741854d3e443f50cd045dc12681b707cc6993f28d40de65dde0dd29`  
		Last Modified: Tue, 07 Jan 2025 10:54:31 GMT  
		Size: 90.4 MB (90412945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:88485147b89f2f2b54e98efac99216467fbea728f5496c74ef1ddf5a247863ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 KB (32122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb81f68f746e96c2173bba807ad480ca008fa4ebb40322f47625827b884259`

```dockerfile
```

-	Layers:
	-	`sha256:aeadf085f014bb6ba6a5b1f6c343bba40b9109aea98346128e20c6467504ecdf`  
		Last Modified: Tue, 07 Jan 2025 10:54:27 GMT  
		Size: 32.1 KB (32122 bytes)  
		MIME: application/vnd.in-toto+json
