## `drupal:fpm-alpine3.22`

```console
$ docker pull drupal@sha256:890433065f8486bc4bf53e468037b0bf2834245a9f59c52b1c170033c22c454e
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

### `drupal:fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:b914917fbf96e9810d54bd1253c607be4be26692d5f87486f6cb8305dd8aa451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59966658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd63c1cb79eae0a9ac55acda75021aa2fb87db08c442dd86ea299f9f37ecc89`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f896ec01cf02db411672be62f368c6417cd797ba4ac276cb094102820fcc89`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3468343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e8913045ee8a77ff25236b174e5b5270a0420a1fe8390a3b6f8ad0e0d20ce8`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d7d5d5b71e3cd3e8d9c1684eb5d30d7429531153a8ba4053f6abcb6cf690b`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fd6c290c910b96c08d96e5cb89bed95b6128732bfad3e447c577af0fd87745`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17eb8dc33b9b4e3f65f9a6e37a480e944276361d70b0f633c3314521470638`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b900a019361d96a7f12ade9f0a4f5bfa230148a52ccf7da5245a6b195d491d8`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 15.7 MB (15706263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f524a204b4c5fc11d1551f24f1fb624e722b67f2f7b17f5e308df6778c27fbfe`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72000d5649d1c71aa1c3407ed74025a7d0b89682d49fa19b0c5ea234d44fc955`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 20.2 KB (20201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dfcfa68f8f4a3901f938a1ed50a22cbd612b6d3e4d999d59cf294898113d55`  
		Last Modified: Wed, 11 Jun 2025 01:13:07 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c39096afafe3372952ec08d3b73d8c5cc20c2b88297708a02f27d2e3df31d7`  
		Last Modified: Mon, 23 Jun 2025 22:45:21 GMT  
		Size: 2.1 MB (2057660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e587d4c6b2efc78b8395013e35cef3f84ac81fe33e2128bda30bf4f321e183`  
		Last Modified: Mon, 23 Jun 2025 22:45:20 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2eddcc2a81fb789f71742c09277f5b7f5b99ef97e8b102ae073d1bcb33be09`  
		Last Modified: Mon, 23 Jun 2025 22:45:22 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73ac20630b2692a0f51cfed717bdad401f4e939698bec44aaf5f8ed86803df2`  
		Last Modified: Mon, 23 Jun 2025 22:45:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70703547492f9a6b3fec5774af48f65807c870b98e4a1e1861f62ccf90b930a1`  
		Last Modified: Mon, 23 Jun 2025 22:45:24 GMT  
		Size: 20.5 MB (20510318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:5d6526b29246941e83aad74af7e6eee3cdb56af47851a49d3523e8508ca96b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 KB (420126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bbd95897072add539485fe6a7ab10259853b933849f65331d7b0c90b71cd53`

```dockerfile
```

