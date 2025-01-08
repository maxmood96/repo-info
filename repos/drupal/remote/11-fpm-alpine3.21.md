## `drupal:11-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:f46e8d1f2502b8ae9de19c4a2e7162832d7d4cff8f759212014f811c3c834181
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

### `drupal:11-fpm-alpine3.21` - linux; amd64

```console
$ docker pull drupal@sha256:6232e271de3653c6dc59894550e72409ad1509cc628fccddf409c024411cedfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55430994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24952837b49201e6668772057b4324060167e76deacfb6ecc0d90452dc7bbc87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
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
	-	`sha256:4da4be68528ba968d3e763461549d2937cfa3bae34925b0d8d41375924de5934`  
		Last Modified: Wed, 08 Jan 2025 00:31:02 GMT  
		Size: 1.9 MB (1921422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8928db3b9965f6a7dfe8850ff4010a350954d25ba43089234031408d65dcd`  
		Last Modified: Wed, 08 Jan 2025 00:31:02 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a425204d465303e61fd37457c9f374bf28586f5e75c95facd8ad8b0e63fc942d`  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cf8d6704668e9b9b569cd5aa5fd32b9a4d3afdb2f8eddae2f43c33e7fe571c`  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47176ee00dcb95c6f9d3286e6e045a2dce1527ebd8452dd5aeea5e6730c69d20`  
		Size: 20.0 MB (20033167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:592fe3b787d499e0810f903316d6f84e7542f49329654ed7ed4c45fbb890bd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 KB (395175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6f3424d4204ecb2f385aee76fb8d4b39c60f7af3f79cb27cdb90d5ad33b868`

```dockerfile
```

