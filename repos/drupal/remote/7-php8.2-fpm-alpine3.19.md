## `drupal:7-php8.2-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:c267f40fa262a4b536c9478e38adf69b2012f49b2483860d4e783a12138df4f5
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

### `drupal:7-php8.2-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:126c2cf6b2f9e5ef6caf20079111af68d5e63e016b1c4d788283d84e181c5b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39057698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f7277939126c0333e01e66a2465bbb29d39308d36f585cf6bacdfd97285b5d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 20 Nov 2024 22:41:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:41:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_VERSION=8.2.26
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:41:02 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:41:02 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:41:02 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_VERSION=7.102
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.102.tar.gz
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_MD5=3e97344b47cc87b0f51fc2048f38ee0b
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734b49cae4d553d67f852d79efe0f7fab29c900a99ab297e833a782894bce36c`  
		Last Modified: Thu, 21 Nov 2024 18:05:54 GMT  
		Size: 4.9 MB (4872456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c2da8a0c3fd3978acc2d7a51d7e5f949d2338e874e3598c743627cab332f2`  
		Last Modified: Thu, 21 Nov 2024 18:05:54 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0185b00c453f3c3100fd442984dde5d7cf66453b28f7ead64c1a9ebb1aa7378`  
		Last Modified: Thu, 21 Nov 2024 18:05:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8bdc9352f0c00e7bfcf3195ff6477335848dd5f69a5484079f65d36107bc1`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 12.2 MB (12160116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9ba93938c1e6819122e0e35e838c04aa5f97e51790efa5407603ed5c290305`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca5eee9757946dd708f4c1f3f3474daca840ae65a8506ce54f1bc33641e5dfc`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 12.9 MB (12860138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ff907fbfc9569b57aa28531be17241b6abb439297602856069c6680aacbec4`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2dcd66a84fa63a604eb9eb09285f9be42854566c5dfd7fb3e8aed43c8b8ed`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 19.5 KB (19493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87571102b5ac222b392f8e5b4b70062e450e16f6378d6ee25cbe0388fb30d690`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a989b808b33f3af032e5d3c7f149ed279348bce0adc77143426bdbfb695e0`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 2.3 MB (2283740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e0bb3f1718c014bc40d9eef533b4ff5f62a57908f07939be4e662cf426bdb3`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95819e5688b00e0a9ce24dc62b953f46e56e8bef49980221be6c7c6b8c699088`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 3.4 MB (3428125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:fa92cff01e61c3a4be1036809c7e10dcc5863eabfdc10326e1535476f6fd65bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 KB (302473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcf048e3826deef0b0f77c37a05d14347d0b1ea4acfcba0d99889321d657687`

```dockerfile
```

-	Layers:
	-	`sha256:097984a389c6aeb383dc8d33a29a872b0bc55c4c452edf19d443bc1668cdf486`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 280.5 KB (280538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59da510a32e64205effb121b2b5626097d0a180f4ba3ae9fc0cdf2d96c3e86ef`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 21.9 KB (21935 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:905f7c0ecc202333d7c3bcbb1a97d186d71c286464033e54c856c6bd643337da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36799035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2675ed2a9a313956243b2661b6870b63cf88bfb89dfd792f452d54da6eeabb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 20 Nov 2024 22:41:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:41:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_VERSION=8.2.26
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:41:02 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:41:02 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:41:02 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_VERSION=7.102
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.102.tar.gz
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_MD5=3e97344b47cc87b0f51fc2048f38ee0b
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d506df09dbdf91185add3a7b93df87df3f96e9e86244bb5a36ce976bad384da`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 4.5 MB (4549552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565c5d4979fc78805381ae54974577a69443306d5cd6ce30896d12062df3b5f`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a131775c3bd5253ef21285ac1b265871981ec4c9eb57a1a2dfc43a3072104`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f171b93f06b88db8bc03d25bfc99caf877d37ef1e3fe04331fa61633eadc41`  
		Last Modified: Thu, 21 Nov 2024 18:52:09 GMT  
		Size: 12.2 MB (12160127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd5b35eb338efe173b790235472886217cb55c0ee1fb5c1f32cc7b6999c4b82`  
		Last Modified: Thu, 21 Nov 2024 18:52:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0778a10dd72b426b972986cf760b586660dc3eb113b8840cd04132274df064a`  
		Last Modified: Thu, 21 Nov 2024 18:56:21 GMT  
		Size: 11.7 MB (11710852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892007957f10e422c2adb01ffd7f930e89d8675f30783d49113669a84444946e`  
		Last Modified: Thu, 21 Nov 2024 18:56:21 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653319027f6be4ec979fde9b38da6418af41e786f9e23018d0d3366c6ae53365`  
		Last Modified: Thu, 21 Nov 2024 18:56:21 GMT  
		Size: 19.3 KB (19328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa8d3c119316b50b7b8f4db004905cd799209fe909973cbfe09d79e6ca1ec64`  
		Last Modified: Thu, 21 Nov 2024 18:56:21 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c79c0b909ec40c337a6e61a07543cc21f4d6271359876619672a82ff2191ef`  
		Last Modified: Thu, 21 Nov 2024 19:47:57 GMT  
		Size: 1.7 MB (1740699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f2979b5b0564fbd303939adb9c5608ce151372097c93fe93096519aae4ec04`  
		Last Modified: Thu, 21 Nov 2024 19:47:57 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db60235dfc38375155b6f6319b881249cda998bfc7420b51e8401711daa2f1`  
		Last Modified: Thu, 21 Nov 2024 19:51:25 GMT  
		Size: 3.4 MB (3428134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:962a6a6b92e668c2cd8c9339c198a2ae6438f763c8bd9fe3c636f0b99062b060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 KB (21807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8d0d23c1b4c6ce7b7f0f2f2cbe1cbde678c2bae13aa0ed5d7fe19eece4d8da`

```dockerfile
```

-	Layers:
	-	`sha256:14b0cd4e826880b1682ed2dd7262b0d1bfec77f646b69c5b41bb425eab493a0f`  
		Last Modified: Thu, 21 Nov 2024 19:51:24 GMT  
		Size: 21.8 KB (21807 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f28250b02ff3b3fb67888ec14f36938e39878b7a89c3b09e4590f55c8ac5ca19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35385295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95196acb5d8c559e41475385badf5a9ef95400cf0319c78ca6d842f591f8a8bf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.25
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0436284ed3df1ea72ee7578e1acedcb3f1d13662da3f84c96df0f7250b0e65`  
		Last Modified: Tue, 12 Nov 2024 04:13:48 GMT  
		Size: 4.3 MB (4273946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f71fe689f2c66318ac16bb591f4263243d0ee583bf8e58b422159d0e8e5f74`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459364abd934a595a7d02d68c9dbf45d3769fec662e99f1aa3c9c4f8554b53a6`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b59c607fb85282b7fd56e37db2071b82899ba9e963888983edc1d7c1154b3fc`  
		Last Modified: Tue, 12 Nov 2024 09:12:10 GMT  
		Size: 12.1 MB (12147088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc16f427a3c401470eb71a7cfa0163e517133d75ec3a72b313d87164fc79b21`  
		Last Modified: Tue, 12 Nov 2024 09:12:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13117e2f72e9e0fda23641c0354074dd075bbd8633fb62155c098b497fe28cc9`  
		Last Modified: Tue, 12 Nov 2024 09:19:23 GMT  
		Size: 11.0 MB (10970225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42241276b12457a118a7b96f2c8d078225f1b71ea3c32e12f45d9b41503785`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578b8ac96ecdd6b35afb34f93b4c06e77a87b8d0927560f440ec09a3c54c287`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 19.3 KB (19315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c3b3a893135b1e439121e07cb0f05201670f6f6fb5057f9d0b24587fb4d7d0`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2596353aeb681d7a3f582dde82273a039a31231876f464fe62f71efe67b1e0`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 1.6 MB (1605434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b79d9f451203f83f31de742c96491b9921a7c3ba4c7914a7f2bfbd892f742a2`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0247ee967ea3f44d6aabbf426a4f6652680564c3b3b023ca2348c7272be5470`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 3.4 MB (3427639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:475404c60d3fb9a276accf9446bea5e76cf0e62a83c31137ae2f78219ac57d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 KB (299716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa33cadccbb85ee723d8329b9955d9a4b1730bbf7bc8409301d8dacd6cf3af06`

```dockerfile
```

-	Layers:
	-	`sha256:05493e41b23f963813d766d72570e66ff1af77a733ef8141c8ec00d426f43244`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 277.7 KB (277694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec6cacfd2883645e0c86d984359abd1ee86f1fc9c2d21e5b42a5679f7804dcd`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 22.0 KB (22022 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ce2f90ce01d676a696f7a3e3ca5f8f8227d1eef21d65dbaf3df53c9ec08ca17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39259584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5c747e7bc5041234931ca402edac52b64f61a6e6543f4f0915aedb5b7379bf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.25
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aa82fe7cb492df316f7b720cc5bd1cf6a0f0bbf25ec9d0738d8bab76eb6ac8`  
		Last Modified: Tue, 12 Nov 2024 04:11:04 GMT  
		Size: 4.8 MB (4810652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf6e72d90a16f21844fd0a2e0521c81b8bbae7a03922cd2d8afe2243befeeff`  
		Last Modified: Tue, 12 Nov 2024 04:11:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a4c00e4542840ffb2d40fc8e730ca3aceef8c5efbd7d8e4d37b0fd2779f28`  
		Last Modified: Tue, 12 Nov 2024 04:11:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4f3901e90f8ad2d1ec9761938f97690a80ed59b1f6d60eef866e1b0719888`  
		Last Modified: Tue, 12 Nov 2024 08:02:44 GMT  
		Size: 12.1 MB (12147082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9fa729289d3494c567e2db6ab5f2fcc15006d632a4d73b749ded01e788d3c5`  
		Last Modified: Tue, 12 Nov 2024 08:02:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0dbfabc1ee57f2e92b4e7cbe8dde5eeee7f3c3ee2f807044609525d45ab9d`  
		Last Modified: Tue, 12 Nov 2024 08:07:10 GMT  
		Size: 12.9 MB (12924674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9657457570fb9cb0592f60dceeca662badb15d5f67b25eb70a08feb1f02250aa`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c782869d8ae2eb29ea1d142deabdff2354e614c387a0711f6d81c46967784e92`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa440590fd2ed69d716222e5622a42463f5c6a4b4bbe356a281f7b77969f7105`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce1f4d7d9c1396222e2aaede8905bd65f556e85e8539259ce81500af6f2ff8`  
		Last Modified: Wed, 13 Nov 2024 02:57:34 GMT  
		Size: 2.6 MB (2557050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0fe849d59b1a52a2432932e945bbe20bcfaa247b74955d71f0d44633186b90`  
		Last Modified: Wed, 13 Nov 2024 02:57:33 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542db18cb9a946e5f3078fd2cfcb1f4ecaf5ed3c99d90c4de4d0c2ec365bd20e`  
		Last Modified: Wed, 13 Nov 2024 02:57:34 GMT  
		Size: 3.4 MB (3427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:7c864181915dbcf401c05861a07902e3f51f7dd64f3954dd110887247cfff0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7933b21758a41f712a66594097f33629e76b0e89903c7353f5df122455997c5`

```dockerfile
```

-	Layers:
	-	`sha256:14ac4c59064991cf2b2bc390c4f00689a599ab9cc3aef6f75d13e64927c3a025`  
		Last Modified: Wed, 13 Nov 2024 02:57:33 GMT  
		Size: 277.7 KB (277706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d64ce5dc9198f3bc5d9fdb47ab30fff11e660a151dffcdecffe60a71d1b0812`  
		Last Modified: Wed, 13 Nov 2024 02:57:33 GMT  
		Size: 22.0 KB (22046 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:22447646d3c868d3e8e86e44dcd4440b67b6f7be68b6ca590c129dd5720f6cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39159436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00a4060d8995ffd71f94502e0feed789325d2c6e244c97732c077de65006ef4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 20 Nov 2024 22:41:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:41:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_VERSION=8.2.26
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 20 Nov 2024 22:41:02 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:41:02 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:41:02 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:41:02 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_VERSION=7.102
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.102.tar.gz
# Wed, 20 Nov 2024 22:41:02 GMT
ENV DRUPAL_MD5=3e97344b47cc87b0f51fc2048f38ee0b
# Wed, 20 Nov 2024 22:41:02 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c725ab33eb10613f4e25c14d6a9d7969d5dddda699c2d3400c0ad51484ca2f0`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 4.8 MB (4760597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f194484a4ff8005848781b520ce4d6989682b6bde760ca09405d4d2111c4d`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bb1bae1648e112cb13601e9ab780e4c35a728072110a279e9a219ff5fb0036`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2e7ebfe7a6fff32603c35d9199cda3125b430277416500ec0b67d355ed2fdf`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 12.2 MB (12160121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40768428598f7cb6e2746cc99bf7a765bf450b58f2b2d00bc17bf778bd89c49`  
		Last Modified: Thu, 21 Nov 2024 18:05:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34af15083d435677b5edd542f5314289b8bc7ea1fc0ccc28420e59cf9e558467`  
		Last Modified: Thu, 21 Nov 2024 18:05:49 GMT  
		Size: 13.2 MB (13205582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062bac573aae17399dc5b58c9839745212f3cb1b47fe4759e080d7a49767578`  
		Last Modified: Thu, 21 Nov 2024 18:05:48 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d91dfc4e56360c1b55154ecc4d9bb900932fb4a90f167e333e8f052cc1e97`  
		Last Modified: Thu, 21 Nov 2024 18:05:48 GMT  
		Size: 19.5 KB (19499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b4e47928a34f0e7244afbf74935c2ccc80f282378a4e5f096989f4b3e1c3fd`  
		Last Modified: Thu, 21 Nov 2024 18:05:48 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1d538136dfb88a766c3f710844d107fd149526d3f66d8482b3d69204f2ba52`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 2.3 MB (2317943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67a35cdc3a809012ad9a31ede8fbacb4eec425067ecabf8560b7b17e62d58e`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eadeb5b2d04f4821d4a5a21e7973c2d46032c125480723abca662ea2d8003c`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 3.4 MB (3428125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:06c9eaee85cf1e607c7ef2b19bccc5efa4ffc11967ef327b36633ba8186be62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 KB (302433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8235a2c860535a80883a73a5fe5ed7983f1185a2c48c9cacc7fd7baf6c2f65`

```dockerfile
```

-	Layers:
	-	`sha256:f7946b33c6894f4e7724f359aa5a68a4ae8594c78f68e274efc9057c1946a619`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 280.5 KB (280523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e528f7b68f90bad2892dfa2397e2aca44234f067f7669f7d6bd6285d585b258e`  
		Last Modified: Thu, 21 Nov 2024 18:11:57 GMT  
		Size: 21.9 KB (21910 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:21f705755de1c7c077ae1cc2112776a1796a84fc3d512957d350fea33a1b279c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39247575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fadc2440a8adf9d2fc44c34d705f2cbe6e50e5536377a1801088503ba1fd0af`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.25
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b5b574e5e7a1963997e6adc5fc6c41ea62b3d72487780713b6d09006e673c`  
		Last Modified: Tue, 12 Nov 2024 03:49:43 GMT  
		Size: 4.8 MB (4816871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4503eb1a8e49f698eea61c5c4dce1fa0040ce6ceca1d52253836027f00e9d7`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6eea919490bc644797b1f6b8249d5e157a311bebf21cec14cdc7315bd97`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb34a1954bb8e077aec75426ca3adeb559dc4cdb53f50ff674502c38993fa2`  
		Last Modified: Tue, 12 Nov 2024 06:12:37 GMT  
		Size: 12.1 MB (12147082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc52540aaccb808d4286076482a85ff933d04c8ff27d7ced025b1b49ef616863`  
		Last Modified: Tue, 12 Nov 2024 06:12:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf188a7a0c68e9cbd682e878d1b05dbaa63d39ea09c1ded0c2578c6c8273800`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 13.4 MB (13352729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f003e7fb73fbe33f0a3cb3c641305a38b0277bb52c2232111e8243526191f08c`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf964a7912f37c2a23b6b679ff502b8421eeeffaad900ddf6cc4a62dd952bd89`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 19.3 KB (19329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98df7149e5827c112b19589b6d82e07f0af68220cdf3de8ec8a6a21cbdd12c`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb3164d58bf5264931beb87d44a234515a6c5b7c884a6b388ef5e42a11881ca`  
		Last Modified: Tue, 12 Nov 2024 16:22:02 GMT  
		Size: 2.1 MB (2105507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5af6028b3cf9dacc1956e361c797019d5f3541e514d3f50a69bf2c180349a2`  
		Last Modified: Tue, 12 Nov 2024 16:22:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1f1e2fdcc20fe4240bee5be502c0c6268435dc8ae0880b71609a95f3a37fea`  
		Last Modified: Tue, 12 Nov 2024 16:22:02 GMT  
		Size: 3.4 MB (3427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:a91dd640349b7bc46ddaef6ab89c5891edfc633782dc0adb9fea69e0b20e836b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e085a3487c49ac2273ad8af82f934ccf7e677a9b61c44f7a7517aaa40f4e5cd`

```dockerfile
```

-	Layers:
	-	`sha256:9109305ef45bfafcd3fe97d9cedaf4c321425dd2bce9feeaa7e0e04db9d0d11c`  
		Last Modified: Tue, 12 Nov 2024 16:22:01 GMT  
		Size: 275.7 KB (275742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a873c300fa803401bb26c3382ee9cc3c62909920d049a06f323653a683957e8e`  
		Last Modified: Tue, 12 Nov 2024 16:22:01 GMT  
		Size: 22.0 KB (21972 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:a8bab9f62da73cfb97465e2592c4b81860225d0be083af2cb64a5e756cc548d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38484151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f218c81b86919863b4f652d8e9fd2502e4b832ff09f4849ca63097f8f405ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.25
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ebb87545715444ed87e790ef4054fd17853711b917372939fcec005a51ddbd`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 4.8 MB (4799270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93607338abaacd48124e4ac15fa9ced5b6d5b12eab2b3a8dede0efab1212c45a`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afbaeae156c89776da7468752d9ee2392816ff4e3ccfeade1d8ecb4f8b6cd24`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a271f5f171f5be7c56b275d054fe96f39f58933c3b54cfe0368a050bfff426f6`  
		Last Modified: Tue, 12 Nov 2024 06:45:59 GMT  
		Size: 12.1 MB (12147079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bcdf93fc1a1d25c560282f775b6e9b808ecef14bea6359c8ce917fc64bb3ce`  
		Last Modified: Tue, 12 Nov 2024 06:45:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e33bb264df7185833f5aef1305938dd1c5716b579bcf698e9af25f7e51829`  
		Last Modified: Tue, 12 Nov 2024 06:49:42 GMT  
		Size: 12.8 MB (12824102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888dc341a8c698cf4720bc793be0a129f8b479d6b3e74e6657dc9e312843a27`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b967bdb6dfc02193909cbe798766157a4ba2854e7ca1fa2a4126f4d6a94a4be`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 19.3 KB (19314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d03f758561d18d2e9bd0605d4ea684d60d2970c57e1b8352396721238837b28`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e25b2d0a2eb16490e3d990d94d028b00317a2bea2492f487dddf36a8ba9880`  
		Last Modified: Tue, 12 Nov 2024 23:43:44 GMT  
		Size: 2.0 MB (1999435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9a0d0ee02bcb3c52e3898d9652243dc011fc9bda724cec29220ebc179ac5c`  
		Last Modified: Tue, 12 Nov 2024 23:43:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5d9478c851056a9f473aad34ca532ea1709407629b9442a0d2e6a84655a32`  
		Last Modified: Tue, 12 Nov 2024 23:43:44 GMT  
		Size: 3.4 MB (3427638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:94b34df9e991014da9a9a3e9dbe0460683ef01f00276b4248c600ecf170fca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1e7b4e1c99aa11edee03dfb2fe4ae494b88901aee96ed3735e7eae22082ccc`

```dockerfile
```

-	Layers:
	-	`sha256:c1b3814af55ee14c6cb75d3a4d7030a6fe004ef7e6ce524bb68f22f2a7004b3c`  
		Last Modified: Tue, 12 Nov 2024 23:43:43 GMT  
		Size: 275.7 KB (275720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d968a38e2e277c84e2bde74af5272208570d3b9f3ec839966a2c70f00f2f37`  
		Last Modified: Tue, 12 Nov 2024 23:43:43 GMT  
		Size: 21.9 KB (21936 bytes)  
		MIME: application/vnd.in-toto+json
