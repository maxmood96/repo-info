## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:971e8150b35f280823d854ebc286e8a1b56a8d8604ad21d324f9c0c99f7994a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:83c2215cc535660dbfd9243a9fcc59180d9260742f8a0fd0a101e059c37427a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39953040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a4acb36b3a14f9985506aeb7d161f4dc095fbad7d3282bf7b8907fefb46ea`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d785fab7b970527612c538d27004d91011246af40de2f46c665f1347bf9c48cd`  
		Last Modified: Tue, 12 Nov 2024 02:09:54 GMT  
		Size: 5.6 MB (5583581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b6373c5b10cf98e59bb320b63721deacbd8d679d2df67893b72b49a7cff41`  
		Last Modified: Tue, 12 Nov 2024 02:09:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127f2cf93ae65391b7e93d2f835702735c7d1944361ded5086395e7cb894cf1`  
		Last Modified: Tue, 12 Nov 2024 02:09:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babee3bd65d0c605def637ff361cd6e6fcfab54894334585a487e8a193a39d22`  
		Last Modified: Tue, 12 Nov 2024 02:09:55 GMT  
		Size: 12.5 MB (12504598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630ada844ef82ac78bef1c0f4a5f4d85a03e74484b6a5c246d110e4e42e59178`  
		Last Modified: Tue, 12 Nov 2024 02:09:55 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc1f4e64ac05a9fef63475c80fe43a5b560646dc29f7eca5a95cbbe65a5731`  
		Last Modified: Tue, 12 Nov 2024 02:09:56 GMT  
		Size: 13.1 MB (13102179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1d1966d9e8a911d9a044075a9c75867c13695fce758cc76db401bcad420b7f`  
		Last Modified: Tue, 12 Nov 2024 02:09:56 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1e7be247a6260a02fa2df612962ccbd63a198020e4ae7c52bff450a8852d5e`  
		Last Modified: Tue, 12 Nov 2024 02:09:56 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb948a29649efcbf7e62609fc0726d4c374a5c4b312c01e78f24ea73e1a02af`  
		Last Modified: Tue, 12 Nov 2024 02:09:56 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdcc5b7c5a3d3544a4531239d5eb7eda39ffc2aa4c1968377d2c1a5696e3733`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 546.2 KB (546218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42f2707bf1f3aaa9b4c7741e19754207d62aeec5c32af2f8e282613c61afca9`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23548b8b5fa92ece59874618919b915210fd55e14afe56eb0146bbc660c77c`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 482.2 KB (482170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1002a066d102f652d31325c001aca90bcd8e0650b419b29eb568af03d8f8c`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 4.1 MB (4073356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a298076cdc55d87a17c8c46ecdcaa123d28c41b8cb78a89924844b3fe754bd35`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0ae092bf7c63e3bc5c8dd6928ba4cea57b7ecee33ffa5ecc0419890919596b`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:f3f71b4f89f2e10990107d8ee3ec685754e997bf1ae469f67e9f5ecb97a5839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bfe415c182423471211eadc1cb87943597eae696dbd742add04849fd51808f`

```dockerfile
```

-	Layers:
	-	`sha256:42d2f908d670ec1bf723c54189dd6d036a168ca2116607ab292a366ef3a91463`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 30.5 KB (30499 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:3111db80ba00a45203f121e5e112981b4c9e2a7aee6111339ec60782d65bd9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37795062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4fd556e215b1b3f0984784c22b151158e6f686ffe74dedf16bda5442e768b5`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077201e66b85be92a47e209273e3a746b6c9fb70abe63fc08fcfdbc9d9725801`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 5.2 MB (5235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f342726194a9999ab374184edacbc753de40c600fb9b4e9fedc6d530e054ad2`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e58cbafd5fc0f6e2372ba8b7dea44a4ee3ddb23dc907076855de93848d047`  
		Last Modified: Mon, 28 Oct 2024 22:05:27 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c28c0130b831a49b4d2850f09ea4f0ee38233b42ea99d5c199d23bdd5cec428`  
		Last Modified: Mon, 28 Oct 2024 22:34:46 GMT  
		Size: 12.5 MB (12504591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4162ac0a5c5b8522341da681638bd01f7d082c7a7ec8ef5d0e95093f6eb5fb`  
		Last Modified: Mon, 28 Oct 2024 22:34:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881e046ec79f2812946138eaebfe2ac59d1d1b1f46f5751ec96ecea496047e3e`  
		Last Modified: Mon, 28 Oct 2024 22:39:57 GMT  
		Size: 11.9 MB (11923782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87ea10ffde6b61f54cd52514ce9aac988824cc888814afcda5193d330b9d68`  
		Last Modified: Mon, 28 Oct 2024 22:39:56 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effc528e7d401252707b6e3012ba03f5ef09a371c0ff40d00930a9755377336f`  
		Last Modified: Mon, 28 Oct 2024 22:39:56 GMT  
		Size: 19.4 KB (19438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefff9971014214a162bd3a0a4b799a7367a8e9c87ea355ee8f8c6fd66b7768b`  
		Last Modified: Mon, 28 Oct 2024 22:39:57 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee841655b5f37c3565eae0da0f42d229ef2083f5bafbfe01b457b15d99232d6`  
		Last Modified: Tue, 29 Oct 2024 00:13:33 GMT  
		Size: 172.7 KB (172694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a11aa748bf1e88de274182947117b3d2fd260882d79febdcc5aa10982d2036c`  
		Last Modified: Tue, 29 Oct 2024 00:13:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0206596d98c6490aa7ed6e491883185bf4c3a9e24c5958b5357752168f77560a`  
		Last Modified: Tue, 29 Oct 2024 00:13:34 GMT  
		Size: 482.2 KB (482234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c697a540da1fc7912d763be1e8afe7e088f78224131235c65c2276c17db39fcd`  
		Last Modified: Tue, 29 Oct 2024 00:13:34 GMT  
		Size: 4.1 MB (4073359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38b3a2854e27e0b2816178152d045c5f7f478988591bba20084d64c0db6c91`  
		Last Modified: Tue, 29 Oct 2024 00:13:35 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe7aef132815ea96562248a6d47a3013569882e80de72309c0d56c63085c306`  
		Last Modified: Tue, 29 Oct 2024 00:13:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:480a318a6d5982a1f15b8d84aa569503702d065d18f0f35a2a4b52c555511df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa37e9d70009571f747f15fa8a4f2ca3e691da6ede43eb6d038837ab7bef5be4`

```dockerfile
```

-	Layers:
	-	`sha256:593d1b4027724800ad6516a25e3c3a0cea80b215a2b92e92c087339de532320e`  
		Last Modified: Tue, 29 Oct 2024 00:13:33 GMT  
		Size: 30.7 KB (30656 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:f1b7ab959d4545b483e87556aadadb88b04318022f41804b5b40f3ca491d2a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36391562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87718807d9d61dfe73b5b93112c1b2aa1f0cb5ec7b8c07e4b9d2f8a9541ea087`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8891b9ad797d2ab4286de450552ad1b01432f19b40117a77957da9b776aef79`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 4.9 MB (4893353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b3a40bd171b3a6ed00704448d5305b7d2f7669e004cdd18e65546b736dc82e`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde5bf81ec482329b1688271c76052169e5a044348e29d19a69c9659d09e46e0`  
		Last Modified: Mon, 28 Oct 2024 22:51:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0981efdd5604896b2cdec1be88d1b30edcf11f73b2c9edd70d79bff41860355`  
		Last Modified: Tue, 29 Oct 2024 00:00:10 GMT  
		Size: 12.5 MB (12504592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd13bc5d3c9220e85ce2330d2f8c8ff60f7d759da8b40209a68ee75c82b6e5`  
		Last Modified: Tue, 29 Oct 2024 00:00:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb86e9dd6b86df429b0d87efb62d5353ae8935f28187d563c23181e2428e38`  
		Last Modified: Tue, 29 Oct 2024 00:03:43 GMT  
		Size: 11.2 MB (11184886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1efc26dbb93281c383155e8416ec802c3d060b784dde011fa95fb0f51baf4`  
		Last Modified: Tue, 29 Oct 2024 00:03:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d8a5299803412a01c3aa6c21876c35b4e6c86ec3f95aea0105a3b3c5016ed4`  
		Last Modified: Tue, 29 Oct 2024 00:03:42 GMT  
		Size: 19.5 KB (19457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da15edaeb095e4c5368fa7ca37ac8b8f85f465aa20c675e02a276548dbeb1a0`  
		Last Modified: Tue, 29 Oct 2024 00:03:42 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbe31f88c62699a14e8346b98dc3f07c1697762c37c6c561e7af39c80535e35`  
		Last Modified: Tue, 29 Oct 2024 02:30:08 GMT  
		Size: 160.7 KB (160727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f22db7a1e910e57f802a3d22572659422315afb940064db366bede5c4d7471c`  
		Last Modified: Tue, 29 Oct 2024 02:30:08 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3080883073dcea89cbf1c75b38d05ad4bf2b8de9466357739a05a578d1aa5`  
		Last Modified: Tue, 29 Oct 2024 02:30:09 GMT  
		Size: 442.3 KB (442336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eb2a8ff1a006213151f23c7029d36da10dba2be77892b185187c0e8213a6b9`  
		Last Modified: Tue, 29 Oct 2024 02:30:09 GMT  
		Size: 4.1 MB (4073354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb1d277dccfe00a84c3163d82db1a4cdeff83160e20bbf7812be45bd6791a8`  
		Last Modified: Tue, 29 Oct 2024 02:30:09 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba57fd21210d849e913fffdd03071426755b6288b9de7fd0d4b582ed1deb7694`  
		Last Modified: Tue, 29 Oct 2024 02:30:09 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:362207bdf4eea2ce8a4be0387a37526c43a08b61bb46e40a1243231f38ef3c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c4ae259f14c32b76d2366fa0d45ae7ecca149d97c9f8a604fdff2f8678b426`

```dockerfile
```

-	Layers:
	-	`sha256:2826faaf73bbeb3b5f26466cbc0941ed0092689745e9857a6bb6ede556bb1fd2`  
		Last Modified: Tue, 29 Oct 2024 02:30:08 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:2d0a2921481d79414053169cdbed5e59696983468cb1b63774811d8e681ceed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41264931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee1ba8a09c67b43d304b898d6d864b4fc1b649edea26065a6b4c6990b41178a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264df05ba819175767d82cc01697d7f7d371d0468273ffffb308b6b85bddcc7d`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 6.0 MB (6044737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19693f1fe8f6d96ea9523a5fd361b05163bd3c9b0476d400db2e699e40aaa92`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebef5cc9bae3e7065c78400102c221ef766371a514d412f543ac0fdb2cfa943`  
		Last Modified: Mon, 28 Oct 2024 22:31:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3a7d1435c64168e62d04e6dc930bce8c2c9d72ff50f621ad45fbae75094ae`  
		Last Modified: Mon, 28 Oct 2024 23:27:14 GMT  
		Size: 12.5 MB (12504588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797fed31a880e49e2b875cc9637f576aa56323a78858370575b6570d624bdd7`  
		Last Modified: Mon, 28 Oct 2024 23:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b532e4569c1c6e32f2d86bf81155b24171097c168f8b34f5b09e9542f1fe3e`  
		Last Modified: Mon, 28 Oct 2024 23:32:57 GMT  
		Size: 13.2 MB (13157088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986bb0644af5b53b5a568dd7dc5236ac4ac9e6271360a79be9cabe28cdc2377f`  
		Last Modified: Mon, 28 Oct 2024 23:32:56 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be7e634a6d1809644c8d22623696cc79f58fbee72ea3a560437e698f403c6b9`  
		Last Modified: Mon, 28 Oct 2024 23:32:56 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea889a4ed9282477001f97cd4c44084e4bb35a72523478410f0f31a14f72343`  
		Last Modified: Mon, 28 Oct 2024 23:32:56 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534be61ff476c7d975047f64f9c5ab1e7662cc63118256381979bf30b65ecc28`  
		Last Modified: Tue, 29 Oct 2024 02:32:41 GMT  
		Size: 815.8 KB (815784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56ad6bcb32d74e0c5bbdab6c900d66125650c151ca05c4306536df0f10350a`  
		Last Modified: Tue, 29 Oct 2024 02:32:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33da7c19d77991ca7fb750aa9ed21677da659edb543f8824f6d878bfcce556ca`  
		Last Modified: Tue, 29 Oct 2024 02:32:41 GMT  
		Size: 544.9 KB (544923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f647082ce712bc56d4bbdd83e734b151f78d6167469a2bac5929c08467bbbee0`  
		Last Modified: Tue, 29 Oct 2024 02:32:41 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01195b5a4a7d473f59a5b75f5e07c16704aa3f136e0754c2760274c6828a6ad8`  
		Last Modified: Tue, 29 Oct 2024 02:32:42 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7376177d85f6d44f5798558f18c942591a7c057042a386651e31b1845299922`  
		Last Modified: Tue, 29 Oct 2024 02:32:42 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:9fae9cc8964a12413595b99b0bbb71fad3010c7cc079d80690ac25f02786a7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de54bcee806abd0446b20a9df4e525a6dfdd5d4092fe4d875a60957822cc9cb`

```dockerfile
```

-	Layers:
	-	`sha256:1b577c7082956b52492f03a84346945f61cf0a5e35ea301472e5893b8e06b836`  
		Last Modified: Tue, 29 Oct 2024 02:32:40 GMT  
		Size: 30.7 KB (30691 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:7ad1583aeac475f2f0c4bca451e22e2e5a2c9333414da360ec768fc04e09629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40003395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0375aedc9fbb54288c0402edfffadc21eb0467897b8043f6dad6b759cc24a7fa`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef060ef573b63f5ffaf825c763750b259259326b5011c0f331710340b895c0db`  
		Last Modified: Tue, 12 Nov 2024 02:09:41 GMT  
		Size: 5.5 MB (5468325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a8c53682f3a22bdf799be285e3d01ad36fa4720b20c5e9df4becb305e4ddb8`  
		Last Modified: Tue, 12 Nov 2024 02:09:41 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93926b72d249094c803c9ce94982e32db96a0b45b6071a67e9bb8e5cc60e3de`  
		Last Modified: Tue, 12 Nov 2024 02:09:41 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8b2396231d9708fca41827cf212309666cfb61f1b9f72761e066031c67218d`  
		Last Modified: Tue, 12 Nov 2024 02:09:42 GMT  
		Size: 12.5 MB (12504590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96be70f5935272dab97abfadf9fa6ce3017798ae30300955b0c958e96b67c55`  
		Last Modified: Tue, 12 Nov 2024 02:09:42 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e104c10a0eba9eada8c861f3ff549c733022a86483aeaee5f6ce6707422107`  
		Last Modified: Tue, 12 Nov 2024 02:09:42 GMT  
		Size: 13.4 MB (13431749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d1e0ef1200e21c23ceea730c804dfc5e1f5940b92db341c29ef47b040fcf2a`  
		Last Modified: Tue, 12 Nov 2024 02:09:42 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937ff2d9fa7c00f49c1527f3c3bc2ab3490600468a068617ba018f24749f84a6`  
		Last Modified: Tue, 12 Nov 2024 02:09:43 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e445e1d0ba8eeb5e597335ba1516a3e8ef8b83cc6abaf5ce518b2de54d2337`  
		Last Modified: Tue, 12 Nov 2024 02:09:43 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e49faa89a90f9aebbfad5f9a73602fcb930e521e2b56aac6900f5208621052`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 529.3 KB (529292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9433252ba198639607f5b6f04f55647599b59a28528f995b8a8b6eb57100ee5a`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de8d4b8128a9fd8947f09707c9507510352d26e544393fbf5278a58a52e78d`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 489.8 KB (489849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa29167848c45a02b91ed140375c2d0135043fa290474ad9d6a7303102ca719c`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 4.1 MB (4073356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d588f81048dfaee1c824fbb3a6a6dcbd60453c5cb240d66d486501f609677`  
		Last Modified: Tue, 12 Nov 2024 03:14:30 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13538060ffb1f11c43c74cea5024579948d89a7bdb63e0301ef40c7eeff890b6`  
		Last Modified: Tue, 12 Nov 2024 03:14:30 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:a28912ef3824a6aa4e8376838f5666b3cf2e154ece9b3b878d86ce69d79f5380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c45db0ef5721bf7a8cd442317c00e67a09c0eb2fc4aff2fae580b5aefb1dda4`

```dockerfile
```

-	Layers:
	-	`sha256:106dbd374667085e9a4d0447c987dcd267156c68b98266092ca01d27014b0df9`  
		Last Modified: Tue, 12 Nov 2024 03:14:29 GMT  
		Size: 30.5 KB (30461 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:73710985f2ae4701e72ccb2b49aef304365212e1d99764903a0e748614879af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40111774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4c25d9896ff8143669966e55548c92e6031985a46300ed56b8884009b83d70`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba6d71b7953e5a539b29c94897df8abc5c8913c9f8cdd74dbe70ff782c2c41`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 5.6 MB (5569355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e67a84c448da04979ae1b4f74b62a87996c3c2cf1c1638e98af4254a5cb01a0`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6cb5989066db70ae6367501c203d0179801d5021cba5499e956b2f3adf9274`  
		Last Modified: Mon, 28 Oct 2024 22:19:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea498a431f81c35411e8d2726248d055de99a058164b0c45ea2c93f04d42640d`  
		Last Modified: Mon, 28 Oct 2024 22:54:08 GMT  
		Size: 12.5 MB (12504601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f257d54c64bc298761ccb488c12a2f2d2cd2828444e6e29970430fb71146efeb`  
		Last Modified: Mon, 28 Oct 2024 22:54:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302076ca16d79aaaaabcb5c57b3d1a899b6d8032f29eb69b9566d9d7647c1bf4`  
		Last Modified: Mon, 28 Oct 2024 22:57:16 GMT  
		Size: 13.6 MB (13598732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1406f8afc5f35c90622217eb54dee1993d60b3ba684248da4980c303937efba6`  
		Last Modified: Mon, 28 Oct 2024 22:57:16 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbaf9f25bc2536b9a5faef80049c5e3588377c0fe3b5775749f7e1f567b464`  
		Last Modified: Mon, 28 Oct 2024 22:57:16 GMT  
		Size: 19.4 KB (19428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94ed671cee4750fd5b295bba2ba7e9b492d138c8a2bb4fe735431204369f719`  
		Last Modified: Mon, 28 Oct 2024 22:57:16 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6a16e4c545bad961567483cff44b3779fb43b1ca3c15390f6bf030f70a2900`  
		Last Modified: Tue, 29 Oct 2024 00:57:14 GMT  
		Size: 208.3 KB (208310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826835b4888d10d301f332fd562d729a89c2e8ebb6363cdb0315cbcad5850687`  
		Last Modified: Tue, 29 Oct 2024 00:57:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2a6fec38897aa7c780346e7152d1f52ebb09ce72cef75aa932421c19593eef`  
		Last Modified: Tue, 29 Oct 2024 00:57:14 GMT  
		Size: 548.2 KB (548195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968f3013aa923d209d45b0bc866a34bc5d3c5be9f2d85c39044c1ddebc63db83`  
		Last Modified: Tue, 29 Oct 2024 00:57:14 GMT  
		Size: 4.1 MB (4073361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed38dde2d8c433f0521d93802e6ef8e20033fc8b4231ca4696dd77ff6eabfaad`  
		Last Modified: Tue, 29 Oct 2024 00:57:15 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07650b874550f1b533005e166849c28ecfc478a39acb5cd3d7214549c8c147fc`  
		Last Modified: Tue, 29 Oct 2024 00:57:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:51411078e5f91344757c04f371e97ea23d3fd410a5f384c57b9d053fbbd79e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4101016775be8c0bcffa4934e27175c1406213fb6360960a70827c6a3b6e49e5`

```dockerfile
```

-	Layers:
	-	`sha256:ad73c676fd89e9cfb0956af28a9c59347609046bb57da4d548cbeb5eea2d29b9`  
		Last Modified: Tue, 29 Oct 2024 00:57:13 GMT  
		Size: 30.6 KB (30591 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:89d02d878d3d96e0506bb8463125559c4892cbc841bedb3ceaee40eae5c71356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39380671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1441afc614b19d12050d51bd1823b3301823a5146f1b4d78d92878b06f7064`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.13
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN apk add --no-cache bash # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158e1a1fd0b2858e6d2273d854776681414260488a4eacc85eb382e65b038ecd`  
		Last Modified: Mon, 28 Oct 2024 22:24:29 GMT  
		Size: 5.5 MB (5530891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12dd8b0c5e061a98a59e1b4355e05fcd6718a2721a5b5d8646d6c3142b0aea`  
		Last Modified: Mon, 28 Oct 2024 22:24:28 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eb97483a4f916d04074d8958a40ef8a540bb57479c459a219658abd26db869`  
		Last Modified: Mon, 28 Oct 2024 22:24:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cce3a1ee94294492a9f892ec20c4c86eac7578825e193aecdb847d67035991`  
		Last Modified: Mon, 28 Oct 2024 23:13:36 GMT  
		Size: 12.5 MB (12504592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c7a7a01bf553853c50a0aeced6dfd746e1704dac091c98591697d6f095ac8`  
		Last Modified: Mon, 28 Oct 2024 23:13:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020a1bc4a635f849b716b373f57f2a482a2fdefd449261fe53b74fe4a4a8abde`  
		Last Modified: Mon, 28 Oct 2024 23:20:11 GMT  
		Size: 13.1 MB (13061832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a74895a2a1f02043b4ff2b2b623ab751f635eb3895728d67051dea0d8153c8`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ea7b63172b9c6f4df6822b3908a30349d0987dd21f35201eecd0b73b2d3c2c`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 19.4 KB (19437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607925f2f61e5707e9cef982684e4503c9e822f53b6eed98e80f7dfd1694765`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed36989d7909e7b485efa7cdb97e30af09ac1f37539ab1ae33ec2530052929`  
		Last Modified: Tue, 29 Oct 2024 03:04:53 GMT  
		Size: 199.8 KB (199821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a3145d726a264ec23306445242e8e86767707e620c6f4abd8f48b8855c607e`  
		Last Modified: Tue, 29 Oct 2024 03:04:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70303a5847291221bac90d220e77574c979de422a59918bbfd4eb2c87bbd60b`  
		Last Modified: Tue, 29 Oct 2024 03:04:53 GMT  
		Size: 511.8 KB (511763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7dad3be233331ea8bfabe37ea25c9277b150e7d35112694a953059fca37d8b`  
		Last Modified: Tue, 29 Oct 2024 03:04:53 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3f223ebf56246379e7be637b2e009f3cdf61cde5604b1698d6732c506695dc`  
		Last Modified: Tue, 29 Oct 2024 03:04:54 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc82ddd6244e95c6264b7566897cdb2cbd1ce0e0e57f1a405ad9a2b32328f0c4`  
		Last Modified: Tue, 29 Oct 2024 03:04:54 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:f49138a460c7d8ac8049f10047abe356fc6d211c92005fa35ce210bb3f97f4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1846934d8f80bbb1f5b25e83ac2c57d9fd97c04a024c7156bb23bb3fae9ddebb`

```dockerfile
```

-	Layers:
	-	`sha256:a0586f61a0e49635790b76a8793352193fb9f5e590cdd05f1a12829f9a128663`  
		Last Modified: Tue, 29 Oct 2024 03:04:53 GMT  
		Size: 30.5 KB (30542 bytes)  
		MIME: application/vnd.in-toto+json
