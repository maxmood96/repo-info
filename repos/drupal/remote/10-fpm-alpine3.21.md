## `drupal:10-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:b18c30020287b0b18b57e08d461c82772e753104dce6690783a23607b24a5111
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

### `drupal:10-fpm-alpine3.21` - linux; amd64

```console
$ docker pull drupal@sha256:87932dee2d8aae7da8e81636c549285a976621e0fd6fda1a14bed597ee5a20de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56863245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98466564bc5adeeba86af77a6b24fd36b23b27794a722ba849233ed09590cfb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83437fe0a4c3a771901ef1e70fce3a16df07a0ea922dc58b5cc0df6d0eab9cee`  
		Last Modified: Tue, 07 Jan 2025 03:30:15 GMT  
		Size: 3.3 MB (3319663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1e60b4f13ec865a4b0cd3b520c3ee5ca5b635fcac92680c4772f5562dc60e7`  
		Last Modified: Tue, 07 Jan 2025 03:30:15 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958ffbb0049b84d94fc38c92fc7bebfa1d429dd102aef35e355850130868928`  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a90996a0f85e5fd58533572a9e26ea25b73b1636f5467cc6ea6b228f997110`  
		Last Modified: Tue, 07 Jan 2025 03:30:16 GMT  
		Size: 12.5 MB (12545715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7892757f58835169c21e1bb7281ee5794b59f7e4ec01a17d1f29afdaeb8c60`  
		Last Modified: Tue, 07 Jan 2025 03:30:15 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92816e910173cf2825cbf274bf7a4eb9911cc953751c2edc5846fd077911ea02`  
		Last Modified: Tue, 07 Jan 2025 03:30:16 GMT  
		Size: 13.2 MB (13199091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d2d265d22a576c0eb6f147d9aa3b801dc9a22077b9925fa1253fd508c6eb2a`  
		Last Modified: Tue, 07 Jan 2025 03:30:16 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023489b36d5687d757a794e72afaa57f869e9e9ec9e6c680e93cef45d40ef814`  
		Last Modified: Tue, 07 Jan 2025 03:30:16 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1044383fd277bf7f5635e388e8dedee33e8e749d19e3232d902be16f2d795228`  
		Last Modified: Tue, 07 Jan 2025 03:30:16 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed379f1c444ae59f0f6c205f4c6df58b0ced540eacaefa0119584ff6f28ad4f9`  
		Last Modified: Tue, 07 Jan 2025 05:15:22 GMT  
		Size: 1.9 MB (1921430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c1d070d6229ce6e872865923d63a4b2be03ea209c74f8a4956418e9cff17b`  
		Last Modified: Tue, 07 Jan 2025 05:15:21 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a461fe0e258ad51ed31ee14bad01395dd8b989ee92ae4b1a383d3ace0fdfcc8f`  
		Last Modified: Tue, 07 Jan 2025 05:15:22 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d43a32632a85951a1994c6344936633ff918d42a9d3d0cf8680ce7715032719`  
		Last Modified: Tue, 07 Jan 2025 05:15:21 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2fe2bb89885317f1bffa8f334a0fdf3663a8f658f211a6e4a14c065bf34787`  
		Last Modified: Tue, 07 Jan 2025 05:15:23 GMT  
		Size: 21.5 MB (21465405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:128e7f37f66ac5db1bb508fe5d99cb5dcdeb4b9a54b20d348fed6247283c28ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 KB (386632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f626a782610b9f82f7b8ade627528806c9f47b0ccbc47f3b07f7c8e53ab46992`

```dockerfile
```

-	Layers:
	-	`sha256:7ac4827b39a81d26b2938fc0a98bfcfc640b106660c87d9d7a24d866d285216c`  
		Last Modified: Tue, 07 Jan 2025 05:15:21 GMT  
		Size: 351.7 KB (351663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da8515f4c5981bf3cc465dd6735a32da2811903a98fda3d3eab4ec32cdb9eff`  
		Last Modified: Tue, 07 Jan 2025 05:15:21 GMT  
		Size: 35.0 KB (34969 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull drupal@sha256:a4b8dfcf34c119dfb5a1fdd21d3a14deac70f7425be5f9fbc399592413c236f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55255227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c5b158757f697d9462633d265e342350b248ac7257f7e8e791a00ea1fc5f4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3015bc8c172f12cc4fe09a12da51e00e780513b39e265561ecdf83d600100`  
		Last Modified: Fri, 20 Dec 2024 22:07:15 GMT  
		Size: 12.5 MB (12545966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373e3d546cbde8439a8d33b94b4dd43b562e1d7c7e7a91409739d55c42ed2b03`  
		Last Modified: Fri, 20 Dec 2024 22:07:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80e80c0330fa80d6105fe73cf9b8112dfd5a6966adc10ad082e40796c09a30`  
		Last Modified: Fri, 20 Dec 2024 22:12:46 GMT  
		Size: 12.4 MB (12403370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d54625d0cec0ed6173f57d2deb7f36f1836db6eba30f1631709339abf12ed4`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4871ed599a983e8f274dcad4bbb5421856b5e4f6e2d41029a509ba54a67ed3cc`  
		Last Modified: Fri, 20 Dec 2024 22:12:46 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccedcad885a243169d01c9a486d7ff2ad32a246cf88ecf72cd997c9d80d3251`  
		Last Modified: Fri, 20 Dec 2024 22:12:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbd2d428a7b2624db5750bcc92d1379dad59a64d4e2a4dc02955137c25d68c`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 1.4 MB (1394140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08caf27db20e957284b3d2bfb3e527955242cccf76297117c11a34c569e909cd`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a70046e577b7d204f1d6cc9b557779cbc11bba2be2b563b2598379ea832a2`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7480e13c602c8b6812f811b6966ba056c91620d2e58ff631ecd9398af9a0d3`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a37a6f2dbcb1c8dcc3fc62948b9b6477b3b7e9cd4f754026e2f9c96404e42e`  
		Last Modified: Fri, 20 Dec 2024 23:21:47 GMT  
		Size: 21.5 MB (21465812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:0a5c3c7ac0e4d584805f450e4a6a0c545fdfa596bb4b335e23262f719be618e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f186e22fbc719bf232e6d235af1b5ed81c338facfb8544c0b27bb346c474a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f140b61ec26e9cc8a4cd50b3f99a8819724f1491ce53ffa726fce30dd201710`  
		Last Modified: Fri, 20 Dec 2024 23:21:46 GMT  
		Size: 34.9 KB (34944 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull drupal@sha256:9d67173059f5b14255c76783697cb11c83807cb2aac3c112e62bf4e4f0f988ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b705118df32c7b707edad6bb3e7526f10c8f6cd48eccdb32a32c3e8adb39395`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394c1cab161152681c4a4923ba5640453fb36651c5d406e1461e78fefca0ff9e`  
		Last Modified: Fri, 20 Dec 2024 23:11:53 GMT  
		Size: 12.5 MB (12545977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6990a988b6908cb902b7b7a84eabefcad3f8564ccfc05aa272984fe5cfb8bef`  
		Last Modified: Fri, 20 Dec 2024 23:11:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcbc81f0ecaf0ea0f2c085b8e8a597757bdac44152166383e29ddee33c99f14`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 11.7 MB (11683753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2efc2a5fb23eb7991af83cfa6efeaf0fe754b457dc9b64ab4a446a53af99873`  
		Last Modified: Fri, 20 Dec 2024 23:15:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3d570b1f188630b1108f81fab18a1b2edb5d7ffc684efa24176a3e4e28e255`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bca6ede7b4638a6fea24b70c80b9afb3f8d9be83b86c49f263c0260744826`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1315cf1c41daf7d97e1478535cac922dd7b72ce02529b20604d89c1cd24129`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 1.3 MB (1289830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1698e879951da7bdb98fcfab0a418a4e12ad6e7b72c4305c89ea5f49bbc635`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac862919ec6319cb42f64fe2a94ccc0bb7458d5ec85ac9462ee7939f38389a08`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13134ca089c732390fd4055015557a17af9c506b8c4f79d4d3aee30c564a513a`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbf80f77b77a03186f5bbf4f06219a3a68ef7326466e60e3015d07d81c75817`  
		Last Modified: Sat, 21 Dec 2024 02:32:22 GMT  
		Size: 21.5 MB (21465433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:243a9df815dc8c84396ceb7f2bf87642e3d6cddaeb7ed93016741c50d4ba5ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 KB (391287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c193f661b294e7ec5eccef47b52d77073eb33d026b9c834a5e55082dcf1ebb3`

```dockerfile
```

-	Layers:
	-	`sha256:08ee97d477cb5c3eab014de4e8950ff765bb55db1ab0099c6a20d0763c748883`  
		Last Modified: Sat, 21 Dec 2024 02:32:20 GMT  
		Size: 356.1 KB (356128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a03416080e3ffe7d289704167bc6d12d20f80be43e0f21f5782f022b82bdfb`  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c5c637e1181033171b29bbdbed2f436de56196d86174159a829bd8c40a99f9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57463119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a021a23ef7d64a1262596783f47cbfc30372ca98e5f86ab7af9951fab2c7745`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40162970ab5d274af508499ec972de793b17d5f14ffee01a11a8e5a5256724`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 3.3 MB (3315021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8949964140eb86d4055cf8d682a19190f4519a76a0135d9c0635b8e590a12`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc0ab84d61c5b652f4966a78d4064b20a3ee74b683b2fff8a31bfa6695fd46`  
		Last Modified: Tue, 07 Jan 2025 04:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0bdb6e7b79499e596b4c2d9e0b652d3ceb130e8540eb6dfe824b8c34c36263`  
		Last Modified: Tue, 07 Jan 2025 05:43:09 GMT  
		Size: 12.5 MB (12545721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b768d70aafa38bea4fd88b3a2661e71dfeda4f3a573a2d4ce3f9d2fbf63405e7`  
		Last Modified: Tue, 07 Jan 2025 05:43:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239500ae7e14c6947455dcfadad35d0694c5bb50ace29e57443e40724d18ffa`  
		Last Modified: Tue, 07 Jan 2025 05:48:23 GMT  
		Size: 13.2 MB (13188572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a58e9aa2fafed1600b8f0bea4f7aa32ab7f092220fc824d0ffef41fa7aa359`  
		Last Modified: Tue, 07 Jan 2025 05:48:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d911c5bf4e9cb436900791ce8016e41a8cd12ce3cbe533217a57b07617bbf9`  
		Last Modified: Tue, 07 Jan 2025 05:48:22 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157db7388a97f4f2f5628be437470f2df23acbe549e689e5f4b58ccd307a825`  
		Last Modified: Tue, 07 Jan 2025 05:48:23 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ad5a41bada24cfb5c83208a68e0eab64752000c517211d9ca31d11e8e937d`  
		Last Modified: Tue, 07 Jan 2025 18:55:56 GMT  
		Size: 2.2 MB (2189775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f33fbc6473665ffe4caedd197e56cd5dec0f71026c612a724d93413a56a6ba`  
		Last Modified: Tue, 07 Jan 2025 18:55:55 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca81e23e5b149dd93d7a76b2cb6a532bba2f9deb29708192203702ff3eda9205`  
		Last Modified: Tue, 07 Jan 2025 18:55:56 GMT  
		Size: 742.2 KB (742238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3ab8069260dcd15e1b9aea85858fdf62885f41d93bb80f20cb37605f540f2e`  
		Last Modified: Tue, 07 Jan 2025 18:55:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74eff2388e39e3323e4a1a16100d26ddc21111dc12b5c1395f38913bee7165`  
		Last Modified: Tue, 07 Jan 2025 18:59:33 GMT  
		Size: 21.5 MB (21465495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:52482c2830235ccd779f4e687346248363364cf96a6c9e1e50483da93668e43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 KB (384228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32463161b8b5837581a1d2db42a36877480d92d7fb2edc49670600b252587cd`

```dockerfile
```

-	Layers:
	-	`sha256:7213188968bd1f63cc8bea608f48301e612f3dec57acbc5b54c3b5ae95f601ff`  
		Last Modified: Tue, 07 Jan 2025 18:59:32 GMT  
		Size: 349.0 KB (349002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcea8aa559fa9e81feec4673aaf0093c048bf12ab444e6f811180f41747d3d07`  
		Last Modified: Tue, 07 Jan 2025 18:59:32 GMT  
		Size: 35.2 KB (35226 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:eb4bdc99e494ac982de256208ecac5deb64d177d603ad3dc54114ec3513cf91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57092618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ab25ae395c7f1c812298b5f341e746f472078588e3f45f3fc827c1b5701c7a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e817d5598706f0b682a7002ab1ed68fb0250684cae87c456ec75f80e07db7b53`  
		Last Modified: Tue, 07 Jan 2025 03:27:12 GMT  
		Size: 3.4 MB (3357001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76966dfdf5012543e163d7dec948ec959c1e20f930feef421ea59352df840cb7`  
		Last Modified: Tue, 07 Jan 2025 03:27:12 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566fef1294a66d01165a6b881243382bcd8d57ac4ed182c5dd5dc1ea08c2b80d`  
		Last Modified: Tue, 07 Jan 2025 03:27:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec175fc53ff1bfc113d9559f52a8826792c5e35813c655e3c24be5560d08b466`  
		Last Modified: Tue, 07 Jan 2025 03:27:13 GMT  
		Size: 12.5 MB (12545707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff5674fb0d579c17bd668b00d0093874403b1db32db84d04e18622d56dca25d`  
		Last Modified: Tue, 07 Jan 2025 03:27:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f93bb0aba8b4df642f7bae2906663228dd5a9121977ba3ededf84799b3a64`  
		Last Modified: Tue, 07 Jan 2025 03:27:13 GMT  
		Size: 13.5 MB (13505777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584df73f63c36bb5163bdb32256836d88e6838a6c3c12711806613ee60fe59`  
		Last Modified: Tue, 07 Jan 2025 03:27:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e9426c4bf28260a2500d83a70b16119905f4367355a4407882c860e3109823`  
		Last Modified: Tue, 07 Jan 2025 03:27:14 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d565dcb29cd7f405858b66841734ae71b623c10b28ee42b7f00eb9edde65c`  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f412c052bcbab34ab5e297346903994a0b79403008896fbc4b37328b7aba9`  
		Last Modified: Tue, 07 Jan 2025 05:15:18 GMT  
		Size: 2.0 MB (1984315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce09489c9ee2b433fded0e10bef6e025a325da7dca285bfb3a9d085666f85013`  
		Last Modified: Tue, 07 Jan 2025 05:15:18 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7aa33d810a87701978d9245aa21a4147a73b6311b2f45d78537ad745790e43`  
		Last Modified: Tue, 07 Jan 2025 05:15:19 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628dfa5de53d694a5b3d85f8f1117a317e443b1c72a41380cb337de2a48cc4a`  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6339d9a4032b463aa37202f9e62530ed50c4eedc1381e0b082ca9fec982546e1`  
		Last Modified: Tue, 07 Jan 2025 05:15:20 GMT  
		Size: 21.5 MB (21465847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:475964c8537ab009d186816c1fa8dae028bc469bc0e9127492fb6d8adf4794c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 KB (386485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f69377a9cc9a954da55f93a376f26c2c28a93fb26c233822c5bc45ea9aa42a2`

```dockerfile
```

-	Layers:
	-	`sha256:3a1aa56a6fef826e1d82eebb8b1d8df0cd6130f1d6b08406ac1ddf83dae7088e`  
		Size: 351.6 KB (351598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea241868974e07f3c4973d34c32396a9c7cfc63c2582b597593f834c544f71c`  
		Last Modified: Tue, 07 Jan 2025 05:15:18 GMT  
		Size: 34.9 KB (34887 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:1fb19249c4667abc53fabdc0cd9d2983416e9771bf1c51924e6192aea60b0c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57178178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac8f2a39e58da6aeadfb4306fb050f7f26981a04322a6511f7d1df1f0d43238`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770cb477b1c68317bfb2860d023b4972e2abdce0461a24b5e3c5d2ff8eadff58`  
		Last Modified: Tue, 07 Jan 2025 03:57:04 GMT  
		Size: 3.5 MB (3462737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8249e7b9c0ca9f3f0f47f0fd9d16c7a924f96930522c42609a86570d36e0ce7`  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91a0f9929fb530faadf31b21d97adcb1eb6d139b4a4d3b93c2e76f0c02b000`  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d18bbea73dafc5073c86b755e47586f7576f1e9933f3818513997210de367f`  
		Last Modified: Tue, 07 Jan 2025 04:57:58 GMT  
		Size: 12.5 MB (12545715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564394c5f4c666576f54f3579d1db896fbe1cc8ad0b6baa6f5b276ecb2b050c`  
		Last Modified: Tue, 07 Jan 2025 04:57:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed30de1dc76b2d5701d66cc857d49b440be96e64aa0dc326890e816eebcd7af`  
		Last Modified: Tue, 07 Jan 2025 05:01:28 GMT  
		Size: 13.7 MB (13669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628d27d1d886c5e276a2dab334fa85dc9b1315404f5247477a75817866c80cd7`  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d367add280466a3bf07369387e128b5320fe7077a036a6939d6ced8f66e585f`  
		Last Modified: Tue, 07 Jan 2025 05:01:27 GMT  
		Size: 19.6 KB (19558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32233286c9277825ca433a8cfad453c1c783bc48d14575fb5fd022df194ed18`  
		Last Modified: Tue, 07 Jan 2025 05:01:27 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67511e60503b16c863cdd5e4d839518c38d45590e3758ab9d4e188a06940717`  
		Last Modified: Tue, 07 Jan 2025 12:04:34 GMT  
		Size: 1.7 MB (1691962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ed6b3be69e021f63519ece14184b808a747ccf52cf215bb77e5acc7a456012`  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4664389fad8e5c129a92e180302a5768aede64d686ba106f5f925d777eca19a5`  
		Last Modified: Tue, 07 Jan 2025 12:04:34 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef9b06915b60073689f3eb08fa69a4130051db8dfec43544558845c75e52ad3`  
		Last Modified: Tue, 07 Jan 2025 12:04:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eff2cc7a44404dc617b8b5da9d27a2398be9aa6c90be54976eb91039dd3d26`  
		Last Modified: Tue, 07 Jan 2025 12:13:46 GMT  
		Size: 21.5 MB (21465266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:1af0af9fc7e5b866dc060587aae4a997864052a205dedd454b6bc76824fb4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 KB (382057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fda0c1691cf316e71ab5ee770c330223f7a1f6b480904403040e5c76327e1b8`

```dockerfile
```

-	Layers:
	-	`sha256:3ff3f4fff4412281c79acf0ebb38b00d8d8610cbda8a86e7f7cba9a82a88dd21`  
		Last Modified: Tue, 07 Jan 2025 12:13:44 GMT  
		Size: 347.0 KB (346981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4059decaebb2536ec4d2e9083514c0af4162c9380836f01f4df7bf5b4e0956d2`  
		Last Modified: Tue, 07 Jan 2025 12:13:44 GMT  
		Size: 35.1 KB (35076 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; riscv64

```console
$ docker pull drupal@sha256:17d5f3edffb4c3f14a5963d0e6453f096d8f16afa51dc310567e532b4339518b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56249376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b057f48ff9c882506fad08fd389c6346985de9440a18368cf13a821a6b11fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
		Last Modified: Tue, 07 Jan 2025 21:29:18 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480f55a34db1d920fdb0fde2a7db7b9921e9c3037a184e705b537b59acbba255`  
		Last Modified: Sat, 21 Dec 2024 04:07:18 GMT  
		Size: 12.5 MB (12545944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ec58601b0f7a00ee0a722ab084eb9dd5ff3a8be49ce3ad70df14cbaab554eb`  
		Last Modified: Sat, 21 Dec 2024 04:07:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b1f931a6f37ee831a17be3bf5d6641bab60244f9bace237fe02d2ce9dd1822`  
		Last Modified: Sat, 21 Dec 2024 05:02:49 GMT  
		Size: 13.2 MB (13180780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914443008895b62b8fb11d43caa8f2b31b8811c7f299ef52aa1fee9a06723108`  
		Last Modified: Sat, 21 Dec 2024 05:02:46 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf011b88caafc3cd9722ad9e0558db1b9db8bb6968edcecec6d5bd398900a2d0`  
		Last Modified: Sat, 21 Dec 2024 05:02:47 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270db71f14920874c2aa4c7b7ad2afe56b7e09418c0c3367fded85dfe466ce59`  
		Last Modified: Sat, 21 Dec 2024 05:02:47 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419175e45548776d9ec79da83672fc2382c19826fd7b3962392bb9de162885a1`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 1.5 MB (1480147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f6a469aebc75ed8b53d78c478cca162c5839d3b6caa78d8b9571d60b0687`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2458aa61f8b4788b1d584f3a1b6061640c2be90d9a56a813bd96327c000fb1`  
		Last Modified: Sat, 21 Dec 2024 18:17:02 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224d8b3ab70570153e4164afff91b229a6cea6ebf5dd0c6d3d6bb9ae869fa15`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910cbf8e5cca9108625804c7da3e0dc1274c1cbd91d4eb5779e815d4340f611`  
		Last Modified: Sat, 21 Dec 2024 18:36:47 GMT  
		Size: 21.5 MB (21466847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:2fb4d8e7b02294f1fb0720709067189535390c8c7eed8c232e8b9dbeed1ccf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac573405e247751c60975aff9383f6e9b9e746cd91632b7feb01578f3de1dff3`

```dockerfile
```

-	Layers:
	-	`sha256:3b0b00210f8139c076d96e024d3a350c9a3c0cd02189c517de73619c2726dda3`  
		Size: 354.2 KB (354155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ce0a5e57ce63e01eb7fee2e56fc6e0d3e19bce633791d5097913f9468c2210`  
		Last Modified: Sat, 21 Dec 2024 18:36:44 GMT  
		Size: 35.1 KB (35077 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:8825f9d51f2693a1a1a09f5d96c54344978a27995e3672e1e45911101be4d1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56553178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad66940aafe29d504745cfedb2de5bdde968a12f8139fb722d3c65e74d06e3cb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 18 Dec 2024 04:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 18 Dec 2024 04:27:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_VERSION=8.3.15
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /var/www/html
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 18 Dec 2024 04:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 18 Dec 2024 04:27:27 GMT
CMD ["php-fpm"]
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV DRUPAL_VERSION=10.4.0
# Wed, 18 Dec 2024 04:27:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 18 Dec 2024 04:27:27 GMT
WORKDIR /opt/drupal
# Wed, 18 Dec 2024 04:27:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 18 Dec 2024 04:27:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81298346f7998688090749dc4a0c5695063618d53944be66940589a7c4cec0f0`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 3.5 MB (3546676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ae0e9cd63cfedbc820ff5cce925cad38492ddd41b8ef4a7dafcfb8c8699fc`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19010506c88f12a8f1bd5ca006528412ce5ffcb1745e840ef9578eb779ec3a4d`  
		Last Modified: Tue, 07 Jan 2025 03:52:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7e5ced940b8fad618c84d8f8c32b8aafdcd51f957979dcfa3ec1f0c305f2eb`  
		Last Modified: Tue, 07 Jan 2025 05:03:59 GMT  
		Size: 12.5 MB (12545717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9937b17fe8adfdc640c52f065c2a60a95efc9c4c1915d615053398806ca3ea00`  
		Last Modified: Tue, 07 Jan 2025 05:03:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f085c55395141a41645ff8b72239d78931fb6b2c06fa1fa9ca234ed7b35ce7`  
		Last Modified: Tue, 07 Jan 2025 05:03:59 GMT  
		Size: 13.1 MB (13149875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6466d7cfa142dfde7b6403209e922028073dc8e157024fc6e56ccfd1081047`  
		Last Modified: Tue, 07 Jan 2025 05:03:59 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e417ae8f16c7fe9eabba4387c7bb3d4bbc1666d541e4d4e43085f7a45411b`  
		Last Modified: Tue, 07 Jan 2025 05:04:00 GMT  
		Size: 19.6 KB (19551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb692df12d74406f21f9d4a7a2356b5d9a37af50a42712c365c2c4a6adcba052`  
		Last Modified: Tue, 07 Jan 2025 05:04:00 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f8e48a53db69adb4974ea64ccb77e0fefaa88e5b6d94b61cbb5d17ff766e93`  
		Last Modified: Tue, 07 Jan 2025 21:31:44 GMT  
		Size: 1.6 MB (1611379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693e82fa06fe73734131ce7447857a4aa907def810bf730ccc5daa5b9688e16`  
		Last Modified: Tue, 07 Jan 2025 19:27:55 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4478c1d92d6a60ff354ffe094c02884da527b3aaadc00b33482b9e7599ad1bce`  
		Last Modified: Tue, 07 Jan 2025 19:27:55 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f525a52c397e329d3a87c715d1e71440e9e3a1723600a8b3895a26f4861d0662`  
		Last Modified: Tue, 07 Jan 2025 19:27:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d5fd9eade7375f25862e9465ff9cbb812c0b07bcb5a0039e42032f6b7aa257`  
		Size: 21.5 MB (21464554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:515ac6c85f18aa3246ad781d538981fa3da70e82b8bb81283db6e8c6b77f7c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 KB (381869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98873f5f4f28b511feb60b774136cc0f62ce786860b592b1e7180ec9716f9035`

```dockerfile
```

-	Layers:
	-	`sha256:af8ddb09b36873b52eb9ebc79243f4e52d95ad1ae3ead488c16ba03cc387442b`  
		Last Modified: Tue, 07 Jan 2025 19:35:46 GMT  
		Size: 346.9 KB (346899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f4f57328b60f232d2bf473eb8997857a9aa1fef6e5a32db3330cc45caad390`  
		Last Modified: Tue, 07 Jan 2025 19:35:46 GMT  
		Size: 35.0 KB (34970 bytes)  
		MIME: application/vnd.in-toto+json
