## `drupal:php8.4-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:c3fe8ee78702cd397312d70608648640e39222dead2e69ac54ee08fe57657c4a
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

### `drupal:php8.4-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:c317ba935fff4a3e67faf9dab14a37aa2ed2c1b283e695c76d0839bad10263f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58947444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2b6ee0840f15ac012b2c2d7105aed634ef1386c7ede8475bea6874c1ecb909`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930bf1c059a1fceee50a025c32f47ebdc2ab68521d1a59a395740ce4a537bbe7`  
		Last Modified: Fri, 14 Feb 2025 19:22:51 GMT  
		Size: 3.3 MB (3313889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf60e095d4a9bdc151d864ae994760e5330a6cca2bd8961f1c3ee5d499d4ece`  
		Last Modified: Fri, 14 Feb 2025 19:22:51 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c010a04eee6f2df5e3a6229a491828219699e08e7fd771bd30a2029063c51bd8`  
		Last Modified: Fri, 14 Feb 2025 19:22:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fdabb59cca7926a16c3431e15529154381bf8f2fed8ea192e6c3500b1f4d6`  
		Last Modified: Fri, 14 Feb 2025 19:22:51 GMT  
		Size: 13.6 MB (13609644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00fa6d1b1ea0491a936fb3542bdbf4e5bae693acc794705f7da9a1c17d47af`  
		Last Modified: Fri, 14 Feb 2025 19:22:52 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ab9cb6d8781f6a28ee539471da99b465e97c40f1e735cfa62f1fe24776d62`  
		Last Modified: Fri, 14 Feb 2025 19:22:52 GMT  
		Size: 15.5 MB (15546064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa07c68b396336e0b4ad336f888d42caa58e2f942b5fcfc41bc3d0a7c701c47b`  
		Last Modified: Fri, 14 Feb 2025 19:22:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722e5693029c54dda9391b8ed7281ee4cc5185701256d28ba78ab231a5c86031`  
		Last Modified: Fri, 14 Feb 2025 19:22:52 GMT  
		Size: 19.7 KB (19704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e83ba3b578c279b84b44945b21d9e4f01119665bf0d71becef2aa8b41cdc9e`  
		Last Modified: Fri, 14 Feb 2025 19:22:53 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f471f0cd03f54e0f3cf2f20666da1a1bc88e0a3ac2ca1e131998928b27a91f9`  
		Last Modified: Thu, 06 Mar 2025 18:24:05 GMT  
		Size: 2.0 MB (2024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43933bcc82f08d1f3e80fded65428d1cf22156199c1bbc29b8886c35864fddd`  
		Last Modified: Thu, 06 Mar 2025 18:24:05 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8bba151fa54ddea12d6569ed6abc7af525b67144ddfd05d422d97201045109`  
		Last Modified: Thu, 06 Mar 2025 18:24:05 GMT  
		Size: 740.8 KB (740818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2918e3b443d525d66d3ff76a75b79aefebf9f8c9af57ae558789e6d07379e0`  
		Last Modified: Thu, 06 Mar 2025 18:24:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8768ac3ba74961f0023749b6b5ee63988d96c018f0000dc51ecd008f7f023011`  
		Last Modified: Thu, 06 Mar 2025 18:24:06 GMT  
		Size: 20.1 MB (20052574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:1467dedbba55f2f9e7958427a18690a87b2359de26ec923f12b11eb0b0808bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 KB (377126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef2cb7ff40b917cb848c0938febff808fdd48458c0089c23dbd61f905626ceb`

```dockerfile
```

-	Layers:
	-	`sha256:eb87b292f0eb4d7f33c787e905b75d4a1fcae56ea3aa8f3b7a61a90af3cc759d`  
		Last Modified: Thu, 06 Mar 2025 18:24:04 GMT  
		Size: 344.7 KB (344747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6742975048fe57ddef59f9c7c4f7fc22f4dd79f5591227b084e0bfbfc115d5c2`  
		Last Modified: Thu, 06 Mar 2025 18:24:04 GMT  
		Size: 32.4 KB (32379 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:1f46bf6b5520f5799ab70e925e86af6807ad9b71c1b28a16694c86ff083af2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56676555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45455fb59991500a0ad2a008d4ada3d2793bf6db98e5f51c99243ea9610209`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:651c28bd7f3e55eeb25f58a0b81aedbcf0c1c1f3a1c256f22019f79050380820`  
		Last Modified: Fri, 14 Feb 2025 20:14:52 GMT  
		Size: 13.6 MB (13609649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f584512e481b9a2cc35da158bfdea06bddc357b8255d94cad43c758ccce5b4`  
		Last Modified: Fri, 14 Feb 2025 20:14:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcfb068573e7930ac7f429c1a84f6febda4853f28f34d907ae46d9a6e86e6c9`  
		Last Modified: Fri, 14 Feb 2025 20:18:30 GMT  
		Size: 14.2 MB (14173528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acab30f05ccf870d6ee1d3bd62ed7f9f884f581d44d22f347d8b6d688c3cda2`  
		Last Modified: Fri, 14 Feb 2025 20:18:30 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ddac9c8212e94033a2c24c8c4308c56453e32e06331a65269da0928df5335`  
		Last Modified: Fri, 14 Feb 2025 20:18:30 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e67ae1345f1ea61bf4ea70dde0da3cb26da1fa3aecce961cddcc60f613996`  
		Last Modified: Fri, 14 Feb 2025 20:18:30 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30469fab4e0f2073a0fbb0a15fe146eb27a6b7543bf50bd756d4d247c2b75449`  
		Last Modified: Sat, 15 Feb 2025 10:50:51 GMT  
		Size: 1.4 MB (1396225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815b2c24f4abc82c265ed864bd3b5e186adc8664efacf0a4cc20e85f3fb4bfde`  
		Last Modified: Sat, 15 Feb 2025 10:50:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d02c7df434e6a51dd532e3a288ca454ddc05c844dfffd730d87b89128d1c5`  
		Last Modified: Mon, 03 Mar 2025 21:16:13 GMT  
		Size: 740.8 KB (740825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5d79ee2c887f437dc79c347fb8a4d6057df0058575b959e6cd8c9765298521`  
		Last Modified: Mon, 03 Mar 2025 21:16:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7500349d10cc12f2f1ba5e2c20467350fec4426f25376097062c96effac5e5be`  
		Last Modified: Thu, 06 Mar 2025 18:23:04 GMT  
		Size: 20.1 MB (20052287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:5abb9021fb5be32777ec609dc304f22f160ac6441713e9f22b0cc97d32770dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57f2f3c0ea7145f8896b6a3fc33625ad3be457c37cd37f1ef31029fc0eab758`

```dockerfile
```

-	Layers:
	-	`sha256:31600cfcd3c36e3724f8295ca572b3ea0e39200b8a06070858873cf0805edf6c`  
		Last Modified: Thu, 06 Mar 2025 18:23:02 GMT  
		Size: 32.3 KB (32289 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:8eb1d2d3d195574f6cc65ffb1a5e08385e22878ebbc2440a77eea54145ea473a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55283062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6e6306516a07265bc8cafebd042b5a162fa6e642c94428c324760503e5379a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:d2081f27c5add62f3abdd10359086d7c7de1fca9aac3bb0cb334b5a0ad175ad5`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 13.6 MB (13609638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2726418c80eb5c4954c50ae3fc9a5992152257e7d79689d82f4e73c8065f30`  
		Last Modified: Fri, 14 Feb 2025 19:57:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435293c58112295134835273f4f10070022d376b79ce1c001f9f3f9bb358db3`  
		Last Modified: Fri, 14 Feb 2025 20:01:16 GMT  
		Size: 13.4 MB (13361098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f237150609f94ca0ea4d817c5238ca044bbe72f10aaf2c436093f7c4843b1d0a`  
		Last Modified: Fri, 14 Feb 2025 20:01:15 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eb663c9a7a02d55de288afd2d34fb42ebeffc4a519e31124d7feee64979112`  
		Last Modified: Fri, 14 Feb 2025 20:01:15 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f0f0f781793a1dabaf0aa8b69657769baa25ab4b900ee2a28c005a5ef73736`  
		Last Modified: Fri, 14 Feb 2025 20:01:16 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2ddb7e5a53130e513df4ba1404792fed3f5694591a15a90bc6e577f128d9c`  
		Last Modified: Sat, 15 Feb 2025 18:12:19 GMT  
		Size: 1.3 MB (1285319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10cbe185bd5e4d6d2805effca2181e14e8cf61bc58afae0408c7edf64e2b643`  
		Last Modified: Mon, 03 Mar 2025 21:24:24 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617acb84d0f59da5e0c2dc8eaada387e3b50003582a3a201031a68bebc130ffc`  
		Last Modified: Mon, 03 Mar 2025 21:24:24 GMT  
		Size: 740.8 KB (740829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04433989cbe8277162a875247b62d1efba38c3b1053b28ef46fb10e5cc37c8`  
		Last Modified: Mon, 03 Mar 2025 21:24:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c3efc32284588e0f1d873626f2ad035638bd2204ab91bfa9f80d40c8718cb`  
		Last Modified: Thu, 06 Mar 2025 18:34:36 GMT  
		Size: 20.1 MB (20052299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:c442f991003265962301398c29a2d9f94720f4a3ddbf37a91f2791b519f8e7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 KB (385724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ab9f28dc638d28c98858e21cc01f7b0400676fe2323be49c89062289a12d78`

```dockerfile
```

-	Layers:
	-	`sha256:263a92aabf4763b92729ecb1ff440b25075e4b088733053db2bdf248df004d92`  
		Last Modified: Thu, 06 Mar 2025 18:34:35 GMT  
		Size: 353.2 KB (353220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bb78666c7f8b281b2988e97ddded84bb80ee0efbd1811e1272739e4ae8cb68`  
		Last Modified: Thu, 06 Mar 2025 18:34:35 GMT  
		Size: 32.5 KB (32504 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7c51374289144dd606a92a1bdec466f6cbfe35899cea4e1a653fa4f138377f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59072862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221e79997c9ec383d7388f6fdd5443256b973ea3a8379f217b420586cfb12f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:04e57e33a629dc74b02e08f74adce2cc444708a41527c8cf367963016d2ad098`  
		Last Modified: Fri, 14 Feb 2025 20:06:52 GMT  
		Size: 13.6 MB (13609637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091c5ef501ce6edf8320ae0654e6065549d0f8252107f6b926b8fc85a4431925`  
		Last Modified: Fri, 14 Feb 2025 20:06:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3c6faab9c8300cebc7d0c0252d14cd213b040f88e521b58230dbdefc3a1b83`  
		Last Modified: Fri, 14 Feb 2025 20:10:31 GMT  
		Size: 15.2 MB (15236917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87588b06132185176d9ffe5992ce3ee7fcfd5123dd4c65a6f04b55c34fb9913`  
		Last Modified: Fri, 14 Feb 2025 20:10:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dcefc8b10528c4938fb52bc52d4f90cb8c2084bcd897fdfac950ecff51daab`  
		Last Modified: Fri, 14 Feb 2025 20:10:30 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb259ef2212bee1386367b3c161e73deed13110a02eaebe5573dcc14ac98bdc1`  
		Last Modified: Fri, 14 Feb 2025 20:10:31 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3487c85c8415c687746f5ab2cca33db1ba2f286eca8f3046a99e6d2438b91df`  
		Last Modified: Mon, 03 Mar 2025 21:22:25 GMT  
		Size: 1.9 MB (1943899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7ba8f3ba2ddf22c1897432e036caed6212f678fd775d950affd17a60ecbe0f`  
		Last Modified: Mon, 03 Mar 2025 21:22:24 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36b5842dd9c00af8dd98a9426638ea82c846348b49788b18a2ade3b3a147eed`  
		Last Modified: Mon, 03 Mar 2025 21:22:24 GMT  
		Size: 740.8 KB (740820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89338f9c01b80e3f2a820f79fd3397c9ac6b05cba9a3c89bb02492b845fb2a66`  
		Last Modified: Mon, 03 Mar 2025 21:22:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db98bcbe83ff78f152e4db4e839d853c4a8915f85991874b8bdf8285a43531e1`  
		Last Modified: Thu, 06 Mar 2025 18:33:12 GMT  
		Size: 20.1 MB (20051998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:524536d3bcac58a0779e16bf2506a35a144f8ebb3a02b9d9afa757582c997263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 KB (385780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc57a3856bf5de06c05b33915dd1249d66600e9bb15e79c64dab5a115f5591b`

```dockerfile
```

-	Layers:
	-	`sha256:4478053226dfaf59fa75a9709b3ba3f13585009dcf328d5ef71f5a340035c5bd`  
		Last Modified: Thu, 06 Mar 2025 18:33:11 GMT  
		Size: 353.2 KB (353240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb1d915efa7349fecc499d3e9a3657fca893e76231e6194d590344822156051`  
		Last Modified: Thu, 06 Mar 2025 18:33:11 GMT  
		Size: 32.5 KB (32540 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:91f81fd185420e470c96f6a9b1e451869ecedde54d72598daea396a223de7b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59349595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6c5a82aabfac8f86aed5feed34647b5d9ac33ae18bd21f0d38560b0c2a4072`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7fbe6b797bad949c1c14c1c2e9934a19f7aad9f3c1e3575704b2d9fcd77f3`  
		Last Modified: Fri, 14 Feb 2025 19:23:51 GMT  
		Size: 3.4 MB (3365465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3539902854c546a0efd5b97350fb7913f91f64db7c33980a7de2a65cc93b30`  
		Last Modified: Fri, 14 Feb 2025 19:23:51 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1c4427557a8e14d0c4bdd1d042a4ad3f8b053b6db6063146c8576305acb7e`  
		Last Modified: Fri, 14 Feb 2025 19:23:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01778b4e7055614831b2ceaef5168b5da5a25bbbef30db8791b1f530dc5e45f0`  
		Last Modified: Fri, 14 Feb 2025 19:23:52 GMT  
		Size: 13.6 MB (13609645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6decc6dcfd76d473f22630637569e41f0a8c1a2e1b9505e6c2db4d96a29e668f`  
		Last Modified: Fri, 14 Feb 2025 19:23:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cdd3803187d37656fed79125611c6bef7a322690e1c2d129c37a4979827022`  
		Last Modified: Fri, 14 Feb 2025 19:23:53 GMT  
		Size: 16.0 MB (15952237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052e4b1eccd9fc63e00dec0b54af0af9c92b01da02e3b0728259d7723599a680`  
		Last Modified: Fri, 14 Feb 2025 19:23:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d518bff58b4727b58df73c24b9cdc42278d8ba10150689bfc850f3a5f2fbde5`  
		Last Modified: Fri, 14 Feb 2025 19:23:53 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b781da87168860ecde70207169501c3858d26c533f6e023142f5bd4ba811188`  
		Last Modified: Fri, 14 Feb 2025 19:23:53 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ea6cafab164c559c4b0bfa8187d65d55bfeb8e8dd2305e09d2e510fe41a35b`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 2.1 MB (2124009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead2d8f1c245d13e1977c819bdf2584923756f9e28f9521a96428d443ec626b`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b69889b1250f07d6715eceeefe36649afc98f2d8da584d5023e11066c0e261`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 740.8 KB (740825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec419fe97b0b4492572710ee8d64f8cfb1f1c5030b15b92f4463852098ec42`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94fa9830680875064cded9e5ab4d11f0be6e098a6abe1e99bdf77e3212ec8e`  
		Last Modified: Thu, 06 Mar 2025 18:24:09 GMT  
		Size: 20.1 MB (20052287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:0af76638fd7d6d4959e40975c97c01c2fad268632aea523ca5b7709dc0520dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 KB (377058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54798acf563e4d659304d0acec7c29fd687b347ce100c9688de00e96e90e2337`

```dockerfile
```

-	Layers:
	-	`sha256:ed327a0b0541a7c7b71a9abdc0908785dd5328f65bce1b0cb737c2dc9e41e09d`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 344.7 KB (344722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26734bd499e827154e4a00cca24365f4f8aafe336d47743dbd5d7ceda5e7e4b5`  
		Last Modified: Thu, 06 Mar 2025 18:24:07 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:bf881680b338cc5a1576bb07a4a1479a4186a17468e477f278cbc1505e6dd5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59197445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e448cacba93172ef004ec721a7bff03ff2f42064e3b63887002a70d9910f5136`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:6e52eff186ab818f0d4e0fec16895ac46b26cbe2317e70559430c7f5817c0de3`  
		Last Modified: Fri, 14 Feb 2025 20:00:10 GMT  
		Size: 13.6 MB (13609653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c5f390cc3031fdb1d2d9ce3afe651033c3b84dedc71b64ec9c403dc1afdded`  
		Last Modified: Fri, 14 Feb 2025 20:00:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62d61d617d593afb263f2dcde44b813b18d441b7dc837aa3ced2afaa09ebd68`  
		Last Modified: Fri, 14 Feb 2025 20:03:44 GMT  
		Size: 16.1 MB (16054215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59a749bba5bc23389225b4d6a499c634a1e5396df347f032c09188c8193c4b`  
		Last Modified: Fri, 14 Feb 2025 20:03:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47162af289f8134757976b0fe09ca5d535a78f5243e928acd3444ba15363191c`  
		Last Modified: Fri, 14 Feb 2025 20:03:44 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fd6eccbe7b4bfaae33db8bb1414b8279bad4cffa40cb83e02433cd883e0b65`  
		Last Modified: Fri, 14 Feb 2025 20:03:44 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ce007ae0574be68045dec2ed294def9fffd51a1e36201bb8f0cf81e3c41b4`  
		Last Modified: Sat, 15 Feb 2025 04:39:52 GMT  
		Size: 1.7 MB (1691088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464382a6fac5556118486416f64471bf4ae788edfa9fe7f49e135852ccab0113`  
		Last Modified: Mon, 03 Mar 2025 21:31:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc21986b73ea1d1033ba2520e8c213f37556172b67c69668e190063787fc5b5`  
		Last Modified: Mon, 03 Mar 2025 21:31:55 GMT  
		Size: 740.8 KB (740830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fa0dea28ff5ae2b4913123894a7bb1bb6cf07d2bb9019547dcee7093e24315`  
		Last Modified: Mon, 03 Mar 2025 21:31:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e7b1ac925e51135006ae9d455c60dd81f574df5f080ba2faa4cdf97943b07b`  
		Last Modified: Thu, 06 Mar 2025 18:36:42 GMT  
		Size: 20.1 MB (20052472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f577cd4bb2238e9a1a270bd1421e48e2f76119c8df719746ea466af2a736f99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.7 KB (383704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3701f82ad19ac4226030c6c65bd3fa080f41cad6d8aeb1bfcc73629c97feba40`

```dockerfile
```

-	Layers:
	-	`sha256:63cf0779c19825e95f3d5e64b26f3af41bd3312afba38ad20cec8209b5878aa6`  
		Last Modified: Thu, 06 Mar 2025 18:36:40 GMT  
		Size: 351.3 KB (351267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4adf7e449593fc041ecf5a6e1b71d55b1c065bc8d03800de901926e54444a244`  
		Last Modified: Thu, 06 Mar 2025 18:36:40 GMT  
		Size: 32.4 KB (32437 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:ea0f99cfcc113e0d33c31027112190be11e84a80da880582969ca752b8fd2979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57753265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807c03b2b685c40bfd017a6d205f1fd3d707c74527718dac0e4850dd31c40780`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:1cc5479694e06d5396dae49cb0a3b946de56bf9968c8f979ed01713a9fa01a0c`  
		Last Modified: Sat, 15 Feb 2025 03:36:14 GMT  
		Size: 13.6 MB (13609652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec4633d9f33632f85cad404366a6fae0c9b7f12b4c5ccece38be99698322fc0`  
		Last Modified: Sat, 15 Feb 2025 03:36:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80898ade42cd78b92ef29d9eb1903630dedfd15ddaeef8e235c08b59c033196`  
		Last Modified: Sat, 15 Feb 2025 04:34:30 GMT  
		Size: 15.0 MB (15012909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ae2621b7459a6cad4b59a74bd0cb560d9886ddc5bd4010d732d236dc82d2c0`  
		Last Modified: Sat, 15 Feb 2025 04:34:28 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f517a64ea8740e17451d49ab38fe5b7cdf673ad8b99ff85b4c0babdc90f89`  
		Last Modified: Sat, 15 Feb 2025 04:34:28 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870cc3b3452a72786690fcd8b7001d5bb1ca202e38a04b2e7d5dbeb0828fc10`  
		Last Modified: Sat, 15 Feb 2025 04:34:28 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6502eb5442f1436bdd9c089db4494804fe04f5a12fb3de12b0d44a28a152ba9e`  
		Last Modified: Tue, 18 Feb 2025 16:30:39 GMT  
		Size: 1.5 MB (1495822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc53f8c44222db1291a91499c229d668e0803936def0b3da07be935fcc4446`  
		Last Modified: Tue, 18 Feb 2025 16:30:39 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dca0914cf9987a7e2c28ad7a7f9c455c6b9eadde35a7a1f182757fb8eedd0f`  
		Last Modified: Mon, 03 Mar 2025 21:43:15 GMT  
		Size: 740.8 KB (740829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a683abc8d6cca256709d4c69a41adf76152f46257a6b3419d2ad5446e1b5cf0c`  
		Last Modified: Mon, 03 Mar 2025 21:43:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb5df38d2dc6e6f1448b34144f84d25b03daa05e49a5ad0346e2dd5f90710c1`  
		Last Modified: Thu, 06 Mar 2025 18:36:24 GMT  
		Size: 20.1 MB (20053918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:01111250e1c9c298f17a06c9e5f7201f787e63803c7365655f12f8341b58ecfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.7 KB (383700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1fca7571e376f62e7b096df3400fbb742a6f70007d3fc43e6f8b540f0f3c10`

```dockerfile
```

-	Layers:
	-	`sha256:6c2a906b7d7246d7b8ef611482f34958dd559665bb21dd4814fa614be01885c4`  
		Last Modified: Thu, 06 Mar 2025 18:36:21 GMT  
		Size: 351.3 KB (351263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0218b936cdbaf3668d1cc9981491e87bce5bd6b65cc57eb967c515f22d6971d`  
		Last Modified: Thu, 06 Mar 2025 18:36:20 GMT  
		Size: 32.4 KB (32437 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:56dec6abf211856e3aa18159e573e304b5fd231d4a8f47ed1c3b9adbae9edec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf7b10179647cef46ebc38a566b4fe3398f2fce108c4a148dc8d00c4d703179`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Feb 2025 21:31:38 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
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
	-	`sha256:dfc9ecb6269793de7fab445c83d411a653ecf7a8e69771bc87ca2088852608f2`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 13.6 MB (13609639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42263cf14380d1dcc937ff4611064b2f903909da294e35d475892063edecfff`  
		Last Modified: Fri, 14 Feb 2025 20:05:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd9f153b12dbf67b7d38e87f0c23b5b19d1745dcec356cfe2a73784a4eb85d`  
		Last Modified: Fri, 14 Feb 2025 20:09:15 GMT  
		Size: 15.7 MB (15740987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740d6327c563948103f2ab226cef9f333f4bd72177de8f7d923e3c7bc1fd80a2`  
		Last Modified: Fri, 14 Feb 2025 20:09:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8eef6b78aad75492ae4707ebc9a6bc1a1fee711087ea1d2fafb74732b9459`  
		Last Modified: Fri, 14 Feb 2025 20:09:15 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adf958d057ff6daf6aa4a8f46db1524e57331de9ef7613d79cbc911d101c9b4`  
		Last Modified: Fri, 14 Feb 2025 20:09:15 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854fd9e30d73ebbebb1b83e0081a9d907f949a4f49967de3a658525fe577acd`  
		Last Modified: Mon, 03 Mar 2025 21:20:25 GMT  
		Size: 1.6 MB (1608392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fe03a3478fce19fe9f7d396c378ad19d2a7dbc31643fd19f9ca0806a45f094`  
		Last Modified: Mon, 03 Mar 2025 21:20:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11559d86c4b05fd7034352489d853ba62741a75bfef39ec6c61800e6bd359abc`  
		Last Modified: Mon, 03 Mar 2025 21:20:25 GMT  
		Size: 740.8 KB (740821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b2bbbfa902141c32ce61db16bfaf1fe7eaebb41a03f2b0f3de265b1d1905`  
		Last Modified: Mon, 03 Mar 2025 21:20:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f58cf7c71afdd4798769323f16d2add6d7933cca284c0aaa269b9da3e0a61`  
		Last Modified: Thu, 06 Mar 2025 18:34:59 GMT  
		Size: 20.1 MB (20051887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:82dccbad3ee4aff0c867ddf730818e03e46b0863fc8a3d1c2ffde12b21f2afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 KB (383613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bb0e7c28db7567e010b46869b92129e9e42a1a70ae312565aee558919fea8c`

```dockerfile
```

-	Layers:
	-	`sha256:6937cd0a0541653f51cfb1fda9fd99a7bfc4fc9010ac61ccc62a78b0d7a34ed0`  
		Last Modified: Thu, 06 Mar 2025 18:34:58 GMT  
		Size: 351.2 KB (351233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e5820d410d0d2130417e238053d82d2ed0050b4ae70a78edd08ffe2a73245c`  
		Last Modified: Thu, 06 Mar 2025 18:34:58 GMT  
		Size: 32.4 KB (32380 bytes)  
		MIME: application/vnd.in-toto+json
