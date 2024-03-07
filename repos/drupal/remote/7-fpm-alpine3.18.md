## `drupal:7-fpm-alpine3.18`

```console
$ docker pull drupal@sha256:4bd3b077460bb19cc8b9de2ef9bf96532c2746896391f961c94acc9e8339ddf9
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

### `drupal:7-fpm-alpine3.18` - linux; amd64

```console
$ docker pull drupal@sha256:172b140e453c44ede06d364065b9936bb4643b6f74bf07d2143e8260d6c6329a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36338684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa65e93ed2f3d502173e179cbd3305f0bf6d0d9f59b6a2cee720629f169c518e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd08544f3979add7a1135032c708137f3a42762bb48446a036a80d16a9c796`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 2.7 MB (2682495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f2d92bc3b905b7db953512ceb84266e42e19d498f9d6c4c91170b5360cf3b2`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7427b71a5dd639a1a4b6123f46f2d5c6e6f8bd6d7bb8f8ca879516220b330d9`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e01f2c9fe6ee3b538599f792256c480c6997a830a333acd7f42bdbc73858a3`  
		Last Modified: Sat, 27 Jan 2024 05:41:28 GMT  
		Size: 11.9 MB (11935708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dff5075da1ce1e459640714390d3aa2af96405c5da393d3da6a161b7a65e1d`  
		Last Modified: Sat, 27 Jan 2024 05:41:27 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92852a605ac728fa2a8e69dc1dfa137a034d86be941af5e8a0704ef872b78c87`  
		Last Modified: Sat, 27 Jan 2024 05:41:44 GMT  
		Size: 12.4 MB (12428771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bcac57b33ac1d5923cae4ce66663cc53057e88f3cc54922898d7be1e2e4e7c`  
		Last Modified: Sat, 27 Jan 2024 05:41:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d4bd2c9e7c82efe03db7213a24e17bb5178a15ae54c97f128dd922565323`  
		Last Modified: Sat, 27 Jan 2024 05:41:42 GMT  
		Size: 19.0 KB (18952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574a24fb80f2106d93ee783d51526f1bd41b0abf15c4f15bae9983a20339e36`  
		Last Modified: Sat, 27 Jan 2024 05:41:42 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062302a843f18972381ed5074f6125c8fff8e7dd856eb60cffe3e79547a60d0a`  
		Last Modified: Sat, 27 Jan 2024 06:53:03 GMT  
		Size: 2.4 MB (2437651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312e1ffe14718298cf0ec9b6c778571b647900bfbcf5fd99d4aab18f3d43a563`  
		Last Modified: Sat, 27 Jan 2024 06:53:03 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a1d8db02d51384ee0080255b689ee7da733c80e7dd98dc67def12487d37bdb`  
		Last Modified: Sat, 27 Jan 2024 06:53:03 GMT  
		Size: 3.4 MB (3418903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:2a51234971b3ce64a18d2394f5eb29e2bc3089b0da39f56b54b63043b1423f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 KB (258253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d81ff4c2c8979d733d4c9521214dff6b06f37949a18829c693633421713aed`

```dockerfile
```

-	Layers:
	-	`sha256:3181e706a17118bb562da4989665ced5c6d63b80a6ae3d42567f7f6f4f1e67d6`  
		Last Modified: Sat, 27 Jan 2024 06:53:02 GMT  
		Size: 234.7 KB (234707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932a799ddf4d423a518529a5fc74fe3a7a582fd720a0e62cadc884e15f5983c1`  
		Last Modified: Sat, 27 Jan 2024 06:53:02 GMT  
		Size: 23.5 KB (23546 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; arm variant v6

```console
$ docker pull drupal@sha256:57c380c89958134a90c39103c0f211d0a583e9542347befa6de942d89829af89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34360700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901bf3ed9e7fab2be8267b3d61d0fe7469b79364bccd83956ad86bc20a11a5a1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:34:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:34:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:34:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:34:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:34:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 06:34:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 06:34:22 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 06:34:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 06:34:23 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 06:34:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 06:34:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:40:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 06:40:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:40:32 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 06:40:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 06:40:32 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 06:40:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 06:40:33 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 06:40:33 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 06:40:33 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62daf641b680894f28bde55f9b558dcd71afae65a613d7289839b0ccc1c59935`  
		Last Modified: Sat, 27 Jan 2024 06:45:53 GMT  
		Size: 2.7 MB (2688488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbdb0364f95226b0ddc30b86f27a68af4cb1b836ca10db53e713f447ff13bc`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72425da7bbe49396c65f29cc1da85be4ba13d8917fa75ad08fd7a48974409d13`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48098cdf5f141f874c791e6c391133337aa69f1588b1fd40e9e4b1ea74f1c869`  
		Last Modified: Sat, 27 Jan 2024 06:49:24 GMT  
		Size: 11.9 MB (11935688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06db97eabdcab282c9c1c4cc1e8cc335a53506eff7bb83ca7ba6f053c149cab3`  
		Last Modified: Sat, 27 Jan 2024 06:49:23 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f91f3d0f6065d971ac1b4118ef01a1526da4ac2dc8d4e0cc7ccfd01a7142af6`  
		Last Modified: Sat, 27 Jan 2024 06:49:41 GMT  
		Size: 11.3 MB (11286306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988a0a6ce604c6edebcab213254697e736ea848d10ce91d2d5c84268b6582078`  
		Last Modified: Sat, 27 Jan 2024 06:49:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c5c142fe4351ddf03c954a2d3262e2cc50695aa6df09544a6f944df8bdcfac`  
		Last Modified: Sat, 27 Jan 2024 06:49:39 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2787f87bfdc6954440038ddc17e128076e69524d29efbb4b587f304e6ff77b`  
		Last Modified: Sat, 27 Jan 2024 06:49:39 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d998b8302c25611977ecc2e22dc4b3d91ef06d799d6fadc607d446d06e17d6`  
		Last Modified: Wed, 06 Mar 2024 22:11:15 GMT  
		Size: 1.8 MB (1844746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef78f115888be0141e2572934a1c4aeacf5183c5f88b7354778d0c1a3dff1f4a`  
		Last Modified: Wed, 06 Mar 2024 22:11:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76e3313e5796679daadc3473c0e9baf1ff7de55c8dc30125bf2efc1926d015c`  
		Last Modified: Wed, 06 Mar 2024 22:11:16 GMT  
		Size: 3.4 MB (3425980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:586421dfcb30669c5005756d7765f29532b3fcc600d53fdd8bd9721ceb0164e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ba0f01d337c6ecec3f9e32c1a1de745ff83e412411f66156fee3742826c7db`

```dockerfile
```

-	Layers:
	-	`sha256:6f9129800246810c9a69cd260e912ba5ea3c7f3033bda4639add8b24b8fa0814`  
		Last Modified: Wed, 06 Mar 2024 22:11:15 GMT  
		Size: 23.4 KB (23407 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f97d25b3b17f1eb16ed90fc76bfeed0170f0d780703f59ab516441c44bf5a726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33120206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b62dd23638ad0113ac97038546e94a4b70f1e29ba72d0066a93ce0b8135ff31`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c0293e5cb723599572c9030f71f9f0162fdfef255b47fc3f6050ff6fe8df3`  
		Last Modified: Sat, 27 Jan 2024 07:34:33 GMT  
		Size: 2.5 MB (2528495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d8a4e0cfd121c4ed651cbed66fbdb50e920d2af857d4dfb1c5778237f334f0`  
		Last Modified: Sat, 27 Jan 2024 07:34:32 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3061407d5bd08863490376ebb46a63256157ce41f373da5cab4489e9ad19be`  
		Last Modified: Sat, 27 Jan 2024 07:34:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e02abd7e9b8961289e177179296586d0ed02d97b82f8c599cb6e27616415e6`  
		Last Modified: Sat, 27 Jan 2024 07:38:08 GMT  
		Size: 11.9 MB (11935700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d484893e101b8446907f27b2d1738cb3ab65e28b3a1202ea50e1ccd5f0f6df88`  
		Last Modified: Sat, 27 Jan 2024 07:38:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affb08bb78eb176cf523314a46ced6d94e901317c11c7fe81b5d8856ee28ec24`  
		Last Modified: Sat, 27 Jan 2024 07:38:24 GMT  
		Size: 10.6 MB (10592867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a454455e13fccc53aeeb7f2de5d9ffeedab242b88049c50f9b5dd68da9215`  
		Last Modified: Sat, 27 Jan 2024 07:38:22 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4302fb182b5972211e9ce88b117a8198d94823a0cb4bef7ce6b175ee99ee454`  
		Last Modified: Sat, 27 Jan 2024 07:38:22 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df709afedb1037f69c6d19c902943e182ee67b0b6a99e780ba679c87307340c5`  
		Last Modified: Sat, 27 Jan 2024 07:38:22 GMT  
		Size: 8.9 KB (8874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b825d3f77283ba02f29f201e83774692727c14d5f54719f7df8a9598dbca42`  
		Last Modified: Fri, 02 Feb 2024 16:41:41 GMT  
		Size: 1.7 MB (1710420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd58f95d1cf5cb9967cf9d66c3aa3436e4e3d9a63906d7bd6c802f4362f3d7e`  
		Last Modified: Fri, 02 Feb 2024 16:41:41 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36273a1e85257615fd8b258c90eee81698ca96549d3a8f55fd3d8b2f66b52d7`  
		Last Modified: Fri, 02 Feb 2024 16:49:24 GMT  
		Size: 3.4 MB (3418894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:abef4e0f916639358552dc5a562c15753deef426a444f0dd2546a4773b8a05f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 KB (254283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d451207b01c61dd042cdb99340b317ee33020d7f9df4e8c1159947efb7a2aa1`

```dockerfile
```

-	Layers:
	-	`sha256:6609d4b79899d23dfadf258f62f585ba68dee093c1253d6c0272c526dea8f7a8`  
		Last Modified: Fri, 02 Feb 2024 16:49:23 GMT  
		Size: 232.3 KB (232267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08d74c1a30bce6b680b29335fee3668a49dfba106d48998a79c52e586367503`  
		Last Modified: Fri, 02 Feb 2024 16:49:23 GMT  
		Size: 22.0 KB (22016 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6bc3b0234229e75c77dbdcd9dfe1d994c960745b79f9823a5b3a537780f89e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36619160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca1bcd3b439fa9511286bd5d506456dcadd741334485a3f9ea9968f62fb0439`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4eb03fe552f5c8aa36cd79b78aa545592812821d1c3169cfeab7c2a2d2dfdc`  
		Last Modified: Sat, 27 Jan 2024 08:41:45 GMT  
		Size: 2.7 MB (2721116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb7467a02f797b3b358a87cd793e73d849cb2dee4668faafaea6ac9037dc7b`  
		Last Modified: Sat, 27 Jan 2024 08:41:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe855ad31e7cd79a1f706abb3a6b77f7e1457b5fb9b89c943ad0e8eb99d6a0`  
		Last Modified: Sat, 27 Jan 2024 08:41:44 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c3fbb85d6948cdadc4e000de9a8e10ca838f39e305d49583f5b0ed0295950`  
		Last Modified: Sat, 27 Jan 2024 08:45:13 GMT  
		Size: 11.9 MB (11935691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2e3a6d8956f07613aee2b4dd21b85400422a41ecb4454cbaa7c26f786e98a`  
		Last Modified: Sat, 27 Jan 2024 08:45:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a086d7c1e25c1b880420ae15fb3d8e557cd0ddc4e158a6e667dfb7cd4b0a9c70`  
		Last Modified: Sat, 27 Jan 2024 08:45:29 GMT  
		Size: 12.5 MB (12472871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed9973abd932ad9b55c72af24a3cea8526210291cf0e2bf2ad1e55f0f0ddff`  
		Last Modified: Sat, 27 Jan 2024 08:45:27 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2701a16d75f5c58b0fab1f8fb40e8bf041c2387972792e9f0e7563d2042b4a3f`  
		Last Modified: Sat, 27 Jan 2024 08:45:27 GMT  
		Size: 18.7 KB (18741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0404818f18608bc5eb9c8cc196cd437331f9087b78215db0ff2645b586d47`  
		Last Modified: Sat, 27 Jan 2024 08:45:27 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e9bbb5edc70785f52b9bdb9678e426e7246f88fc13816c42c56e5179592cc`  
		Last Modified: Sat, 27 Jan 2024 19:30:41 GMT  
		Size: 2.7 MB (2704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0920cc44f4b289a99c0b7d9e95e4f45f65146a22d8acdc9247c1728e8e54e991`  
		Last Modified: Sat, 27 Jan 2024 19:30:41 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6a67237205d4e06dea74ad5c7f0a727edd75b4cfcf0c79178d2375aeb31b6`  
		Last Modified: Sat, 27 Jan 2024 19:32:13 GMT  
		Size: 3.4 MB (3418891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:eb8fc84bb3d99a88e639f89961bd8082e48ad8d1027ea6f774b49ce27ad95a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660182620714a8999e1cd15f84201fd498cfa4af52ed842dac9ac3edd98e7677`

```dockerfile
```

-	Layers:
	-	`sha256:c21e2f4afc4f74d73649d867132db441a82b88ecbfbcfcbd008a0cc321a73334`  
		Last Modified: Sat, 27 Jan 2024 19:32:13 GMT  
		Size: 232.2 KB (232242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3236c56307b0396b41b61bdf20b26f5aff774e28a4781af270f601231b19252e`  
		Last Modified: Sat, 27 Jan 2024 19:32:13 GMT  
		Size: 21.9 KB (21931 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; 386

```console
$ docker pull drupal@sha256:eb10e04b574e64c55f48595a82e553ce4961e1ffb1c2f58cce61cde20dafbc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36401748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339c103ae62948ed40317fbe611197af6252bf81ff2e619e5425be42b4a22749`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:03:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:03:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:03:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 06:24:41 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 06:24:41 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 06:24:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 06:24:41 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 06:24:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 06:24:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:37:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 06:37:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:37:39 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 06:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 06:37:39 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 06:37:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 06:37:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 06:37:39 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 06:37:40 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6d2f12df1b19df541851aca59cb3e004d030eea096ff568038497561d6df4`  
		Last Modified: Sat, 27 Jan 2024 06:47:46 GMT  
		Size: 2.7 MB (2727226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c7b40044db0622103ed0e4a3fa021b8c4579d1677fd27d6e9116d5d8e48c5`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0514c3edcfd0f1b5d370eb4eeea4e395ebadba50de6e4f2065e48323f90afaa`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187560cb5012359e365117b5070bca1384129885b8a4795e0515b088df8abb7d`  
		Last Modified: Sat, 27 Jan 2024 06:51:58 GMT  
		Size: 11.9 MB (11935698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c51ca4d0e5a3019f61848ea714a09fd0a056612c099953fa07f1f38600a5205`  
		Last Modified: Sat, 27 Jan 2024 06:51:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8298c9f8ef1e5d82d6923309a0e09a9b5c0c096d4ef273f2a029934552ae19d9`  
		Last Modified: Sat, 27 Jan 2024 06:52:17 GMT  
		Size: 12.6 MB (12613537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3049c4eb731d76c26262f225530cc8cb4995fbdebd33c1e3a3109ba9b3ebe`  
		Last Modified: Sat, 27 Jan 2024 06:52:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a72e41a6f69a11de849afd81ec0cd2d2db5baec7bf5b6fd9e5c1720a7f4c9b`  
		Last Modified: Sat, 27 Jan 2024 06:52:14 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e7ec57a56b06f9d758dd21aebc2e3bb2af9951f8b7d5a610182adaf89d8e1`  
		Last Modified: Sat, 27 Jan 2024 06:52:14 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccb277e0a8ce4b4ec5dfc5dbe5e0ce673fae00d67bfac1f296da3a77864ce1d`  
		Last Modified: Wed, 06 Mar 2024 21:51:42 GMT  
		Size: 2.4 MB (2427633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef39ea68f8185122b6a37bf73ea1663d62376662ee152a0ea572a006bbe53b4`  
		Last Modified: Wed, 06 Mar 2024 21:51:42 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1689d47a4268eca9e55f9bbacf52535ba321408355826b854d294bd20b20992`  
		Last Modified: Wed, 06 Mar 2024 21:51:42 GMT  
		Size: 3.4 MB (3425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:b41b7b8bd57a49c582e575229ed5df85be552c55c12f2b4ebf177d2ce1ece9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2ed7b735c7f90d73eb729daed91c13a2390bdfd3118089953b33168d0f6b6f`

```dockerfile
```

-	Layers:
	-	`sha256:0a7b8e5d7d15c946a1d7bd11097edd36e2f73e566ed8342c9a9b9e7ec47d5ac3`  
		Last Modified: Wed, 06 Mar 2024 21:51:41 GMT  
		Size: 267.5 KB (267546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5fd3dd0c9e344701b11a017ac6d1ed005e596c00e6596932936b17a62cba2c7`  
		Last Modified: Wed, 06 Mar 2024 21:51:41 GMT  
		Size: 23.5 KB (23523 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; ppc64le

```console
$ docker pull drupal@sha256:c25a5a65692b1be9bc0abd2570641d5cdcedd96c05674975b11352b7b8343992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36553868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb3bd012c30521eae719395233c65e2fc499c403719c7eb8256748b55c8947e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:35:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:35:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:35:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:35:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:35:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:10:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 04:10:48 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 04:10:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 04:10:49 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 04:10:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:10:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:16:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:16:15 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:16:17 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:16:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:16:20 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 04:16:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 04:16:22 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 04:16:22 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 04:16:23 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a7a89d73e4ee9a28b90eadd129944afbcac67d80107089f98662fe261ca2da`  
		Last Modified: Sat, 27 Jan 2024 04:23:07 GMT  
		Size: 2.8 MB (2768094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73447972e8407c67ac46260eccde3029f8c096a6bcd6ecfa99d54c3b4f02551`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af6a1382346f24ae6f048ea13c81e62a254330bb7b5b1baa18f25dc2245ec31`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad85d5677777aefbe8db9f7c7a4cf8217ed6d2b795789483b5ff60e1be0d1240`  
		Last Modified: Sat, 27 Jan 2024 04:27:20 GMT  
		Size: 11.9 MB (11935678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491bc34a093e00bc76eebcc64713fbe324d3affbd18bf80e84214aa7559401fc`  
		Last Modified: Sat, 27 Jan 2024 04:27:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae98950e5ed5cd103ad69d377ebbd6be7405e4ef19fef749c73cadf2aff1f57c`  
		Last Modified: Sat, 27 Jan 2024 04:27:39 GMT  
		Size: 12.8 MB (12793556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd8e49650f5e03118fca03bd0f7d9e81c1dfbffac94e6657edab17f354d2b8`  
		Last Modified: Sat, 27 Jan 2024 04:27:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232ab53d919dd6f1c881e680a9a18353af40631f480425aa59a01db92ff923ac`  
		Last Modified: Sat, 27 Jan 2024 04:27:37 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b99ad0ee60e74a96ea32c39292bc5931e8f8f8a0552b0c1d8d1e5f2e3b8ecc9`  
		Last Modified: Sat, 27 Jan 2024 04:27:37 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a85ac97f89cf50004992ffc208b4d40d4e6e40feb774d893b5533abe9281a4`  
		Last Modified: Mon, 12 Feb 2024 21:45:59 GMT  
		Size: 2.2 MB (2249669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784ef9d1c50cefcb2b3712ae6b4565fc37aba0d2ff0e248ece6a18f54699e733`  
		Last Modified: Mon, 12 Feb 2024 21:45:58 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39aa2b84dd08c3cf87498e5d416e206370200c1514131b68059a39bd86d1522`  
		Last Modified: Wed, 06 Mar 2024 22:33:50 GMT  
		Size: 3.4 MB (3425991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:56a2911856b7123dbd007f2cd113574adaab3aaa84e4e46b45753b4ed8dbc6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 KB (285042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daae0fca808cee4e3a2b09bb132c710fa91b5c9e0a0d0246118197421badea00`

```dockerfile
```

-	Layers:
	-	`sha256:24c12ae56c29c61bd1dc5b1dc6dfbd6795b138a249424def8685cd437d22fb39`  
		Last Modified: Wed, 06 Mar 2024 22:33:49 GMT  
		Size: 263.1 KB (263069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02cb322d4f75d3d04fcda9912cb0733daedf6c4f1e8aa5c70d433f087e3b18d4`  
		Last Modified: Wed, 06 Mar 2024 22:33:49 GMT  
		Size: 22.0 KB (21973 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.18` - linux; s390x

```console
$ docker pull drupal@sha256:410653cc6f11f8a3ee3868a141eafb85a1b9311dad0ff73f2ad289347d579dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34984357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d395109c5f21d905d9d98d593c8a0cefb1478a9c9b8d4a81e71b1f0d6bbf564`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3413052a1d508babdec59ce57cce40835c4c1cc4cd0a76ca57367f5157bfac`  
		Last Modified: Sat, 27 Jan 2024 13:02:31 GMT  
		Size: 2.8 MB (2792799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853cf4113ec71c9f8cf3d722ca3c5c66d434d7d4a34d817fd59a0beacdc2041d`  
		Last Modified: Sat, 27 Jan 2024 13:02:31 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6540cb25a1124aa604da77e43818a829a1aaa3ba794e7dec5929005ae8753aba`  
		Last Modified: Sat, 27 Jan 2024 13:02:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2ca59d2adda6158b99009b36d5fa0bfcece7210e3ad3766b2f58e8b5d5d69`  
		Last Modified: Sat, 27 Jan 2024 13:06:03 GMT  
		Size: 11.9 MB (11935694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437e39e7fb7ecb9e1b6bd59de82811290aa6d1938e1f414716917d58ac979e5`  
		Last Modified: Sat, 27 Jan 2024 13:06:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f12dc0dab29c52e03ad3c4d36ea86ca9a55f6ca8dbb38fb8ebc9777681fa5a`  
		Last Modified: Sat, 27 Jan 2024 13:06:16 GMT  
		Size: 11.6 MB (11596442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948e73d3e0e9e48d6f24abd67e00d1ace09cff5ffbb4806bff594d3a12b2f877`  
		Last Modified: Sat, 27 Jan 2024 13:06:13 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b0047f3e662664c4ece240f7c1a02101eca3bbaac8963062ceace7e53a7fae`  
		Last Modified: Sat, 27 Jan 2024 13:06:13 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c87428ad0eaf048139fbc3c1cebcdb5319faa41686c4898793678dccad3187c`  
		Last Modified: Sat, 27 Jan 2024 13:06:13 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa77bd582ce206c73773fc219f85448495f7122229666d30d15eb48db2f244`  
		Last Modified: Sun, 28 Jan 2024 03:57:39 GMT  
		Size: 2.0 MB (1990559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78457db23d116c868d97e01b468f038b9aa02877a970296426d5fd6c85bb0adb`  
		Last Modified: Sun, 28 Jan 2024 03:57:39 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e393068d673147653ab898ecf6958ed34342e133003b340e891e9f7e9233dfc`  
		Last Modified: Sun, 28 Jan 2024 04:26:29 GMT  
		Size: 3.4 MB (3418898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:d2b1456e2cf294683639c1d348f1770a08d442591402e256cc26e06ef6149a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 KB (252515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c63d3d8bce1b96129a2335f46d31a8c422ed1dbd1e68e6302b77ef678f3cf4`

```dockerfile
```

-	Layers:
	-	`sha256:bb9fd826bc3001f42ce53673d3ac1f93d7815e82b1e28201f94cd6aded627930`  
		Last Modified: Sun, 28 Jan 2024 04:26:29 GMT  
		Size: 230.6 KB (230595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f198575e59a81721de7d8a2c3322a736741d6f2a9d18edbe6d74c2c45af68e2b`  
		Last Modified: Sun, 28 Jan 2024 04:26:29 GMT  
		Size: 21.9 KB (21920 bytes)  
		MIME: application/vnd.in-toto+json
