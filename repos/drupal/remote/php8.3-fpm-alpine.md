## `drupal:php8.3-fpm-alpine`

```console
$ docker pull drupal@sha256:5d66b8df176dbc99d9420f869cfb1161fef1c1b4fef753ba553ca03cb11a869c
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

### `drupal:php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:ed80bc7cb0df010ef8063d5e44201ffec3455a6898a8deb84a9ed4248bb69a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56328456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bdd796f52d3e5adb6a75f996b26872c4b6cbec761dba45322b8ca227ae31de`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94070b1555eb9d39ed22e649983becf2bb72fb22585bec7a49df36fe4190e13d`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 12.6 MB (12576238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f137985dae9d6f442dae7a80f57cbc8e5053df43b00bbbd9c15302ce781fa`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb82a003d3c63378e7b84743d024507052e3b2e1996a8e94c844c881b05261b`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 13.3 MB (13261198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03c593a7b00608ea5c8534062562e946bc0a3d159cf20ea6cc8c7dfe01e57e0`  
		Last Modified: Wed, 11 Jun 2025 00:03:27 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896200a5c564e7c88a17f3acd070645c4775fd2e146a8e3bf7e792bf0a3d94`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c93710be8c8a941cb7c19437dc1eef7f885ec0979268aeaf706f3b24f3f415`  
		Last Modified: Wed, 11 Jun 2025 00:03:28 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086393896285e6fd37dfa8e4917aca7620e9bfec803bd4e0215d1e4e809b411`  
		Last Modified: Fri, 20 Jun 2025 22:04:01 GMT  
		Size: 1.9 MB (1928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aa63923daab5a9fe84008b660d5e1e14b3ae8f9f1296b8820f3f2aac0efa06`  
		Last Modified: Fri, 20 Jun 2025 22:04:01 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0f94dedc15b3572e1f6de2d4c9b31832f895e2e8d671054cc2408d1622d325`  
		Last Modified: Fri, 20 Jun 2025 22:04:02 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5ba872a672bd23c9a68031c8b7aaf6edf6cde5de1e9474836df20ae9b0a8e3`  
		Last Modified: Fri, 20 Jun 2025 22:04:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706a577895733dcae5d7f034296dabd0f093937509359ae6a2ae1cf4071aa976`  
		Last Modified: Fri, 20 Jun 2025 22:04:03 GMT  
		Size: 20.5 MB (20510340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:8cf3c7ebb839bd9d63981f5d059c6a51dd5e8f84d215cf30fbf9c663eb2b97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.1 KB (415069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860f71069bf1aa841a854710d0626a73720453a07acc5293148b1b8c1760baa1`

```dockerfile
```

-	Layers:
	-	`sha256:8b5b90d00e707ab53d425aa19ad65bcd8ef8dc690b4ca3d8e04fd4bfa6c15312`  
		Last Modified: Fri, 20 Jun 2025 23:01:06 GMT  
		Size: 381.4 KB (381371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160ba32f3f1d656cc0c070bc081bdd3adc59fe1174d49e0a9a1bd32d3b896a14`  
		Last Modified: Fri, 20 Jun 2025 23:01:07 GMT  
		Size: 33.7 KB (33698 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:d51e30ded0b4bd469a0e3f1c989ce866c7f7322009394664cd8ab6447728e42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54188903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b27ee62fd0c47effb9432a8030f56aabf2bc9bd2226fa8ca19154e0cb51fce8`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:5ac11d5235a67120776936d38667565cbdffd4ac8ea60379c6ae325e45cddd17`  
		Last Modified: Wed, 11 Jun 2025 02:06:38 GMT  
		Size: 12.6 MB (12576215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8ded7ad6d5ef460c0cfba9d881395bd34a516249f00edfa731c433f47ff2d`  
		Last Modified: Wed, 11 Jun 2025 00:26:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd60cc5ec2ae4ca5dcb86d22960561f6f6776b4ca0dbf76427144d196b2b077`  
		Last Modified: Wed, 11 Jun 2025 00:11:23 GMT  
		Size: 12.0 MB (11980215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb0e18ccd8618a7c07d0968e7edaa6e107e56109af4f9a87582b4695ce7a8a`  
		Last Modified: Wed, 11 Jun 2025 00:11:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1050cff899c42eaaa91898e407b579e8652dd0173e41e205bc205c4c96a9aa`  
		Last Modified: Wed, 11 Jun 2025 00:11:22 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c0a9d4320573f99db6862efed00b13c9650e8af1587c3006ad598c0e5f25a7`  
		Last Modified: Wed, 11 Jun 2025 00:11:22 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c364f48e8bcf30b0fb8b6d7cfc84898fb4539e484a4835c8adc6f3b1cf2d312c`  
		Last Modified: Fri, 20 Jun 2025 22:09:35 GMT  
		Size: 1.4 MB (1402184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cca30e9802a50029af643f53a7ed8e91e687ad4bc72523e4a84504580f856f`  
		Last Modified: Fri, 20 Jun 2025 22:09:35 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45878767e60d2f93141fb05023c5fec9bd5643a36df66a7c47a6863f8f26c5`  
		Last Modified: Fri, 20 Jun 2025 22:09:36 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5b7f8b5fd4dd446e18688d6e860fffe7400f83463a23ebd28937c2d65edeb`  
		Last Modified: Fri, 20 Jun 2025 22:09:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a552757537478f0c47608e56784826ba75b4a47e1d1d471fccd7f0340cb05c88`  
		Last Modified: Fri, 20 Jun 2025 22:09:38 GMT  
		Size: 20.5 MB (20510420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:bd2ecc273b22c703514e5797f7a2c9002a4e12917b49925d90d42753e314258d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 KB (33639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a574b23906284bde8b9f87bcabcd84e0a5841aa0ce6a901a40b9377991aa4f5`

```dockerfile
```

-	Layers:
	-	`sha256:859738a85ac489f9c2267bbcbae4c64b37d35bca6c9d9722145843bca7cd267c`  
		Last Modified: Sat, 21 Jun 2025 02:03:03 GMT  
		Size: 33.6 KB (33639 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:25780e5f3216adeb160ec305de814ba12793eee9f78f770ff0e58c6461b2f8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52919546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8c8a3429f799f5c11234025c6f21ddeacfc73430192fbb3b6c10c6825a1b9e`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:0e4283ac42685038a3ed46bf05fa54ab4bfdaa975c17e26e357143c8c0323ea7`  
		Last Modified: Wed, 11 Jun 2025 11:58:48 GMT  
		Size: 12.6 MB (12576225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741687b0c9e57be621e022c7972e29e049714b0076fb944fa8713a06d0bb1bab`  
		Last Modified: Wed, 11 Jun 2025 11:58:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08a3c676bee3ca3ea309b1b4da6db64f4e2308209926dbbd58055cba3c9cbcc`  
		Last Modified: Wed, 11 Jun 2025 14:30:57 GMT  
		Size: 11.3 MB (11284618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4416e852da4c41efcdd6c391639f54029fbcc58339233d239ee6ba226fcf4`  
		Last Modified: Wed, 11 Jun 2025 14:30:56 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1888b69799ae098e199ecdf068e825e5470de6c91593dad7209ca7ce43afdc65`  
		Last Modified: Wed, 11 Jun 2025 14:30:53 GMT  
		Size: 20.0 KB (19985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8604ddc2d70d5a8cac9a2deb8a8953d575f9d49c24f2b6623140c6a9681d966`  
		Last Modified: Wed, 11 Jun 2025 14:30:55 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee840010a17c747cfc2a25aab6fbb2ebd40b35db67562d08bac031921e30b5a1`  
		Last Modified: Fri, 20 Jun 2025 22:21:38 GMT  
		Size: 1.3 MB (1295009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf057ec2e96806c4ec7e6e9690bd6a8f43f01149ccaa29f1edc8559b8dec6bce`  
		Last Modified: Fri, 20 Jun 2025 22:21:38 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ac9a8a5e6e44181a4e8497809a97c3146dd3dec811dc5ba8eb6cc4d40f217c`  
		Last Modified: Fri, 20 Jun 2025 22:21:38 GMT  
		Size: 752.8 KB (752766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60686b4c25a44a26e140c75fb2951612acc0943ecc44bda9b0738c17ddbd840e`  
		Last Modified: Fri, 20 Jun 2025 22:21:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2de72539c2b7e7f5d9175466c55749c88fa46f0f663b15fa66ccea08e90e49`  
		Last Modified: Fri, 20 Jun 2025 22:21:40 GMT  
		Size: 20.5 MB (20510572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:0caed022250b629593755ec10440f24c27f0f17cdeaa03e0707e17a8c72ded5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 KB (412303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9940b83afcef7a912ce2fd0e412efe3f77b04385456ecd7e7c8475418b93fca`

```dockerfile
```

-	Layers:
	-	`sha256:fc576088142dc5f51fe5215da51f7327273e7d3f28dc603c1c0f0ac5b770b813`  
		Last Modified: Sat, 21 Jun 2025 02:03:06 GMT  
		Size: 378.4 KB (378449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1eaaed06d642bc3dbee21097ff0d19340650745c6edd4d5e23244d64bc5087f`  
		Last Modified: Sat, 21 Jun 2025 02:03:07 GMT  
		Size: 33.9 KB (33854 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:f8947a1b2481a6d3715dd1b978097934da1981e4cc383d34c66510e7c84e45ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56919072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b337a73f369e3d1924572baa67e595c4bcf704174404285f8b0c464abc5817`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:7b05602459d95eaaad97b5b9b000a31ad26f0eb610cd660e6c00286ab14e83d6`  
		Last Modified: Wed, 11 Jun 2025 09:24:40 GMT  
		Size: 12.6 MB (12576220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6009a2fef25c68c3e1fe283a09950eaaebf7b5f614e8bb226e39e53cf92d1`  
		Last Modified: Wed, 11 Jun 2025 09:24:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f115d6f00f4bbc4cc814ae5670851a1f02750a06b80561a1ee2185625f162d1`  
		Last Modified: Wed, 11 Jun 2025 09:30:44 GMT  
		Size: 13.2 MB (13247738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc702833cec2a0a6825bca526fd38028f3799551063bd1048096ba9ad7ed67cf`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6580f3bc4f6b18f970b0c9b596701e82571b2c6d73d9aa40230f66dd8d5d4d`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e2521d26864b360fc0ab74e2f1eee99d2266ab700a7983d2fef138d11d4b3`  
		Last Modified: Wed, 11 Jun 2025 09:30:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16191e8dc4e9faeb5300182b40adc8f3cd5f26a35f0edbd934680f16ae18eb`  
		Last Modified: Fri, 20 Jun 2025 22:11:43 GMT  
		Size: 2.2 MB (2191762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502e5acc65f072337c62eece251886c68d703f5c6c3fff3f77f016b9c04fe771`  
		Last Modified: Fri, 20 Jun 2025 22:11:43 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93fadb295c8d73c347fe28d54b9c3cd2aaf265590ea3cc888f02d685d62c81d`  
		Last Modified: Fri, 20 Jun 2025 22:11:43 GMT  
		Size: 752.8 KB (752765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf3d92a3ae063b52277f89291fd900408497ab50d212700cabd3277054a26e5`  
		Last Modified: Fri, 20 Jun 2025 22:11:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add622f363a1a1ed8ecffcce91d8dbd342bc54aed17b050ff438e2950488a06a`  
		Last Modified: Fri, 20 Jun 2025 22:11:48 GMT  
		Size: 20.5 MB (20510247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:27228a804ea8e547c7e1ddea6bea7ccaa1348e29547e6a9e03e90e268a1dbc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.4 KB (412391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d1a829735d9577d51e1874291c091612fae1842d8492c2d8916030ee39d9b`

```dockerfile
```

-	Layers:
	-	`sha256:9054c66b1fbc56cc60ec9449775efe85062e680d8a1fc058e166e6b91a5c37eb`  
		Last Modified: Sat, 21 Jun 2025 02:03:16 GMT  
		Size: 378.5 KB (378485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fcb34a733a6a1ee0747eb6d52da90e7638528df8c8513be5e598add24b86bf4`  
		Last Modified: Sat, 21 Jun 2025 02:03:17 GMT  
		Size: 33.9 KB (33906 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:f53b5896e36b458ffcbc553d927bac3da7b5c6714df27cbff5af810347b73093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56575199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa12a3733a83c47ddcc39f1039b691f0dbc86fec72f56f030e92a3cff8efd97e`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad911242465f6c0cde3d5c906eab3d46a4a5ef9c7959a31a3d1fa6e2c6310b1`  
		Last Modified: Wed, 11 Jun 2025 00:03:49 GMT  
		Size: 3.5 MB (3527771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a9a58e768c9776636ca4a31bfe145f187a1aa794aba4343c2a36d409fbcbf`  
		Last Modified: Wed, 11 Jun 2025 00:03:48 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d40d469b1d335f5f75a3ca1e9009ea157e2d54d9f8f61e936caed41062bfa21`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247f555e5a9a340d6f13b22e0edccaca28f84b48a0731579c4ef1e178998fa81`  
		Last Modified: Wed, 11 Jun 2025 01:12:58 GMT  
		Size: 12.6 MB (12576205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba38f0252f574dd5ecbe60077dfd2d4bb6b4d891de9666188cfc453d01b4f9e5`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8dcd7c62a9397ebd3cdb5f345e9a780ee480007c66f294144644a649cca201`  
		Last Modified: Wed, 11 Jun 2025 01:12:55 GMT  
		Size: 13.6 MB (13568984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9804203e712fd340caffff86c88e0159c4b29e9da61cbead1d4e61bd1c4344`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d14795a33b66d09a16300a068ab99ef988e380bd1b6ca61c3804e9cda5c40`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0709fa6924910761a3c3cfa28ac96d5b7c288b1a728826a48c01351ea1f75c`  
		Last Modified: Wed, 11 Jun 2025 01:12:53 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c85bb4dda04247d4fe1fb87816b6b78f0ffad04cb71dacd95aab52c16000c5`  
		Last Modified: Fri, 20 Jun 2025 22:04:37 GMT  
		Size: 2.0 MB (1988897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497e621a382c2cd27b618d4f3b1e11446d67b75f20abb7af95f504e7c53d6d1`  
		Last Modified: Fri, 20 Jun 2025 23:26:29 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5f44f96a2d143ba45c5afc4e980cf0693e6d7c92bee746e135f8768dcc718`  
		Last Modified: Fri, 20 Jun 2025 23:26:30 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbdeb69942a7c4a633e1d7c8bdc085994dbd10650a6d76e6871a61b66fa8501`  
		Last Modified: Fri, 20 Jun 2025 23:26:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d37ccbde73febe0484208257fc8ef12d768cb6727a3de19c3267d0de3e3c67`  
		Last Modified: Fri, 20 Jun 2025 22:04:38 GMT  
		Size: 20.5 MB (20510654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:041a7419e8ee4a8a70fa44f52595a7d3a0cedb0f038dff1214c177986b5f9651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 KB (414961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3de3091e6a34736bb7191b9a63e065c50caf20dbf26066af70a09eebc9d7a3`

```dockerfile
```

-	Layers:
	-	`sha256:990433143a7909a377f0b87e42d536ad61a217279d872e9b4b6fe4261fb57bcc`  
		Last Modified: Fri, 20 Jun 2025 23:01:20 GMT  
		Size: 381.3 KB (381326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4549c3a47db29d6ab72b1b50dcf012233847a391d36e9085f9e472440b2553`  
		Last Modified: Fri, 20 Jun 2025 23:01:21 GMT  
		Size: 33.6 KB (33635 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:4a5198a677a3dfbaf5b5685aaddc1d63bf886cf1bb7d5c7fa564741b7c1b4815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56650543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e578a4a3196d9858934e3c975e496dd0f3a38c9455a3ab7b859d7c2786afb0e9`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:6e98527d27dfe373bb05fe4a32feae4e983c3ea61c6e75a47cd18dbaa9f06e4c`  
		Last Modified: Wed, 11 Jun 2025 09:28:04 GMT  
		Size: 12.6 MB (12576214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb3390ac49f9efbf6d20912051491cbccf67620aecd18d32594e6dd87b74ba`  
		Last Modified: Wed, 11 Jun 2025 09:28:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e6a25b6101b313fa34875b028b172cad9c9680cee80e292f115adba7417cee`  
		Last Modified: Wed, 11 Jun 2025 09:33:22 GMT  
		Size: 13.7 MB (13731670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fe4afc2b18dee11686be563ce289d666303ac2ef846948fecd695bafb4e813`  
		Last Modified: Wed, 11 Jun 2025 09:33:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b543d2869a32f83c6fb938daf392dfd4df558264decfb7bf19f32c754301f3`  
		Last Modified: Wed, 11 Jun 2025 09:33:18 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2cb99f9caafa35970bee68bb6e56af35e3687bf7d9e6a59a802258a0d7675`  
		Last Modified: Wed, 11 Jun 2025 09:33:19 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4dd1bd694bc40eee4abe8d58106c989b1446c3f6998d99a58b79dfa5586f62`  
		Last Modified: Fri, 20 Jun 2025 22:16:31 GMT  
		Size: 1.7 MB (1696207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7eadc30855dd54877592fb7ec836cd6d89f352e1a09f6fc885b4c1077f7e98`  
		Last Modified: Fri, 20 Jun 2025 22:16:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ce45eec517b2ab33a4efdd8ee83dd03eee57e51390ce8a1fb67aac5bd70ad`  
		Last Modified: Fri, 20 Jun 2025 22:16:31 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d320a8cf07a46b57e6ff796f316d6600517117ae64d40c2e61f0006e05315`  
		Last Modified: Fri, 20 Jun 2025 22:16:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a01dabfd9a855239d5d324a17534a9f52c14f95590677b4c7bd7e79407f8b9`  
		Last Modified: Fri, 20 Jun 2025 22:16:34 GMT  
		Size: 20.5 MB (20510616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:51b7e4eb6fd385c9db56504f7578b8e2d96eca75a1b5e4ee543bfadc1126a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 KB (410268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612389e48fd618288d90026b8cf0a6f810b0bd589c8ff68034dfe71eaf017932`

```dockerfile
```

-	Layers:
	-	`sha256:3124e8929d80f19758961944d7d73d48a9d1b5a5dd1024f7e37e98706bdef11a`  
		Last Modified: Sat, 21 Jun 2025 02:03:27 GMT  
		Size: 376.5 KB (376488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf4e254c75822cc04e50b993b880df6158feed448105288984bfbf4f35de8a9`  
		Last Modified: Sat, 21 Jun 2025 02:03:28 GMT  
		Size: 33.8 KB (33780 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:0b206c99f15927aad4e7befc87295c89a90e95d370435da8510321b20bbdf55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55232095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5a01810d0e390b74a4bfe4e66091049bdc407898802c7a1bbd85ef7bf36e06`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:27b5cafa4d9818b0979221ee32a634774fa7f630af34e28dcd203e49994f474f`  
		Last Modified: Wed, 11 Jun 2025 08:15:56 GMT  
		Size: 12.6 MB (12576232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27333500b47fd459f2d6ae7fe8c9965e6a2e171e3413cd3721da70944d32400f`  
		Last Modified: Wed, 11 Jun 2025 05:27:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94ea32cb34db450a708bccf88f34888f12a69e81197c5e562becd545f55c0e`  
		Last Modified: Wed, 11 Jun 2025 08:16:04 GMT  
		Size: 12.8 MB (12758742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba1091c9bd27a689d500d464782b521cfe4d3ba3773b31deaa918405bf00360`  
		Last Modified: Wed, 11 Jun 2025 06:22:26 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ac07f2e6ef175326e50c1bd2cf85379e771e86f4a328b5c55b1aea2a599461`  
		Last Modified: Wed, 11 Jun 2025 06:32:48 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c55ca73095fdaa794aecbd4c3aebff6b42c5244d706c4e6738e71ae615d03af`  
		Last Modified: Wed, 11 Jun 2025 06:32:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecef710e0ddc1ffaa9849f8f36e3940be10fbddaa19b5600597b8741945237c`  
		Last Modified: Sat, 21 Jun 2025 06:49:29 GMT  
		Size: 1.5 MB (1482410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d4094b244719037de63eb0220918fe54163e666e1cd6a4684d0269fc4c6205`  
		Last Modified: Sat, 21 Jun 2025 06:49:29 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20fa0aa444db000b04ecf24a1aefaccd48bc9bf3c909f9f8bf9359c1f6a32fc`  
		Last Modified: Sat, 21 Jun 2025 06:49:29 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a49134a9d393a19985daa108570b6b87a89fdc63b84757c20c4c6c64e0b54a`  
		Last Modified: Sat, 21 Jun 2025 06:49:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b0182a5180428435652fa819cf385a5aba73f3202001686fd9748f6426a685`  
		Last Modified: Sat, 21 Jun 2025 06:49:31 GMT  
		Size: 20.5 MB (20511049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:9a79cf39f6ff6598e21ec4826447fc9c09c09274f60717822dbf3d9b66396580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 KB (410264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e455c1fc52853a4586bb3f4f3dd8de400b20282ce2ebec192544b3f3b3e5d2`

```dockerfile
```

-	Layers:
	-	`sha256:e3c0025ed863310c4c936f5f3d4940f5424573362037a7d7b63a59f62a93b725`  
		Last Modified: Sat, 21 Jun 2025 07:56:42 GMT  
		Size: 376.5 KB (376484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c22aa0f4b478d136b7d6d525ccf69ff387a681f4e5f75540002e9f7b569881`  
		Last Modified: Sat, 21 Jun 2025 07:56:43 GMT  
		Size: 33.8 KB (33780 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:14a466c229c7b9cdb4c99de40d8bfbb419936c827f5ff3ed8626c982d21704f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56048107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6afb946e61902fabd3636668deda268b85b3d793cb7ead23d3e8f1281d6d9b`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_VERSION=8.3.22
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Mon, 09 Jun 2025 21:43:33 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
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
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
ENV DRUPAL_VERSION=11.2.0
# Fri, 20 Jun 2025 18:38:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 20 Jun 2025 18:38:37 GMT
WORKDIR /opt/drupal
# Fri, 20 Jun 2025 18:38:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 20 Jun 2025 18:38:37 GMT
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
	-	`sha256:f9334ce794586a4a7b7438e664ddb5b86e3cce1e0a2fbc690532ce8b60488510`  
		Last Modified: Wed, 11 Jun 2025 08:16:40 GMT  
		Size: 12.6 MB (12576237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b5f7350b3a92e0711dac2da50783a7725cd1b40cd633e7547d23d902a052cd`  
		Last Modified: Wed, 11 Jun 2025 06:28:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06397ddb79c96539ad6e6e015a2347219e602ac265e8c83e456493f63b715bce`  
		Last Modified: Wed, 11 Jun 2025 08:16:50 GMT  
		Size: 13.2 MB (13209660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2df9cd85e7507e6e36c9fa149c62836bd4b44b04ce7b6e06f9a693162ab357`  
		Last Modified: Wed, 11 Jun 2025 06:31:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c988da2e76568a30f08e12cd28d8d8d543c44ca483fa49f5c95e8701f8b897fb`  
		Last Modified: Wed, 11 Jun 2025 08:16:57 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6af9f1c9f1c764ed8d022da83252658376c197bd19dc5d80b780570bc4dc7b`  
		Last Modified: Wed, 11 Jun 2025 08:17:02 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac67db8e47e9d296c907732c3989a5c5696465febc17c39bb76842605e50b54`  
		Last Modified: Fri, 20 Jun 2025 22:13:37 GMT  
		Size: 1.6 MB (1618901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cba998bd266ca0b23687da68197f49a17f7228afa74e74eb04cc8c686e18b5a`  
		Last Modified: Fri, 20 Jun 2025 22:13:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da58f0cb0c7bf078f8c0dd362ded03fb641c3ee94cdd666fdcda57d75711092c`  
		Last Modified: Fri, 20 Jun 2025 22:13:37 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af5a5607d2177af28505adfa55c268be053f3e41b7291e912d28f33912b7a1`  
		Last Modified: Fri, 20 Jun 2025 22:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf27f79629567f1a3710981bb2229136c3bbd5823b1681028450da34d38a897`  
		Last Modified: Fri, 20 Jun 2025 22:13:38 GMT  
		Size: 20.5 MB (20510285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:604cea95073688a95c77f54c5eeb1bd5c20beb60812d68008ea538f9b1c1ad66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 KB (410126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7184727812c161e0c58564ff4fbf88a53219f30631fe68f6d22d6951682e52`

```dockerfile
```

-	Layers:
	-	`sha256:f06fc67f5a817c16d3dea8eea5ff151ef9e89b5b57d456bc4dc527a25e1aded3`  
		Last Modified: Sat, 21 Jun 2025 02:03:40 GMT  
		Size: 376.4 KB (376430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a784850e41a33dde1762995fcfc0e879b53034a1cd5f8a62ec3dc8ffa51a2da`  
		Last Modified: Sat, 21 Jun 2025 02:03:40 GMT  
		Size: 33.7 KB (33696 bytes)  
		MIME: application/vnd.in-toto+json
