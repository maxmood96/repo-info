## `drupal:11-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:8052cbe53ee0d5c078c53fca545646e17e5f1b0616d755a7d99ef38bf53639e0
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

### `drupal:11-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:a9c477bdef88f1f8e72c3e170a75bcf2de6a20c18cff157079d9bea2b0304b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55376741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b901ec4a95403ffd714aeeb89ae4d8472f4fac33ff638db164fbf8b265539110`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9897d4ec1041097c5033a0a9d262372beaf5bdbd874450d8baeafea3772fadf`  
		Last Modified: Fri, 14 Mar 2025 00:19:11 GMT  
		Size: 3.3 MB (3313896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84c6e0383cf96ff3bc2b3949b3ee3343a85253c4d6a31a17a3d29898ea91188`  
		Last Modified: Fri, 14 Mar 2025 00:19:11 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bbdd3e0e0a9fd64969387962f37f1e8b2aa48be866cf549df9e33d409dd82`  
		Last Modified: Fri, 14 Mar 2025 00:19:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbec0a553a9a1e6c7f90cfc8ee4d305412b8c4f97e28414900d3d7e13ac195e`  
		Last Modified: Fri, 14 Mar 2025 00:19:11 GMT  
		Size: 12.6 MB (12582215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59384ae8b4438fe5a7c0979d856827c15c39d449bbed9dd6124f17dcae16aa31`  
		Last Modified: Fri, 14 Mar 2025 00:19:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8f5ff3d0bd3484ec63c85278aa7e485a56abe73e50dab9847792a62c2f2f37`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 13.1 MB (13120129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20e4d84dd0b465d133a1d11945a5e27e8743bc701b3343c2c02f8940470d8b`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9123c443eee724be756cdf1a649ef878f41d8e4cc4818c20438abcd1544b6b`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 19.7 KB (19701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b103ad385a984f4a5e74011d64c3df1ce66adcb923fc7749d070681e2c133a0`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c751e5238b0abbe1664c7ae1a8665e2168d745a4bebf22aa1d7d9a925c729087`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 1.9 MB (1902183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022d62888e879a43c6e73e3d54c56abf8544e715bd8dcb1ec7f7261c41d7844e`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c66a031e414fb58b7970d0da6b9ee0e64a44d2b669db58cc2771213005c54e5`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 740.8 KB (740823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90ebd394b6537adcaac6dfd22e8edcaa68aa6220bbf756cb857963a7c66b61`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feeae75fb85331df62c9acf1857e47fa57a27f3e2774de73ba41ef255c97180`  
		Last Modified: Wed, 19 Mar 2025 23:21:50 GMT  
		Size: 20.1 MB (20057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:a36adbfff0685a30dd6f819b7a20dd8a3a86b88852a29410782d2e9e5bebe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 KB (391009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b387a00ddd836e82de4b07bef305a95210f7303a77dcb3a51ce68d80d569a`

```dockerfile
```

-	Layers:
	-	`sha256:4dd43c4b82f6f198fd0eabd62a44db743bb2e57e36c4846c016d19d62a492305`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 357.3 KB (357335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a162307aa782c74314113f900e503019446d71cbe4a904b3ebf79f2c111d4c`  
		Last Modified: Wed, 19 Mar 2025 23:21:49 GMT  
		Size: 33.7 KB (33674 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:23ff534c90878758ed7f374bf8099f1d0f1a518d30852d4f33cf6be111c50262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53411670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723e31d8a21f0087d823391602e7f5d7d1097b4cb8246beaaa62dfe3a0559acf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0f79d4d985a64f9865dca6388accc72536a8134bb71d173eb4214c357889d`  
		Last Modified: Fri, 14 Feb 2025 20:14:52 GMT  
		Size: 3.3 MB (3298263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffe6d763475cabc6526162b5d931425de2a4941987a9a47a37817994c917fe`  
		Last Modified: Fri, 14 Feb 2025 20:14:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be80b03c756f18e75ec416857bff7aeee3ead6c2ab8410c9194efd506877e5`  
		Last Modified: Fri, 14 Feb 2025 20:14:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e68c063264688e9e3f2dadd7fca5c92f41dfa2b4647e343237d2a64d84f56`  
		Last Modified: Fri, 14 Mar 2025 01:44:36 GMT  
		Size: 12.6 MB (12582227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9fec638a56d4e5aa485350cfaccdd639c1091c2bfbc600ad04ca916e4f48de`  
		Last Modified: Fri, 14 Mar 2025 01:44:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb399d0fc9a3248bbd8c6f00aaeadc58f76a0bc976192b72987d6825cdfddd1`  
		Last Modified: Fri, 14 Mar 2025 01:56:16 GMT  
		Size: 11.9 MB (11941924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcd6f1d8c9d4ac6754611f00bf3c0198d8740792655598023f88d1e2ce2c4f3`  
		Last Modified: Fri, 14 Mar 2025 01:56:16 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa56bebb69fde9d7c01b583a4c40bdcad7cf0dae97df0b0c42f826fb78c2f90d`  
		Last Modified: Fri, 14 Mar 2025 01:56:15 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb8392a181a93f4081ad4944b408d0036a0ce61aa3aa087cb9f02316539d2b`  
		Last Modified: Fri, 14 Mar 2025 01:56:15 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23dcc8ed0e4a3775522f42930e2a36f74e25bf84c505608e178871571f38d52`  
		Last Modified: Fri, 14 Mar 2025 06:18:09 GMT  
		Size: 1.4 MB (1385555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83c00be252181ce39f4304c79a7662a96b84aa23453849f2c2cd7babef842df`  
		Last Modified: Fri, 14 Mar 2025 06:18:09 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0cfa5bcf84e46f379f1bc289a9725d9cf358b06d6a710ad761b138ae526c3e`  
		Last Modified: Fri, 14 Mar 2025 06:18:09 GMT  
		Size: 740.8 KB (740818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871cae1ce3ec7641aed6fda6fd3df2652c6c5dafa5d141a3f32eacdcbe5cc3cc`  
		Last Modified: Fri, 14 Mar 2025 06:18:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4849a0afa676a8975c713ece7d2750cec928417ce108325f239157bc28438fef`  
		Last Modified: Wed, 19 Mar 2025 23:25:28 GMT  
		Size: 20.1 MB (20057124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:b41f196503c31c4805d4411925c32603cc1d7af65991932bc5bc67f69853c486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 KB (33614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e4e4dffd591adfe5a26c6c220d9a45a4ab4db76e4ccde8d25eb4cb14dbbab7`

```dockerfile
```

-	Layers:
	-	`sha256:c19c2dd86df0d36f10f276c53af39bfbea2903ff236105b536844937042325b0`  
		Last Modified: Wed, 19 Mar 2025 23:25:27 GMT  
		Size: 33.6 KB (33614 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:bd446accd1a926d484b93531dfdd241140039aa8acc818bdbef555879ab58b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52084088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccf7bb8b17882f27fafbbc05e4757e0b00045f029fe3f037ddf1914768d1ede`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f435e04ea18170faa15db5a195b7a456fd6855803819a3ec1feb1150cc547b`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 3.1 MB (3104652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d965c1f9e2eeb816a67542a273f236e46e8776d2aaeabebc43098c502ee68`  
		Last Modified: Fri, 14 Feb 2025 19:57:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151a378a33b3d6443d5e2151a40e50e2c7f67f3b501115627d75e1ce417f91c7`  
		Last Modified: Fri, 14 Feb 2025 19:57:12 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd4097822b7af3c7920a7c5b85a179405f4ae0314bbf1821b7d3d480d2c05e9`  
		Last Modified: Fri, 14 Mar 2025 02:09:05 GMT  
		Size: 12.6 MB (12582209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12554657cbfdff0638fdafde23f90fc69ad564385a3d5cc695043a43a7d021`  
		Last Modified: Fri, 14 Mar 2025 02:09:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da8145ee76219bfd8231b50dacb57aedaba707c61f133895528b3d976d6d405`  
		Last Modified: Fri, 14 Mar 2025 02:12:41 GMT  
		Size: 11.2 MB (11194217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd605e81c4f9b0f3d096f40acf104a5a9e28b0ac1f231aef1a90a3632c8901d`  
		Last Modified: Fri, 14 Mar 2025 02:12:40 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19cfb05607bffcc8c4cb049daacb55ef04ffacc23b686c6dae38b780616bdf`  
		Last Modified: Fri, 14 Mar 2025 02:12:40 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26acb8696b63a1ceec45ae8483cacd726c8142b2b2e3715296847a3061c528`  
		Last Modified: Fri, 14 Mar 2025 02:12:41 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb989cffae2abf6a5f2e5210437169e9e77921e1d3361722e9366377f20a7d94`  
		Last Modified: Fri, 14 Mar 2025 16:26:08 GMT  
		Size: 1.3 MB (1275878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a64383102d58c39b8e69e774edff59cb2a35fc849e27bcf08f5975871d790`  
		Last Modified: Fri, 14 Mar 2025 16:26:08 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf1be4b521be20db73be671691193e87e63d54dbbcd9f8d93c700a7f0c1a039`  
		Last Modified: Fri, 14 Mar 2025 16:26:08 GMT  
		Size: 740.8 KB (740814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b2d5471aa1024f1fec2c4b5382f6ec35218b8bf682d1d1bc17dfd9871b8fd2`  
		Last Modified: Fri, 14 Mar 2025 16:26:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d247cc8fb66895a6e9c37a106f7e291fd8193e5413fd1bd08fe16ceab701662e`  
		Last Modified: Wed, 19 Mar 2025 23:51:46 GMT  
		Size: 20.1 MB (20057119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:175df215d015152c78c0d625bb0198826afdcebc6e8408cd122de13c799c5aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a42eea8a9ca59b6f611e9ab11a8868781d7dab5b5747c36bcd5bf8ed6fe4049`

```dockerfile
```

-	Layers:
	-	`sha256:494bbefb94c8c5f8dbeac2ebb8099334313cfe434075f433e4cc2804f0e9cd41`  
		Last Modified: Wed, 19 Mar 2025 23:51:45 GMT  
		Size: 354.5 KB (354542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b0cc8dc64bba26a0c9a033e612246b7ff5e2b063e71adf780222a777ef9cf1`  
		Last Modified: Wed, 19 Mar 2025 23:51:45 GMT  
		Size: 33.8 KB (33830 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:626f0c32a53f10c7697843b95fe26be69c02131ac15bcb0314168bb230a9645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56223841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baf3f45ac3393dc5068e98dc2f9bbd3d84af096a671ae750b8c88718aa0615a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64278622ee4008648cd0d08a890af70672bfae53a983eb2b10fe4a65ed3b936`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 3.4 MB (3365209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95666ce1b88aa4cfd448a2dfecfe7a221115807ae27fb0bd41f2d5920815884`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa970535345bac62ab689111e4438c3ed5b2c57f743763f4381c198f307d845`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997de3f717edc81938963f38c31a2b0a0254452e3a266831c8982f385ebe995`  
		Last Modified: Fri, 14 Mar 2025 01:40:42 GMT  
		Size: 12.6 MB (12582214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aae8c37580030752aca71610ee57df6c33ae061869f4be1845db1a9fb92233`  
		Last Modified: Fri, 14 Mar 2025 01:40:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ef4b3ebadee3b616bfa3e9d7d96b43fa022778b8b6dc000c038cdf8039464e`  
		Last Modified: Fri, 14 Mar 2025 01:46:32 GMT  
		Size: 13.2 MB (13174346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5441928aaf129a39b4e6ad5cfcfa7f4a9338274825dd294a8344eafcbcf9f94`  
		Last Modified: Fri, 14 Mar 2025 01:46:31 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fd48cf88b17ee80dfe058e885f9f3476fd854c584a5f1bff7d36a3b50a683`  
		Last Modified: Fri, 14 Mar 2025 01:46:31 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d112ad84680f99b6aaba94796695c4b54ca39a4c8129d85fad914ce5f865b9`  
		Last Modified: Fri, 14 Mar 2025 01:46:31 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e241b095cd2cd7a0d16fabcee6caba6cf2b877a6d0ccbb78befcdc15abe47cc3`  
		Last Modified: Fri, 14 Mar 2025 22:17:13 GMT  
		Size: 2.2 MB (2179404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e62087852a94a3165211b533ec73890a1d144b8d6c96555e7b4b9509724b31`  
		Last Modified: Wed, 19 Mar 2025 23:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e205beabb3df65f895b0d48640acd2f6ea163f7b16c6847c9291e2d765770f1`  
		Last Modified: Wed, 19 Mar 2025 23:41:45 GMT  
		Size: 740.8 KB (740825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f95dc900aadbc34911ceda9ca0ea789f3706c2c1fdf44c75e2c54c6a344234`  
		Last Modified: Wed, 19 Mar 2025 23:41:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10052c6eb84a3271b9ed3bc2439a14be3737d37bff5c4906796e631b59f46de1`  
		Last Modified: Wed, 19 Mar 2025 23:41:45 GMT  
		Size: 20.1 MB (20057464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:2ba185c2c62e55013e311a9e0a0732e03e4d028ed3b9af6841f4ebe429974193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 KB (388460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075efd2ccd4c754d3b78588ab7876a27132e16971395e94dd67cb5f06175aa20`

```dockerfile
```

-	Layers:
	-	`sha256:633bb4c2e0b51f25e4b62e63fbbd7e991485cf9b866baaff6137fef9062bce92`  
		Last Modified: Wed, 19 Mar 2025 23:41:44 GMT  
		Size: 354.6 KB (354578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f708eef936449c5a3b4b09bcc945a8545e185632df64bd2faa9a321bbe02a5f3`  
		Last Modified: Wed, 19 Mar 2025 23:41:44 GMT  
		Size: 33.9 KB (33882 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:2fd06a503ce6916290cb48ca6f74ea38e0ff39d963b2e705d47145ca2393a8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61008456966270c3968a1c1829733b63cef63bc4ef77535be2ae5f9130414b3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d125ca47b043f8f90dfb7112384ddda481c1aaabc2a65cced021f07318b2d7`  
		Last Modified: Fri, 14 Mar 2025 00:19:23 GMT  
		Size: 3.4 MB (3365467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a12b4ca79e0ce76cc7a500480886834cc5e11314fda3f5feb3acf65b98666a`  
		Last Modified: Fri, 14 Mar 2025 00:19:23 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d0bb20f677c574d8d37f05e646fab6fd8a91e9d38c3cebfd923480ef697c0a`  
		Last Modified: Fri, 14 Mar 2025 00:19:23 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f373756369ea32f6df839bc25246f7c0963bb2c645a7524f0cd2c03883da7`  
		Last Modified: Fri, 14 Mar 2025 00:19:23 GMT  
		Size: 12.6 MB (12582213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4766e09e4bfa00d21393e67d0990d065071c8ec63f6f054225f8bd9b95f24698`  
		Last Modified: Fri, 14 Mar 2025 00:19:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faefff55d4fc940dc217d7a7fa040bab84d0450ceda2b87f8caceb791df2aec7`  
		Last Modified: Fri, 14 Mar 2025 00:19:24 GMT  
		Size: 13.4 MB (13447983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8e7bbd1c3db80bb82f5b2f3629507c5df6f16239c05891dd0bec913785594`  
		Last Modified: Fri, 14 Mar 2025 00:19:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c0af806ddf2f5eada9251129f6355d5f7aec343ddba4d8969060a9e8e4f1bc`  
		Last Modified: Fri, 14 Mar 2025 00:19:24 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49883aed606458301b9028d03bc04965cd2f30ab10c6a7027ed3e26108bcdedc`  
		Last Modified: Fri, 14 Mar 2025 00:19:25 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731b64ce53c7853a6665d9ce0b3f9c85b51cf92cb3e11a61cf2df21baea4080f`  
		Last Modified: Wed, 19 Mar 2025 23:22:03 GMT  
		Size: 2.0 MB (1963384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24b69751bfd15cdfd5ddc83254ba54bf34b4d63256b51399c613e21fc57a38`  
		Last Modified: Wed, 19 Mar 2025 23:22:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec205839722501fa518b4f41dac416a269148787f54c1af07cf88993a9ebf30`  
		Last Modified: Wed, 19 Mar 2025 23:22:03 GMT  
		Size: 740.8 KB (740822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e42cb949e85b03e0442a4f292d8821a376353469bb423a0c67e5ba8c5ee697`  
		Last Modified: Wed, 19 Mar 2025 23:22:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61186d5b750d42be226d8bc7afbfe62d11446b5b83d8ee9ecfd51b8a35e2bd`  
		Last Modified: Wed, 19 Mar 2025 23:22:04 GMT  
		Size: 20.1 MB (20057372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:708fa64d9ab49a671b645ef3f20bd84e27a15ba0388a752f467af65847f67f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 KB (390901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e33c7e5be118f6db6a6f66c5eac758e364ff2a4bcea8e62d655b1bf04e27748`

```dockerfile
```

-	Layers:
	-	`sha256:ee91d329cf88a57e7341266a0daa48cff42248540f9946bb4086c7ccb8d3ee38`  
		Last Modified: Wed, 19 Mar 2025 23:22:03 GMT  
		Size: 357.3 KB (357290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a1271d88c78cdc352f1040533f46db3f71157859314e04590598b39a1b2d41`  
		Last Modified: Wed, 19 Mar 2025 23:22:03 GMT  
		Size: 33.6 KB (33611 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:e2b22f2c28aaefdec0c81aa58a757a7bbede82ed089662d8484eceded8311b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55724774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eefae853ef5937f9f0006bed8e075f6e4adef4954da8f00c9363baa27551cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718db6fd9663f5523b8df9dc0bcd9d39b076fe66cbf8b070276f7f03946d69a3`  
		Last Modified: Fri, 14 Feb 2025 20:00:10 GMT  
		Size: 3.4 MB (3440270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6b0a520a6ed496f43bb191ac088029379c10ac94401a28b7441591d37bfae`  
		Last Modified: Fri, 14 Feb 2025 20:00:09 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31ee6d075a91e74c7b2a672c463e871265f9016719d4905ed788b321d083a2`  
		Last Modified: Fri, 14 Feb 2025 20:00:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4182bbb4f41734bcfabf1022d1a06bf1c75085882b54f09acb2d267bdef07cf`  
		Last Modified: Fri, 14 Mar 2025 01:26:03 GMT  
		Size: 12.6 MB (12582236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f820194058c1d7c9a9acd768a6ff72568cf6ec829f16c588eb903563540805`  
		Last Modified: Fri, 14 Mar 2025 01:26:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97af1ec7ead9ce3890f79cb4c70285a83fddfa13afc33d686b00395e5a8e2496`  
		Last Modified: Fri, 14 Mar 2025 01:53:22 GMT  
		Size: 13.6 MB (13614912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24483b70df7d8e840f0e7168b649ee6b916444081136ca4b28fb412f5ddaeb25`  
		Last Modified: Fri, 14 Mar 2025 01:53:21 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba3c8c3cc05a152e41b2918712856771235899d2574c3300fb1b403c2457ca`  
		Last Modified: Fri, 14 Mar 2025 01:53:22 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc294cb4127705c601643aac38f98166f71de4acb2b1ca7f6fc8f1967c42df1a`  
		Last Modified: Fri, 14 Mar 2025 01:53:22 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd779934c026252b2cdd2799ae362215011b049b595d5e86a94e8e178e7662f9`  
		Last Modified: Fri, 14 Mar 2025 07:28:33 GMT  
		Size: 1.7 MB (1680351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf175573d2cadf34a5f9133686c70370eeec1eae6b8ecdab67dd7d2dec3a9922`  
		Last Modified: Fri, 14 Mar 2025 07:28:33 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bd1d01bacadbacbacd3602786831a77df7e0e4bd28ad9d5950381c5a07c2f9`  
		Last Modified: Wed, 19 Mar 2025 23:42:33 GMT  
		Size: 740.8 KB (740826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca7c27d2d221f11a27fe208e3d78ea31746df6caac9e55deaa11e68753a743a`  
		Last Modified: Wed, 19 Mar 2025 23:42:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c114fa219215e3f8cd43723e899e9d78d71f04cdab6786fc1c1a9eaa9a71ba1`  
		Last Modified: Wed, 19 Mar 2025 23:42:34 GMT  
		Size: 20.1 MB (20057281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:409e73ca9d8f39e98f7ba87ba1382276b9fef36ae27e09b7e8bbfbc55ac92ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 KB (386337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c3a1d325b3df70806d593b2b1015d6c71b655e87d35bb8038bdace281aac22`

```dockerfile
```

-	Layers:
	-	`sha256:127effab552157e0f0c75a8f02cd5bff0071d351f905aeb3b4d6be40eb797524`  
		Last Modified: Wed, 19 Mar 2025 23:42:33 GMT  
		Size: 352.6 KB (352581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0513a1cf8ab909befa7e959ff125bc91509fea8618f89ab1986e8a3f412f8f6f`  
		Last Modified: Wed, 19 Mar 2025 23:42:33 GMT  
		Size: 33.8 KB (33756 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:fd1d83e0611929ebe6c59d0c28d977f17fb6325f8152c1707ce7f422fe39de92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54381470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63322f0012c22794f4a45f31512d1689e2a1136be6eb4ca42cee37eaa2d09b4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78faa668cf7c574dd9c2d56f59a6bc250dc74af7e4e18fd9791effe1480d2a`  
		Last Modified: Sat, 15 Feb 2025 03:36:13 GMT  
		Size: 3.4 MB (3433648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3f638d71f849a7c907c65e1460552ada965ad760ca4f24c59cf89e1f65e23`  
		Last Modified: Sat, 15 Feb 2025 03:36:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af6ac6ee454c1a8ef152ca8385e86f0d68ce72adae1c15b5ce36f9a3634e22`  
		Last Modified: Sat, 15 Feb 2025 03:36:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5a608ec08fa9afba1eb41dfc9b42b42dd96ff40b66d92f2f6d49c10bb550b2`  
		Last Modified: Fri, 14 Mar 2025 19:15:26 GMT  
		Size: 12.6 MB (12582221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe59bce3da096325469c2d31f00ca225aef5117f9180d9effd99b5938d0cacc`  
		Last Modified: Fri, 14 Mar 2025 19:15:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9f51dfe842816b5cd81bbd04276f73b0c82a015da2e162ac6347d6a0af7116`  
		Last Modified: Fri, 14 Mar 2025 20:10:28 GMT  
		Size: 12.7 MB (12677239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486992b0a248cf3e59eb148076bf25d00a14c4acbc3fc5994543eb48a2ded790`  
		Last Modified: Fri, 14 Mar 2025 20:10:26 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9868786d4f719f3b44b1bed02ddd7333b7cf9bf097804ddcc1ea816ab9fbbea`  
		Last Modified: Fri, 14 Mar 2025 20:10:26 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f39126d5313d7eafa9bf522766213067a05daa25f900ed806cd3bef1202b35`  
		Last Modified: Fri, 14 Mar 2025 20:10:26 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1b936d3015bda904f378b7554cf06a9b2be147f5f7d6edcba646424126523e`  
		Last Modified: Sat, 15 Mar 2025 08:04:38 GMT  
		Size: 1.5 MB (1483078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c80b3cc18c5ab6df1885654b9885c236c671d0808acf6fdc2dec4877acd90f`  
		Last Modified: Sat, 15 Mar 2025 08:04:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299e778ed439c3f81476022ab9c7aa90cc4230bb6ec96cf2d2ccec7ff7f085fb`  
		Last Modified: Sat, 15 Mar 2025 08:04:38 GMT  
		Size: 740.8 KB (740822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eb5cac32375a42761572afb2f44053dd39f3127c477cdecf76989403e35f78`  
		Last Modified: Sat, 15 Mar 2025 08:04:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de1cec5636f91581754fa822d6ddbf6bb878a91d69bbe7810d6cb19e6376c4`  
		Last Modified: Wed, 19 Mar 2025 23:52:18 GMT  
		Size: 20.1 MB (20057980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f4dc9d1dc5053f685977977a43e3c23c0885b261c22afde303f7f4a8678ece7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 KB (386333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a51e8f9ce78cc8b5683856e5efe445bbb50a905cac12f62c52d8db97373a1`

```dockerfile
```

-	Layers:
	-	`sha256:dc34781399fc29aa8ab0c2fa15c6accc77b81d3cb5cc48b2a7bb66d89ed7d85b`  
		Last Modified: Wed, 19 Mar 2025 23:52:14 GMT  
		Size: 352.6 KB (352577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb3b22feecb8118494350c1e61615c346096bc99d2877b1418adf0a0f6e99b0`  
		Last Modified: Wed, 19 Mar 2025 23:52:13 GMT  
		Size: 33.8 KB (33756 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:2a0920319ba511480fd595d16b4de4e9cebe96705cc47746a84424c10ad7a6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4822dcf005e3cefd9c868d7cec03c6fabe4b5c068db7b58f75e93e37a2f00d7e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Mar 2025 15:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 15:35:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_VERSION=8.3.19
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Thu, 13 Mar 2025 15:35:23 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 15:35:23 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 15:35:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 15:35:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 15:35:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 15:35:23 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV DRUPAL_VERSION=11.1.5
# Wed, 19 Mar 2025 22:22:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 19 Mar 2025 22:22:49 GMT
WORKDIR /opt/drupal
# Wed, 19 Mar 2025 22:22:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 19 Mar 2025 22:22:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683ab30aba68efec0e2ca4cbd43732f742f065f5166f0823fccc53a1442ec2b`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 3.5 MB (3507248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51174c28ade76e443d57a717e1e8717bf8083c3163cd3db4d02012e3c317ecc1`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b8be851aac921eca8fd7c62858736f1ef819ffbcf1db33078cfa5c544a77a1`  
		Last Modified: Fri, 14 Feb 2025 20:05:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0b8ad0c62f581ebfdae24e51cd1fa37ef0d702d465545636e9b4b68d75fd55`  
		Last Modified: Fri, 14 Mar 2025 02:56:17 GMT  
		Size: 12.6 MB (12582212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9aa688e2cd6d7374c9f46d86f3c6a9a127e60357bb6bb9d4248e583cf6baf5`  
		Last Modified: Fri, 14 Mar 2025 02:56:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea8d48fd02c15d2dce7a3f7cde6789d95108e5a24e1eddeb993ab2466e60848`  
		Last Modified: Fri, 14 Mar 2025 02:59:56 GMT  
		Size: 13.1 MB (13077472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b65978b4670e39446cc6b062ad96eea33b768acea11f32c8fd91448c14b57`  
		Last Modified: Fri, 14 Mar 2025 02:59:56 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3cf659db55acb9a43c8912abe08cd1ce631636ebe1463dbdb39acf1c3a5720`  
		Last Modified: Fri, 14 Mar 2025 02:59:56 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1588bef3eaf295aa06841e0b67bc0b1803561903c919efc78c70d8872b7457f`  
		Last Modified: Fri, 14 Mar 2025 02:59:56 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66be96556a93295cd75c62a8ddf0ffcbde4d4b59fc52170946748a0605192852`  
		Last Modified: Fri, 14 Mar 2025 16:14:08 GMT  
		Size: 1.6 MB (1597231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828c4c9e2e3b632ace08c77741e3f908e205ee7ea9b54053b7001e0510189bf3`  
		Last Modified: Fri, 14 Mar 2025 16:14:07 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d32e1aba10e5f65e7e213d47b3fed3ff136e6645e1d03e91345db00ad53ba`  
		Last Modified: Fri, 14 Mar 2025 16:14:08 GMT  
		Size: 740.8 KB (740820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a350a901c8d8e8e69f1cf2a9e8b9071aa81a297cd86c66c9fa3b5f3cef38ad9f`  
		Last Modified: Thu, 20 Mar 2025 00:29:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2439391db3e15dccc4028ec55d4a83c973be51fc88f8451fd972aa61e44574`  
		Last Modified: Thu, 20 Mar 2025 00:29:39 GMT  
		Size: 20.1 MB (20056495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:d0b7a47956b7c11b94a250a258a42baeb215d703939a25b5aa0a37affee20da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 KB (386197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85fd4686ea44d639ec1b7f7acd2fec73e28928dd3858a1599ffd90dd451a040`

```dockerfile
```

-	Layers:
	-	`sha256:88ef6fdab9553254ef844bcb659d204cca72c876d49b8e139a2c53c5ba0ab9b1`  
		Last Modified: Thu, 20 Mar 2025 00:29:38 GMT  
		Size: 352.5 KB (352523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5556cad32721cf793410e802ea14350a006573c5daaa79f11a5f80e2c5a7d0`  
		Last Modified: Thu, 20 Mar 2025 00:29:38 GMT  
		Size: 33.7 KB (33674 bytes)  
		MIME: application/vnd.in-toto+json
