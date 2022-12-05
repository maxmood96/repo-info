## `mediawiki:legacylts-fpm-alpine`

```console
$ docker pull mediawiki@sha256:a288aaa459878b52b9af0826a9b1c1527da778425af0ae68411eda9c92bb2b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mediawiki:legacylts-fpm-alpine` - linux; amd64

```console
$ docker pull mediawiki@sha256:a0641e067ed3b22ff0d067f1a3a9f2d745279ec24076afc518705d77a5c87694
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154162766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f25b25cabe09a5930222fa765be532275748c00201dfb85e39e832ba0ec7ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:36:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 08:36:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 08:36:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 08:36:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 08:36:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 09:02:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 29 Nov 2022 03:45:32 GMT
ENV PHP_VERSION=8.0.26
# Tue, 29 Nov 2022 03:45:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Tue, 29 Nov 2022 03:45:32 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Tue, 29 Nov 2022 03:45:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Nov 2022 03:45:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:53:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Nov 2022 03:53:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:53:26 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Nov 2022 03:53:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Nov 2022 03:53:27 GMT
WORKDIR /var/www/html
# Tue, 29 Nov 2022 03:53:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Nov 2022 03:53:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Nov 2022 03:53:27 GMT
EXPOSE 9000
# Tue, 29 Nov 2022 03:53:28 GMT
CMD ["php-fpm"]
# Mon, 05 Dec 2022 20:47:53 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Mon, 05 Dec 2022 20:49:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Mon, 05 Dec 2022 20:49:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 05 Dec 2022 20:49:19 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 05 Dec 2022 20:50:26 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Mon, 05 Dec 2022 20:50:26 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Mon, 05 Dec 2022 20:50:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Mon, 05 Dec 2022 20:50:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b78b4fe0ca1ca5277d0b56997b3a74ac05ac52ff34cf9d5c6c063bd3feca07e`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.7 MB (1721291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6040f2a28f7fd4288a87be2db7a8886104a1080402d0343e1c527c232d8963`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e66b89284d71ee13c90182fe35d46d2461573064ae7f020aa4c22c1235e2a`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05497c4b6f53b581cf07d926f6f282cbc0f177cbb6e146b695be722fcce23448`  
		Last Modified: Tue, 29 Nov 2022 04:24:45 GMT  
		Size: 10.9 MB (10888639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a30d168d1fb3d525d7c296d6c0ea3cbe4a2b94abfdaf01e8bad7b29927cbd5`  
		Last Modified: Tue, 29 Nov 2022 04:24:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb384cc931b07b8b8d7965e5d5704a4930aab45507b2c9bdd3c3886f5fd0076`  
		Last Modified: Tue, 29 Nov 2022 04:25:10 GMT  
		Size: 12.5 MB (12460485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b7a0d9ae62972e89af6944b8192d9e7393b5ef9eeb9adf405bd2990ecdf67b`  
		Last Modified: Tue, 29 Nov 2022 04:25:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74527b27d94cc294195e21b43419b0a2187bd100c07f60cea08feb7b9008b6f0`  
		Last Modified: Tue, 29 Nov 2022 04:25:08 GMT  
		Size: 18.7 KB (18689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f1bf3aa8e69c29240e3cf8fe5172731c06efc6e0d0c56d58b46c36920479c9`  
		Last Modified: Tue, 29 Nov 2022 04:25:08 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22261ff4a143619fd51de0209779e710c75843ca7145fb28df36fb57970ea3f6`  
		Last Modified: Mon, 05 Dec 2022 20:53:39 GMT  
		Size: 68.5 MB (68489041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793cfcbdc97f8a4a626113a08129ae619113f54849c1abe6a60dc232e64138`  
		Last Modified: Mon, 05 Dec 2022 20:53:30 GMT  
		Size: 7.1 MB (7143202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ecf522bc0a14ee04ac076b323e649ef0bafb9c67cd1661201aff2a15d571a`  
		Last Modified: Mon, 05 Dec 2022 20:53:28 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc48edf040ade8bc2366a71f3da118607c0f79e9a841f4b7515d35c21548c421`  
		Last Modified: Mon, 05 Dec 2022 20:53:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb8d7d227c1155a3208328cf3b5feba9cd42110828949c4724addc626390285`  
		Last Modified: Mon, 05 Dec 2022 20:54:49 GMT  
		Size: 50.6 MB (50621612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts-fpm-alpine` - linux; arm variant v6

```console
$ docker pull mediawiki@sha256:81bc85973ad371bb256f69ea2b086ef6fa2b2c8ad5365e47d3319a71f49d5369
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147248360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13908c8298449a4ec48e6e530cc97c7743c5030b568c6725b0894989ca5b65cf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:54:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 04:55:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:21:40 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 29 Nov 2022 02:59:40 GMT
ENV PHP_VERSION=8.0.26
# Tue, 29 Nov 2022 02:59:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Tue, 29 Nov 2022 02:59:40 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Tue, 29 Nov 2022 02:59:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Nov 2022 02:59:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:09:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Nov 2022 03:09:46 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:09:47 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Nov 2022 03:09:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Nov 2022 03:09:48 GMT
WORKDIR /var/www/html
# Tue, 29 Nov 2022 03:09:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Nov 2022 03:09:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Nov 2022 03:09:49 GMT
EXPOSE 9000
# Tue, 29 Nov 2022 03:09:49 GMT
CMD ["php-fpm"]
# Mon, 05 Dec 2022 20:55:22 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Mon, 05 Dec 2022 20:56:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Mon, 05 Dec 2022 20:56:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 05 Dec 2022 20:56:28 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 05 Dec 2022 20:56:54 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Mon, 05 Dec 2022 20:56:54 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Mon, 05 Dec 2022 20:57:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Mon, 05 Dec 2022 20:57:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089b5ea696a25e03b2eaa2ba4c2d7ca2b161473cb9f1686ca8b9af4b714cc216`  
		Last Modified: Sat, 12 Nov 2022 05:51:25 GMT  
		Size: 1.7 MB (1708068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c879de0e59a35d228a53d3c70813c09859b8647217f5bdf53e6b8058daa80`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b9d16af9cd3acc95ea5a8da94a040a0f63b8af95a60a4ad30aaddbab836604`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeecb3f5485e621dcd0c13f90b93dc5430ab9cf6aace0fb255aff3fb868d2b9`  
		Last Modified: Tue, 29 Nov 2022 03:41:14 GMT  
		Size: 10.9 MB (10888623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d8ab326daec8a4930a174d144cb830be417f513c5a405ab781bdf34de61b47`  
		Last Modified: Tue, 29 Nov 2022 03:41:13 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2e4e7a4ab231cd5f34767106316246731f295cf53240534c78de3af8d0f56`  
		Last Modified: Tue, 29 Nov 2022 03:41:51 GMT  
		Size: 11.4 MB (11376257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e831f66b8b7703dfb2771f2c339ea7b4866fd63342d32d7bb3c0972b41f6d9`  
		Last Modified: Tue, 29 Nov 2022 03:41:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1affb5a0ec4a39b2798f0b76a658911d05c0183813dab931a2be089d0341c792`  
		Last Modified: Tue, 29 Nov 2022 03:41:48 GMT  
		Size: 18.7 KB (18707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971583676d391afb27f4c85c147d94af3aaa053558c5f832b5d1aa9b133bfc68`  
		Last Modified: Tue, 29 Nov 2022 03:41:48 GMT  
		Size: 8.6 KB (8573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d19b0c5ee1cbd4e7081669e14b0a59c92aa338c61919c3cdf20897ba0ef609`  
		Last Modified: Mon, 05 Dec 2022 20:58:34 GMT  
		Size: 63.8 MB (63759558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd07909e2c5f6ed9649b640d51609075d32aaced08051be1939182a40ceed74`  
		Last Modified: Mon, 05 Dec 2022 20:58:23 GMT  
		Size: 6.2 MB (6247168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74b81c3b2bab205a24e322ea801562d6b591f2418ce187bc5e6bc2ca08c76d4`  
		Last Modified: Mon, 05 Dec 2022 20:58:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039178d4f223a29fc895dd991998e2ab0ccc32c33cfa524741fd9d60b5532e84`  
		Last Modified: Mon, 05 Dec 2022 20:58:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11e287a500f0abb9a307bfa0703154f77643f778cccfb2397bac72154e5adaa`  
		Last Modified: Mon, 05 Dec 2022 20:59:09 GMT  
		Size: 50.6 MB (50621437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts-fpm-alpine` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:6e65fd6be10ba732ca4d9c54b324c54f71daa42dd627bdf253e4326c325ec042
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142664592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571f59cc6e9c02425d1498198bcf8df704efef490a0b7a1bcc276f5a981e8bf4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:47:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 05:47:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 05:47:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 05:47:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 05:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 06:28:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Sat, 12 Nov 2022 06:28:30 GMT
ENV PHP_VERSION=7.4.33
# Sat, 12 Nov 2022 06:28:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.33.tar.xz.asc
# Sat, 12 Nov 2022 06:28:30 GMT
ENV PHP_SHA256=924846abf93bc613815c55dd3f5809377813ac62a9ec4eb3778675b82a27b927
# Sat, 12 Nov 2022 06:28:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 12 Nov 2022 06:28:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:36:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 12 Nov 2022 06:36:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:36:59 GMT
RUN docker-php-ext-enable sodium
# Sat, 12 Nov 2022 06:37:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 12 Nov 2022 06:37:00 GMT
WORKDIR /var/www/html
# Sat, 12 Nov 2022 06:37:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 12 Nov 2022 06:37:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 06:37:00 GMT
EXPOSE 9000
# Sat, 12 Nov 2022 06:37:01 GMT
CMD ["php-fpm"]
# Sat, 12 Nov 2022 17:12:48 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Sat, 12 Nov 2022 17:13:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Sat, 12 Nov 2022 17:13:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 12 Nov 2022 17:13:45 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Sat, 12 Nov 2022 17:15:10 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Sat, 12 Nov 2022 17:15:10 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Sat, 12 Nov 2022 17:15:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Sat, 12 Nov 2022 17:15:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525864ff6d6c3a1a9ca039e0999c8d05701858671326bac7253a25aa21de91b9`  
		Last Modified: Sat, 12 Nov 2022 06:53:18 GMT  
		Size: 1.6 MB (1575444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09a62104a768e3175677dcac32aa6ba859b0b7917b110ff8fdda7c64447d13f`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd62154db22fa402fe200d63a35937ed4a35c102677a20c24eff0fca7ad7981d`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f305a23ff6f5e07b02e352f64307039f732eb382da5b4cfc53ebd5dafca66769`  
		Last Modified: Sat, 12 Nov 2022 07:00:47 GMT  
		Size: 10.4 MB (10440228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48052a702a4799511d281444b45ca486f464142f097b35a2f8531082962be3d8`  
		Last Modified: Sat, 12 Nov 2022 07:00:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d382c232afc473fa94596ea01a38fd34cc70665682081674ce342bd7ef9e0`  
		Last Modified: Sat, 12 Nov 2022 07:01:38 GMT  
		Size: 10.1 MB (10089534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf6e0dba114e226fea10d947fe850bd53ec6cc00d9a5db7776945c646ec57b`  
		Last Modified: Sat, 12 Nov 2022 07:01:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39816518f3df428d6ac0c244c0cfdb66022bd789ff5908160a2ef5e18219c94`  
		Last Modified: Sat, 12 Nov 2022 07:01:36 GMT  
		Size: 18.6 KB (18642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7f14a94cfbe4184e10ca09f49ac3788e40e34629a9dc87f630c640623f3ebe`  
		Last Modified: Sat, 12 Nov 2022 07:01:36 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56093b173fe1fa3b44ca399ce1d78d38d3148c2e396bccd68eb875953752cec`  
		Last Modified: Sat, 12 Nov 2022 17:17:14 GMT  
		Size: 60.8 MB (60828056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb08d75b0c8d23136f0b1174647c6b616b27f7afc3a29f3a96ddb963ffac0bc`  
		Last Modified: Sat, 12 Nov 2022 17:17:04 GMT  
		Size: 6.7 MB (6659288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad18bf1ad098fa6d29d6d936710f5272ce33290372ed3f0af4901fa031ee6a`  
		Last Modified: Sat, 12 Nov 2022 17:17:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231fd58ee24815d0c6caa54f5ce63ff7d4df7c8020cfff2ec84ae7bc6fe11986`  
		Last Modified: Sat, 12 Nov 2022 17:17:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab106f6959ce89d209d0e14b0e160aa3fdbea71a6c1ea327be1c90a2317eda3`  
		Last Modified: Sat, 12 Nov 2022 17:18:36 GMT  
		Size: 50.6 MB (50621312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:fc51e40c4bb26cbe559e62d38612b887447446cb1b90013ff06881296e186fc4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151756085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add32e8e11d316ffa59a566b7c6469c24c0b7a2f513dd0042ed91df9241b4edc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:37:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 04:38:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 04:38:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 04:38:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:38:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:03:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 29 Nov 2022 03:48:32 GMT
ENV PHP_VERSION=8.0.26
# Tue, 29 Nov 2022 03:48:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Tue, 29 Nov 2022 03:48:32 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Tue, 29 Nov 2022 03:48:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Nov 2022 03:48:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Nov 2022 03:54:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:54:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Nov 2022 03:54:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Nov 2022 03:54:04 GMT
WORKDIR /var/www/html
# Tue, 29 Nov 2022 03:54:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Nov 2022 03:54:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Nov 2022 03:54:05 GMT
EXPOSE 9000
# Tue, 29 Nov 2022 03:54:05 GMT
CMD ["php-fpm"]
# Mon, 05 Dec 2022 21:10:40 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Mon, 05 Dec 2022 21:11:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Mon, 05 Dec 2022 21:11:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 05 Dec 2022 21:11:26 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 05 Dec 2022 21:12:22 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Mon, 05 Dec 2022 21:12:22 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Mon, 05 Dec 2022 21:12:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Mon, 05 Dec 2022 21:12:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d018a6b8f2b9d3c88bb51b66bb27c7840ca587dc27d7b18ed9d29271f7a801`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 1.7 MB (1715697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd698c26bd17e47cae3e287202cee1112230b8c1e3b6eff40ab1c13d26737998`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d804918576056f288bba1c63c140494fb4cfd8c845d79c029e38fba1f5665ee`  
		Last Modified: Sat, 12 Nov 2022 05:25:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a980de96c700dbe884cf714d361ea665dc0ec93d35fe88794ba0a575b3d174`  
		Last Modified: Tue, 29 Nov 2022 04:21:04 GMT  
		Size: 10.9 MB (10888643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca807bbb9c3870cbf8964952196d91a6ebf5a21db3a730765d3c8c7654864e`  
		Last Modified: Tue, 29 Nov 2022 04:21:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f21845d8b836fe0402a156039eb5a8e45e6772e4682dfffc1dcbae69dc663`  
		Last Modified: Tue, 29 Nov 2022 04:21:29 GMT  
		Size: 12.0 MB (11959263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f0a7554d6a11b9e151143008b07c2c0527ffcba7c8aada343e2e0e3853a4d`  
		Last Modified: Tue, 29 Nov 2022 04:21:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7a5fa45322f38a8af491a1ee2e611e7619a1a4ec50864a8dea6ed05bc5df35`  
		Last Modified: Tue, 29 Nov 2022 04:21:27 GMT  
		Size: 18.7 KB (18703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170798bb446f0f62ed14592dd7a4c7d04da29775827f6c475f2ed59259cb058a`  
		Last Modified: Tue, 29 Nov 2022 04:21:27 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60521b4f58be482a86ab751fca78e61f1decd38ab819245c1b3b9a3d012f639`  
		Last Modified: Mon, 05 Dec 2022 21:15:25 GMT  
		Size: 67.1 MB (67054274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04c03ea502b6117c41308518980c2c9c3c477a13687a2fe1157a0ec69f0a4c`  
		Last Modified: Mon, 05 Dec 2022 21:15:18 GMT  
		Size: 6.8 MB (6776835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3062246cd2a255f8e2eda86944b3fe1669b579de5b06668f7388fd8369678d89`  
		Last Modified: Mon, 05 Dec 2022 21:15:17 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3903ba9cdce8dd21b6194a5dcf897cc295cae577d0b67c9250376fa04eb50bf`  
		Last Modified: Mon, 05 Dec 2022 21:15:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d547b2cf3957f99492ce93891e19d1d2ade07efb187d245caee306906eabe`  
		Last Modified: Mon, 05 Dec 2022 21:16:29 GMT  
		Size: 50.6 MB (50621379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts-fpm-alpine` - linux; 386

```console
$ docker pull mediawiki@sha256:885c0c3b214d3b1f908a59bb9675aef2f35f39f9655d21b78dfe7f76a51e619b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154021104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1531d186763b5db30977a81b8be39ba7ed59aed2637ac0f517c73c5b43731892`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:08:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 08:08:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 08:08:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 08:08:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 08:08:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 08:08:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:08:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:08:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 08:36:20 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 29 Nov 2022 03:56:42 GMT
ENV PHP_VERSION=8.0.26
# Tue, 29 Nov 2022 03:56:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Tue, 29 Nov 2022 03:56:44 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Tue, 29 Nov 2022 03:56:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Nov 2022 03:56:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Nov 2022 04:04:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Nov 2022 04:04:45 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Nov 2022 04:04:45 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Nov 2022 04:04:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Nov 2022 04:04:47 GMT
WORKDIR /var/www/html
# Tue, 29 Nov 2022 04:04:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Nov 2022 04:04:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Nov 2022 04:04:50 GMT
EXPOSE 9000
# Tue, 29 Nov 2022 04:04:51 GMT
CMD ["php-fpm"]
# Mon, 05 Dec 2022 21:07:34 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Mon, 05 Dec 2022 21:08:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Mon, 05 Dec 2022 21:08:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 05 Dec 2022 21:08:57 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 05 Dec 2022 21:10:25 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Mon, 05 Dec 2022 21:10:26 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Mon, 05 Dec 2022 21:10:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Mon, 05 Dec 2022 21:10:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529c1276f7fbbfab5754449ae3db2b4a04a98af1d706770d02ddb1654a806e5e`  
		Last Modified: Sat, 12 Nov 2022 09:10:33 GMT  
		Size: 1.8 MB (1820471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5a372dd65c07f12bc395d2ea0e1266225dc55c9a1673efe9894a022f00e41d`  
		Last Modified: Sat, 12 Nov 2022 09:10:32 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839f3c42dc99fde076c817b954f4cc26d21c68b993eedfc6e5a5428d4b49c393`  
		Last Modified: Sat, 12 Nov 2022 09:10:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f2d8caf08dab17691465f0a6ede5ead156808ad16037ffb0040853352c335e`  
		Last Modified: Tue, 29 Nov 2022 04:44:17 GMT  
		Size: 10.9 MB (10888408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b0cf270dac181593e96c57e19309df502e93d1cd5572dbedcb51d3bf7b41f`  
		Last Modified: Tue, 29 Nov 2022 04:44:16 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd8d385f10d55eadf770d8f74a51a87290176bea6448e1bd94865627fccc899`  
		Last Modified: Tue, 29 Nov 2022 04:44:48 GMT  
		Size: 12.7 MB (12730781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb4e15b150c69a5f003ec2e15eae7e651c14b562beeb303f0c5f7424bccc66`  
		Last Modified: Tue, 29 Nov 2022 04:44:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3b84fa7a3e701a1eeea495e775a8d086fe5b7c07c1f2b939d1c71df627393`  
		Last Modified: Tue, 29 Nov 2022 04:44:46 GMT  
		Size: 18.6 KB (18606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63142fecbf663344995eeb31124974d5edef718e1628c5b59293acfe7474792e`  
		Last Modified: Tue, 29 Nov 2022 04:44:46 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78b86e8d8fab4f0eea247fe7734b9cd264b6a5bf231afe9ab7c1b04556552f9`  
		Last Modified: Mon, 05 Dec 2022 21:14:24 GMT  
		Size: 67.9 MB (67891989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c3015a994e799b52071802319491794d441320ff0045e2741dfb9063a22562`  
		Last Modified: Mon, 05 Dec 2022 21:14:15 GMT  
		Size: 7.2 MB (7227602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06c105adab384e254923afb8abf550ebbccc3a8aba3183ea271e4d7bc1d9fc8`  
		Last Modified: Mon, 05 Dec 2022 21:14:14 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8923000eb59c2cd879d95d768ebb2b6a30bd6c640b4a1d97b65d14c9674309`  
		Last Modified: Mon, 05 Dec 2022 21:14:14 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e60ecc30ab8139863fb0106f90ce7faee51a5a75a2d72cfa75ee85626effb8e`  
		Last Modified: Mon, 05 Dec 2022 21:15:42 GMT  
		Size: 50.6 MB (50621461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mediawiki:legacylts-fpm-alpine` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:a78c0e36d6fce4b42ee349feee09a7eb423596501a5b765851585790946387ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159966133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee1b00192118d4baef8e9c0e39852f6167d3e20451e4f983fa82d1cdc9a99a4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:14:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 07:14:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 07:14:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 07:14:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 07:14:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 07:47:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Tue, 29 Nov 2022 03:21:19 GMT
ENV PHP_VERSION=8.0.26
# Tue, 29 Nov 2022 03:21:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Tue, 29 Nov 2022 03:21:20 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Tue, 29 Nov 2022 03:21:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Nov 2022 03:21:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:31:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Nov 2022 03:31:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Nov 2022 03:31:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Nov 2022 03:31:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Nov 2022 03:31:25 GMT
WORKDIR /var/www/html
# Tue, 29 Nov 2022 03:31:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Nov 2022 03:31:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Nov 2022 03:31:26 GMT
EXPOSE 9000
# Tue, 29 Nov 2022 03:31:27 GMT
CMD ["php-fpm"]
# Mon, 05 Dec 2022 20:47:11 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	;
# Mon, 05 Dec 2022 20:48:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.21; 	docker-php-ext-enable 		apcu 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del .build-deps
# Mon, 05 Dec 2022 20:48:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 05 Dec 2022 20:48:45 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data
# Mon, 05 Dec 2022 20:51:12 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.35
# Mon, 05 Dec 2022 20:51:13 GMT
ENV MEDIAWIKI_VERSION=1.35.8
# Mon, 05 Dec 2022 20:51:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del .fetch-deps
# Mon, 05 Dec 2022 20:51:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194dd51b13c32835b9a76fe58f7580e66a1df8a2acea27095b556cf63b31a98`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.8 MB (1772559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e966c695081973df431189ce4bf6ed44556dad53c642dfb26fa5c0df97e5a7`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd33a80e474697f7ae3aeeba872662ed64ab312628cb4eaf63bd9cefb1b5a3`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a7de1c9c701905b87ad4afbfe476e0389783367dd4a2b90e54400c7fa89aaf`  
		Last Modified: Tue, 29 Nov 2022 04:13:00 GMT  
		Size: 10.9 MB (10888645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4756efc489066b21ee20194d533c606ada467b623c5401da1bb68868e406d0f`  
		Last Modified: Tue, 29 Nov 2022 04:12:59 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311b0f0c02dc94009d284f329a8466596785d2b848238d61f8197a4e15da8df6`  
		Last Modified: Tue, 29 Nov 2022 04:13:38 GMT  
		Size: 12.9 MB (12925238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515edd22e600362bfa9a5f648d5a54fdfb9d0f4bc0e0a462a474b8ff933c0ce0`  
		Last Modified: Tue, 29 Nov 2022 04:13:34 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3689d3bb2013aca21bdb81a0f9d4ce50c207463f55645b6a1c12792d8f2d6be9`  
		Last Modified: Tue, 29 Nov 2022 04:13:34 GMT  
		Size: 18.7 KB (18696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7f98bf5eb612040fc75f7f2a0c5fe7e48181e7a7ed67049ea6093906be921e`  
		Last Modified: Tue, 29 Nov 2022 04:13:34 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b08ab3d851b6a1cfd4817c14940a41f3327d06a6bd68ec351e9837fbb45007`  
		Last Modified: Mon, 05 Dec 2022 20:56:36 GMT  
		Size: 74.1 MB (74082998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8fb696af8453dd64a6eb294ef6b922de6d6557a5367d66f858387d9dce5d3f`  
		Last Modified: Mon, 05 Dec 2022 20:56:20 GMT  
		Size: 6.8 MB (6841307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b319612fa731a68704006a183550ed81820828b0e2a042d5e220f1ee2e0f106`  
		Last Modified: Mon, 05 Dec 2022 20:56:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bb7c416f6db8287c3b10b1201b515b6ee78b689a1f46354922e3deeed9edf2`  
		Last Modified: Mon, 05 Dec 2022 20:56:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872be1905b5c671dae68070c6695a51cb3d24c1dac5aca73abaac10e94059e01`  
		Last Modified: Mon, 05 Dec 2022 20:58:22 GMT  
		Size: 50.6 MB (50621593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
