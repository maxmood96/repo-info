## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:98a467eada9fee7a7523f351ba161ed959a1aff921cb0a674168dd10f7e7a5b6
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:be08db30a0dde3f7512628186935075adc166910a098a0959c0bd69ae4ea9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43266057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be86fef3887b1cdf5928fc49536d16057d430fd4c7b761ccb4a0bfdacdc0b976`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b16f419f0e84d206d1c75bb7e7dc82df08577c70c1a4666c51198d49e473155`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 3.5 MB (3463767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bf062eed91850e9eef639f785d294e0217ff17d118cc2b508893a9e13dbbba`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3739b494ab73f745d356975c51d0786c7432eaacec564f8e1c70d414795320`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f10ba94659a998829a6d7a9ca43c3230072facb64e82e187c031a6935bbaa89`  
		Last Modified: Fri, 24 Oct 2025 19:18:03 GMT  
		Size: 13.7 MB (13665833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ded0a5d63cf08eb3bbb2ebbe2ae2c31bdc6a8ff9ad3ae62f6ca214a678e4dc`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783bb9d009dbe9189b962849a49d19d820a1e4c97a17b2d3a5050917c481f2c0`  
		Last Modified: Fri, 24 Oct 2025 19:18:03 GMT  
		Size: 15.0 MB (15029604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0212706b5f97db8f7bdde5809473b6a967163920afffd25ef5b5a082fb734a3a`  
		Last Modified: Fri, 24 Oct 2025 19:18:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731fc6ecbbe00d75552781db246d614759e94c4377912360ad9f5cdc579d80d5`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 20.1 KB (20081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78761c868be8f46ff256cc8a2cad5d4dbc2810e8b39b3b002ee7e6dd3763b260`  
		Last Modified: Fri, 24 Oct 2025 19:18:01 GMT  
		Size: 20.1 KB (20072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fb1c507fe27657440005412bfdcd17a8524ea7273820a3cba167a4440e6c4d`  
		Last Modified: Fri, 24 Oct 2025 19:18:02 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578827c873b3e06d05d2d3b289374d69766ba8cd995ab76ee2776055f7499157`  
		Last Modified: Fri, 24 Oct 2025 20:18:45 GMT  
		Size: 691.4 KB (691426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f734dc37299f17cb965d8c1255fda9a6f85b44b2360c4a4e71652e1a5aae1a0`  
		Last Modified: Fri, 24 Oct 2025 20:18:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7c095ca3c084377cbb2fc3f0fd2243934e274fed8f0fda746b6a6f610dc45f`  
		Last Modified: Fri, 24 Oct 2025 20:18:45 GMT  
		Size: 481.8 KB (481759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2631c4e4472cec9257b7571c2b24ad115ddb811b3a8c14de2e0cd0a0eb3a8f2`  
		Last Modified: Fri, 24 Oct 2025 20:18:46 GMT  
		Size: 6.1 MB (6073648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4d683162cca3e72c2b61acb51b9d3244ddc09272846a3ba76243505bd54518`  
		Last Modified: Fri, 24 Oct 2025 20:18:45 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7954686fc34484b7c60c2d28c70a082aa14f12333ce55203d951df3dad15bc6`  
		Last Modified: Fri, 24 Oct 2025 20:18:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:a541923b3dec10a46005fe9284473f338916ed6363e818fec3bdd0d5253c12ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636fec8d6ff354eca80af0ebbc935b8c446454b4640f372d2aabc05c05266f12`

```dockerfile
```

-	Layers:
	-	`sha256:cb12a1ee44886cc630112dfcfad402aafc8f23741c06f7a13980d2918d9bc5ef`  
		Last Modified: Fri, 24 Oct 2025 22:43:41 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:137598449a712349352bcb69406dc0e23900362b78dcafade7d321d7ed98f628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40940069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a78a3f630571b4294793af716e1f334de9b6460ffdec7d1abc4fedbaaf3a60`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92403a7591eac3005b3589514439adb33ddfd0cdf573f41acb7b2f59795ad7`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 3.4 MB (3428323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2061b8000d4d8033b2b8390df19f894b799a70f19e1b18ad00ff070e834c448`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3886f04bed6533c2ca443852c6834c95a2bf593fa2353717502597cdc730e4`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd1a9174acca2de2efe60b1e5cf175e94ea545d207404d68eb7a6926995659e`  
		Last Modified: Fri, 24 Oct 2025 19:26:52 GMT  
		Size: 13.7 MB (13665833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4a424954978a6cd3cba5774af71e47d6c97e6728c83e3899b1fcd10ba52333`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac9d73dfb30c08de1abc5306032f9574f0eba811d4d4090f9fad874cc718c8`  
		Last Modified: Fri, 24 Oct 2025 19:26:53 GMT  
		Size: 13.5 MB (13538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699cb4a2053f9254a0a4dfefc109b3fb39dffc96925f3e588dae2a715f359c29`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed039b4242793ac1048a40ccd9ecbe9b676e629a192474ad6a65240080e615c8`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ae72b7943613b0014374abeba4ba8bd402c01377243af8ac92c1ad8b0a5887`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9e2bd3858b40d6bea844272ca1d3348d3fcd072c5c34a56a519739edcf5418`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98358bc62b38382b25bfe3c5b7eccd1a9f17402571f7b03c45e2678f9ef1a`  
		Last Modified: Fri, 24 Oct 2025 20:41:15 GMT  
		Size: 191.7 KB (191697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c2c851678d290b0938f21a9e4e7bb2da87cc96fff7133d7361fd510c411190`  
		Last Modified: Fri, 24 Oct 2025 20:41:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a5e5f37f04772ecfb29140027990168d20270ed4b0e92507b6a6845bcfab9`  
		Last Modified: Fri, 24 Oct 2025 20:41:15 GMT  
		Size: 481.3 KB (481306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62659e812b1cef25877fef794db65d7861f87b31e729b2c40a70ae1956635ec5`  
		Last Modified: Fri, 24 Oct 2025 20:41:21 GMT  
		Size: 6.1 MB (6073654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fcb29c6101582ab2314db4d7fecb1142062103b9ce4e93fb7165809ba313c5`  
		Last Modified: Fri, 24 Oct 2025 20:41:15 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5946c6d58f7855f6f5ce6be1f8018ab1da5e692f5dd27549ec29977dea738d`  
		Last Modified: Fri, 24 Oct 2025 20:41:15 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:31476b5ae07c36d568131a6524c13c37e71b214ca08a874774fdf2984615564e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383522a0926bf5160e35148445c3d35e423190fbec8557d2beea158288dcdc13`

```dockerfile
```

-	Layers:
	-	`sha256:6b54ff21de8aaaa75d2365a48b4179055c78f417f644d739268fa1684b06ecf6`  
		Last Modified: Fri, 24 Oct 2025 22:43:45 GMT  
		Size: 31.9 KB (31856 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:73f00b80bd687a7196eba9c1278295f4c97faf46db331d644818531d6a3ea0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39667752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744794c533f6139171267f16b3cf97b71d25f0e19abdf442480fbbf591dc9ba`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349fa73d15fda6e28286a047cffbfd7d4275678c442d4cec2a15b09c4fbf5c0c`  
		Last Modified: Fri, 24 Oct 2025 19:50:35 GMT  
		Size: 3.2 MB (3244400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8c91c07b658e9a347224bb1ef8aa048ce91f902de5d1f3bef44f2e4d18e24`  
		Last Modified: Fri, 24 Oct 2025 19:50:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1492d25c54ff9f9187c612732f3898ae4b5c40662f618074d3c45152406262`  
		Last Modified: Fri, 24 Oct 2025 19:50:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013c3bcbe172d251263781a31499d3b042ca272e19649db50a6dfa3b4a7d17fc`  
		Last Modified: Fri, 24 Oct 2025 20:00:28 GMT  
		Size: 13.7 MB (13665817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f0aa4e5931a543e703c8d53689526588382950c4e015545fa6d12518fc49ad`  
		Last Modified: Fri, 24 Oct 2025 20:00:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90920be6b93ed3b83d316cb17a5d00e9f2ab3c71dc02e671958d964f3fc0c9`  
		Last Modified: Fri, 24 Oct 2025 20:00:30 GMT  
		Size: 12.8 MB (12784622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38170f079b3ce128c79538e13cf4e04639aef38b6babbc7215211f518fa202a`  
		Last Modified: Fri, 24 Oct 2025 20:00:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dca837d0df052abed3731f4216e5f7eed25907f0970a05ae9d16425585c006`  
		Last Modified: Fri, 24 Oct 2025 20:00:27 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1732bb542648e8693175825b75d8ddf36f284132c6c57fc13f9e7ded119953`  
		Last Modified: Fri, 24 Oct 2025 20:00:28 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e3dfd31d0734b5c6072582a10e879b23a681867d7aa49e6ff93bd406461c4`  
		Last Modified: Fri, 24 Oct 2025 20:00:27 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693932f4a1341b3ea5ca5769efd59ee750a8bf6a4eb86a67d13bd66f3bc650c1`  
		Last Modified: Fri, 24 Oct 2025 20:49:03 GMT  
		Size: 178.6 KB (178601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc624732fa958246cdf084b1b51c729584e470645b8dbc1c9a1a025c1c42fa1`  
		Last Modified: Fri, 24 Oct 2025 20:49:03 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7879d13333b41cd373f0f7109d658611f2741e8d4c9caf7106e4f989cb4d0b33`  
		Last Modified: Fri, 24 Oct 2025 20:49:03 GMT  
		Size: 442.0 KB (441989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c2ff56f0a0117acaa59481d11c22c43420a15246d94f4a98b643f758b5ea99`  
		Last Modified: Fri, 24 Oct 2025 20:49:05 GMT  
		Size: 6.1 MB (6073651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df551a2db619c0054e863aa16a8cf0f28a2fca4fb7b6c47674a111c9cadebfd4`  
		Last Modified: Fri, 24 Oct 2025 20:49:03 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11bdd0ec44e8d9f5c88056bd64b37958c874242e916650824230e2d4a8091ed`  
		Last Modified: Fri, 24 Oct 2025 20:49:04 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:a97dbb6dcf17476b676cba301ba78653324b35dce66a41fbfe60a5d72a60a7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4db4832eaf59b27e24f2cfe1df53effb0773fe6fa6f2fd26a3c59c5c5a3b5`

```dockerfile
```

-	Layers:
	-	`sha256:bd05bfd52c9a7859a1c59b77c4a6c3ce3c0f220fa6e6527f979381afeaf4991b`  
		Last Modified: Fri, 24 Oct 2025 22:43:48 GMT  
		Size: 31.9 KB (31856 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:88bc19b77e3a1382b847c110255ac77c2fb2d0bf0856c188454ac52bfd730975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43212491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bab28e9f2ba71eda4a71a333a9f6aba61b6213ab42a0532062448d00c60c805`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8e5431b232ea17dba82b276ef0be159d4f17c1baa4241a844a7b01c3e1637`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 3.5 MB (3466793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ce22d647b16d86d811ad7012fcb0a30bd7f4c67d6b03c589ec46713b5993b`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8bb39caa5c2a35dfb662b748f9bc7d43e825948833fd999fa42e2f41eb5157`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1173d7d39d051594d1214455df0e9b827af087c50bee98d6218d22df6a3b29c8`  
		Last Modified: Fri, 24 Oct 2025 19:09:34 GMT  
		Size: 13.7 MB (13665829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9906ab540a197eb6d0e8fcebc12aaf96b4292fcd43f1e3b3ef22ffcec0ec5e`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004bab9208b7f170c07010bd52092b87b8d52b74760cf8226e1916d24d9bfec`  
		Last Modified: Fri, 24 Oct 2025 19:09:33 GMT  
		Size: 14.7 MB (14662584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb6d29b1fbefe333c41f572dcfb804cd86e704f85c1335f6433f427cc0188f0`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8321364cf7bc051d33580705ee0ccd3772e7556ae3e3d887eb479cb98478d345`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc5b613e04a782a82701623cf30a1144da2c73fa60ea319a3823b573d86386`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28308b34248ebbd014e8930c21a5e224bc3166644a6c194dd37792c839d8c71a`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dedfc021cfc0a1bcfbc25964957a672bb99afd52949b56eac184248e2601a4`  
		Last Modified: Fri, 24 Oct 2025 20:18:16 GMT  
		Size: 611.9 KB (611867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a9feebb85e9b84ec0d9d6aed2bfb20c5f94a0c9f63706f59c26c0fd6b5cea0`  
		Last Modified: Fri, 24 Oct 2025 20:18:16 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5923d9a37b0f48b229e15af34de035b02669a6ec877e6afff929a3013cc64021`  
		Last Modified: Fri, 24 Oct 2025 20:18:17 GMT  
		Size: 536.6 KB (536573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f20979329ff5c2ea02a6e6e2ad7019a9eab820f09f21fccf2a808288a868af`  
		Last Modified: Fri, 24 Oct 2025 20:18:18 GMT  
		Size: 6.1 MB (6073651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34a807b70193d2fa93869376319ce23de5ed7837dfc6ddeaff6054f1c6c9723`  
		Last Modified: Fri, 24 Oct 2025 20:18:17 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffdd5c010c7a96d86782fb47a56c2ffa66b99986c143f461ef22d01b086713f`  
		Last Modified: Fri, 24 Oct 2025 20:18:17 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:9689a440a258365076aa5ede0014c16d5780935f9ecf28662e28efe473b5d5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599fa2dc6dd5b5fe9202e34696b34fa77bd1327c96c69f966988882d686422d5`

```dockerfile
```

-	Layers:
	-	`sha256:570c92e3a640206fb2b83ec30beb091512ebf7cdb63c63a65b4a4a4413a3bf55`  
		Last Modified: Fri, 24 Oct 2025 22:43:53 GMT  
		Size: 31.9 KB (31886 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:14f3067688ca4dbc0735224ca841538b12134e39ba6e78b5016a5de6545f7e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43577233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245c5e456ce6c0578fc92ccbac3cfa2b1161c88041b858db850fc2430838680b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1444848509bdf400cf25254b5a91a7dfdeec4142f50ea44edac57008365d37`  
		Last Modified: Fri, 24 Oct 2025 18:35:35 GMT  
		Size: 3.5 MB (3522959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e864fc1ebc7c6c71faeb528833ccbfc642ca81339edf62dc9fb9bd4038bd68b`  
		Last Modified: Fri, 24 Oct 2025 18:35:34 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39398f3bb71f09f3f0eea379781fb08dd54d31cdb3be565275e22779b52139b`  
		Last Modified: Fri, 24 Oct 2025 18:35:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879b50c2e498ab549b3e24742c30ee380bcb4e6f018700b70b5518424590f74`  
		Last Modified: Fri, 24 Oct 2025 18:42:33 GMT  
		Size: 13.7 MB (13665807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc38abad9de38268e70fccdf96fc473b958031cd3863312a5d0046cf5b76b3f9`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292cc7f774253f31fc2f7a2f1eee4a866a4a145bb10358871dc4a27f1c8b3df`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 15.4 MB (15430524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb66778eb86cfb8959efd588322e477a01cd1167e5c3a0f397c7804b7a51fe1`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272bacd0bba02c93fad763ef48351d61c4c7774d19530c32fe056fc0cd32d50d`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 20.0 KB (20045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6420922474cc847e8cdb4b5cd90cd80c7335494d22836fcb013ea2a6b77ffcd8`  
		Last Modified: Fri, 24 Oct 2025 18:42:24 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3196a033c4b3d6b6242ae63336336d7ed101f0728e37b07b193aa70e566937e0`  
		Last Modified: Fri, 24 Oct 2025 18:42:23 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b0e65f2f82b9478177f3e3aade484e0d26fb3689962181e007ed65d8257962`  
		Last Modified: Fri, 24 Oct 2025 19:19:52 GMT  
		Size: 718.4 KB (718372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d3ee87e0c0afef86124588af98aafefdcd1518e204404aa9536a68d57eaa27`  
		Last Modified: Fri, 24 Oct 2025 19:19:51 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0064cfccac2dc4c1b41df12f78fccb25447b3b54c6666c4413da8e7c7cdd8cc`  
		Last Modified: Fri, 24 Oct 2025 19:19:51 GMT  
		Size: 489.5 KB (489474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719a0071d06fb86791d44eebcfaae158bc58c53b1f3e5945961f5af93513d8fb`  
		Last Modified: Fri, 24 Oct 2025 19:19:52 GMT  
		Size: 6.1 MB (6073651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b42c576731416e66df374984ed48a2e08d397a9cf83d2ceab055c9993791d46`  
		Last Modified: Fri, 24 Oct 2025 19:19:51 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136b1724466d0ee20e076111a65104ce6afef8d274bdc6b0401ab4a7bdb91651`  
		Last Modified: Fri, 24 Oct 2025 19:19:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:17f525d64a97d6180aac6c6731dee523268283599a104d6f3cc696020cd30f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe0dda82d4f556315b9c0812406fb33f59fec337ef7f2158cd70d3fe928ec12`

```dockerfile
```

-	Layers:
	-	`sha256:84c7dfc3c7b4d7505b0e0b388d9522424133ecf629b7512eb0bd675bd4ebe459`  
		Last Modified: Fri, 24 Oct 2025 22:43:56 GMT  
		Size: 31.7 KB (31697 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:f804ab80da81a0c920b17b7b532074dcc496f7dee1e9c2191a7d56901b51badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43425184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b13f7893b1cca29838286a5dc08a720e7e26e8c5461325d7b7c1eef6186a538`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38c73f3ff68aca00580e73801a535a988fbae408500c93468879ece8ebc678`  
		Last Modified: Fri, 24 Oct 2025 21:07:27 GMT  
		Size: 13.7 MB (13665827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a00a631bb9c16ed735305bb12fd93d2488d0741a8597255ed7563e7d728ff6`  
		Last Modified: Fri, 24 Oct 2025 21:07:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55347fe38a80eed1f01b266efd7062c2382aa6a2f9bcb42e78efbbf1c2ddc068`  
		Last Modified: Fri, 24 Oct 2025 21:11:34 GMT  
		Size: 15.5 MB (15505292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44493fd3399d4fb640eeb31a9b02338535a982da8853096a1d526fc5627371e2`  
		Last Modified: Fri, 24 Oct 2025 21:11:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca3bb9b3453d52fbb030ff35bdd522b794d57f08369bea5d464ec4f6f2fa2a`  
		Last Modified: Fri, 24 Oct 2025 21:11:31 GMT  
		Size: 19.9 KB (19879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e82f6144ff8ca5291c59732eea23f2490e28664ae61d222316906f7c807493`  
		Last Modified: Fri, 24 Oct 2025 21:11:31 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8269b0bcc9dffb336a47f8c1837b9817bc841800706a1822dc1847396bd65629`  
		Last Modified: Fri, 24 Oct 2025 21:11:32 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7e91571f7694c36f349e7cff8bffd1ef0bc0f0db3f435f98e96e7a6f3b2960`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 228.7 KB (228715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b413a561c55bd083b43fe7758f24e2af919d2d2c0c45981c34b45a21f741136`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041f8a6de0c5f08a6e94ae20c9cfc09906aecce685ddaaa4883d0267fb30077`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 547.6 KB (547612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1de770ffd78261057e0ca2cb4cfd0c3622f428d2813f327dfbb963385e2ebb`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 6.1 MB (6073640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dfba38719fcaaeea729596f397e8b7dfd34db9e3526fc68f920c7e90c9dba3`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db6300b17e9aacd69b2bb19f61a66adf029b677460d19ec54d13ea39d84eb`  
		Last Modified: Sat, 25 Oct 2025 02:53:04 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:fe4ec17dad8845e9d89d916f1f026d9c72f0f9937f0b1f122a85a1fc319f9e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade5601330ff641ff1524c1ac66a25d43ff17dd0f4261452aed72b1fe3aa6e7a`

```dockerfile
```

-	Layers:
	-	`sha256:d257a15268b34c93836c21f9053eda04c574254e23139c68ba7ea05e2517d058`  
		Last Modified: Sat, 25 Oct 2025 04:43:02 GMT  
		Size: 31.8 KB (31787 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; riscv64

```console
$ docker pull yourls@sha256:d4bc6a56344a19f3b26a93795fdc2ace89a5a858ab9757008f788568ec435b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42046925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd40bb5c9010ac2f01fdbc0809a0ea23a073b7fd208007c996791f9cdb7b6a1f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b115bacca67276dbf1b2b88c75a1d93a783abab20ad055d2f456784c91848a14`  
		Last Modified: Sat, 25 Oct 2025 20:07:26 GMT  
		Size: 13.7 MB (13665823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa643ca26895c691b4910d72fd561ed485d1c71232f505a04f7dcb490535d6a`  
		Last Modified: Sat, 25 Oct 2025 20:07:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac82528ef89ba199fa9a827c4bd8409f1c48e9bb940e815d244a616b3dabead2`  
		Last Modified: Sat, 25 Oct 2025 21:07:43 GMT  
		Size: 14.4 MB (14436751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b18b58be31334fa65bd1af859bd12db9fcc5f13a122f9f7f26b0722e08bfa4`  
		Last Modified: Sat, 25 Oct 2025 21:07:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7ff08c7d685eeebea163070b62df3a40314ab8a5edbe9cc8a962ee64270e8`  
		Last Modified: Sat, 25 Oct 2025 21:07:42 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9659e4ffdc323f83fa2235589fbe99b653368932da43087b6df6a7d30753850b`  
		Last Modified: Sat, 25 Oct 2025 21:07:43 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64c51340ef186f37942e3635e337fff5aa4639cd8cc3d614c9405eec594367`  
		Last Modified: Sat, 25 Oct 2025 21:07:42 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467e4ab2f6e7ee9ea265152eb1b6388f849f32c8017947a4a60e741d5c1a31bf`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 204.3 KB (204310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded03fa29cc82a92c417b50ead7115421d04f93e14af6cd05a4af658911612b`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576ce723b31fdce90206c2b77cdd9a89f9a57e6c9a37bebef25ecfe6f48c7c53`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 493.7 KB (493716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7812a46f6e57521a564ad307afeeafc623f1ebc9e895cd15c7c9462e50aa7980`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 6.1 MB (6073654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70792f053895dcdb438112d67e99c1652760ac8856f4310f6f32671a6a1ac665`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408e0884567099a9725f96c2e528d98c5c2df883511a025e627d17258a0d0a48`  
		Last Modified: Mon, 27 Oct 2025 05:01:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:ad6cf490a9048a35f62c269775352ec1e40439c1615a57a112cd9e8a9acf1c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2d7fe332b470486895f28f808e8ea1222e4abebb952e98f69832ea3a4b068c`

```dockerfile
```

-	Layers:
	-	`sha256:c91ad5a28449cf9f68e7c90225cef9d8169dd662089d321d73df7622ae164467`  
		Last Modified: Mon, 27 Oct 2025 07:42:52 GMT  
		Size: 31.8 KB (31787 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:f736b21e0c52b85420f612fc55bb5825474ad1e65c751840bc1aa773baeb5964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42772795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf31274dd1595777e614dfd981eacb81b9f21619bd5165d2464a42c23477f02d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN apk add --no-cache bash # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea27060aabd36ff31ca9055725e9085bf08b94fc0d4b40028e0d7c21102f40`  
		Last Modified: Fri, 24 Oct 2025 20:03:31 GMT  
		Size: 13.7 MB (13665851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70515c51ba3110abd59c349a4cca83963c57d9e8eea1f5a9531ee7dafa31ec26`  
		Last Modified: Fri, 24 Oct 2025 20:03:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77309d755a588d7c519ed0deeef546e0b7cc1b47be8bf73c7d88f3a7b0fa2f7`  
		Last Modified: Fri, 24 Oct 2025 20:07:32 GMT  
		Size: 14.9 MB (14903510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359170f19924c1507ce488c65f65b9fff6ec51c9a2fbb6f4f3d505f1d0b9410`  
		Last Modified: Fri, 24 Oct 2025 20:07:30 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6e3d5e31fff153abe27e280bcabfc2578db765ec334b995b7f2a8281c69c4`  
		Last Modified: Fri, 24 Oct 2025 20:07:30 GMT  
		Size: 19.9 KB (19879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5dd3025b70cb276637dd10d2258bc050dd4d73a73207ac33f0a02cae9ccb18`  
		Last Modified: Fri, 24 Oct 2025 20:07:30 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b46d8c8f6d7fdd582ff610319bb0a56f3918e50848507cc628c7aeafa517f3`  
		Last Modified: Fri, 24 Oct 2025 20:07:30 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77c0b3a0ef07ea88d0c6dcc2a6dc48d03c9fe01eaf6f3cf693fa7ee154af64`  
		Last Modified: Sat, 25 Oct 2025 01:55:32 GMT  
		Size: 220.1 KB (220056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec199797beca21074e7d5b432399bc7cba63b72b84ceaa9cadcedb8fdce29e6`  
		Last Modified: Sat, 25 Oct 2025 01:55:32 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c8469fe17525d880f295ababaa2d24866f2e76a462e555a0a9d62e2f071f6f`  
		Last Modified: Sat, 25 Oct 2025 01:55:32 GMT  
		Size: 510.6 KB (510595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d202a278bc8d699c20e3295b84cb2df7644a569c2bb0d16fe36f3a43ba04454`  
		Last Modified: Sat, 25 Oct 2025 01:55:33 GMT  
		Size: 6.1 MB (6073651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43004b63e132f1baa683ec95b0af5db201c44d71acaaa88b7d65c9e1f219131e`  
		Last Modified: Sat, 25 Oct 2025 01:55:32 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d50ad245d58e6689c3829609c3e940d7d1a07b3aeec679683f6c952392bc23`  
		Last Modified: Sat, 25 Oct 2025 01:55:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:cbb04fbbac8ee07ff273e6a007eff383b5e88dcda7b2e9063b739ff5edb5d23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ccc255467cd2aa0dd03f0b2ea07b9d91b344f5e65c6e9e5252461b29f0abda`

```dockerfile
```

-	Layers:
	-	`sha256:af6316a949ebbee4882537b56d28acb6b0501abd01b555ed557d4a96b2ce7630`  
		Last Modified: Sat, 25 Oct 2025 04:43:06 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json
