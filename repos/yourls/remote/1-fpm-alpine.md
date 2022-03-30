## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:3a5a59a2c98caaa555f6916cc8f2a588233ecd7af94c686825ef8d0c61476433
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:81c959b92a1adc99f418d9ebf9ae10e383fdb10f79d016e8fb3b43c89dd6ee50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31111822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95677ab90886f2c6750e3a8ed70c6b07abd323b342631fa0c28509114f8349f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 01:54:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 29 Mar 2022 01:54:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 29 Mar 2022 01:54:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 29 Mar 2022 01:54:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 01:54:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 01:54:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 01:54:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 01:54:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 02:54:37 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 29 Mar 2022 02:54:37 GMT
ENV PHP_VERSION=8.0.17
# Tue, 29 Mar 2022 02:54:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Tue, 29 Mar 2022 02:54:37 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Tue, 29 Mar 2022 02:54:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Mar 2022 02:54:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 03:06:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 03:06:05 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Mar 2022 03:06:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 03:06:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 03:06:07 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 03:06:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Mar 2022 03:06:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Mar 2022 03:06:07 GMT
EXPOSE 9000
# Tue, 29 Mar 2022 03:06:07 GMT
CMD ["php-fpm"]
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.title=YOURLS
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Wed, 30 Mar 2022 08:51:08 GMT
LABEL org.opencontainers.image.version=1.8.2
# Wed, 30 Mar 2022 08:52:07 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Wed, 30 Mar 2022 08:52:07 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 30 Mar 2022 08:52:10 GMT
RUN apk add --no-cache bash
# Wed, 30 Mar 2022 08:52:12 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Wed, 30 Mar 2022 08:52:12 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Wed, 30 Mar 2022 08:52:12 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Wed, 30 Mar 2022 08:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:52:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17005d1e8de68c2ac61f45c442a3e4d468ac85ae2e52186fb37403bfcb3b8c38`  
		Last Modified: Tue, 29 Mar 2022 04:21:49 GMT  
		Size: 1.7 MB (1701406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4c7024b8161889c5e6873aaf0b4a89a1f818337c80ec6248c6e5aa04dec40`  
		Last Modified: Tue, 29 Mar 2022 04:21:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42f86642e80559b4c67fd7bbab62a46d4e10b6605dc69944f367a84192e81be`  
		Last Modified: Tue, 29 Mar 2022 04:21:48 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3eb3b60765a112a781055ff00904e24640089aebe7ac9fb89cc2a5024b3731`  
		Last Modified: Tue, 29 Mar 2022 04:26:29 GMT  
		Size: 10.8 MB (10790993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0b69785536315b4facf2724e94332cd47412a5d3beb4a5dff6b40fb00c98b5`  
		Last Modified: Tue, 29 Mar 2022 04:26:29 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb969a672788baca4cf66228ffd71b0db85efa68df533781a7a763f9960681e`  
		Last Modified: Tue, 29 Mar 2022 04:27:00 GMT  
		Size: 12.0 MB (12043087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca845e31a88685070e6bfe5bf58e023c8f1eec24ff5644d00d5e4f502b1b943a`  
		Last Modified: Tue, 29 Mar 2022 04:26:57 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fcc0ca981c834ea69b56f9f0ea88eded50f117980d40620d4496a4a30f3a7e`  
		Last Modified: Tue, 29 Mar 2022 04:26:57 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f68bca864e345d8b4649a1cc200a64f128051fca5d18cbcdc820754d237777`  
		Last Modified: Tue, 29 Mar 2022 04:26:58 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fb98707ed42293673943eaf55b4142d03481ffe3015c81fdda2fb22d8b76b9`  
		Last Modified: Wed, 30 Mar 2022 10:33:44 GMT  
		Size: 685.0 KB (685010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293c6972a169030d8add7068ba4d0d59b8cc33570e33992dcef840c15a7cbfe7`  
		Last Modified: Wed, 30 Mar 2022 10:33:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf8d05572753b233a015c8895539273f796c495daf8f9d8d26ae35775c87a1`  
		Last Modified: Wed, 30 Mar 2022 10:33:41 GMT  
		Size: 466.9 KB (466934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3998e7b1718a9fb243833e675c64b957e8d07d0b1e0e229297868b0a41e75e8`  
		Last Modified: Wed, 30 Mar 2022 10:33:41 GMT  
		Size: 2.6 MB (2574518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9189b0bda874dfac4ec0325be4f5b485beee77e5d29dc22b0218b816db5549e`  
		Last Modified: Wed, 30 Mar 2022 10:33:40 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f201a0d4ea5455dca2d50a57c44291e04d9ce10e45195b35fb5cdf39803722d3`  
		Last Modified: Wed, 30 Mar 2022 10:33:41 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:4e9f7be8da372f633739987215f7b04f7f0e72d18d710e0a82471878fa531f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29470380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdd7476e23892e5d61370fd3fb78e8cce2160b50e2bcd30c792a02076acd756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 00:52:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 29 Mar 2022 00:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 29 Mar 2022 00:53:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 29 Mar 2022 00:53:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 00:53:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 00:53:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 00:53:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 00:53:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 01:13:01 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 29 Mar 2022 01:13:02 GMT
ENV PHP_VERSION=8.0.17
# Tue, 29 Mar 2022 01:13:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Tue, 29 Mar 2022 01:13:02 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Tue, 29 Mar 2022 01:13:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Mar 2022 01:13:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 01:22:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 01:22:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Mar 2022 01:22:43 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 01:22:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 01:22:44 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 01:22:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Mar 2022 01:22:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Mar 2022 01:22:46 GMT
EXPOSE 9000
# Tue, 29 Mar 2022 01:22:47 GMT
CMD ["php-fpm"]
# Tue, 29 Mar 2022 06:40:24 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 29 Mar 2022 06:40:24 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 29 Mar 2022 06:40:24 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 29 Mar 2022 06:40:25 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 29 Mar 2022 06:40:25 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 29 Mar 2022 06:40:26 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 29 Mar 2022 06:40:26 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 29 Mar 2022 06:41:38 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 29 Mar 2022 06:41:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Mar 2022 06:41:42 GMT
RUN apk add --no-cache bash
# Tue, 29 Mar 2022 06:41:45 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 29 Mar 2022 06:41:46 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 29 Mar 2022 06:41:46 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Tue, 29 Mar 2022 06:41:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:41:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe53ded3c8dfed18c755c20bde3fa9baf5de7bd4585f13c4f7d88f7362e56b`  
		Last Modified: Tue, 29 Mar 2022 02:09:02 GMT  
		Size: 1.7 MB (1688709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9299665eb6bcbd5348bac0dc47eda3eafbe3b85a84ee7ccf8682387951cadd91`  
		Last Modified: Tue, 29 Mar 2022 02:09:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aadf0c132610db01f4060b07461c5b046a4afbca928ee871168737de0ac046d`  
		Last Modified: Tue, 29 Mar 2022 02:09:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e745f6d8470c1f1ef90f698974626c527c5838bf10c225e9d738ab8dcec4d98a`  
		Last Modified: Tue, 29 Mar 2022 02:12:20 GMT  
		Size: 10.8 MB (10790979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39e9504128a0d229b6fbc532a7516b8236ae8902ffc1894d84274cc2c6464b1`  
		Last Modified: Tue, 29 Mar 2022 02:12:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bf6eb673e49edb324ef750e4fdc2123030c4da3c9af97705ba1cd6cbd9fe8`  
		Last Modified: Tue, 29 Mar 2022 02:13:07 GMT  
		Size: 11.0 MB (10968439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2a925874e3fd535d2f90e6e28e4e84b8f603d01ec4cfdb1a83bbc2f3093490`  
		Last Modified: Tue, 29 Mar 2022 02:13:02 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74214e5fb99ac795dfd8849d9052d297e8271d61dee971945c609c544aea46d`  
		Last Modified: Tue, 29 Mar 2022 02:13:02 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b5d2e7b0e526eb39b7d3cd50bfc74b8c55e9df8e7c87004fc1c4d2d7240ed2`  
		Last Modified: Tue, 29 Mar 2022 02:13:02 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ed35bf551451440282d257500eb3db38354cdc8b16669fe7577d2b8ca8158d`  
		Last Modified: Tue, 29 Mar 2022 06:42:21 GMT  
		Size: 335.4 KB (335364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c54c8c6140777ccff26a011ec9b2bf1265e0bd4c0a388e0939fa2cbf42fe12`  
		Last Modified: Tue, 29 Mar 2022 06:42:18 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c585dd656aaf0c3a7a5212ae67b9ad21a657431c7bbd9c8d9a825d1619af4a`  
		Last Modified: Tue, 29 Mar 2022 06:42:19 GMT  
		Size: 455.1 KB (455081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621795acdf72dfe159af484f667600d44b4deb8ae3c2ff51febf2c75254ed64`  
		Last Modified: Tue, 29 Mar 2022 06:42:20 GMT  
		Size: 2.6 MB (2574524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202cf6960290b0630c84e70ba04501db81307ad319a1de14d0bf9e46257f8f3`  
		Last Modified: Tue, 29 Mar 2022 06:42:18 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac45ca5761fd9e5f4c5cc342febeca146336f2fea5cba875e21d717b2aa86ad1`  
		Last Modified: Tue, 29 Mar 2022 06:42:18 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:9136fc34ea79910e88003a8b6bda653d4e6f2ebe67599dcf4952f9f0ee899a7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28421882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e01be6f38ebe963b16e6af06e0a9fd9b5645dfac4239505c744bdf513a2ba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 29 Mar 2022 02:13:28 GMT
ADD file:8c959b80e3661beea7b3468017b88897d981bf52ed43c074e7c87ecb753e9059 in / 
# Tue, 29 Mar 2022 02:13:28 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:32:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 29 Mar 2022 07:32:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 29 Mar 2022 07:32:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 29 Mar 2022 07:32:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 07:32:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 07:32:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 07:32:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 07:32:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 08:31:20 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 29 Mar 2022 08:31:21 GMT
ENV PHP_VERSION=8.0.17
# Tue, 29 Mar 2022 08:31:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Tue, 29 Mar 2022 08:31:22 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Tue, 29 Mar 2022 08:31:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Mar 2022 08:31:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:41:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 08:41:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:41:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 08:41:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 08:41:13 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 08:41:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Mar 2022 08:41:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Mar 2022 08:41:16 GMT
EXPOSE 9000
# Tue, 29 Mar 2022 08:41:16 GMT
CMD ["php-fpm"]
# Tue, 29 Mar 2022 18:32:21 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 29 Mar 2022 18:32:21 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 29 Mar 2022 18:32:22 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 29 Mar 2022 18:32:22 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 29 Mar 2022 18:32:22 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 29 Mar 2022 18:32:23 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 29 Mar 2022 18:32:23 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 29 Mar 2022 18:33:31 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 29 Mar 2022 18:33:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Mar 2022 18:33:35 GMT
RUN apk add --no-cache bash
# Tue, 29 Mar 2022 18:33:39 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 29 Mar 2022 18:33:40 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 29 Mar 2022 18:33:40 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Tue, 29 Mar 2022 18:33:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 18:33:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22b1e5a07a97d7af6fdc335e3b3a975b73908fa19b084289c408a00814da0398`  
		Last Modified: Tue, 29 Mar 2022 02:15:28 GMT  
		Size: 2.4 MB (2424303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42554dad8e7b3486982f8ca444ab1d0a9c39f8d9e0efc0cab04005b04649de9f`  
		Last Modified: Tue, 29 Mar 2022 10:36:02 GMT  
		Size: 1.6 MB (1556472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd50495801bf9c4fadfed49ba9fba3273dd7cd5a5292928260be16ed5f10857b`  
		Last Modified: Tue, 29 Mar 2022 10:36:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6000a923377829f6674cd4337bb2916c96fc144e0d45d4df09dd5549aabf478f`  
		Last Modified: Tue, 29 Mar 2022 10:36:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5311c21b291a0b694ade268d8c1526fe80300793dfd9cf04b6a2850729b312d0`  
		Last Modified: Tue, 29 Mar 2022 10:43:13 GMT  
		Size: 10.8 MB (10790983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8283082454477709521e9ac649f8ecf6ee5ec504770d071c0e9de316ec28561`  
		Last Modified: Tue, 29 Mar 2022 10:43:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b8e42c2572791a99ec6d151a9ffa2befebadaa4706fcbfd66c70c66aea965e`  
		Last Modified: Tue, 29 Mar 2022 10:44:01 GMT  
		Size: 10.3 MB (10318907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0f17073ed53828354e46db7f52016fda9d021a88f17c28bd1d3e8b3c136cee`  
		Last Modified: Tue, 29 Mar 2022 10:43:54 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3cb6f303edde7cfe40864ae22ada1bbdb51326ae64102af4836905b771d68e`  
		Last Modified: Tue, 29 Mar 2022 10:43:54 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b73a268e70a3d532e121bda18e158646b511a3f483feddfa4ad845b0b46b65`  
		Last Modified: Tue, 29 Mar 2022 10:43:54 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452ace97cfad04b0a22684efe2e516a7a878cdbc39cf3ad3240403a97ac849a3`  
		Last Modified: Tue, 29 Mar 2022 18:36:13 GMT  
		Size: 305.9 KB (305862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9abaa18b3660285104f457f7a33d584b83261f8e669b2d4d163d3fc52e89e`  
		Last Modified: Tue, 29 Mar 2022 18:36:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba0826a6ceac614f3ac9a3f00ba922b5999d5eb085e640e03bac66c4410d999`  
		Last Modified: Tue, 29 Mar 2022 18:36:11 GMT  
		Size: 415.5 KB (415504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54a7b0adec8b1bc60589added0e7c22ed30b40e365951455fb5405d4c455fe1`  
		Last Modified: Tue, 29 Mar 2022 18:36:14 GMT  
		Size: 2.6 MB (2574516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d0daec7d5cf8c3372a66d612d7fb6ddf286d6b746abb62d31868a1be2e230`  
		Last Modified: Tue, 29 Mar 2022 18:36:11 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386fee66fd688a48af53293296b67bccead4870ceb90f1e69f30d50743a028a7`  
		Last Modified: Tue, 29 Mar 2022 18:36:11 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:bb5994d089198046e2a3b7ab3b3bbe81d6881eef3d99906d07638fa263172592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30164119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b6b56e8d8c9ba4a06bbd9e83fcd8878e98f6e02b6f11936eb1ca2b583191c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:23:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Mar 2022 06:23:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 24 Mar 2022 06:23:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 24 Mar 2022 06:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Mar 2022 06:23:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 24 Mar 2022 06:23:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Mar 2022 06:23:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Mar 2022 06:23:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Mar 2022 06:35:26 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 24 Mar 2022 06:35:27 GMT
ENV PHP_VERSION=8.0.17
# Thu, 24 Mar 2022 06:35:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Thu, 24 Mar 2022 06:35:29 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Thu, 24 Mar 2022 06:35:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 24 Mar 2022 06:35:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 24 Mar 2022 06:42:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 24 Mar 2022 06:42:53 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 24 Mar 2022 06:42:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 24 Mar 2022 06:42:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Mar 2022 06:42:55 GMT
WORKDIR /var/www/html
# Thu, 24 Mar 2022 06:42:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 24 Mar 2022 06:42:57 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Mar 2022 06:42:58 GMT
EXPOSE 9000
# Thu, 24 Mar 2022 06:42:59 GMT
CMD ["php-fpm"]
# Thu, 24 Mar 2022 11:34:15 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 24 Mar 2022 11:34:15 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 24 Mar 2022 11:34:16 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 24 Mar 2022 11:34:17 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 24 Mar 2022 11:34:18 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 24 Mar 2022 11:34:19 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 24 Mar 2022 11:34:20 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 24 Mar 2022 11:34:49 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 24 Mar 2022 11:34:50 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 24 Mar 2022 11:34:51 GMT
RUN apk add --no-cache bash
# Thu, 24 Mar 2022 11:34:53 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 24 Mar 2022 11:34:55 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 24 Mar 2022 11:34:56 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Thu, 24 Mar 2022 11:34:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 11:34:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fea5eff5ec13ee04313e09e625717c93e3d538ada26c96641c1c76980f169d`  
		Last Modified: Thu, 24 Mar 2022 07:02:13 GMT  
		Size: 1.7 MB (1696228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156c89b11261527df9962f5d43088cf38d8e0c86c41c2ece9b7517fd1811115`  
		Last Modified: Thu, 24 Mar 2022 07:02:12 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be23f7dd190d1fe2c3f9e661222a003a659013b2cf8bb9bfb3a8a286fc5503`  
		Last Modified: Thu, 24 Mar 2022 07:02:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e880f2e80bffc6056fc1eed70da2a01c23b4d87a25ab130c1814b59e4775b8`  
		Last Modified: Thu, 24 Mar 2022 07:04:15 GMT  
		Size: 10.8 MB (10790757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912c473551f6d4d4cb276c085696763e6db9190866570315a066dea09e5593f`  
		Last Modified: Thu, 24 Mar 2022 07:04:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4574ee68b0aa65d3799e2eba4a4cb2646669a5abe0408a303d45a5c138f9b979`  
		Last Modified: Thu, 24 Mar 2022 07:04:48 GMT  
		Size: 11.5 MB (11530788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803795a04347fce87672e4b965b88bdae5bb676f51e6dd6cd3fff3573259c3cf`  
		Last Modified: Thu, 24 Mar 2022 07:04:46 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63e6067b9cffab669113d395828c091589592541d8f6175d791aff9058e58d9`  
		Last Modified: Thu, 24 Mar 2022 07:04:46 GMT  
		Size: 18.3 KB (18305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba864bd6daea6dd0d3ced774dce68994e0a08281285d4e7c296fc859d21481bb`  
		Last Modified: Thu, 24 Mar 2022 07:04:46 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e61acc61bb3677ba6fc312e6712d6cee318362bdc7eb1736564861622a7bf2`  
		Last Modified: Thu, 24 Mar 2022 11:35:46 GMT  
		Size: 347.1 KB (347079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73e9de29611e5ce46559423caa80fb1d41ff54a68d4683323468627e1bb9cc2`  
		Last Modified: Thu, 24 Mar 2022 11:35:43 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62177fa231120f4a8114559f5501fc9ec1cfdb93d91998918db354cb0761c2b0`  
		Last Modified: Thu, 24 Mar 2022 11:35:44 GMT  
		Size: 474.0 KB (473959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c991cb614fc3500504e0127831a572d5a0ee51ff8e69af689c01a1aef34deb2`  
		Last Modified: Thu, 24 Mar 2022 11:35:44 GMT  
		Size: 2.6 MB (2575553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53a56133bdf3ae423c8380ce9b05b4f51f96d739b6da8836a3a83f537652af7`  
		Last Modified: Thu, 24 Mar 2022 11:35:43 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169cff8947a114a4aeeb04f57d80b60a816f43fdd1d51623fb5e61f113d5d726`  
		Last Modified: Thu, 24 Mar 2022 11:35:43 GMT  
		Size: 1.5 KB (1542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:21218b5cbd95f8cdca70f4ea4dbaa4f106055171d5305f97c9225d7d9a4e4de2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31485409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd6d4ea62e4de52ef1b97e308b393d96b4dd39604c6a91144f3f928094d4a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 01:40:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 29 Mar 2022 01:40:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 29 Mar 2022 01:40:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 29 Mar 2022 01:40:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 01:40:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 01:40:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 01:40:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 01:40:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 02:20:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 29 Mar 2022 02:20:07 GMT
ENV PHP_VERSION=8.0.17
# Tue, 29 Mar 2022 02:20:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Tue, 29 Mar 2022 02:20:09 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Tue, 29 Mar 2022 02:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Mar 2022 02:20:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 02:27:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 02:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Mar 2022 02:27:03 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 02:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 02:27:05 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 02:27:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Mar 2022 02:27:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Mar 2022 02:27:08 GMT
EXPOSE 9000
# Tue, 29 Mar 2022 02:27:09 GMT
CMD ["php-fpm"]
# Tue, 29 Mar 2022 20:36:50 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 29 Mar 2022 20:36:51 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 29 Mar 2022 20:36:52 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 29 Mar 2022 20:36:53 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 29 Mar 2022 20:36:54 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 29 Mar 2022 20:36:55 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 29 Mar 2022 20:36:56 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 29 Mar 2022 20:37:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 29 Mar 2022 20:37:45 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Mar 2022 20:37:47 GMT
RUN apk add --no-cache bash
# Tue, 29 Mar 2022 20:37:48 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 29 Mar 2022 20:37:50 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Tue, 29 Mar 2022 20:37:51 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Tue, 29 Mar 2022 20:37:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 20:37:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5273bd8fcb76483466b707c03417a57b5a7315e914f71e9287a046036f4df97`  
		Last Modified: Tue, 29 Mar 2022 03:24:32 GMT  
		Size: 1.8 MB (1800026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bfd573c4de53ba875fddf78db9d3172f2c97494f431fd1043f5eb168352530`  
		Last Modified: Tue, 29 Mar 2022 03:24:30 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d620d43f8d45fd951ae3535e5ef347816b664212673b2932770ed5b6258e913`  
		Last Modified: Tue, 29 Mar 2022 03:24:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2c9637f589e1a8ef676c81d8de3931baf79ff6084ae378f9f69c856ca349b2`  
		Last Modified: Tue, 29 Mar 2022 03:29:58 GMT  
		Size: 10.8 MB (10790743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e417ea7a3691bc25c62d93ffea6d5ad87542a28cf0915af93b439d07ade2f88`  
		Last Modified: Tue, 29 Mar 2022 03:29:55 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cbef01353b7846a3626bffe00a8ae5bee3f44b48a39d54042aa82c985ee3ec`  
		Last Modified: Tue, 29 Mar 2022 03:30:32 GMT  
		Size: 12.3 MB (12299191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16227d9f043f2c6b8fd3d832a5ef85af410685c65026914aed57794517962d2d`  
		Last Modified: Tue, 29 Mar 2022 03:30:30 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c54b037f36018dce6ccdc0bf28aaff9f59b9b1b51c74d1f6b70eb69f831b82a`  
		Last Modified: Tue, 29 Mar 2022 03:30:30 GMT  
		Size: 18.3 KB (18294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8d3671aa5ba39c00d11bda96b12576bf800b83b7546e820caa3838107cb2b3`  
		Last Modified: Tue, 29 Mar 2022 03:30:30 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6dd7d1e51fc252eb9702d6d2cc601103d5dfd0382c479bbe187bba66bb63c4`  
		Last Modified: Tue, 29 Mar 2022 20:39:50 GMT  
		Size: 662.4 KB (662406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7effe2957e863232c45cd3c12f97a47ba41cfe3505f0bef26951ff925a2efda3`  
		Last Modified: Tue, 29 Mar 2022 20:39:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a96224d8cc8ada92892611ebc6a0bce1cc42391148fe4a89bcdc404168c5a87`  
		Last Modified: Tue, 29 Mar 2022 20:39:47 GMT  
		Size: 503.4 KB (503383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e32d696ac5bc5c7825e06da874af1930e9c7112298d982fb349282d6fe0034a`  
		Last Modified: Tue, 29 Mar 2022 20:39:47 GMT  
		Size: 2.6 MB (2575553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325e58a79081a8242cfb697fdb834d7f1c33984f8fbc91b9f87cc2b4d1c06f6`  
		Last Modified: Tue, 29 Mar 2022 20:39:47 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce405587e5494b92ecfd9a59f1826fef0b425c1212cf59f01cba61fd628d269`  
		Last Modified: Tue, 29 Mar 2022 20:39:47 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:d181c7cf038cff64b05071e0f3c9d25389b642a9726c6db631fd6caf2708a1cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31336361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cb8b5f0e79e1e2d8a1c2c2d03fa307c127e93150aa3f47da3199523b3911a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 22:04:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 23 Mar 2022 22:04:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 23 Mar 2022 22:04:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 23 Mar 2022 22:04:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Mar 2022 22:05:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Mar 2022 22:05:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Mar 2022 22:05:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Mar 2022 22:05:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Mar 2022 22:18:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 23 Mar 2022 22:18:08 GMT
ENV PHP_VERSION=8.0.17
# Wed, 23 Mar 2022 22:18:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Wed, 23 Mar 2022 22:18:15 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Wed, 23 Mar 2022 22:18:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 23 Mar 2022 22:18:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:29:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 23 Mar 2022 22:29:10 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Wed, 23 Mar 2022 22:29:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 23 Mar 2022 22:29:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Mar 2022 22:29:23 GMT
WORKDIR /var/www/html
# Wed, 23 Mar 2022 22:29:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 23 Mar 2022 22:29:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Mar 2022 22:29:36 GMT
EXPOSE 9000
# Wed, 23 Mar 2022 22:29:39 GMT
CMD ["php-fpm"]
# Thu, 24 Mar 2022 08:37:50 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 24 Mar 2022 08:37:58 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 24 Mar 2022 08:38:01 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 24 Mar 2022 08:38:03 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 24 Mar 2022 08:38:10 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 24 Mar 2022 08:38:15 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 24 Mar 2022 08:38:21 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 24 Mar 2022 08:39:18 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 24 Mar 2022 08:39:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 24 Mar 2022 08:39:41 GMT
RUN apk add --no-cache bash
# Thu, 24 Mar 2022 08:39:48 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 24 Mar 2022 08:39:50 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 24 Mar 2022 08:39:51 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Thu, 24 Mar 2022 08:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 08:39:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f78867943bb57fcac766b3eb0b022125f22323ef1867a2a727cc5c9d010c94`  
		Last Modified: Wed, 23 Mar 2022 22:57:07 GMT  
		Size: 1.7 MB (1744638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7b3ac49454cdc93d74a8a9baf849cf874409439c0452d6e75b385c1eb8068b`  
		Last Modified: Wed, 23 Mar 2022 22:57:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68badc43ad09521b584065557959196c069547e694debc7f5ea441eee76f06c5`  
		Last Modified: Wed, 23 Mar 2022 22:57:06 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63caa854675aa3324c7328b8c18c9c3daf22a1ffb22bbfa0e995249fac33867`  
		Last Modified: Wed, 23 Mar 2022 22:59:15 GMT  
		Size: 10.8 MB (10790995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603f4c42423835185201691e3210a43e8f71b6469fd0f86fb9e8bfe85fcb744`  
		Last Modified: Wed, 23 Mar 2022 22:59:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfbec03a826f50ce9daacdc8f52f07f5baede5d92a32aac0b6451fbbd91a965`  
		Last Modified: Wed, 23 Mar 2022 22:59:57 GMT  
		Size: 12.5 MB (12451407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9cb155d41691c25401070abd0a9533f93c67defff5a5c52bbd38ee94282a8`  
		Last Modified: Wed, 23 Mar 2022 22:59:51 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225ad6fb91314376eb2be79f5ff025e233f65a6f02ed11d6438a7b86cb8ff7af`  
		Last Modified: Wed, 23 Mar 2022 22:59:52 GMT  
		Size: 18.4 KB (18392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e25449f57bca6d7dfe9b90867df6addcdadb8f482792e24746538a37fb92ba`  
		Last Modified: Wed, 23 Mar 2022 22:59:51 GMT  
		Size: 8.6 KB (8573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888d879c7f08edbf81ce5b265c5528193ae88e4806f8318b0ede7d143d435e0c`  
		Last Modified: Thu, 24 Mar 2022 08:41:01 GMT  
		Size: 397.0 KB (396961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a995f8a7f4744787c7aabf835a37672e8328f5ad95511c2bbbf562406967fe`  
		Last Modified: Thu, 24 Mar 2022 08:40:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5095d57d0bb48631427a8592fc6e1e472c756d9a9b9f116ae5fe0d746ce684a2`  
		Last Modified: Thu, 24 Mar 2022 08:40:58 GMT  
		Size: 528.6 KB (528594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b098dd3b5737d9751ae3f80ee0466a6b115a4ca453fa40c2daac59904d0c5d`  
		Last Modified: Thu, 24 Mar 2022 08:40:58 GMT  
		Size: 2.6 MB (2574518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc17336db4aa855e97e263117612b9963853d3f3544605cfea8827e6597ef976`  
		Last Modified: Thu, 24 Mar 2022 08:40:58 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a36369d1f5549ac1a392ab72bd5beee8a41e4fef52fe9d0e1fab5f5ea134b1`  
		Last Modified: Thu, 24 Mar 2022 08:40:58 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:c1ce79c34e331d454e575dcccbfe1b9db9b6bdf902b3022b22ea88966d83f2c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29895700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1465386762ef912dd5666fcdd41cbca2b54589e64056d45182896496db683c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 02:45:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 29 Mar 2022 02:45:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 29 Mar 2022 02:45:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 29 Mar 2022 02:45:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 02:45:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 02:45:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 02:45:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 02:45:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 03:29:30 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 29 Mar 2022 03:29:30 GMT
ENV PHP_VERSION=8.0.17
# Tue, 29 Mar 2022 03:29:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.17.tar.xz.asc
# Tue, 29 Mar 2022 03:29:31 GMT
ENV PHP_SHA256=4e7d94bb3d144412cb8b2adeb599fb1c6c1d7b357b0d0d0478dc5ef53532ebc5
# Tue, 29 Mar 2022 03:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 29 Mar 2022 03:29:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 03:35:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 03:35:46 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 29 Mar 2022 03:35:47 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 03:35:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 03:35:47 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 03:35:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 29 Mar 2022 03:35:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 29 Mar 2022 03:35:48 GMT
EXPOSE 9000
# Tue, 29 Mar 2022 03:35:48 GMT
CMD ["php-fpm"]
# Wed, 30 Mar 2022 10:48:49 GMT
LABEL org.opencontainers.image.title=YOURLS
# Wed, 30 Mar 2022 10:48:49 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Wed, 30 Mar 2022 10:48:49 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Wed, 30 Mar 2022 10:48:49 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Wed, 30 Mar 2022 10:48:50 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Wed, 30 Mar 2022 10:48:50 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Wed, 30 Mar 2022 10:48:50 GMT
LABEL org.opencontainers.image.version=1.8.2
# Wed, 30 Mar 2022 10:49:12 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Wed, 30 Mar 2022 10:49:13 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 30 Mar 2022 10:49:14 GMT
RUN apk add --no-cache bash
# Wed, 30 Mar 2022 10:49:15 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Wed, 30 Mar 2022 10:49:15 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Wed, 30 Mar 2022 10:49:15 GMT
COPY file:6b25ad92f8d7ceda57a7891b5b9f6f74a178e41b54c0d1e9644ce8ca0debdaab in /usr/local/bin/ 
# Wed, 30 Mar 2022 10:49:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:49:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35bba215d4ee2f93074e8177d9205d08f24a2d0b5b3d833cec760ce0bd923d`  
		Last Modified: Tue, 29 Mar 2022 05:02:30 GMT  
		Size: 1.8 MB (1760651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56f50ba6a709cd4c993cb01b66fe85bfdaced9c618b7da437fd5e9cc9145102`  
		Last Modified: Tue, 29 Mar 2022 05:02:30 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c090ee84889abbf8f19bbdf4a5986d6cd1e405a8fdcb49cb31eefaae45b93b6`  
		Last Modified: Tue, 29 Mar 2022 05:02:26 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1cb1f0b77d2eeeebea4290c180b7d4dd03ad53c2028d27349d45e41be35535`  
		Last Modified: Tue, 29 Mar 2022 05:44:22 GMT  
		Size: 10.8 MB (10790999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e13e47af73545a35c13cd51d3ef63b91a18c37939267890081b0270a0ab273`  
		Last Modified: Tue, 29 Mar 2022 05:44:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c102528ab3396d010110a68260ef1ca38926cee9b1de080b0e47652bba2b9bd9`  
		Last Modified: Tue, 29 Mar 2022 05:48:47 GMT  
		Size: 11.3 MB (11297732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a77040f7d78a993074b6634386ad3a2c33d95ed59877dbcd9cfd66eca6165d`  
		Last Modified: Tue, 29 Mar 2022 05:48:47 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b226128b8a411ed78c90266eb46c8b79a548c3c217eeaaf2978549659c301304`  
		Last Modified: Tue, 29 Mar 2022 05:48:47 GMT  
		Size: 18.4 KB (18413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6f63cc1ddb3bf7d717cb24331fc2961ce671a127445dd1a480c61a87c863b`  
		Last Modified: Tue, 29 Mar 2022 05:48:47 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0493aa348bd90ae346dd325c27ccac2bf88f4be6c1d60aea570736e15a547c1`  
		Last Modified: Wed, 30 Mar 2022 10:50:33 GMT  
		Size: 352.6 KB (352575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f16c94871a9590c32b22020c3fbf5df1a0e033c43484a19f2ee7f0ccd9acf1d`  
		Last Modified: Wed, 30 Mar 2022 10:50:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928e7027cb2179017e88eb49d42e03029bb662ec9d78f3aeffc186e2e720a1e`  
		Last Modified: Wed, 30 Mar 2022 10:50:32 GMT  
		Size: 483.4 KB (483417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd07fd83ff372d14c25a802e0fed6ba7d6fa23b820b781c79588098147efe2f`  
		Last Modified: Wed, 30 Mar 2022 10:50:33 GMT  
		Size: 2.6 MB (2574519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231dc26994dbdc16354bd2f2d51bf2c4953e10d3f9b815cbb9d1d5f6665e283a`  
		Last Modified: Wed, 30 Mar 2022 10:50:32 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942b6152e97df46f9750aff92ee9fd319712cda4b619b1e165be8e76c4d3f521`  
		Last Modified: Wed, 30 Mar 2022 10:50:32 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