-	Layers:
	-	`sha256:f22d80c389981b3850c069cb99d04b656111bef782fc3c13c61055111620e2cd`  
		Last Modified: Tue, 24 Jun 2025 02:01:35 GMT  
		Size: 383.9 KB (383897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6d5a02d1aff8853c4da628c398bee6a1347979c243745f87afd46bd8497ed0`  
		Last Modified: Tue, 24 Jun 2025 02:01:36 GMT  
		Size: 36.2 KB (36229 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:5318b069d6175825362f46b279af8c2cea6d705b80d307057c8532bcafce7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57506007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e330ef845f82e883df087ee4971de645b4899c6ec31ddb083ae511b14ef2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4687138ef1b3e99885659dae1a5cf5349f783843ae00824004e438ab7ed8351`  
		Last Modified: Tue, 10 Jun 2025 23:58:25 GMT  
		Size: 14.2 MB (14221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0744f400b10ac6f4b3cf435d4e3ef449c59b28a5999fd5b7097dff792a0ee9`  
		Last Modified: Tue, 10 Jun 2025 23:58:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e812a32f76d7ef633d060ca2ed16cc333fce43a92341c1a8285a610af3191`  
		Last Modified: Tue, 10 Jun 2025 23:58:25 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0966900079d27d1ee2bc63b304027ae72dbeffbd8c77619ac24ef0ab45b9ca8`  
		Last Modified: Tue, 10 Jun 2025 23:58:24 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ef50046926d86d1085d95439659f368c2d24ef20c64a899afddf25d7c15b1`  
		Last Modified: Fri, 20 Jun 2025 22:07:51 GMT  
		Size: 1.4 MB (1413209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20433aa46f14d7472e0826fc86da14c74a9ccd1a550b7709d3dafa0bd1e4debe`  
		Last Modified: Fri, 20 Jun 2025 22:07:50 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363881254f3a5fbbf6a1f23f851c987453f3e1def68ea95c1050561363cc5d7d`  
		Last Modified: Fri, 20 Jun 2025 22:07:51 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ff2b8d1da62923f3f77c6c3e294a7b1d825a39c5f39ea5acba01b8c57155db`  
		Last Modified: Fri, 20 Jun 2025 22:07:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e4c90ae6b82121fa764d36dd37c704d92ffd3cad90ebc070e64af4389d5e6f`  
		Last Modified: Fri, 20 Jun 2025 22:07:53 GMT  
		Size: 20.5 MB (20510658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:19a1956bebb31e6e30e0d924a4760debb8e96d3694263474f2fdc4057de7cb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 KB (36234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12190a18ec5df98a937b28014f12b43c1cad0ffe0fed9a8f22bc9031e163dbd2`

```dockerfile
```

-	Layers:
	-	`sha256:3e3f14206ca4770bf627fa6f743434745d3ac444eb6d6c63aa0449eaf7228352`  
		Last Modified: Tue, 24 Jun 2025 02:01:51 GMT  
		Size: 36.2 KB (36234 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5a2a507f7698054dc18c6e5723b8f07c99e44015b2d13fbad9e659afe915f71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56177074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7ee026d9899740591d26901a0b34cf8a1f90edf0134bcebf5bac893fa2c39`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90c7d1200e63780d07ea41b0a7f65c74d5dab904749dab0cc513a3a64c00be6`  
		Last Modified: Wed, 11 Jun 2025 11:46:07 GMT  
		Size: 13.5 MB (13467909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aece583aaea2971fef666ff25988fbb135f21ab4e3b13a358686e5ab47d1c2`  
		Last Modified: Wed, 11 Jun 2025 11:45:59 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525be7ff5e53c3bb5385a0532c7b0827e98188562e24b0f83496c931075a0e97`  
		Last Modified: Wed, 11 Jun 2025 11:45:59 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e8a98be8524df081a3db896ad41983cb1cf45ea14b4f530b750ff83c0970f`  
		Last Modified: Wed, 11 Jun 2025 11:45:59 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df1da20062bea6dc349058b61feaaf3bc8dcedf9a33b6dc5f52ba79b505c1d1`  
		Last Modified: Fri, 20 Jun 2025 22:16:41 GMT  
		Size: 1.3 MB (1305394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf5007a78dc8b6fbb7589dfe0e394530a5fe0782c8e3aa019f386992ead540`  
		Last Modified: Fri, 20 Jun 2025 22:16:40 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7870d9970e3bfec4f277fcdc6b3be3ad12b40367b645b8145005e13d1ef4d8`  
		Last Modified: Fri, 20 Jun 2025 22:16:42 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1ae2e1fbf343241c11c8fe9cbdf29e3983b2abec4799a43986066979906c26`  
		Last Modified: Fri, 20 Jun 2025 22:16:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d177d0e6768a3dd8321777ebbc1824641be2b73a582a3d322859cce21dbac6b`  
		Last Modified: Fri, 20 Jun 2025 22:16:43 GMT  
		Size: 20.5 MB (20510110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:d7154309fd74e76430483b9e34ff4dd337c0254d96f950c94240bce4b3ecfb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.5 KB (417488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655d7688393631d56e24a1bf2de09c982afead66104ebdf8b5ee4863ffe3e4bf`

```dockerfile
```

-	Layers:
	-	`sha256:ef893da0eb0687837f06dcaa818e34a6aa1dcb069a7e65e41eb8d788c7461cab`  
		Last Modified: Tue, 24 Jun 2025 02:01:55 GMT  
		Size: 381.0 KB (381039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26b5af4b342aee62c81b81c165e849888bf6962c6adb4313c7edfcc726045d4`  
		Last Modified: Tue, 24 Jun 2025 02:01:56 GMT  
		Size: 36.4 KB (36449 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ce135d888e29d691a5f4eeebeb31e1d32466387c196d0338a24b4eb189988eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59844260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a677855681152c1641001c51f377cf10160fb4ac1af6e766366dc57a1867713`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee1ad5083d6c4a59de1d5515e08e5dd3cd31c6471a9a82a3333d688becfb7f2`  
		Last Modified: Wed, 11 Jun 2025 11:00:34 GMT  
		Size: 15.3 MB (15337097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8608b81f668e802f30cec533788f1d16f71831b2d9f82475ef00765ce68bb2`  
		Last Modified: Wed, 11 Jun 2025 09:12:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b44b30cf1128a40808315f58f68f1ae723578bf308a3ef8813ee864bc2f6807`  
		Last Modified: Wed, 11 Jun 2025 11:00:35 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d987a346aae09d6c3aa428d6dc8bc4feab41037086790f310b57d33cf2f7bc21`  
		Last Modified: Wed, 11 Jun 2025 11:00:37 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6847edea10ef5661618b96893db0b3bdcdd09d49876e16013f85cb9eaf22580`  
		Last Modified: Fri, 20 Jun 2025 22:06:38 GMT  
		Size: 2.0 MB (1963306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9b2d896461127b0f7f3e35bb3fdf49ce4f200b3794b6c527e1076deb07759`  
		Last Modified: Fri, 20 Jun 2025 22:06:36 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b202c631bccf2b1a20317514bf1ea3d15efad5e904a56a8f1b18d5f2e6aeb2`  
		Last Modified: Fri, 20 Jun 2025 22:06:37 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef53cbd7304b54d7ebaf53b169f8087fb0b7091a251f9a3c1aacc2a2cad2fcb2`  
		Last Modified: Fri, 20 Jun 2025 22:06:36 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab23f5ba8783b471bc35ab9637d2c739165290e98eb0d864803233869b0cc3`  
		Last Modified: Fri, 20 Jun 2025 22:06:38 GMT  
		Size: 20.5 MB (20510226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:05514e0ea3a15473f0bd40abe16a3510b1f0c2a1c5b1cc80be7d0fb6a4e47927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 KB (415441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bbb4d795dede15310cf80da3bc44e67ccee52fd93800c3d3fb639b07678b2d`

```dockerfile
```

-	Layers:
	-	`sha256:766e41c876425bfd86f04be811bdca487dc519a53b59638cab7e71a0c07f94b8`  
		Last Modified: Tue, 24 Jun 2025 02:02:00 GMT  
		Size: 381.1 KB (381107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03c31cb6d0dbd809acd192176177b11fa47bdaaea247e19e23c2f07fe18ee60`  
		Last Modified: Tue, 24 Jun 2025 02:02:00 GMT  
		Size: 34.3 KB (34334 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:f705ab42792a63f15f20e6dff9551b1749f6ecf83e2d47f9d89601204308c6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60345570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94db8461abce93aae5c3d0e0dfc3099ea982047c0ff47d72206ab9f9dc62d24a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527bd29aef5241e34b340256391e5f3892945ecd834ed23ada4c7a1e28fb7aa2`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 3.5 MB (3527783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6792ddea86a3f97df62a6befddf412803268834373b0ef544f3f2b1587b73db`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d7d5d5b71e3cd3e8d9c1684eb5d30d7429531153a8ba4053f6abcb6cf690b`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fccf898fdd5cbee119e3e1ac47546722e332be49a545c0148b065868494af8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:06 GMT  
		Size: 13.6 MB (13640485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17eb8dc33b9b4e3f65f9a6e37a480e944276361d70b0f633c3314521470638`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba819796aff4a25a71559119bbe3426b4c50ef8106192029b45b8c81babc83`  
		Last Modified: Wed, 11 Jun 2025 01:13:05 GMT  
		Size: 16.1 MB (16099708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9356444cb387ae516483ff866b21883fdc5100d3387ebc2a373086619a18c56`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37c383a8d9cc29556868a2a8bbcfe357991e0b915aec5541a5f21adce65e584`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd78e2dbadda7fc4bb16203c0f3455586a10ffc83f774dd86fefc88251afcc5c`  
		Last Modified: Wed, 11 Jun 2025 01:13:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26149a341545d6fe79dba483f5b21bbf2792e2c0d62d4e446725831dd557e38b`  
		Last Modified: Mon, 23 Jun 2025 22:45:41 GMT  
		Size: 2.2 MB (2164371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81887433bde2dcfd7150e74216e71fb7df3bb4b83c90163399d8bde031166265`  
		Last Modified: Mon, 23 Jun 2025 22:45:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59fb1ec88f709c692b42d9a060f1c2079fbd1f39273d35848d0472e2276da05`  
		Last Modified: Mon, 23 Jun 2025 22:45:41 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245f59b73ee5320b845f69836409de1c40ef51fa443d8d368a5c66598b3e705`  
		Last Modified: Mon, 23 Jun 2025 22:45:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b53bdc16dac93b90e120136d5b78b90f0fd9ce57515c69c103c4579edfedfc`  
		Last Modified: Mon, 23 Jun 2025 22:45:44 GMT  
		Size: 20.5 MB (20510516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:dc935e2b041d1c66f7ad5487fb78cc36886dbcbee8ab197799679f2569e8e04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.9 KB (419938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c39f9b46b43b40f16dfdff28ca4ca03d03642931b2bf43adef3f4633a0bf18`

```dockerfile
```

-	Layers:
	-	`sha256:b1b9129d613063119f6629a8e12b48179283fcb5dd5434d5a97b331fece328fb`  
		Last Modified: Tue, 24 Jun 2025 02:02:04 GMT  
		Size: 383.8 KB (383812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf6da7e67ee1dc1ca8d2ae42ea091e71d88c99c6e07cacfed38b79302d260a6`  
		Last Modified: Tue, 24 Jun 2025 02:02:05 GMT  
		Size: 36.1 KB (36126 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:33e0e781f4f34065ab45db1190c4e797a4715c31a6485931a3e107c461bfb48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60174438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a719f065409fb467074afaafb2cfb3ada4a12655abae08f1d3579124ee91c1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a73dad1c4f1fd0a13e426ae43f5ecd3bda92bec9ca55546fe406c5f29914b3`  
		Last Modified: Wed, 11 Jun 2025 09:17:35 GMT  
		Size: 16.2 MB (16178552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7c082c6bed833e8bf8e283b0a9f0b6e4fb5b4a682794a83b35e78aa5a83cb`  
		Last Modified: Wed, 11 Jun 2025 09:17:32 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321b6a769983fe59fcb99aaab516277d9f8189e1bf14e0b6632950ad121e1c2f`  
		Last Modified: Wed, 11 Jun 2025 09:17:32 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8dacea5ba1e3c8c6e15f0cd3330ccdb77704e1d5043caab32bdfeabf9bac20`  
		Last Modified: Wed, 11 Jun 2025 09:17:35 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c5a4c6996631f4fa50d90d420a1e76d80a148f975dc2cfaa9f10becbc6975`  
		Last Modified: Fri, 20 Jun 2025 22:11:51 GMT  
		Size: 1.7 MB (1709803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f17654afb6681dfd4bc76ea59cbbd4e70d549e4e7c48ad212a7a4ea6c2435f`  
		Last Modified: Fri, 20 Jun 2025 22:11:50 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0fe25e615d1005fd3015b733688580f113c71255328af11203eefd609f96ff`  
		Last Modified: Fri, 20 Jun 2025 22:11:50 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc502e89abbc1d9d19bee7f206b12e190260d034d917e214de3f0cea42acf05`  
		Last Modified: Fri, 20 Jun 2025 22:11:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab994578d4cf76bd310f2136fae037f9308b97d6dc63c42dae269f8978da8b2`  
		Last Modified: Fri, 20 Jun 2025 22:11:53 GMT  
		Size: 20.5 MB (20509734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:db38e05f9fab18d0791490832bad1a7b42ddaa0ee3915e64a58e79db859448a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 KB (415421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302d6741a2e4bf590a0031edb8ea2107b9637a488ed3074a2a5b3306f33834cb`

```dockerfile
```

-	Layers:
	-	`sha256:73c4cc6a2d0a58de93e85b37877ce5adf3199eb3418cb8e5fda6d1b4a81443ea`  
		Last Modified: Tue, 24 Jun 2025 02:02:09 GMT  
		Size: 379.1 KB (379062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8c8eab2639820a909c466d4e082842c3e10baa99aa99a448ace0235862c72e`  
		Last Modified: Tue, 24 Jun 2025 02:02:10 GMT  
		Size: 36.4 KB (36359 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:48f34ebcd6912d0862750b4f75695c614d3120e940a252180b4491b9294df062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58662793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526ab47843a5e45c51e028f0420ac487016ee61ef385cbb7202bb3dba19c78e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112a7ca61ae91f0e3c82d961eb3626e4e76928c5b852baf3e6a498233b2c6ca5`  
		Last Modified: Wed, 11 Jun 2025 03:32:54 GMT  
		Size: 15.1 MB (15111627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680550dafa433ef13a31340347ca358c20955f90fb9d34e4f905236721fc119`  
		Last Modified: Wed, 11 Jun 2025 03:32:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e735e6aa6f16d6212a39c6bef86dc04b6f4ff72a1f76bd74293a8071eaf8f4d1`  
		Last Modified: Wed, 11 Jun 2025 03:37:47 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd62d8ea2f454c60af6403e1ed3e7c3b74a95c292a6653e913cd613d2489e39`  
		Last Modified: Wed, 11 Jun 2025 03:37:53 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e7ced698da3d4809f3b9c582b75d9696d4d03f4884a9fabfba78cb5325b484`  
		Last Modified: Sat, 21 Jun 2025 06:36:24 GMT  
		Size: 1.5 MB (1495699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02afae9cacb37d9bf2330b233827e8fa58b8bba3f5f4253388d4bfafa3e9e240`  
		Last Modified: Sat, 21 Jun 2025 06:36:25 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a070ebe86d5cad707ed0e985f844fb52176f25cacef06e1aaba63b068d31fac`  
		Last Modified: Sat, 21 Jun 2025 06:36:25 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2003c286fca550fa09f0fb408fcd557c8c72671f2cd7d70b19155be523d32ad6`  
		Last Modified: Sat, 21 Jun 2025 06:36:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e2a25b7413ad5f4c7e92602e6e63e722f060d8d1ec806f00d13f86dba3785`  
		Last Modified: Sat, 21 Jun 2025 06:36:27 GMT  
		Size: 20.5 MB (20511287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:fa8dd942689be22b797fc1c3d1cefda597d8bb34acf1a437815ab6d1a420aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 KB (415417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83452f202cef914f52b253f3934e8ae1d42c5720aaf5ef763181f4a7e041e79a`

```dockerfile
```

-	Layers:
	-	`sha256:332b083a518ba37ff0f60ee248e2df33cbd95cec1d51014e6879184000d93214`  
		Last Modified: Tue, 24 Jun 2025 02:02:14 GMT  
		Size: 379.1 KB (379058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a7e4f0e620df0a905b49d9626ebce7d0bc2a87ebe5845869225f89eca428af`  
		Last Modified: Tue, 24 Jun 2025 02:02:15 GMT  
		Size: 36.4 KB (36359 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:b06c47426fe8961e38489e5797dacc7b4a921bc5709235b2731759f85e2a6bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59801820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3a71b8fd98feed4a47c0eae26315bdc2e93e87115f58e4a89c52babf85273`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 21:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 21:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.4.8
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 21:43:33 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 21:43:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 21:43:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 21:43:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 21:43:33 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869e89e860a0e8efe4b13fabc220788c0f1938fe54d423cacf0d87024d0c858`  
		Last Modified: Wed, 11 Jun 2025 08:13:39 GMT  
		Size: 15.9 MB (15886808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e55c0f834ebc37dce366fd44aa345e322607bdde81376395f5739edd01046c`  
		Last Modified: Wed, 11 Jun 2025 08:13:44 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276a4796f856b8a46f6948818f7eeec7af4badd16db241f076b8cc3b9bb4f20`  
		Last Modified: Wed, 11 Jun 2025 08:13:48 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab310fd6a38773f1b897350464ee4ae855982514b7c0b268a0f5124397693708`  
		Last Modified: Wed, 11 Jun 2025 08:13:51 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8740170380395a8e8f7517561aca1253614c97c4d8adf770727953fd839550d`  
		Last Modified: Fri, 20 Jun 2025 22:08:46 GMT  
		Size: 1.6 MB (1630997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f9c490c548532f97b12bbe9d869874bbf6b90748d2a7667140f246a5d404d8`  
		Last Modified: Fri, 20 Jun 2025 22:08:45 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b369e54940dae4c618b0c376549aa298a94e99f413c268287b680772b6e989d`  
		Last Modified: Fri, 20 Jun 2025 22:08:46 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff201f05e118b9ea566a32887be85af821a9db27801ab0f473549b5771011cd8`  
		Last Modified: Fri, 20 Jun 2025 22:08:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170bf1a5a70077d72d1ef5d0362d492647070335d17805c2c532028f2f0b3a6d`  
		Last Modified: Fri, 20 Jun 2025 22:08:48 GMT  
		Size: 20.5 MB (20510467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:df3225f265d316099accfd0c9778b7bab442cdf28cbe53098dade1f5d6fe8fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.0 KB (412987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b652add6747421fb02760e41d4266ad23269f9de88c765397ec240a1c2bfb2ee`

```dockerfile
```

-	Layers:
	-	`sha256:10a36c55e8d3110628a0f9d0d8e927be35cc5f5a11bffede187efcc24164aff1`  
		Last Modified: Tue, 24 Jun 2025 02:02:19 GMT  
		Size: 379.0 KB (378956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e94cc02950d5eb386f01481e6990ca0b61992a04167c60dbaef77c5fd6dab5f`  
		Last Modified: Tue, 24 Jun 2025 02:02:20 GMT  
		Size: 34.0 KB (34031 bytes)  
		MIME: application/vnd.in-toto+json