-	Layers:
	-	`sha256:802428a82ad7395c1fd28327959d51442c484fff822c57fe23a2ecb5c5f5c1a2`  
		Last Modified: Wed, 08 Jan 2025 00:31:02 GMT  
		Size: 358.9 KB (358937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854e01d1ffe7ca7e8620c1080d7e526c72674ee9b5506580843b32b95dd31f2d`  
		Last Modified: Wed, 08 Jan 2025 00:31:02 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull drupal@sha256:4361ed50c584e0d904af25a98d343676609e992e63b7762f219a6283b5f66fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53330214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8419fe8bc8dd8c08fbb9881048be0d62d75ee60e2c31a7ba8e87e90eac5fbd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bef010c611114840926e80cb28932ac752a42db1830688c08b53e3b0479b57`  
		Last Modified: Tue, 07 Jan 2025 04:04:46 GMT  
		Size: 3.3 MB (3288904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6270f8fc8d436fea30c28e682f01c03d0fc9e3ad4d478dd522e49204e509af1`  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d76c367f31c843767d908ec20d1f4689fd733c923fd9605738b522084ac5a`  
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c587f8e3b21b4f953e85642c1d9b53e22989422a76bf5d7fd6b963c289dce3`  
		Last Modified: Tue, 07 Jan 2025 05:17:35 GMT  
		Size: 12.5 MB (12545717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eca7738b5173391c480ee08af65e2b60146afdb7c2adc74ed70422b43cfd9`  
		Last Modified: Tue, 07 Jan 2025 05:17:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f977e0c4fb6fc0d66e2a04f216007e843e6e8a5a9ff99aff56e1f0b7487344ce`  
		Size: 11.9 MB (11932135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a5d6383779af0bb0de20a36cfbd98c24ceb42607ad110cb2d3e4a5d11c709`  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee7b9e4a5d32d178e781bce7dacf758f8bb9551635121700871b457a579dd09`  
		Last Modified: Tue, 07 Jan 2025 05:21:30 GMT  
		Size: 19.6 KB (19555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a84c69ae060942eafc5b4b2205fdaae61934c19f0bec3cdd142aad6c9429452`  
		Last Modified: Tue, 07 Jan 2025 05:21:30 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d529b88d9dd9d7741291430caa8a1fb19ccbde61371d012524dbefc06bceef1`  
		Last Modified: Tue, 07 Jan 2025 20:23:55 GMT  
		Size: 1.4 MB (1393608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f4c38cc139c8f98a813edc8ed785b22b6864f567e292ed2239aafa362cc33f`  
		Last Modified: Tue, 07 Jan 2025 20:23:55 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b036e7ea7eb376501da1312bb9afc913efc83f0806aa55f7c132aeaf8f945d`  
		Last Modified: Tue, 07 Jan 2025 20:23:55 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c513e09506f9bb1b6909f2e85d1ffbd4e76de2dcf611ab7662cb150d72abc6d`  
		Last Modified: Tue, 07 Jan 2025 20:23:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e24ce0f9732aba33acac91d2b0d907aeba3c7e5c9530ae7bdf9b9f1aae4f1c8`  
		Last Modified: Wed, 08 Jan 2025 00:28:21 GMT  
		Size: 20.0 MB (20033285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:be1310f2f35e4c8b2c349b1a9665f66adda17a661756a7b357dcbfa3da82e7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 KB (36243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88b0c5260b9d5a92a6d812320f88d953df74d759122052bdffefdf46e36029d`

```dockerfile
```

-	Layers:
	-	`sha256:3bfe16aaf356d3417e07c6f7fc3fac257e94b7f7627a11cd531607ea5d875888`  
		Last Modified: Wed, 08 Jan 2025 00:28:19 GMT  
		Size: 36.2 KB (36243 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b60cdb5c0349891f4a3e0e186132386162fe6b94cd0fce317cbf3f37d188a38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52078647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719605e6867d0fc660e31d49c7d0f97d101a7b30c0d7dcd3e9046ceccf9429ce`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a46a05ef2f8f5dc8f91bb48ccb26f8769e182e5d38d1a1d557e82d060b4ec5`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 3.1 MB (3097878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0ae4122e18dac51504a788ad60f49ca9ac0b06ecc7c0df42385e05efeb7e30`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90539fb79bdae2b2ecda3212490766029854e00ebfa8dd5d8618634d5b8b789b`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89756a191fc634d0cc74ddf3a32dbc238194745f8fb9ec49e56190f6ba247c24`  
		Last Modified: Wed, 08 Jan 2025 03:31:08 GMT  
		Size: 12.5 MB (12545715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f95167d47aeb3a435077aceb7d8705c818b486632725b186c95787b67034b1`  
		Last Modified: Tue, 07 Jan 2025 05:00:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b950f93713574e66a68a9cf5c594595e585411adbb3fc9154187609b8f69aa44`  
		Size: 11.2 MB (11245553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2709f15732b62e164d5667ce262200d91fb3090201e3ac7ba1df18947cfa32cd`  
		Last Modified: Tue, 07 Jan 2025 05:04:00 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5819d3ced69491a713ff5da3f13042730a03e175dabe19ebb66ca4eb739fdf`  
		Last Modified: Tue, 07 Jan 2025 05:04:00 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498cf49a11358c0cd539bbff975a5ffebd01232b53877c0fdd27afa023b3c651`  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74c13dfa8a3acd5ea2d813fe4fa70ebc8126d1549e87ec191a0084522da659b`  
		Last Modified: Tue, 07 Jan 2025 20:57:32 GMT  
		Size: 1.3 MB (1289765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566ca98b3697b59578235225d49243fccea4d62f22dfaa210c66d81798bcd55`  
		Last Modified: Tue, 07 Jan 2025 20:57:31 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163aff3da70d9c3c02d021fd585c444db6944fecea098c5d910568633998ebf0`  
		Last Modified: Tue, 07 Jan 2025 20:57:32 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402159f9c45e0ce79e2032718c7720bf3f56b37fa4fa9f047330c772f8b21d44`  
		Last Modified: Tue, 07 Jan 2025 20:57:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7899dea8b322412745be4ff89ab0e1474d867e46ac64a7275bfe504e3bce3e`  
		Last Modified: Tue, 07 Jan 2025 20:57:33 GMT  
		Size: 20.0 MB (20030954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:966dfde38c5c44aa207f3a781f5134679ccfcdc86d2e25ab20b6b1b9277a5129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.7 KB (392713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efa885cc95193585950266fe306c143e9b0aecff15a1912a385fda916bcfa49`

```dockerfile
```

-	Layers:
	-	`sha256:ee63f1441ac3311b250efd6098f1610bcbcbb3189a2c03587d476696cada78fc`  
		Last Modified: Tue, 07 Jan 2025 20:57:31 GMT  
		Size: 356.3 KB (356256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794973670eeb0325b35cea7d18bd3bab597d3ef572fadb1e0d10bc1b794ad24e`  
		Size: 36.5 KB (36457 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:798785f9c2675c526323edb32937af6528d37723fef83da6ba6e0741dc2d4fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56028580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cc34bebf596aa68a6453195e560ddb868cadc6f263cb5370439dec8bdf89d1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Dec 2024 22:27:38 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
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
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239500ae7e14c6947455dcfadad35d0694c5bb50ace29e57443e40724d18ffa`  
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
		Last Modified: Wed, 08 Jan 2025 04:31:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46aa35fe0de2ccb0e890df16bda61f31fd23f1152ff5e38cb7777f319f0fb85`  
		Last Modified: Tue, 07 Jan 2025 20:08:19 GMT  
		Size: 20.0 MB (20030956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:5a985bca8592d1db2fa6db120fd2054c3b56dffffc5f1ea3b8593b6a55c40691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 KB (392866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fd0fcf3192eed608260539fc27bd29c9174de58f378b5d096e38192b2f31e7`

```dockerfile
```

-	Layers:
	-	`sha256:4c4039a23d94c1cfc614a71b22e56b48328500b95aa3283ddc681ed6ecacd3b8`  
		Size: 356.3 KB (356324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dac178df52c6a25756cdc91c950db7ee5d9416ac2b234baae1644f88a3a32a5`  
		Last Modified: Tue, 07 Jan 2025 20:08:17 GMT  
		Size: 36.5 KB (36542 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:1feb1ffd2b7f95519ffd7b606bc85a8f9623643865f06eecc18f4e6b3987dff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55659999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f3459898da8f2c4e33ae42d8ef42980f5d8805aef2f59bb04ba9337c3c911b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
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
		Last Modified: Tue, 07 Jan 2025 03:27:14 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92f24dac4c35864bb34fdb796c1c0305cd002e2826c5221ed25b6739372756a`  
		Size: 2.0 MB (1984322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba5f636d593cfd45438f6f094461cb8166e5d596a78b05b43dc43368922643a`  
		Last Modified: Wed, 08 Jan 2025 00:29:20 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594d642e9e6b2938fa7335888084d6018376a20857304e4445352c77241314cc`  
		Last Modified: Wed, 08 Jan 2025 00:29:20 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0625a21990577417e06c5f48144ece5214097e76b424429d9c3e3ec5556ca2bb`  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfadc02f013aea5159be691c488d7ed0017a38cfc67c051d66c47a929a90598`  
		Last Modified: Wed, 08 Jan 2025 00:29:21 GMT  
		Size: 20.0 MB (20033220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:07dc7f2ce880761ddf9e7b8ca9b85aa7d5e992dd755061493660ef7965121660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 KB (394987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ebe72ffeffc4b8c3e1980e515a68daa4462ebdd35338b0ee080f01a94e120d`

```dockerfile
```

-	Layers:
	-	`sha256:fb93a6a2d5c2fed04114144567d5011fdc04076f543e857c59bbdd54c637d58d`  
		Size: 358.9 KB (358852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64be339dee08f3ea7f2c02df3deb5f0cc570b880a47ef75b8027d991eb905879`  
		Last Modified: Wed, 08 Jan 2025 00:29:19 GMT  
		Size: 36.1 KB (36135 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:ff5c7e5864aea7091ad2928447bfc4e426d05cfbaeef0362c9e0b31a1af6e3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55746132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e405b1c9d8db2ab9f5b2d78d49a190f6b5f4ec6d63256c4bf77cfa3333a2ed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770cb477b1c68317bfb2860d023b4972e2abdce0461a24b5e3c5d2ff8eadff58`  
		Size: 3.5 MB (3462737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8249e7b9c0ca9f3f0f47f0fd9d16c7a924f96930522c42609a86570d36e0ce7`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91a0f9929fb530faadf31b21d97adcb1eb6d139b4a4d3b93c2e76f0c02b000`  
		Last Modified: Tue, 07 Jan 2025 03:57:03 GMT  
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
		Last Modified: Tue, 07 Jan 2025 05:01:27 GMT  
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
		Last Modified: Tue, 07 Jan 2025 12:04:34 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4664389fad8e5c129a92e180302a5768aede64d686ba106f5f925d777eca19a5`  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef9b06915b60073689f3eb08fa69a4130051db8dfec43544558845c75e52ad3`  
		Last Modified: Tue, 07 Jan 2025 12:04:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af4dc4141f124c1a29d4e6a275fd04ae9a3373add429f7d8ab2a53d0ebfb57`  
		Last Modified: Wed, 08 Jan 2025 00:32:26 GMT  
		Size: 20.0 MB (20033220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:19ca2dca8b689f69afc5037016c45e555afc92c830432dd1f653160c3139ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 KB (390647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d704e1720de5b1df51e9cbd41ad264e0c8a782b806412878794071d3cfa6b`

```dockerfile
```

-	Layers:
	-	`sha256:3335476bf3a7372ad3b5afb4dc03ace043959600d459ee300ded38f5151a45fa`  
		Last Modified: Wed, 08 Jan 2025 00:32:25 GMT  
		Size: 354.3 KB (354279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51117195c2a400c7922bfe81f616726dfb1f6975b495ae67c9294889a3fa85af`  
		Last Modified: Wed, 08 Jan 2025 00:32:24 GMT  
		Size: 36.4 KB (36368 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; riscv64

```console
$ docker pull drupal@sha256:8f3cf9e6da1d3cc540c4f5e31b8fd10f78fcc1d97c181061f401491a5495bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54813465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5c5339465158c2a6b1ad7ed2bec8643efa2b33010e65e09c0552394ea1f63b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
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
	-	`sha256:480f55a34db1d920fdb0fde2a7db7b9921e9c3037a184e705b537b59acbba255`  
		Last Modified: Sat, 21 Dec 2024 04:07:18 GMT  
		Size: 12.5 MB (12545944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ec58601b0f7a00ee0a722ab084eb9dd5ff3a8be49ce3ad70df14cbaab554eb`  
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
	-	`sha256:57f6a000aefb554fcf8c079110c6293bd9550b2e3a29709b1ce9b336e6ca76df`  
		Size: 20.0 MB (20030936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:03f6db6ddf2bca45d1b54525d878db2b5f01472dc9b9e658b2d5019a329462fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 KB (397822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ea17f01aec216917504ae750c4ec5b27cf354dea45706a1f2821b385b2227c`

```dockerfile
```

-	Layers:
	-	`sha256:9f90fee47186178eca7c607c1516b03fd99a660412a7628aa9a5008e590ebc04`  
		Last Modified: Wed, 08 Jan 2025 04:37:48 GMT  
		Size: 361.5 KB (361453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac031ed217d75108db5c0c649b9647a9707fc5fff8d6bb32ec1a8d302e24e96`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 36.4 KB (36369 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:d523bb99f5efc3007dd90bc341369ac7998dd5f24b3737d08bea9250e94f9a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55121746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e34f89c66692ab8c06a86c9df93a71eb9bea877ac137715fa9bf46dc78aaf8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
ENV DRUPAL_VERSION=11.1.1
# Tue, 07 Jan 2025 05:03:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 05:03:34 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 05:03:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 05:03:34 GMT
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
		Last Modified: Tue, 07 Jan 2025 19:27:55 GMT  
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
	-	`sha256:a70f4d04293a85cc1137fa91aa484e20360b105ccb4ade9d780a8c1926633897`  
		Last Modified: Wed, 08 Jan 2025 00:30:55 GMT  
		Size: 20.0 MB (20033122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:7a5c9a878b63e5c9b6b32b07ce57d5b2b7b68fbf3efe52b3dc9ec394d1debf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62144fe9a43347e298dd6f11064e02f5e40f554414a19d85db765fcb9fd8f9e6`

```dockerfile
```

-	Layers:
	-	`sha256:7ddf096a799a5ddcb5f6da0e7b30ca0deae8e255d81c1dd9c5a9601f2b5d2115`  
		Size: 354.2 KB (354173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e0f34155bbe40b819955e33316cbb3613679e7def3f4c3471d79977f5eded35`  
		Last Modified: Wed, 08 Jan 2025 00:30:53 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json
