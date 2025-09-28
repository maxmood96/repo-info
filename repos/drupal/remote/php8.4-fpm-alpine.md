## `drupal:php8.4-fpm-alpine`

```console
$ docker pull drupal@sha256:996ee922140a1cb07496c9cfb4151a572751b6d49e03054b018d3f298023f797
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

### `drupal:php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:bd7c272dfe8fff68ff3a8cb9071e6cc0b1d3c6709395ec7e76d689d3b4928bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61244079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc79e3c25b6bfd3617d7333aaa3aaa7f1f688dd0dfa3c82fd6f3f6e1c45c66e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ff51f2ea727a7043940cfc2fb2f68d58d10d5359a33071855155359a696d7`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 5.9 MB (5928421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6daa090ca97098274aa0ed6f7f64465168f8ca337b0f30c1857ef21f07fd7`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b84768904846715613a8f5e76a29acfae483f321bc82fddfa7a83b01b8433c`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd732135359065fba3dbf169e55d4c065122a69ef438a8bf6c5c3659e31de7`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 13.7 MB (13667228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd0b9cf1437dd9feafcc659c5af008e174d71acd7fefe9b71aaa96c30467a1`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced1fcbb1ef657a0b3898a127e963131a0099545af83077a1b2bcb5ed37d898`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 15.0 MB (15027081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415445076d113094d936a74399c4de54c2fb68d515a2d582984fdb9fd4c5a569`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1b29d39ef81a71d52ae54f98679eea8a543e664cc6d99459c1379e56c7772`  
		Last Modified: Thu, 25 Sep 2025 21:19:03 GMT  
		Size: 20.0 KB (19960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f0f032c840a150ab2997e4d529b6df675086c1d128b5f5a07152558e26d31`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0912e70f8c7e6581863c92ecb8a53705ca16cd033ca9f05ac05b69adac4181`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf644e985a6fe4bdae6ba76928bcdd24354356b1e56835ba7427502d2af7d78d`  
		Last Modified: Thu, 25 Sep 2025 23:14:01 GMT  
		Size: 1.5 MB (1492545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba094af2b3875e7c61eacca6b03c0fd014430c039568aa8640d7e893391ac600`  
		Last Modified: Thu, 25 Sep 2025 23:14:01 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5fbb03835e61947b7b899f9d4b29999a8ba8bb160be9b0cc848eb82776d140`  
		Last Modified: Thu, 25 Sep 2025 23:14:02 GMT  
		Size: 751.5 KB (751475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5d9a720b5e8ba71bbae178c9f3a1ced345619511175a1467f68b70d1ba778`  
		Last Modified: Thu, 25 Sep 2025 23:14:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11258e4e581f4d105b801388e6ae582e0629fc2ca8526b6c74980603fbc5ee06`  
		Last Modified: Thu, 25 Sep 2025 23:14:04 GMT  
		Size: 20.5 MB (20523992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:5230dfa81948a8c3f69bb83cc5fbdd205768a31563bfc014dc5ca51703616c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.6 KB (416634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e789d64c1001da65f4c09c60884af79681f8803be7e266cfa7e4822c87e466`

```dockerfile
```

-	Layers:
	-	`sha256:ee70e21ccff9059d3e774195d956ac202120803ce1c3bc9a3d70e026e2ea9754`  
		Last Modified: Fri, 26 Sep 2025 02:12:54 GMT  
		Size: 379.4 KB (379371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b0b1059def66909c82962109d9f8be9e9e2bb9d19b37be59b1a827d597e5d1`  
		Last Modified: Fri, 26 Sep 2025 02:12:55 GMT  
		Size: 37.3 KB (37263 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:b5e7c778383ff1cda85b5c370fcfb4f7663fa6d14001e6bbc8c4547ee716f6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58898672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22ec43b28922bac96909bc510ff0885716384ec58956e16cbc7270d687cac65`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a67790b167583e60e508f6d629f5d12e582a6660df9d0b1eeaf3f40d951d80`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 5.5 MB (5532141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff4e845b8d460a651554faa7fd3e340b0ee89de9f36dcac5ef8e4c8d2f2108`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b147fa84f71c751a59eecdc171fcbf8585b1a6cc0999bb778ce7437a7eeb9dc`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07cecaff067ecfebe81f2148d35179886b6eea43dab6621362d9c90f28345fa`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 13.7 MB (13667216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764709b356f09b5c5483ada2c6af7267987584736c6a097028b9329f8f5ecab2`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fb754ed6d5d711f9fe45af29b81435ac6d016c9f104a197e02ae38a8b6ec`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 13.5 MB (13535949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5dd25f3cef6b4a020c2164e5827c3e14045977a81fc65c25ba2d3747b77cc0`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213638172a84ca00b4daad0e22bbaa5a22b80472d4866a27791add5e689e10a1`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e15e130a9409610e44c3bba79fada57d94acf47d2f14e31ad32f4d6176e976`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caa106576197fa7708918ef456b7a91916c9d67e486d8b6cfb5b457a3303ecd`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9910bf2d410cd9144da6aefa39b1d4e65e498bb1512a8fbe6638e8eecee420a`  
		Last Modified: Thu, 25 Sep 2025 23:22:13 GMT  
		Size: 1.3 MB (1333719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86027f98997f425db134500b0d03f2846a760ac4b20a165ab540bc1862c6a828`  
		Last Modified: Thu, 25 Sep 2025 23:22:07 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0878e615cc198711593ae6a37507cc049651c1ad60296c0f7ddb58e4db824e3`  
		Last Modified: Thu, 25 Sep 2025 23:22:08 GMT  
		Size: 751.5 KB (751475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a408a142f4034055750dadc5ca2041c49eaadb4025a435444da92adda0e2af`  
		Last Modified: Thu, 25 Sep 2025 23:22:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64a5ebd4a1364bcb3511d431cd5ce67d31096ec51275082b0c378657e547a6a`  
		Last Modified: Thu, 25 Sep 2025 23:22:10 GMT  
		Size: 20.5 MB (20524059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:2e6f801ebfc8d24eb3cb7a2fe0ea413789d5489106f935e63a7a87856edd4521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0379e2e1cb1469eee3580bf681aff0c50be0395edf41d259ce34cae332269ed`

```dockerfile
```

-	Layers:
	-	`sha256:dd236208f0f33cabeba0e1edda15d0189db2aacfe56e5ee674ab93461762de66`  
		Last Modified: Fri, 26 Sep 2025 02:12:58 GMT  
		Size: 37.3 KB (37272 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:cb25af7e09a570b32a7c4ba7645fc26203c14570455777fc9a5ceb6c8e2b831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57411080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94734cf3fd89b806a6174e1848e79634977b66bcebaefb3328f810c5ef8c8027`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa32fea9d18e0bb21aa5d036fefbf058ad92b637b4745b85cedb2e309f8c143`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 5.2 MB (5180910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fb35f74d20fb8549fc68209ec760e72c2c583bcff4fac189065d64b7aa383b`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a16a4e21aed64875cb326e0988ccb265d6db5eec435587012ba9ee5b634e8`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bbdca2e9a981657abd022c957bfc454eb758cdf37c2001c8d49e5b1f371eb1`  
		Last Modified: Thu, 25 Sep 2025 21:24:20 GMT  
		Size: 13.7 MB (13667207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b031fe9573eaa2ce66a637df5c3891656df759e88de025d1f110abdb0403737`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830af3ffe9544082402754722668d5862fc0e25372119c0d9dcd51e2cb775b11`  
		Last Modified: Thu, 25 Sep 2025 21:24:21 GMT  
		Size: 12.8 MB (12782275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8452452133ceb6d3804fa2b5df4420830ff13bca809abd4c7b8645f64aadab`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b731097d3f08cc776d90474f4d20964a8d77b0a2396e76d49494b8c6ddbd8`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcec5fac0bb0ed9143225112878db8b7ab8cbcd55f1f1fbfdd08f39a18d3fb5`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 19.7 KB (19725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cc70e10c7e338f96cd087abebe29b53bdfd6e988f6f7735e3703f943dbf4f`  
		Last Modified: Thu, 25 Sep 2025 21:24:19 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0bce04ddcecfdba3776ee25f5eec863a8e6fbaaf72bb7da948709500cd849`  
		Last Modified: Thu, 25 Sep 2025 23:14:14 GMT  
		Size: 1.2 MB (1233023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2286aea0022a62df4eb082767ecd2aa3b21bb6a879a95eb71dfe04a8439b18e6`  
		Last Modified: Thu, 25 Sep 2025 23:14:14 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d011edabc6c336eaf6c7d0f48b5cb9f0d6cffd0935b33821ec16a8b0ac186c`  
		Last Modified: Thu, 25 Sep 2025 23:14:14 GMT  
		Size: 751.5 KB (751475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae140251e26ebb7d4faf5e13f562c5de58a232c2cadc23a9f06b8c196b47dfae`  
		Last Modified: Thu, 25 Sep 2025 23:14:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c388dbdc2a2b5e36d7831053f5cf751c3f83186ffabf5cda689c7b88ebbce181`  
		Last Modified: Thu, 25 Sep 2025 23:14:16 GMT  
		Size: 20.5 MB (20523962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:96582e49add1a09f3fd13c3a81dae58d4f5f5a60a909308bf47e46778226c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 KB (414000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd76e1ee4508a4d2b994aefa489d69d42b91e2a9e18140bc8e94d53084e7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:a9f4ed8f7d6381bf6fa6c3d7df837d3625cb4f69bb0824b6f8f04ab32266d3a9`  
		Last Modified: Fri, 26 Sep 2025 02:13:01 GMT  
		Size: 376.5 KB (376513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98be77151349efe8b7446456d002e310549065eb49ece1842f8c49d229739aa5`  
		Last Modified: Fri, 26 Sep 2025 02:13:02 GMT  
		Size: 37.5 KB (37487 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:1a2eee6eab43db1aa4d794c8949824a89510458e4cff915ff3c84e1fc92d4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61493322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f4f38f38d78b7eccee82c9cfc08860a92d339ac243fc65740e8e29f41c0d09`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42762833876b2891840162bb3f2b2dc8e337b6405e803877384d81f6d7f859ca`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 6.2 MB (6228304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7e50b72b234b509972818d92d08709e6c7c9f021cd8bc4734296b33e074985`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496881f94362cbc448851f854f7343b9f991445464c5064fa768ba1a5f6e9da4`  
		Last Modified: Thu, 25 Sep 2025 22:10:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf93b637fd1c3f389acc6e90f0d387d5c23d661d11d853624c023d9617fe14e`  
		Last Modified: Thu, 25 Sep 2025 21:19:58 GMT  
		Size: 13.7 MB (13667208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7f61d2a4e13b96e05bd135218b8010a10de187149881190f100746490e9dc1`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6736c2f6b95f249926307a489dd76d28c534dbed06ba64ef475e3d76b48aefcb`  
		Last Modified: Thu, 25 Sep 2025 21:20:08 GMT  
		Size: 14.7 MB (14658309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d423cf999628f922fe623e5eddf38a175f746cd4130e45df74da6850e16776`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce53955b4bd84116f9401c48f4b471f28d7afa1a4d9b994cc56bf78c07adec7`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c65a21eeaadfe7e7e4f930a073089dd938d24cac9b2b464f216c8b48fa3ccbb`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16ededdb9cf830ca8d46d9fd8ca6ea7b6af37668e16de43e313c681758552fc`  
		Last Modified: Thu, 25 Sep 2025 21:19:57 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff5e443834f751f191edfa421a5b7230fc37db60f6542760e057bc5e436800`  
		Last Modified: Thu, 25 Sep 2025 23:12:58 GMT  
		Size: 1.5 MB (1480040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d7817137fcc87c32167dbe43729386abf2964c3c003a9db07175d59e367f03`  
		Last Modified: Thu, 25 Sep 2025 23:12:58 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a37efc602154c017d6df3111216bfdeaf8096db283ee2bfe951ea7be754dfc`  
		Last Modified: Thu, 25 Sep 2025 23:12:58 GMT  
		Size: 751.5 KB (751474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1358d22f121cab603351b8b6f6f43baa91972721a031c62549a0ef046b1ad43`  
		Last Modified: Thu, 25 Sep 2025 23:12:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87769ee1d38ecb84c1a881cb2016b19c9ff9624c32d19b52d1ddf04f669b1012`  
		Last Modified: Thu, 25 Sep 2025 23:13:00 GMT  
		Size: 20.5 MB (20523996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:94139b2c42a91e2c89785175df52f2e5e5d0de1916a82fe5de6f078299e54b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 KB (414148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d753bac330b4be499ad83547d19074c7baf2743a286c00f21d777b0ae25358`

```dockerfile
```

-	Layers:
	-	`sha256:9264cf97607734a3be3ea17efe7bb7c9d90f711e7f820f420518cc9981bc3d09`  
		Last Modified: Fri, 26 Sep 2025 02:13:05 GMT  
		Size: 376.6 KB (376581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82207a2ec4900229807aa84c1d4ecef1cf656772e8c051e3f658f0eff8a66246`  
		Last Modified: Fri, 26 Sep 2025 02:13:06 GMT  
		Size: 37.6 KB (37567 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:81ee652a934063884b6fd83b6a903d9b6fb399df6b9ca6d030fdb5d1c3ddcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61409913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6130b93e5adabecec667bce306f14820a8cc7284564cf6e18ce76826edf7c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5992baace3a2271f05ed2a94a020aaf7e05936e26e120dec169f46809566bdaf`  
		Last Modified: Thu, 25 Sep 2025 21:19:18 GMT  
		Size: 5.8 MB (5794064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea4bb153034cccdd78ae6b08206ff8960d8d3cf59b6f478405d1518224e28c3`  
		Last Modified: Thu, 25 Sep 2025 21:19:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9269a2570ff3e6d899fe152395b9db64f5756dd6c597c345742ba90637212476`  
		Last Modified: Thu, 25 Sep 2025 21:19:18 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be885cd77dac459ec23a86aaa280568be2eb0255ee171946cb89efdfc7dd1089`  
		Last Modified: Thu, 25 Sep 2025 21:19:25 GMT  
		Size: 13.7 MB (13667217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd218f1c89dce4e0b5544963d80e132403796afc41eb1ed4fa8805171bc6745a`  
		Last Modified: Thu, 25 Sep 2025 21:19:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e111e0ac52e8d2b90c086e7fad36365f4e0363fd0088059b3e3dceb06c46e9`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 15.4 MB (15426681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8048db63577e741e6f77898284e7d2d62fa4c423a085cc9d894339342f2b810`  
		Last Modified: Thu, 25 Sep 2025 21:19:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d91abb36b14d95bf6a6a07bf3ca58fb37531c4ad9ca98b2f199b5697a068fae`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a47c7b1dfd01ad18bf5dcfe3c4a3b79cc3eaf79678cb3b7e8782c8788a4d941`  
		Last Modified: Thu, 25 Sep 2025 21:19:20 GMT  
		Size: 19.9 KB (19926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6077ebd6864105a246e69252003a68b05fd57f1613c9609c7efbf61916f43382`  
		Last Modified: Thu, 25 Sep 2025 21:19:21 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c458327a7aa93a0a0bd4d4b162151bd3b47be16c94724e85e3104f13d1cbab`  
		Last Modified: Thu, 25 Sep 2025 23:14:24 GMT  
		Size: 1.6 MB (1577904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a22ab2b17e7fad9fb42c471dc9dbadfd02757dd738ecb5d73d6452f3bfdeee`  
		Last Modified: Thu, 25 Sep 2025 23:14:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09360912b48510584ca027f2795706aee9328d62c6769c18ba8a97ffe393db35`  
		Last Modified: Thu, 25 Sep 2025 23:14:24 GMT  
		Size: 751.5 KB (751476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4567e0523808da5274b0b2b6f7ae666b8334079d1bb93acc49a3497f87b25`  
		Last Modified: Thu, 25 Sep 2025 23:14:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6d5b1b1b0e5e10d989289beab5ac42c5c7f4eb45f292319bcca0f2c79841d5`  
		Last Modified: Thu, 25 Sep 2025 23:14:25 GMT  
		Size: 20.5 MB (20523969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:db6850b9cdb6f3962cf63c9e0311baf4baacb1e9894fa24532ed0772a6798d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.4 KB (416446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff7c20295f7b0c18990f713393f67a10d40bd642775e3ab2a670161aaf2c73c`

```dockerfile
```

-	Layers:
	-	`sha256:0a0c12fa3d53744e25d6a7658561a212256efe9559b19062a531d8303522b488`  
		Last Modified: Fri, 26 Sep 2025 02:13:09 GMT  
		Size: 379.3 KB (379286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dcfa9780f5b97240e586446009f59feaaa7774b105954a5633d2a2f0c53bb4`  
		Last Modified: Fri, 26 Sep 2025 02:13:10 GMT  
		Size: 37.2 KB (37160 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:fca50d19cbf19d6cf30dd25c4ea5f2636542d41047644629dc931cdf1d0f5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62250969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cce3832e8d753b21a3f490f4a8e20f79c4d9694abb32ee023f950e17f2c30f0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d165415cc65159456128153815546067ca89254c2ee16739d9a593915c2bbe`  
		Last Modified: Thu, 25 Sep 2025 21:50:59 GMT  
		Size: 13.7 MB (13667229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf9d58c2d24e175afe73c83186c70a54653d4a7a9e169b42a187588df2f087e`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a8582978935292b01078a8bf867fa366e4ae24fdd3a6b63289a97e9e36a9b`  
		Last Modified: Thu, 25 Sep 2025 21:54:19 GMT  
		Size: 18.3 MB (18302097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b74a94a214cb2f71f482afa4faacf43be7ff3885ebe5681a2a2948dacf6bd38`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657f121eb8a9c561c1df8375d82ca583c0d2fef78c3fada98ea8bb02facc836`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e1cf882843f2a8c239ed219c88fff5529cf3ebaa3d261c34d572fdeb471ea2`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810f4a524095951e7a04f5fac55938c485ab06b36becbb1da240b347bae343f9`  
		Last Modified: Thu, 25 Sep 2025 21:54:17 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6d07e263dceb6376cace0d29a26f4b57c1260bc3d736553f86d1405de6a3a2`  
		Last Modified: Thu, 25 Sep 2025 23:20:30 GMT  
		Size: 1.6 MB (1614677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefbed01d68ab8c16dd95e67c51682504d98a1ea1e8f71283d347058eeb2a4d7`  
		Last Modified: Thu, 25 Sep 2025 23:20:30 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e6743962910f6206bac1e011d45bf05e0a716b6c577178badc840bafe895b`  
		Last Modified: Thu, 25 Sep 2025 23:20:31 GMT  
		Size: 751.5 KB (751476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c96523748d5726f156201eaa9855b964e90f9a1256a2d94c6cf57e945c3259e`  
		Last Modified: Thu, 25 Sep 2025 23:20:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0156f2f3fd8ed910502cee3e6af842d1c09a6aac8c42eb44fea8087502791fe9`  
		Last Modified: Thu, 25 Sep 2025 23:20:32 GMT  
		Size: 20.5 MB (20523967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:f855d1819be755d193bc135659b79be8303003153cb75ebdc52d686d6dcd617b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 KB (411929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a764262e3e5bd091c4f103795c002b7d3eaeeba7bd4680ef8faaa73246df7c22`

```dockerfile
```

-	Layers:
	-	`sha256:75c57e6d16791605adb787158c0354c66c69ea5b22f14e5001799caad8a80043`  
		Last Modified: Fri, 26 Sep 2025 02:13:13 GMT  
		Size: 374.5 KB (374536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9c1a347adc2076a25aaa7ecfef383773ea786b2889a7e469cfa8159ab32fdc`  
		Last Modified: Fri, 26 Sep 2025 02:13:14 GMT  
		Size: 37.4 KB (37393 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:3269bcf7f60d080193cb752fdda0164a12f6b4233162a8ccb402f4f2db61980e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60566059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e01441259e93433f6d9badcff77fe2ca8b642749020cf9d107b632fd691afdb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce54772840e390ce79b2bd312dffccae5a0404b88de7d2cec073f06bfc4a7447`  
		Last Modified: Fri, 26 Sep 2025 06:57:14 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6b22cf755134f26369ac0039e67fee0e571a02ceb8a94e09289af33125353`  
		Last Modified: Fri, 26 Sep 2025 06:57:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410e2dcf97d734b0c6aa57f526a2f6790249dc29a3db1b8d560391854969845a`  
		Last Modified: Sun, 28 Sep 2025 03:53:22 GMT  
		Size: 17.0 MB (17049187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07818f4ff36efa1ca4dd2b14c543ff6486b20831e6367e4ae3115f78b17913c7`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12efdb41f2b3b1d5745bb1b2f116cd955caac98ddfc6a5099a65804355ee9f8e`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c5e4d1b398c9c371a721bf982bd522681338b5af4b3afc2856ca84f04924ba`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61d787deb89cbb48a17297405231ffd0f4ba5c4ef059cc29a6225599872e80`  
		Last Modified: Sun, 28 Sep 2025 03:53:21 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df219b714b06f26fe8cdd041429b4f7350f3ffa51dd98e0ea2a586ebfedc47e0`  
		Last Modified: Sun, 28 Sep 2025 09:18:20 GMT  
		Size: 1.4 MB (1413833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8517f753160189d43b3c7c594046904f9eb08553b638e489a1bcf083767563bc`  
		Last Modified: Sun, 28 Sep 2025 09:18:20 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2223ff768038c95e96981ba5683265c340912490e6a7f0fcaf6da59fe2967`  
		Last Modified: Sun, 28 Sep 2025 09:18:20 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1522a013ca19433477551d8d0d2ad53dcb3c9c54b8ed56fb031afb003e55ec3`  
		Last Modified: Sun, 28 Sep 2025 09:18:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c417e3e44c008b23384c6df19d5fb72b03c8eafca7662c1fade112c9f7d77a8a`  
		Last Modified: Sun, 28 Sep 2025 09:18:22 GMT  
		Size: 20.5 MB (20524157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:eda4158aab1c8afd71c53583084eb23b16c5fade45ade487b2aa776e3578b855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 KB (411925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88949196cb7d5f9fee7c7f05331e8ff8285794652025c1320ceef26bd2c342ba`

```dockerfile
```

-	Layers:
	-	`sha256:e57f57db37621b99d40b9ff808ce8a1837c271cd2ea0894ad69f817cd7967068`  
		Last Modified: Sun, 28 Sep 2025 10:56:12 GMT  
		Size: 374.5 KB (374532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e378fe8998743ccc90d2adbe923dc6b0dd03b66f28dbabade97dd9c989523053`  
		Last Modified: Sun, 28 Sep 2025 10:56:12 GMT  
		Size: 37.4 KB (37393 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:fe0787a3645b5d7542d41436c2fec993da446de5f8a24c6ce623db1d52091b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61531185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e4ec6514d4582edce420be397c10f37855e02e8fd9be54dea67111458be6fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Sep 2025 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 09:27:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Sep 2025 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 04 Sep 2025 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a3d587fe45527c5fb9d0f6c3e87577a24ab838aa52feae75c98a13d113ba79`  
		Last Modified: Thu, 25 Sep 2025 21:48:21 GMT  
		Size: 13.7 MB (13667205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aa7a56f2ffb6e0181fc8c56485409ee3e9cdccb2244fa89a1fb4aee0d3d31`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01789d2f734019e508a5d3ecdd9f51a0822d95e2d4b9ab5dd118731e4b244f`  
		Last Modified: Thu, 25 Sep 2025 21:52:55 GMT  
		Size: 17.7 MB (17671315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15f0850d24368c212cf078cdb77767416e9757af489ea505ecb9611bbbf0316`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3013684b773ccc2ab01f27c859679e86bfd68cbf6693b35ebcd1e1a75123e300`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1ecf3624fbc0d6d100154c4e3a79ec2874f74d8db894a62a7fd8f8505f3cf2`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ed9966c1b20ebbdec26707359e143a71a352650d3f56aa91db62ca653a9a7`  
		Last Modified: Thu, 25 Sep 2025 21:52:53 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51b6c538a13162b45d06943bc19aed98fe8ea0035b17ceaf287a33386b2496`  
		Last Modified: Thu, 25 Sep 2025 23:16:20 GMT  
		Size: 1.5 MB (1539066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddce71e23517c69aee27260a7c6216435ced08ce409b250ad7a2fc224f99226`  
		Last Modified: Thu, 25 Sep 2025 23:16:20 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ea747cd59c7635dbeb956c2fd994c89f4da87d28ec3416210f7c8825af0876`  
		Last Modified: Thu, 25 Sep 2025 23:16:20 GMT  
		Size: 751.5 KB (751476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f28ac39f2ad5e031209b89a742028a1a06dbdb6cb32ea9ea5479cfc0b2c29d8`  
		Last Modified: Thu, 25 Sep 2025 23:16:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9200d90c292b83bdecc7961841ff942ea2ca33f3e577545bd22ebd01d9e648b`  
		Last Modified: Thu, 25 Sep 2025 23:16:22 GMT  
		Size: 20.5 MB (20524048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:73fbac84dd9fa2eda5ba9fa643545c5c0bbd680e0db7993084ffc34e4595bd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 KB (411693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daa54757f7936089c4ab931564f27d5237f10e92ffd6b0894b90fd6d8f29782`

```dockerfile
```

-	Layers:
	-	`sha256:ff32882deacf75b89fc6ce38bc191a2d615b535d6b234f81a2a0e6d8dfb835ff`  
		Last Modified: Fri, 26 Sep 2025 02:13:21 GMT  
		Size: 374.4 KB (374430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7f0528debc900859cbbcdb1e38783ca6b3c61630464ca045ed0d694f1a89e0`  
		Last Modified: Fri, 26 Sep 2025 02:13:21 GMT  
		Size: 37.3 KB (37263 bytes)  
		MIME: application/vnd.in-toto+json
