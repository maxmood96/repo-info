## `drupal:10-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:4e9ce3bbf2847bee510e17333de53ca273ba7139d3afc560a46da77e0834c1a0
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

### `drupal:10-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:93548b820b9f77c652070ca699b8b3aaf057f97846e2f1db941be06643c47988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60445938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de26ba9e864e3b4cb0b9fdd0ae5bac5bad1e0dd693037e308efb1effe17228d9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:43:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:43:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:43:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:43:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:43:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:43:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:43:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:46:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:46:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:46:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:46:13 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:46:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:46:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:46:14 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:46:14 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:35:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:35:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:35:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:35:24 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:35:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:35:24 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:35:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:35:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae13e4a5bcbd750adc27d389a97030fbbeafed578f43496cd14c4aeb089f23c`  
		Last Modified: Thu, 07 May 2026 16:46:07 GMT  
		Size: 3.5 MB (3464879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecf102b845317e529368a90f52189b7f628ca1c9f8ede720086d80065d0f6e7`  
		Last Modified: Thu, 07 May 2026 16:46:13 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362728127f5b40372aad82c07e57a0b90b090aa52370bd45263287a1aef4065`  
		Last Modified: Thu, 07 May 2026 16:46:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de29b28fa2e499f846db4cfc9f729ac6c9f1be09eeb2e6e5724b864f5065168`  
		Last Modified: Thu, 07 May 2026 16:46:21 GMT  
		Size: 13.7 MB (13739985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2145a0be1ae4700b054845bebb98d643ae0fbe95a07ef4022fd6436c74ca5a7f`  
		Last Modified: Thu, 07 May 2026 16:46:21 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcade6e53bfbfb7078cb84af6a77e652b6f566c349d0409b844cd521694dd8f`  
		Last Modified: Thu, 07 May 2026 16:46:22 GMT  
		Size: 15.2 MB (15176894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d9e799c49630abbbdf17e88d2a37951e66d827922cf4895c366ec28ebe1fc`  
		Last Modified: Thu, 07 May 2026 16:46:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f59cfa97a19db0498d0264b6ac63f7cefda4c15b4b40c0b5d5f198ea5ed63f5`  
		Last Modified: Thu, 07 May 2026 16:46:22 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73c4fe1584f450d3b33b935c9d92923948ac216ebd5c79790e903263de27166`  
		Last Modified: Thu, 07 May 2026 16:46:22 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c94e7e8387d741e72ec3d6c43d0f18d23ad9c61644bb60d66a362d4a4fbccb`  
		Last Modified: Thu, 07 May 2026 16:46:23 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f8be196e218b13d7227b85dd8a1e66f664f04eecad7fef3048a55023d0d35`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 1.5 MB (1493990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caec81ad1220a66a2e5a9379ec0093bf96fc29be7d279ff872d58916d01b544`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df9449c0e08096a4653361cbae87dfdd5accd99c9aa32070df3ec4d4be1e6d0`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517076b0d460373d2001d9a97ac343d4edc8c97a4fcd638448c9f90e998fb32`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52ae42aa4036726574bf9aed7753e4d74feff7281bb69e9e6da2e78eb07231`  
		Last Modified: Thu, 28 May 2026 22:35:43 GMT  
		Size: 21.9 MB (21885612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:2cd697952341e0b2548cb19be3c345c8c7d8fe1b42e22b1b5764db15e94bcc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 KB (401697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bb8e85c6a7d9edf0f14fc2c77d32ee12de9e59fd59754439d50811936d0043`

```dockerfile
```

-	Layers:
	-	`sha256:cacc5fe675c9db2ff7798ffede104aa4e5890cb89e90c79c055bb16aabffe9c2`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 367.8 KB (367834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c32fdee2964a3aff9ddcde8d22805a1b586c9795a69dc7dcf0710a995c08c4`  
		Last Modified: Thu, 28 May 2026 22:35:41 GMT  
		Size: 33.9 KB (33863 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:05413e4f894528661544064d79b3043a201319c2c42eeb7b79b2197c5d239f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58401675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc407af6784e4cfc27a7402e5fa0f0164311e7adf1af8e25f5854c9fbc6cb36`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:43:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:43:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:43:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:43:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:43:44 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:43:44 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:43:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:43:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:46:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:47:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:47:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:47:00 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:47:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:47:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:47:00 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:47:00 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:35:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:35:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:35:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:35:39 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:35:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:35:39 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:35:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:35:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94188b3fba853fe56477a2aca1a3a079f155340d32408f510c7c264096112a5`  
		Last Modified: Thu, 07 May 2026 16:47:06 GMT  
		Size: 3.4 MB (3428199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d4cdcd21b736624d479affc7e7f0a65880a9a0a28dad29be098327c4fc6595`  
		Last Modified: Thu, 07 May 2026 16:47:05 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61387e63944a16dbc156c1bb87554ad574f0c66c312e52efca7683253311edcd`  
		Last Modified: Thu, 07 May 2026 16:47:05 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b840dcfdb0d6eefab6efb87685627973dbc9623a0967bdf2d622de4d13e48914`  
		Last Modified: Thu, 07 May 2026 16:47:06 GMT  
		Size: 13.7 MB (13740031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895069530853a4c67a1c53742a2b829cb630c70ae995dfff066675a5eb7f4aab`  
		Last Modified: Thu, 07 May 2026 16:47:06 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b227df25c922735acf7b4cb1453a98411ebd63a38abab570092fe0cad919e040`  
		Last Modified: Thu, 07 May 2026 16:47:07 GMT  
		Size: 13.6 MB (13628018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ad8075590a7daef50b9b3ce920b9a55f441c4e5ebee5b76a5992b39b3b8e6`  
		Last Modified: Thu, 07 May 2026 16:47:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c1f993b47c3239425e00e0fbd25c2379d0e1c3e96bc041f393cce1f1d730d7`  
		Last Modified: Thu, 07 May 2026 16:47:08 GMT  
		Size: 19.8 KB (19841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aab5637b9c7a438fbc49b68233b58f44aaa14dcd91e87010074c695910fdc0`  
		Last Modified: Thu, 07 May 2026 16:47:08 GMT  
		Size: 19.8 KB (19841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a825761d3897dff68e2fa032667afed924397d3ff96b9b8a91e50023f8e335`  
		Last Modified: Thu, 07 May 2026 16:47:08 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24615a41f84748f5005cff27d728419adf3315b01133a62a085203846a3baa`  
		Last Modified: Thu, 28 May 2026 22:36:00 GMT  
		Size: 1.3 MB (1336436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bbadb980e7de866aceedc015e0318ff16381b223bcb90c250542b065e7d6d9`  
		Last Modified: Thu, 28 May 2026 22:36:00 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daad1a6c8b7af3e7f0d37c057741015e73ae9774199088c24662b7840826d832`  
		Last Modified: Thu, 28 May 2026 22:36:00 GMT  
		Size: 822.5 KB (822516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b3e717207b04c39d30757406ca4927f7fe131c82fd113eff7cfafbaf3fae1`  
		Last Modified: Thu, 28 May 2026 22:36:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4909cdf00c0dc97052401338a6df91292c4e02494bf9daa8f495d66269f2e9`  
		Last Modified: Thu, 28 May 2026 22:36:01 GMT  
		Size: 21.9 MB (21885603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:35e4c349b5df38a4462a87f6577b58d5b22bfa952110da2dcd014bca1e6e19f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 KB (33792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5905a01e5e22a22ecc199fcf45383cf62652e9370a07824c0ec8dc5e2061994`

```dockerfile
```

-	Layers:
	-	`sha256:bf831099c7224e103fe317347221075cfd59883e86b7e02308b9416f1f40de92`  
		Last Modified: Thu, 28 May 2026 22:35:59 GMT  
		Size: 33.8 KB (33792 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:88c705d282103d03fa355913d779b6209b3cdd74a4f2c530f595f3faa97b142e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57078852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630603209cfbd16dcae4ef0c1e0114bb30c64f653ebc437aae2647164f8b55f7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:51:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:51:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:51:36 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:51:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:51:36 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:51:36 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:51:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:51:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:54:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:54:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:54:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:54:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:54:42 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:54:43 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:54:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:54:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:54:43 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:37:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:37:50 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:37:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:37:50 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:37:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:37:50 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:38:03 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:38:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d5ea70c829e270eddb54ceea0d3ced4a0ec7edf288dd9366916bb577b541d8`  
		Last Modified: Thu, 07 May 2026 16:54:49 GMT  
		Size: 3.2 MB (3244458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5afa4f5fdf13125ec4846da793f48ae5b163b26b7ef4e0961c03ac9984e07`  
		Last Modified: Thu, 07 May 2026 16:54:49 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b5c8558be4afe18dc5479f0a7c4553f8c18eece30eb4e9528048221fe88d8e`  
		Last Modified: Thu, 07 May 2026 16:54:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b2ded46b7d71dfbc0f6d26406f6b1708babbec1668c3676822d5f2d5820d44`  
		Last Modified: Thu, 07 May 2026 16:54:50 GMT  
		Size: 13.7 MB (13740015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b86f4bc5766c7ccc0145971613ed55cbc7f4fbd42a596359ed9210f93155cb`  
		Last Modified: Thu, 07 May 2026 16:54:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b963cb72c5837a327535b27a000a1774c450c29d50a7c305e17af5a8d596b8d9`  
		Last Modified: Thu, 07 May 2026 16:54:51 GMT  
		Size: 12.9 MB (12872774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de8218b6b84ca74f9835cc7d6e68ca18e73e95f4ea2bd5800104a3ea595f756`  
		Last Modified: Thu, 07 May 2026 16:54:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176f4fcd7cb67a70c8dac35d48389a8dd7c525ec62575e0832853cb1fd14c4b`  
		Last Modified: Thu, 07 May 2026 16:54:51 GMT  
		Size: 19.8 KB (19820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65768f74f3f63fe0861c85a26089348e4ba8f5011ccdfd114bce2bfab3c0f393`  
		Last Modified: Thu, 07 May 2026 16:54:51 GMT  
		Size: 19.8 KB (19813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a3939395afca918f0443e80066d0f7578d00fb138c701fa5149839f145cdfe`  
		Last Modified: Thu, 07 May 2026 16:54:52 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dc170ff6e19eb57c2af22c01f7bfdf5ffa17246872aeadc099cace6e1be296`  
		Last Modified: Thu, 28 May 2026 22:38:16 GMT  
		Size: 1.2 MB (1234296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32327657e83f390ed4b51f6d3bc5fcc2193bfa4f4e14ff0ebdf9aa21ad44ea45`  
		Last Modified: Thu, 28 May 2026 22:38:16 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e891f49892670d0e2dcc3f4de5503a66a3a50ee00dd18825901d86c8622635f`  
		Last Modified: Thu, 28 May 2026 22:38:16 GMT  
		Size: 822.5 KB (822515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b3cf79f48a082fbe578ee20bb306f577c9dfc6f06b34036a1a082a30c43c0b`  
		Last Modified: Thu, 28 May 2026 22:38:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256e0cfe2a7c45468a0241f037f3572c3bd38e25a7340f645c79410edf66035d`  
		Last Modified: Thu, 28 May 2026 22:38:17 GMT  
		Size: 21.9 MB (21885524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:06ec9115ba3e35c5efd6a0e3e856dfa199bfbda5d0b6ba62a22117158a4b05b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 KB (398903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0643aedec720ba927dc2294dfb5790f1e44155f6b3b7f4fe79ed729b4895548`

```dockerfile
```

-	Layers:
	-	`sha256:68b47d21a3b6513eb04a3125525ea460c55f6d90bf48c638ae571ed7e953392f`  
		Last Modified: Thu, 28 May 2026 22:38:15 GMT  
		Size: 364.9 KB (364896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb25e09767aac6cf933b18fb2ebabdf8c74f18f76e9b8a9026adc73126d0b882`  
		Last Modified: Thu, 28 May 2026 22:38:16 GMT  
		Size: 34.0 KB (34007 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:9108c3a06ce4b83fb917dc60968a300371f3f5938f02b8751bd85a8dc98af4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60395170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980c86e51468516612ba482ef78ef15ab72dee7caa3a06100f790bc80abb1600`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:43:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:43:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:43:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:43:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:43:33 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:43:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:47:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:47:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:47:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:47:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:47:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:47:10 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:47:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:47:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:47:10 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:47:10 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:35:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:35:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:35:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:35:03 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:35:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:35:03 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:35:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:35:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d03dc95db4d3c5e80594e114f8114f07f67fdef7ee41752bcc890114918505`  
		Last Modified: Thu, 07 May 2026 16:47:17 GMT  
		Size: 3.5 MB (3467698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3044dfdfa3f96d1ac13bfd6de0d3f8fe36a123746648a73e8e68d40c192f23c`  
		Last Modified: Thu, 07 May 2026 16:47:17 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf51a06801072b78ae20b5b7fa0468bba41cacbf88dc085c367ad5b30916020`  
		Last Modified: Thu, 07 May 2026 16:47:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71249d1c47b68993152439b26992283787ee51dad37b83b2278dccc830b9003c`  
		Last Modified: Thu, 07 May 2026 16:47:18 GMT  
		Size: 13.7 MB (13740019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c314b2227a04f16fa092dcc416d72719887239551eacad7ccc4b972ff173d2c0`  
		Last Modified: Thu, 07 May 2026 16:47:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521547111bebab186bf98849033edd5fc276d38d39bac7704ae6daf67aaa0df0`  
		Last Modified: Thu, 07 May 2026 16:47:19 GMT  
		Size: 14.8 MB (14802743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f61d30ba859562554b154495660da18094925390b42333fb892902155ad7a2`  
		Last Modified: Thu, 07 May 2026 16:47:19 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30960b4dedecbbfe4518b4040a54b41359bb707a82a22745c5a66673a52fa446`  
		Last Modified: Thu, 07 May 2026 16:47:19 GMT  
		Size: 19.8 KB (19827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74c66985594dea8cf542fbad9aedc2886033d6bb94d0ddb7470fcb634885be`  
		Last Modified: Thu, 07 May 2026 16:47:20 GMT  
		Size: 19.8 KB (19825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b811021741682b2625515bf1cfa8a989dcfb9831d17580edf816c981ecfd2`  
		Last Modified: Thu, 07 May 2026 16:47:20 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003bf73be7e8d2d473f43bae9188435787e692be7a45897dc2d723ea9a515d92`  
		Last Modified: Thu, 28 May 2026 22:35:23 GMT  
		Size: 1.5 MB (1481193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fe6480f61e7796486cd2c9cf4b1fb2c733d305318427308cd87cc15b6d4aa`  
		Last Modified: Thu, 28 May 2026 22:35:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a4a4d3f87e1ce5787dcf220a7ecb91b4f4a6e2f59a84401bebe4737afb576`  
		Last Modified: Thu, 28 May 2026 22:35:22 GMT  
		Size: 822.5 KB (822519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f9a302f67671d0d5d16d53c06f0aca78ea14e720d74345c28447105e0abc08`  
		Last Modified: Thu, 28 May 2026 22:35:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0356ce52c7e25d148131af94f1256b1cda523e83fd80fc5d98f2ac5dd6e549`  
		Last Modified: Thu, 28 May 2026 22:35:24 GMT  
		Size: 21.9 MB (21885635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:0fd1570779cf9d6ffa7e847df390f1a366a5491940dcf116fce68654d6077144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.0 KB (398971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db48d690c674c828081268de92155cf025ad81979c12a5549e21e9d58c8544e7`

```dockerfile
```

-	Layers:
	-	`sha256:f1238c527fb7ee6b98f1bd7477dd07c08d677f38fc225a7b8488d012406cc8a4`  
		Last Modified: Thu, 28 May 2026 22:35:22 GMT  
		Size: 364.9 KB (364924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762622960e56c2404c423b74448cdddfeea03360b88b5e8a19ef048230fe2afc`  
		Last Modified: Thu, 28 May 2026 22:35:22 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:c0acd8dfd04ee9d3b630732432f53f522261a82f68a5b151746fdc0f2a7faf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60807161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b72d11dbb93c2f6938ab218efb41bf6d1e60ace3e26dc65d461c5e30a97e4db`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:43:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:43:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:43:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:43:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:43:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:43:13 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:43:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:43:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:46:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:46:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:46:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:46:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:46:07 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:46:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:46:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:46:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:46:07 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:37:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:37:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:37:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:37:04 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:37:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:37:04 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:37:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:37:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2325bf7be608501c30a1dad59e1aa329248781b0ff49461ae88d1c59803d6d40`  
		Last Modified: Thu, 07 May 2026 16:46:13 GMT  
		Size: 3.5 MB (3522676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecf102b845317e529368a90f52189b7f628ca1c9f8ede720086d80065d0f6e7`  
		Last Modified: Thu, 07 May 2026 16:46:13 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8b909127ab335fcc88e5a7cf3a3731ff87f7921c0978e2602769ec8f186cf`  
		Last Modified: Thu, 07 May 2026 16:46:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81d8c55937bb88a9c27fd35605c380d33499ed0c403f8f32d713ee923e71bbc`  
		Last Modified: Thu, 07 May 2026 16:46:14 GMT  
		Size: 13.7 MB (13739994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f24e91f3136ad16f2c73921c674653edc10d56d7897eab0ea2de78fa1fa39f2`  
		Last Modified: Thu, 07 May 2026 16:46:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff760ee64efae93d356ad2c1996d2f7cab11e06d3b001360141d89ae6682268`  
		Last Modified: Thu, 07 May 2026 16:46:15 GMT  
		Size: 15.6 MB (15578381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf64fbb195c30619b5e135bcc783bcd162dc59b27d1e1c31deaa1e238ef23337`  
		Last Modified: Thu, 07 May 2026 16:46:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bee79b53bfdc87d23fe6612db998f0d786763fe4b5ef75f46467e41d920b1`  
		Last Modified: Thu, 07 May 2026 16:46:15 GMT  
		Size: 20.0 KB (20023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6055b168d07ef156644bbcd07261fcb756b3f8e0b9bda2f17e862ce43b107924`  
		Last Modified: Thu, 07 May 2026 16:46:15 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76fc0d162e103af57b0ed83b4e338a0fd9bdf2a48371289b5044942155d187`  
		Last Modified: Thu, 07 May 2026 16:46:16 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ad8aaa8022bc5d8036db9d2daaed1cb9d56283fcf2542f396c57e162508f0`  
		Last Modified: Thu, 28 May 2026 22:37:27 GMT  
		Size: 1.6 MB (1579401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71af8f3fc0fefcc470269ff73f1f12328092b67ca0aef9bf350bf21d5e3b616f`  
		Last Modified: Thu, 28 May 2026 22:37:26 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57932ee6f909b46e9be86ebd75577b66f9969a94a3847cfe1b3dfe4c3be9cb6c`  
		Last Modified: Thu, 28 May 2026 22:37:27 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5959374ab5358c9eed9ed9482834b23454251c7555ced8ff27759b2db051731`  
		Last Modified: Thu, 28 May 2026 22:37:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ddec9a2b04ede4a192d740b7de2fbf358946e8c652086b04d06b883593f82`  
		Last Modified: Thu, 28 May 2026 22:37:29 GMT  
		Size: 21.9 MB (21885618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:d079273706921eda26f605b87b1739a6629fc365ef7fd56a20a4f8c28e9c2b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 KB (401609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105ad1e50e5c5faa04a03ac8aedd825c3205d8e6b2fa42306105bc82418fea3a`

```dockerfile
```

-	Layers:
	-	`sha256:ab4403ffaa51e97cff4196f09fb0861fb0cbaed310efa8f4557f5448b0df15da`  
		Last Modified: Thu, 28 May 2026 22:37:27 GMT  
		Size: 367.8 KB (367799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bdbce150e49635e8f26a14c7693dd6e06d566dba26be08d03d5ae8d7f3d27c1`  
		Last Modified: Thu, 28 May 2026 22:37:26 GMT  
		Size: 33.8 KB (33810 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:a815131c4b31592bdb8e90556299bb06a521c98ee6b5e249085a7c30d336eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61399699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa417e1c1ce4f8716105875b6fd16f1c582fd48293a78ac4ca77c8a3daf53f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.4.21
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 17:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:03:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:11:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:11:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:11:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:11:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:11:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:11:18 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:11:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 17:11:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 17:11:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 17:11:19 GMT
CMD ["php-fpm"]
# Sat, 09 May 2026 03:39:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 09 May 2026 03:39:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:19:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:19:04 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:19:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:19:04 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:44:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:44:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e338e7955d85460985795dd64f0d45a3d8e07c9187a71fb859c9e820adc1b112`  
		Last Modified: Thu, 07 May 2026 17:07:42 GMT  
		Size: 13.7 MB (13740049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453af6f27b5d9b13ee84836e8bb5a5780e682cc1a8bc1a422855f3f2485418fb`  
		Last Modified: Thu, 07 May 2026 17:07:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c22aab8d03cf57857be77a362092114ddea047943026f69d05d32d16de89653`  
		Last Modified: Thu, 07 May 2026 17:11:32 GMT  
		Size: 15.9 MB (15930560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13057a112f180116df9b0703e4f8f7661fcb39bd4c130a4ba555b8deac01573`  
		Last Modified: Thu, 07 May 2026 17:11:31 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a230c0dfdd7ccc90cbe60ea10e47ea622935e3831f5aef895fd8bb5005ab57`  
		Last Modified: Thu, 07 May 2026 17:11:32 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d05ef93e07e99e8ba2446ee03d6ad902cd02e013c85f462c86e88bc5e672be`  
		Last Modified: Thu, 07 May 2026 17:11:31 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5203cf3a306bb4aa4fb094f25a0c2d08195dc6dc41f6b6a3e3e6e7e893cb16`  
		Last Modified: Thu, 07 May 2026 17:11:33 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e06834f827d772e8b84a2da1692e656e8326c14df6af71d4d4a13c6f0886574`  
		Last Modified: Sat, 09 May 2026 03:40:13 GMT  
		Size: 1.6 MB (1615920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab9fb4d1d88937aa331b39ac79bc1f4cf49e887cdb66fe44e3c2b250284a875`  
		Last Modified: Sat, 09 May 2026 03:40:13 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a4a1b208cadc8bb506da06e2a6b790d12f660d3294d41cce7749f08d5c98ab`  
		Last Modified: Thu, 28 May 2026 22:19:51 GMT  
		Size: 822.5 KB (822526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7914486711767bc885d0b23200df43f2eeec06afb5e557e43219fcbb540f6ac0`  
		Last Modified: Thu, 28 May 2026 22:19:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebd71f5ea57bcdac4bab973e223809b6a7af6efacc6f57e76203576268dd2e1`  
		Last Modified: Thu, 28 May 2026 22:44:39 GMT  
		Size: 21.9 MB (21885407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:f4d38e5e5959cb8689f71bf203a9e201345c89e96ad9d38fe39a847d10cb3926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 KB (396868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7c12a1b3ffdb004a9757f80cc3545ca13181df608dd4125000fb56b7800acc`

```dockerfile
```

-	Layers:
	-	`sha256:d9f8e559959505a9b149fe825341ee07cacc3480e9b15e5d1c46d360f6203dff`  
		Last Modified: Thu, 28 May 2026 22:44:38 GMT  
		Size: 362.9 KB (362935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b121c93158b7d3415b8be1f6561bc96515b018d6ad24ab984bc02370c1726c`  
		Last Modified: Thu, 28 May 2026 22:44:37 GMT  
		Size: 33.9 KB (33933 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:9fdc84a06823b3cee3271604157c579265d74696a0ea9834c99a506b8dd9594d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59805819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ee46e088c737b47c3f6faf042e4e00c2d6131f799c9ec644634f051286e6f2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 11:02:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Apr 2026 11:02:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 18 Apr 2026 11:02:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_VERSION=8.4.21
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 23:50:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 23:50:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 01:44:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 01:44:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 01:44:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 01:44:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 01:44:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 01:44:34 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 01:44:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 01:44:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 01:44:34 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 01:44:34 GMT
CMD ["php-fpm"]
# Tue, 12 May 2026 02:08:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 May 2026 02:08:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 16 May 2026 20:12:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 16 May 2026 20:12:07 GMT
ENV DRUPAL_VERSION=10.6.9
# Sat, 16 May 2026 20:12:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 16 May 2026 20:12:07 GMT
WORKDIR /opt/drupal
# Sat, 23 May 2026 08:44:50 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 23 May 2026 08:44:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aba8e387b0f52a066bd16fc16548380bb5c1ba358c87f632f41bf0e1538804c`  
		Last Modified: Sat, 18 Apr 2026 12:03:48 GMT  
		Size: 3.6 MB (3600194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0aef12c28ba880017fb96a48e3e22f4b4e363ee1be8f9a85075a131d12b72`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a7d02aa931427745ea3ec5ed71cd22b97056886e6224d2e88e3226411519f`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052bd2c7b2aeff15a4b447ae486974de63a4e5a3163771deae1103d5ccd33aab`  
		Last Modified: Fri, 08 May 2026 00:47:35 GMT  
		Size: 13.7 MB (13740004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7266a0855b3e56923d6b4c779112115a2dda3d0a4ab2d84497e2a165b976aaf0`  
		Last Modified: Fri, 08 May 2026 00:47:31 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2029ad05454fd042584d9d4c0133f16b51d7ddffe99cba0f0e89acbe9cdb8a55`  
		Last Modified: Fri, 08 May 2026 01:45:27 GMT  
		Size: 14.8 MB (14800500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f486f542dfdf9b8d040f9a0c53dca8578a9b3058f39d64ae6263b37e962dd4`  
		Last Modified: Fri, 08 May 2026 01:45:25 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8870a50d87064698a9c766a70c13641715df6e83835aef7c40094f6b36de863f`  
		Last Modified: Fri, 08 May 2026 01:45:25 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7441e657fe5d07bfbc0c79b7173d0e85fb820e4525a21f28073a45aac0e236d6`  
		Last Modified: Fri, 08 May 2026 01:45:25 GMT  
		Size: 19.8 KB (19840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664fd640bea06bd919c8c4c50b708ea03a0d8ce43229a6bf2bdfc72e01774e27`  
		Last Modified: Fri, 08 May 2026 01:45:26 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a75d4162a2e39a58ecee6076165cb82fafa898dad86bd9ea01d968db03cdb5`  
		Last Modified: Tue, 12 May 2026 02:12:00 GMT  
		Size: 1.4 MB (1415497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feffba4175799aac7faed48a57812207a969291910783dcdb09bb24d79e30df3`  
		Last Modified: Tue, 12 May 2026 02:11:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25654ee9e75d0c1f717d313b6ec18297ba813090626da03baabf25bb198a0a0b`  
		Last Modified: Sat, 16 May 2026 20:15:23 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b7303ca85dd253390a87f724be2f0c7b34e874ab088d73d5aefcc3b47e9381`  
		Last Modified: Sat, 16 May 2026 20:15:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0fafe0fdb8e9a44612a4184413148ce29db6a36ab6e8522b30c9fb94ff3109`  
		Last Modified: Sat, 23 May 2026 08:47:18 GMT  
		Size: 21.9 MB (21884464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:85e8e2086ed210d6d33a48224f79867d4683e5e1d8675ab3d8f307ec1cfe98ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 KB (396843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e35a57662032c1fe9332c92ed6af4335d00af24251f7de976a376eac647844`

```dockerfile
```

-	Layers:
	-	`sha256:6a5fc6788f14fcdec62ec12ca1e125fc2e9e743de2b00c56536bffa5a59e3bc5`  
		Last Modified: Sat, 23 May 2026 08:47:14 GMT  
		Size: 362.9 KB (362917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c721b9c040d2ef6cc3f701791d9f6d6e89e2ceeeebedc73e63c7b597b32f4b5c`  
		Last Modified: Sat, 23 May 2026 08:47:14 GMT  
		Size: 33.9 KB (33926 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:5bf0be602a295b58c428a6aa8b5b88037ea0a1962a72f498f73bffd3bb7e88f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60429168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ea5e5ba7a8a7a9ff1d228f2c43144f7fa70094ce4e3cfa913a87431083c3a1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:52:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:52:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:52:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:52:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:52:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:52:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_VERSION=8.4.21
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 05 May 2026 23:52:33 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 17:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:34:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:45:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:45:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:46:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:46:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:46:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:46:16 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:46:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 17:46:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 17:46:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 17:46:19 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:13:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:13:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:13:21 GMT
ENV DRUPAL_VERSION=10.6.10
# Thu, 28 May 2026 22:13:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:13:21 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:35:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:35:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9644d70748936be9d74a8cddc95a8f5238921ce5877a5f4e28141531676deae`  
		Last Modified: Wed, 06 May 2026 00:01:32 GMT  
		Size: 3.7 MB (3691325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273a5d3f6deb47ba0d072dcd55a4e7d866429307ea1166bbe32ab47d1734bde`  
		Last Modified: Wed, 06 May 2026 00:01:31 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb185e44da86992805627c72cd931543f45b144e0af32bc974e75629a0d224`  
		Last Modified: Wed, 06 May 2026 00:01:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9e864e8df95247ea0a379f781e9bcd262291af8273ccdc99344841a7bb0ccb`  
		Last Modified: Thu, 07 May 2026 17:47:21 GMT  
		Size: 13.7 MB (13740033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf83ab2cb408da9782850c4e7e14132ee3c5fb624d8030743a6f023c899fe58`  
		Last Modified: Thu, 07 May 2026 17:47:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2244c49c6085791543ff0f6f8a12d40bf87f5de4d498cab2b0528c28f78d9d5`  
		Last Modified: Thu, 07 May 2026 17:47:21 GMT  
		Size: 15.0 MB (15041559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bd7305fe4679353795eacbe1a570fd305358a3e3c5d60172874141d26d233a`  
		Last Modified: Thu, 07 May 2026 17:47:15 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bd829dd6c2be7ec8e318c2f9a03d8df4c79ddf43cf17f12539b520309fb3a0`  
		Last Modified: Thu, 07 May 2026 17:47:21 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c6cbffc81327a9947ba5918d7f7f0a26de2ccf873d52f1c10471d6d207cea2`  
		Last Modified: Thu, 07 May 2026 17:47:21 GMT  
		Size: 19.8 KB (19833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa62b1dfffdd3a8ba22c511e1f00aee55511673bf4bf3ac3cc6edffd1e9ffc6`  
		Last Modified: Thu, 07 May 2026 17:47:22 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaf22c2d8fc814766400b9c1f61de48957b2dc83e38cc4cfa61324ed36c35a`  
		Last Modified: Thu, 28 May 2026 22:13:48 GMT  
		Size: 1.5 MB (1540708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbf9c2be83582fc9887a9edb6bf645b966077114ba57a7a0b8ae02060f05c60`  
		Last Modified: Thu, 28 May 2026 22:13:48 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709bd825ba7aad99f8ed81a2801fc5f08377d70391651052c2ff9cbadf637d`  
		Last Modified: Thu, 28 May 2026 22:13:48 GMT  
		Size: 822.5 KB (822514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b9e02a24897d85df30985d02f1ed4f77ac5d6b50a833cf2ddfadf3ebdcb78e`  
		Last Modified: Thu, 28 May 2026 22:13:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b3b46e4f7f04c785f0d31b7f956b4a7864aa267653098c70ac19a97ec8285`  
		Last Modified: Thu, 28 May 2026 22:36:20 GMT  
		Size: 21.9 MB (21885661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:4792dd03c678499fbca0965f3101ff63d3b52d75c4de8e9fa3ef3a975425ac16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 KB (396756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ff45a33c689956d25959e6b5718a00d3d5f60345c73dad87aa98ab8daec212`

```dockerfile
```

-	Layers:
	-	`sha256:a5d94631f066c3320046fef3197a64aa44fb8dbac7cfd474ff9c3912ce838650`  
		Last Modified: Thu, 28 May 2026 22:36:19 GMT  
		Size: 362.9 KB (362893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efc2361a6d1a2fc02f2d337cc39c7dcae0e61cd1fdfdef2810ebb512d54f6084`  
		Last Modified: Thu, 28 May 2026 22:36:19 GMT  
		Size: 33.9 KB (33863 bytes)  
		MIME: application/vnd.in-toto+json
