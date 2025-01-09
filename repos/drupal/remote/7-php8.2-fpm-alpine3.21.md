## `drupal:7-php8.2-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:79d91598fad9e7fe903144a5cfbdedea8fb48ed09c9c9159928750b2435020cc
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

### `drupal:7-php8.2-fpm-alpine3.21` - linux; amd64

```console
$ docker pull drupal@sha256:3f177bb827fdbdfba6c2d46793610083a4f74da095252035c2f7770ce8566fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37501231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b547cf104002b68dca304eff1df3bfe458c6b39e8bb8f44852b9b2f6475d5fe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc38c2a4941ad701ab44fbcc1c173ad2a3f045a7eda86ff0a5e635a01e19853`  
		Last Modified: Wed, 08 Jan 2025 18:11:21 GMT  
		Size: 3.3 MB (3333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6ade65926f532f58d1495f0801397e48d6074e4877702516fdcffae116f406`  
		Last Modified: Wed, 08 Jan 2025 18:11:20 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb538d175e44179f87fbd4eeeed2138882929e119c2e54eac1eb45782bdb37`  
		Last Modified: Wed, 08 Jan 2025 18:11:21 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a8a15c7e4cde4985687b664d93da335bd978d49ab39d80d439d4c7435a923a`  
		Last Modified: Wed, 08 Jan 2025 18:11:21 GMT  
		Size: 12.2 MB (12172452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c424f018ab09a022ef6f5ac7fbdf94bc2b07d8ad69fa3c6e4dce4d3b322f58f6`  
		Last Modified: Wed, 08 Jan 2025 18:11:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d09a1edaa3b9bc5eb7c606e524a3585ae7bf01fd6debf8acb46603301c659`  
		Last Modified: Wed, 08 Jan 2025 18:11:22 GMT  
		Size: 13.0 MB (12972112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2af29dadb8d7cb7a17cfd22d5cf08366ed54d914814a53653ecd52a261057`  
		Last Modified: Wed, 08 Jan 2025 18:11:22 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46fd636a5a8b2c3fcb864ed662371b0d18fe0491f3c98a988e672fddf83fc8`  
		Last Modified: Wed, 08 Jan 2025 18:11:22 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff12f084cfd61483aef81b4e6e219fb00e3b75fdd125a34d8f6e16f050a6a5a`  
		Last Modified: Wed, 08 Jan 2025 18:11:22 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb37b22fccae73553d383114574ddc67cecf2248f717e0d4f7491b1dfe185ea`  
		Last Modified: Wed, 08 Jan 2025 18:24:01 GMT  
		Size: 1.9 MB (1918691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032d5111da01d93a83102aad33a6cd58d9c1f1741879a0932828bf505c1228a6`  
		Last Modified: Wed, 08 Jan 2025 18:24:01 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c0d0e2b75efb0582732f277ba6c7fed79bddff046ea23545abd7bbace5cc78`  
		Last Modified: Wed, 08 Jan 2025 18:24:01 GMT  
		Size: 3.4 MB (3429012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:97e455d974b53318dd4cbf48d500d26d2d9fff7fb4f57129c5492b6e6a49e96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 KB (306943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e924a366c0d1bb6bf214a92e171b764fc1d5657d90e1b3299b4f66e598b3818`

```dockerfile
```

-	Layers:
	-	`sha256:f992dd9daf9ada8499c5ab12c216095e49a76c6fa96f9f15d2689ce3a98715e3`  
		Last Modified: Wed, 08 Jan 2025 18:24:00 GMT  
		Size: 284.4 KB (284355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e34face6cf16a5748bbb0c64ba470fdf8d2a53758c74612dbf73850dfbc741`  
		Last Modified: Wed, 08 Jan 2025 18:24:00 GMT  
		Size: 22.6 KB (22588 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull drupal@sha256:75ee97de4042efa6f4f332a41c48636f94b3fb3cbeb1114f548d94815710d318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35408542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8198c5eb132755f6f61665b4338677517845ad9d8eb0a1240ef7577899a585e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcf1f0807671d9306ea1ab243153c7bcde2002f3c731d26bb99051fe4f57ad5`  
		Last Modified: Wed, 08 Jan 2025 20:21:35 GMT  
		Size: 12.2 MB (12172465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e635007a241ff0ec581b83304425db7ece2c2919bc3aa3af29309a5423e1f7d`  
		Last Modified: Wed, 08 Jan 2025 20:21:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2fea9835375f19cb5ef5661158b345e4cb7591a24260c63c626d4758bc2ee`  
		Last Modified: Wed, 08 Jan 2025 20:25:13 GMT  
		Size: 11.7 MB (11717513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e1a33da5a4522de8301357f5921b6794fd7b1b9eeffb5940d256eef4cbed05`  
		Last Modified: Wed, 08 Jan 2025 20:25:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1b4cc2b1f8124f010e83abfb27373237f419b9f532842409ea80bd2162769c`  
		Last Modified: Wed, 08 Jan 2025 20:25:13 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e23d11eea2bee8026228d526232bb4d3dfa1bea824231228c3d536c4f072c3`  
		Last Modified: Wed, 08 Jan 2025 20:25:13 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b762bfc98960416c7bdc5c359e5f94740486c2dc4a25d16d035763824972a78c`  
		Last Modified: Thu, 09 Jan 2025 09:18:37 GMT  
		Size: 1.4 MB (1391718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9c91f6e98afd342f690c3881419ab7af9caedf76bcb084f7ea7a8b12d4daa`  
		Last Modified: Thu, 09 Jan 2025 09:18:37 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402da21e9ee74a4a73d8405f0434ca36dcc00e8c86b8ea5a17d4dc5b532fb0a`  
		Last Modified: Thu, 09 Jan 2025 09:18:37 GMT  
		Size: 3.4 MB (3429010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:c36e933c81a3cd5a3130d9a0ad664f19c69f6a4f23b624db22914539650cfd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cff8ef120f532756c6653d67c053cdbb759458b3abb06745a3d9af1b8bfe1e`

```dockerfile
```

-	Layers:
	-	`sha256:da03fd0e25cf52686e3051d9c174d468f6a1cbdeec7ac0e6f40a45c6031f518a`  
		Last Modified: Thu, 09 Jan 2025 09:18:37 GMT  
		Size: 22.5 KB (22474 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b8e27897d4729a5989868a4645cfdcc4044ae016e1baac59cc9d96b259e2d118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34172606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8165493cef97359305a8b741c4ce84d82dbbc9b66d60c7c09d0d016976efc864`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e815eb8d83c83c8c21088e8f1bf0255f3d84f8e19bbada52f5e66bc17e905e20`  
		Last Modified: Wed, 08 Jan 2025 20:23:32 GMT  
		Size: 12.2 MB (12172459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7586341578f4ed430a6267fbf5372f9398bf11bdd25a6f820c8b7880cb80d4`  
		Last Modified: Wed, 08 Jan 2025 20:23:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648736d14064880b412d6e25300ab72d3b3574787ae8115bb7190f8beb14ecfd`  
		Last Modified: Wed, 08 Jan 2025 20:27:11 GMT  
		Size: 11.0 MB (11037442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e19c93e2cedf58146d9a6609fc2daf6e7a3c33c886c589deb1f14cdd5307415`  
		Last Modified: Wed, 08 Jan 2025 20:27:10 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef369aa2863988beab5502d9d60c358d7233c61dbba268f0fc93ad4054070251`  
		Last Modified: Wed, 08 Jan 2025 20:27:10 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7671a5f96e2975db25431d64dbb74379b14654378ec5c87e8eaf76aab128c1a7`  
		Last Modified: Wed, 08 Jan 2025 20:27:10 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004b702908b0d7f31e136e740cf92cf4ef0065bcd672c187c87372e3e1d53843`  
		Last Modified: Thu, 09 Jan 2025 10:14:11 GMT  
		Size: 1.3 MB (1287769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670859d646f17f435ff2c16a9df1cdd38ed2813f73cf22f8e6cbbb6e0af7907a`  
		Last Modified: Thu, 09 Jan 2025 10:14:11 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7c38153e175b59199688caad58b82a2b4c375b4f9f989ed23df17586891057`  
		Last Modified: Thu, 09 Jan 2025 10:14:11 GMT  
		Size: 3.4 MB (3429010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:7a4a796503213727837538af60f00e7db2bec171c15a8e6186710ad8bf4af086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 KB (304267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572fd9fde8fbb230a7b49d82b23f2529f832ffd438c2b40bed93f8a0ae29c7bd`

```dockerfile
```

-	Layers:
	-	`sha256:96b628606db11c3c2c6d02015f28f3e7b2b9fb4af7c1e018e247aed5d931d3d6`  
		Last Modified: Thu, 09 Jan 2025 10:14:11 GMT  
		Size: 281.6 KB (281578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f0d0dc0629b1b3590ff2995d20756bf816848b43315e10844781faf024598f`  
		Last Modified: Thu, 09 Jan 2025 10:14:10 GMT  
		Size: 22.7 KB (22689 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c59c1426cab03227878685e8c25ddef5fdce78ec3d81d8736c957bae7cc6bc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38114675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a69ffec67ba69f2de2f2e9b807a737a1f29903760a38313ada037a47a637a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e98e3ebd4b9eac921eda1970ff1f5a0b9c0d38b18db50388cabe3eb7e0fad1`  
		Last Modified: Wed, 08 Jan 2025 20:27:44 GMT  
		Size: 12.2 MB (12172491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a42363fc0749344f97c0ade7a9791d6a2ccfe4f280ecc86020e4c7b8826f8c`  
		Last Modified: Wed, 08 Jan 2025 20:27:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8bc2ac6f32f495869a1287afe252518ad77d6cec8ee1f1866d64cd5e5675d`  
		Last Modified: Wed, 08 Jan 2025 20:32:24 GMT  
		Size: 13.0 MB (12972653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d6898d1842ac861ad909d90f9a8b89a0c4a0704f84b6e62500af971d8ccb68`  
		Last Modified: Wed, 08 Jan 2025 20:32:23 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169fef3e4f30aac1d429a6c6d0ca13926ea458fad20b3e996db2272afafc4705`  
		Last Modified: Wed, 08 Jan 2025 20:32:23 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a57a37a2641c22aca5d567d1bdb83fc56d87ccf3a50774f6eb21a6d3d42add`  
		Last Modified: Wed, 08 Jan 2025 20:32:23 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846d28e14458e371c6c21fa0f15de8c359948458baf83765dde037d91f224751`  
		Last Modified: Thu, 09 Jan 2025 06:54:19 GMT  
		Size: 2.2 MB (2187026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4cde75c5d311587f3ce4b26e028eb501b19fc2d315c10b5b75ce8ccf0cd444`  
		Last Modified: Thu, 09 Jan 2025 06:54:19 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bbd487ff5476be6d0fc15049f4c61d2f58ea5fdb750d32765d050dca3ed827`  
		Last Modified: Thu, 09 Jan 2025 06:54:19 GMT  
		Size: 3.4 MB (3429009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:c249d5dd71d0d9b699e5102720f255bb3b302b7c72a95ba8f405017a20f75d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 KB (304320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc7bb82b9fadda1b38b615a3e37c9965e49adc2dc268e82147a740b0a14c5af`

```dockerfile
```

-	Layers:
	-	`sha256:558452ecb705cfe316d2fbcd8a7421f8ef3b1dec6f88e7f722248706845f8baf`  
		Last Modified: Thu, 09 Jan 2025 06:54:19 GMT  
		Size: 281.6 KB (281598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17edf19021ef691f8ac5f09ffdb352dd62c7dd56d3442283a1cc0e28a228ec25`  
		Last Modified: Thu, 09 Jan 2025 06:54:18 GMT  
		Size: 22.7 KB (22722 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:df30460dfb5c909a143037a15153bc52b378b985355aec9815db2dbd5de014aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37747354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0e9a8f39c512dd2e506cd1d9c271ad6696c127c9500906ffd1d7b90d750b8e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66be3593ce573a2b14939e1941978d0e58881d91504f2d72595016c3221f3f8`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 3.4 MB (3373759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acee8e51bd928e0a7b472f91061032b654014fc700b17a437487c573bd88bc6b`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacc8835cc2911f3b61dd517967f3e6d9e41efcdbedfaf9afdc7953a84ce9a0`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7089b6fd8890a4c3203d6d46aa159d10670399da5830aed860b70a9832faadc9`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 12.2 MB (12172429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dfa6306555c93ba76d340fe930d27a0c8257187b76e5e2751110073c35af4e`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f9cf45627020c3f68a26dc7abab24e4dcb3e23e178eb401bef38564817771`  
		Last Modified: Wed, 08 Jan 2025 18:06:59 GMT  
		Size: 13.3 MB (13293174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52dc4e6aed61c96bb05884ae5b51738a1a1bf6accc943794259947e79be7745`  
		Last Modified: Wed, 08 Jan 2025 18:06:58 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546ae297527880ef63de5a98f27b5fdd12c75795188752f53d75336cddff5930`  
		Last Modified: Wed, 08 Jan 2025 18:06:59 GMT  
		Size: 20.0 KB (20030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be962d299448a346e757674d37a7a10ef6a3d7853ca4fb125e88c5955c2cab12`  
		Last Modified: Wed, 08 Jan 2025 18:06:59 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8b26f404f627d530abfebf772f4ac46eac04cc653cc471f3ca575bafb06d7`  
		Last Modified: Wed, 08 Jan 2025 18:23:58 GMT  
		Size: 2.0 MB (1982196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf91573031844c274f7ad16180ec64d0ce1558d7f7716597ab994d95b7a5321`  
		Last Modified: Wed, 08 Jan 2025 18:23:57 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c2e05e63ee8362dcfb03f00057ae54be5d7a8fb58f8a687fbd97257df69db7`  
		Last Modified: Wed, 08 Jan 2025 18:23:58 GMT  
		Size: 3.4 MB (3429026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:aa0af85a7775d51a23b52a6df368a1c0340a06c3b5950274d052254e00f33164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 KB (306882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c586a3c5a52fb57ba475bc12dabfa286c7d04bf0a7fac98f73150eae875a7d1`

```dockerfile
```

-	Layers:
	-	`sha256:26a25872f213190b97add0322305a3ca6a0321e5ac87bd1de1ec405796a404d7`  
		Last Modified: Wed, 08 Jan 2025 18:23:57 GMT  
		Size: 284.3 KB (284330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb43e05767a66bf09b4bc3d8765f535fcfb4537b34aca9b20c12b2550c3fe2aa`  
		Last Modified: Wed, 08 Jan 2025 18:23:57 GMT  
		Size: 22.6 KB (22552 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:222fc82fdc8d9b7710784d434a88eb781b80477acdea7a0dc1547e098e74a202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37815967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927b34c8a34b9047adf53e10e5ac53e9982e43926dc293a9e6c8854a074b42e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0ea8c932a5c006f90ce62c4d48f8274a43e5a9ed94c4e0fbf70f222f9c46e8`  
		Last Modified: Wed, 08 Jan 2025 20:05:00 GMT  
		Size: 12.2 MB (12172487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ea894b8027cad58c9e1e7f870fd9a57505738381bd93f157f3c5d165ac6d0`  
		Last Modified: Wed, 08 Jan 2025 20:04:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c609704d412ff04689597ac1bcb8eb74276bb34894dbc822bf7bd6255f80e6`  
		Last Modified: Wed, 08 Jan 2025 20:08:21 GMT  
		Size: 13.4 MB (13439875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbba5a7a0b80a061360ff520bb2a24633d7e5404b35f4df517e1f17d080b5a36`  
		Last Modified: Wed, 08 Jan 2025 20:08:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e199f0c805cf5c02006fab292ed5e7e4d054fb4e92abe0a08131bbdf46dfac`  
		Last Modified: Wed, 08 Jan 2025 20:08:20 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d61f29155f04073a85f0c2d90fc47f1157e175507e27bff440e04318a754cb4`  
		Last Modified: Wed, 08 Jan 2025 20:08:20 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a1d7b411a863d285457259ff176529b7a190a324b8bc21a356ef961edc84c`  
		Last Modified: Thu, 09 Jan 2025 01:31:47 GMT  
		Size: 1.7 MB (1691187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbabd539f6df0f203c7a474d0c65c0709ae1ec2bcef39ae8c65fb14484904c26`  
		Last Modified: Thu, 09 Jan 2025 01:31:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d46bc3180f264e57c1a84eb10362dd21171165eccc94c381426fb047826065`  
		Last Modified: Thu, 09 Jan 2025 01:31:47 GMT  
		Size: 3.4 MB (3429009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:5be56efc7030635fc1449664d0466b75e941291011beaabb0098e34f179a8307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 KB (302261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50c51cf0a63482562ecbf12a9bbd1eb9621e38471e03456a29bce496cf2ef0e`

```dockerfile
```

-	Layers:
	-	`sha256:409684484b8cd6ae35ee7efd438dd5da966491266761e633b3d9d4c926e353be`  
		Last Modified: Thu, 09 Jan 2025 01:31:47 GMT  
		Size: 279.6 KB (279625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a94026da00962f87d5297569c8b1f97fee7e62fdbdbaff7f2962f765e4a7573`  
		Last Modified: Thu, 09 Jan 2025 01:31:46 GMT  
		Size: 22.6 KB (22636 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; riscv64

```console
$ docker pull drupal@sha256:c6548560bbf647b6173577c2e5410ab294d910f3ac06d3f97927e22e41985c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36654064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf132abc8d415d03e2a817a0d58428d4c3cca74577c20c7a3cf2397f0ab123`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c725d2b7cda04131943f46fbc9ab5daedc4d0bdf3c30a0e37da7d34d14947341`  
		Last Modified: Sat, 21 Dec 2024 09:20:51 GMT  
		Size: 12.2 MB (12172525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711edafacbefbcdf2dac55ada0d1a7a162cbf509eaf229c0a3fb50b55dba5dea`  
		Last Modified: Sat, 21 Dec 2024 09:20:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb772f0f4be3ba733f071837b62477b2daf71e1d9c183ab61f98645687f20b`  
		Last Modified: Sat, 21 Dec 2024 10:09:23 GMT  
		Size: 12.7 MB (12741335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd122e552aba01f4120ea99b2d763b434fa0e72279ee26d80dac1412c4d22e`  
		Last Modified: Sat, 21 Dec 2024 10:09:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bf562dab2e4e07f18a80907746097a85fa9f24e42d2fb241494260e4370bd8`  
		Last Modified: Sat, 21 Dec 2024 10:09:21 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb0f64acd62efcb6fd3bb51cec1762fcda8690fd8004e4fefccb881d4bc4eb0`  
		Last Modified: Sat, 21 Dec 2024 10:09:21 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc6811f760bc19d43b7ae32fcae0cd751c0e6cabd234012c21ffed7bcbf2743`  
		Last Modified: Sat, 21 Dec 2024 14:52:40 GMT  
		Size: 1.5 MB (1477894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e2c3b5326bb79866facf4fd239dd425b218f99238df7aa270067c5ae298973`  
		Last Modified: Sat, 21 Dec 2024 14:52:39 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1721dda542b0c982e4c468cb14bca47c7a734d903b962eddec444e6984806602`  
		Last Modified: Sat, 21 Dec 2024 14:52:40 GMT  
		Size: 3.4 MB (3429011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:e1c794c49495c0abdc5d867f90f964e1398a5518649d2407b772ad34f604752e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ac394ca19e302b293817188a24d608dc6076a55f149b16580bbda2b69eb9c8`

```dockerfile
```

-	Layers:
	-	`sha256:5c4a047fa7e4ba44488723305c49af41930f478cae47ab7f53dbbc6f73a4d019`  
		Last Modified: Sat, 21 Dec 2024 14:52:39 GMT  
		Size: 280.9 KB (280921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366a1962f32cd4f9818fd72f8df8f3c87bb729ad12ec283d80e846008a02defb`  
		Last Modified: Sat, 21 Dec 2024 14:52:39 GMT  
		Size: 22.6 KB (22636 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:f950d6b8ef0a7086aed0e9c96aba7d53a117a24cd2fc0de954d0638d8f875ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37205164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c9a5f4edc8469303e3817aab90ffbc81f9b53421b5ac51fae04536c0760b4e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 13 Dec 2024 23:34:35 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 13 Dec 2024 23:34:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Dec 2024 23:34:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_VERSION=8.2.27
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Fri, 13 Dec 2024 23:34:35 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Dec 2024 23:34:35 GMT
WORKDIR /var/www/html
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Dec 2024 23:34:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Dec 2024 23:34:35 GMT
CMD ["php-fpm"]
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_VERSION=7.103
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Fri, 13 Dec 2024 23:34:35 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Fri, 13 Dec 2024 23:34:35 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec0d3a15f04a7cd8474ceaef05bff60216e4ce99c2c8d564d99e02a1ffdc5b5`  
		Last Modified: Wed, 08 Jan 2025 20:34:44 GMT  
		Size: 12.2 MB (12172476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44ab3fcd84fb316e6858c7ba596bb51a559787c7a001458d8f8257008c3f5ee`  
		Last Modified: Wed, 08 Jan 2025 20:34:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a14346a4f46c807797008d89c5ba67d731e99506ab2a97038048e76e082025`  
		Last Modified: Wed, 08 Jan 2025 20:38:36 GMT  
		Size: 12.9 MB (12932096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1182d8bdc4f3380be1e21a5c6b40b6fdf32832c61c441ced816ad025553dd2a8`  
		Last Modified: Wed, 08 Jan 2025 20:38:36 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3aa6ba743160da0485dbf33485bdc0ff960837152ecdb97362ce20d5175e35`  
		Last Modified: Wed, 08 Jan 2025 20:38:36 GMT  
		Size: 19.9 KB (19850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0082470ea70f9dedceb98ce3ffa176782196f28d95459fee084c02cb1b450b6`  
		Last Modified: Wed, 08 Jan 2025 20:38:37 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf9b704ef80eb1b14c5e6d762898404f7a5321d7fd75b0554c51b4456f6b3f2`  
		Last Modified: Thu, 09 Jan 2025 07:38:56 GMT  
		Size: 1.6 MB (1609978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747c5c6816604fea972d2844e3109d985ca70a79fb65681b6a663d06ff1b56ff`  
		Last Modified: Thu, 09 Jan 2025 07:38:56 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1ec73bfe28d405f5b652f2d8024aeddd28f315d4bab6b796aef7aa807a1d1a`  
		Last Modified: Thu, 09 Jan 2025 07:38:57 GMT  
		Size: 3.4 MB (3429009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:8273c13dc09fa2f903beba62e6d534923773942f2b7148741f1b1e4e9597ecb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 KB (302179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fc7d58ef68803ed192a1383ab96375b7f655687a35ce20f1ae5fb1f6b7a3ac`

```dockerfile
```

-	Layers:
	-	`sha256:e1137e60db4de3198212234bd03c21281f91c4716af84e9f6a18f6e2ab343aaa`  
		Last Modified: Thu, 09 Jan 2025 07:38:56 GMT  
		Size: 279.6 KB (279591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673de6da20c562194decd8f7070665a3b58aa737cd0d2f368a4ff216015bc84`  
		Last Modified: Thu, 09 Jan 2025 07:38:56 GMT  
		Size: 22.6 KB (22588 bytes)  
		MIME: application/vnd.in-toto+json
