## `drupal:php8.3-fpm-alpine`

```console
$ docker pull drupal@sha256:24029c66eef94e6afaf38a603fbfdcb2b9fc47368e39c8e606cbc735b23a582e
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
$ docker pull drupal@sha256:251bf3fd822ac3d69091ffcc1a85536cc0bdf07983f712cbc50d0fd078961765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58850687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da38caa98b4cd6b09b9f35ffd4f356dfa2976e4db07ad19842bafdedf281ec88`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef952cbf360f9accebc7c2beaa1888046fd2decdb103e9cb37ca7fe8901e8448`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 5.9 MB (5944405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb247df7bed499a5b20b7a8f5275f005942ae29ff269444f08485852b0a82ba`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896673d396d677374e76584f6148d05009f4bf9cb800ff16ece4e2b1cf7f785`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b045c0c09a16557279905f885315501ebc707dad24429e3f76c4ba889eaea8`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 12.6 MB (12599155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c8125335db3c68c8f6abc01bbf84258e57476bb185eff879d4c1a3466b8eb`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d7dbac9207c1e11b7b23ce6aad0740e3ba427719588e966776cc44421a861`  
		Last Modified: Thu, 03 Jul 2025 23:05:44 GMT  
		Size: 13.3 MB (13261724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac6221624b83e2f407497538d9cda65f3c6bb6028088b26532eb138997df78`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80922a9956d152b4e0a3bc8fd473151f805337d5823f8bd37b68e79cdb206f7e`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26906d4e70978b9475681f326ed2a302b23ae885e81ae8770bb41a1c51135f3c`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4226ad16511c854708eeb106b22f950a04e5db658db5aee0703cfdc687c5a9dd`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7333e182cfc2588050ca9d9901b1354a3e188513038cebb780e8d38ab1b2d4c`  
		Last Modified: Fri, 04 Jul 2025 00:13:11 GMT  
		Size: 1.9 MB (1928760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e80609e7401ea9e8166ec0b27bd1dbcdbea9c6d4281e08206577517ccacce1`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa6d1cab31f7e504f5df1b5a23f8eed0c7c8cc06bf137fc2bfd022419329372`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 752.8 KB (752757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2affafc7dda64402ee538d30a88943d162a88315431cdf5ec8d16faa14780d`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51d2d70288ce347f3415f88b2ec9528ebf335a372be3ef6ad560bc2c6ce3fa7`  
		Last Modified: Fri, 04 Jul 2025 00:13:12 GMT  
		Size: 20.5 MB (20512917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:19b0cd4b74b53e4944065a2159f8d32f930976479844dfb6e1f69d9c67aefd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 KB (416161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89708d49b69298923c7f0511246a5ccb6c230b5ccffaf806ebc4b0ee6918947`

```dockerfile
```

-	Layers:
	-	`sha256:beb70b70760bce144b25e5ae17841417f4a7f607113680c16c6484eb553b361f`  
		Last Modified: Fri, 04 Jul 2025 02:03:26 GMT  
		Size: 381.4 KB (381371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:803faa5a21fb5d7ba8e62b604935fa3e972049500676a83c5323609b0cd685de`  
		Last Modified: Fri, 04 Jul 2025 02:03:27 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:7b06b6382a1a7ec18dcd79d4d60cb82437683dcb727dd90523fcb22655d3babf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fed1e0a44dfd7a71ec18d3ce1ede20276e127a535a37eb2a9282f5ed4ad759`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
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
	-	`sha256:6146672ba2c374cbf86842c858594d7c0b44ab2080ad5e2ec35b1d430d956546`  
		Last Modified: Thu, 03 Jul 2025 23:34:21 GMT  
		Size: 12.6 MB (12599121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb5f1af16a6958fa9af152ac28632aff56dd315585de1020a729fb999c3dee`  
		Last Modified: Thu, 03 Jul 2025 23:34:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d236cf740ccc769ceb4ead8aa9d45e86ed16335a52d930c4fe0a9c0557f9f`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 15.1 MB (15107434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14679d7fe0b4602f2402b4899b623f618df96d2ba33280d5cf4a4afc825bb7`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7a906289e5476e4a4fbca6e72f2a28c1274a886810de274c3d9d075537bdba`  
		Last Modified: Thu, 03 Jul 2025 23:39:43 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab072a5208326c03096cd254e9205b7fd25f2fe20d9e8723ba9f85b55faab72`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a3d59f66b3f5f865439aa342092b634c80b67cc2b0976838e9806ffba9bd8`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ec4bf2b4e9fab4b71dc16e339f4c453d8403b55a553c761fa4b4bdcd9f33d`  
		Last Modified: Fri, 04 Jul 2025 02:17:29 GMT  
		Size: 1.4 MB (1402135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16caba9cccfb336602e96af6cf581cd01eecbfa1aa62e840a8864b1f00fbe534`  
		Last Modified: Fri, 04 Jul 2025 02:17:28 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ffbda8fdab80f0787bb5053a08493c5dbce33ceba4c20c407d410c7efb5afa`  
		Last Modified: Fri, 04 Jul 2025 02:17:29 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61b1b966ff20ee48eff7b9419e169e35e13268f69f4fd10e3238147508b035`  
		Last Modified: Fri, 04 Jul 2025 02:17:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c0c42d611091acd072e3bd33c54a856483a931010ff334262d2c923ff4e938`  
		Last Modified: Fri, 04 Jul 2025 02:17:30 GMT  
		Size: 20.5 MB (20514520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:09468ea0f0c1fb620c5ddbe8abcd249c344facdcb278008e89a8f95fb4373279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85924b692a20abac931e8a2a73fc65abd631fb7700644bedb53ca9edfee159`

```dockerfile
```

-	Layers:
	-	`sha256:0c63e1d7b1129d5620414023b4a3ce6bfe333b2eb54bd14862dfd159885131cd`  
		Last Modified: Fri, 04 Jul 2025 04:57:32 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:578ce0e1083bb4fd4390e59e890461ff18e735491fb19eddbbd92728a0a42bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55864300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2cff56456f5c64ddef800796540b18acc60839c7a422cc04dea896dacc6f45`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
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
	-	`sha256:c10b98e00e904012800430f69cf8aa74332ce1ebba99fec9635378d4af95147c`  
		Last Modified: Fri, 04 Jul 2025 00:56:41 GMT  
		Size: 12.6 MB (12599135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f60ea7cbd06e3b78423de30e2481ff24a10dc4900a14d875723aad2768ad1`  
		Last Modified: Fri, 04 Jul 2025 00:56:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb773ed9018828b3805869de0c29dadb3d8afe8bbeb5822a9bff92c509f1546`  
		Last Modified: Fri, 04 Jul 2025 01:00:37 GMT  
		Size: 14.2 MB (14183204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190e2dc48065b7d79d07964079aaae471c5266f4ff8a5b4a74844f8c4ab4873`  
		Last Modified: Fri, 04 Jul 2025 01:00:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d95fcde3e122763b3e8cf8c659f3cd57854c41b3dcfa893ff0c0154ae3cc7`  
		Last Modified: Fri, 04 Jul 2025 01:00:35 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb02f2dc6fc67eb54948f0631c60eb801811b049464f631461da3fe4d7b8b0`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ae500fa45bd59acbd59702482718a33f1d4d98384e11ef6d394ccf019f51a`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2c879ebd63e6423d893ddff2c40cb5dd242a2476a2b8c0462138cddb8d547`  
		Last Modified: Fri, 04 Jul 2025 05:36:04 GMT  
		Size: 1.3 MB (1294989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ec91e768a107e2628affe82a23d71c87a05fb744193268c63a43de8767f2d`  
		Last Modified: Fri, 04 Jul 2025 05:36:04 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08379265c38a0e3bee7f6b522219a1ffe878f4d8a51e80862e48ea811a3678f6`  
		Last Modified: Fri, 04 Jul 2025 05:36:04 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc96dbc4ef9dee6615f9a1d1b0532d87f793d49d2c7c4032de912e3a66b7fd32`  
		Last Modified: Fri, 04 Jul 2025 05:36:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebc4b7eb0d0ab6d4deef4ddebeb4abcec4229d0af11c6132dba34000b89c04b`  
		Last Modified: Fri, 04 Jul 2025 05:36:07 GMT  
		Size: 20.5 MB (20513834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:4a9e7c1a99bd86bad18573049939274e0dd7f8deabb134c5fd3220782418dfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.4 KB (413395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb9a37ad4dd5055995ae6ef1e53fc76ad14173131888d61d6faefedc049d7c6`

```dockerfile
```

-	Layers:
	-	`sha256:4731bf72530a453623161665bb6071e793c439ec58ece896883a300c83378829`  
		Last Modified: Fri, 04 Jul 2025 08:02:41 GMT  
		Size: 378.4 KB (378449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe81271f4f0d111feaa5400a9971773dd290e33bd3bc1d0559d6b329a23b9bb`  
		Last Modified: Fri, 04 Jul 2025 08:02:42 GMT  
		Size: 34.9 KB (34946 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:a8a2ed180fd9fa8532bb558ebe01601fa7359333fe75b3666d3c325b5a6b49d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59727914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3843b85900c7ccbcbdb5980aeb80c4916c130cd9b87711697e5f0fb5ffffc01f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c1dc6ad948ff6b6024c13aeb8e1504ab7c78c613d2c0c92070d4d25d125ea3`  
		Last Modified: Fri, 04 Jul 2025 00:22:31 GMT  
		Size: 12.6 MB (12599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f819ea982f77ab1a8ba8076019600ba3f9145ff91f7458fb0dcf5614950956`  
		Last Modified: Fri, 04 Jul 2025 00:22:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37d5631afd1425fe5eb2c8e749a3c65200e29d24c36d318080ca48b2cd90c53`  
		Last Modified: Fri, 04 Jul 2025 00:27:41 GMT  
		Size: 13.2 MB (13248864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934bc624a617ff8f7747e6413a288c2e89d5b658c0f017d2ea39ba3f3c409a0`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba469df90540c13439c3903a06bc064d1b88891a0ac0890503f07e7e9392d5be`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d902dfe696ab15d26a6522405d9b7fd7cc42fd2a15a790f9700e3a1b3344207`  
		Last Modified: Fri, 04 Jul 2025 00:27:40 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b378ed1259e9def290ea50e62e695383be8cb81433a8155ef802d3ebf414`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e340bd296ce8fb456572f6569ea109f9c773ba749385bf6e6604bc5aa06487`  
		Last Modified: Fri, 04 Jul 2025 08:38:17 GMT  
		Size: 2.2 MB (2191760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10801bff3a8a329a54a93533b53ab12988e46d62829d3f41783a6702c40b90c`  
		Last Modified: Fri, 04 Jul 2025 08:38:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b02961c16acb7ba9dc048ff5b6ffa7115cc058e69f779cafcb5deceed12e7c7`  
		Last Modified: Fri, 04 Jul 2025 08:38:16 GMT  
		Size: 752.8 KB (752764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db96df81e7ae9858b1b6e3f9a3b6e0fef44d49e3e4c252355f80260116f7a8a5`  
		Last Modified: Fri, 04 Jul 2025 08:38:16 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc79bf9637845894915cb883a41a5774cd0035dda7fafc9515d040f07af93a65`  
		Last Modified: Fri, 04 Jul 2025 08:38:19 GMT  
		Size: 20.5 MB (20513812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:8b599e2d1c24cfa08849095c100faa6b0c994962ff1e4c71d081726309252b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.5 KB (413483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201df1f95973525364bce5171c03487e081462cdfcf5280fd67ec8663bffef7`

```dockerfile
```

-	Layers:
	-	`sha256:37e1706a2c971d8b61bb5e5ffd156b3ead78d38c4463754c7bf54658ac926610`  
		Last Modified: Fri, 04 Jul 2025 11:02:22 GMT  
		Size: 378.5 KB (378485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29d5dc72deb8f3124d05d993bfcbd73fdaa653ae4e04e4a6c414a3f42a3eae3`  
		Last Modified: Fri, 04 Jul 2025 11:02:23 GMT  
		Size: 35.0 KB (34998 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:85b97af617cca58fa036f5bf30cffa0abe66d5ca9858f4fc09b877b8e3293e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58903092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cfe9d8af9764089875cbb110f5d817133a4e3fb0d176aecd52e9ea71c724cc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807332f552a5d43d50bf321942aaff6f62a51ea718c4bc5c92889c7da5518cc`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5952ed3b34bc2bb95e5d92041b0d1e2f1102370e20445fde4e6ae170753fd54f`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26cd4edff9c58bc8c1207c850646d9dfdfc9668c692e2b02ccedbcd463e458`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b172088b57748f502c5aa1cb684e21421b0497fea01813cd1a37fc90acd2`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 12.6 MB (12599126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0cd325f2b5b783c7b8a674f750116f3312bd602ddc978c5b9f679705430ed`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a1d58746e581f9623e1af350bf3217a46d1bf2421a049c667ce7611ed9234`  
		Last Modified: Thu, 03 Jul 2025 23:05:47 GMT  
		Size: 13.6 MB (13572591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86069b8c031ffbd54f99dcbf2ae53e9e0957fc9842ceeaa4a5c8036b2f82643`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef072b2e721a30c9933cc7e4efd20c954bbd7be2cf4635995276b751a09425`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b7b0119a26af8eff640f542e3e4ca243bddb6c7bffcb62f9018e53e27a28d`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bce8958e293647dbc8485a223c57de84e18b7d627799a89f7217e466b8dc86`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076a4c83bbddb668688ccc714ea256d1e208ffc2ba2536157f9d40a43be03a8c`  
		Last Modified: Fri, 04 Jul 2025 00:13:08 GMT  
		Size: 2.0 MB (1988894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3518241ae91cc9ce555838ef6a25423d978bed8db7436f3ac01caf3c53fc019e`  
		Last Modified: Fri, 04 Jul 2025 00:13:08 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f1a6c9656c1adca51d07392b7e42e830a232984e71c80f44e7a64e44cc9a47`  
		Last Modified: Fri, 04 Jul 2025 00:13:08 GMT  
		Size: 752.8 KB (752766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d346fe93dffecc437f6f550fd9a9661de6fa33721ab28806950bca292648f`  
		Last Modified: Fri, 04 Jul 2025 00:13:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63704190e6d1a28a5f3a11e2ad9a60a1b83f3a98e85762dd434bdb98afe9d3`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 20.5 MB (20512610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:999c92ac321fcf66ffa414f5c128cda5fdfe834b68d45b4ec1ba97805bd41313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.1 KB (416053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6531c1159f5fb033aae180cc1277316de5d469d60a9b27388f2a0777a332f15`

```dockerfile
```

-	Layers:
	-	`sha256:de4b51f53d28b014dc64e4ca1483374888aeb6cacb40101cf0ff9cff9f18dc18`  
		Last Modified: Fri, 04 Jul 2025 02:03:42 GMT  
		Size: 381.3 KB (381326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:491016ec023d8546aa92f4d9789f2ebc63163d3f72e89b68fb80e53a913dd92d`  
		Last Modified: Fri, 04 Jul 2025 02:03:43 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:4e7ba737697bf041a5cc7cc74da1a6c0c7e279108f843c243f7d483d82ab4631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59025422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a08989d0676a0b22d707d73512d4883ce8ed3f675cf7cd0a1b8d047da6bce1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daa18a322ff81fffc7ceb1c57d422d1adf54055433564c7dc442f903760a8f1`  
		Last Modified: Thu, 03 Jul 2025 23:54:52 GMT  
		Size: 12.6 MB (12599136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3f6203202b10d68495a456bb29733beccaa33785d2412fb041f620278679d`  
		Last Modified: Thu, 03 Jul 2025 23:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e866d6eb8c3a035680c0d3efabfbca205989bcd4bee91b8a71c55a705ce9184`  
		Last Modified: Thu, 03 Jul 2025 23:58:30 GMT  
		Size: 13.7 MB (13732933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531b83a89125d0ee7a5f425580e0142fe836b2078ec7b9b0a04717c2d8c675b6`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316ae9dff514804b8e62c75c316fc9f7a2a98cdcf43b08a879887c8865e8d2`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068cb2008a5c83784fe82cf109b583e810ad10f6cf9461dba75b4bc3693fdfd`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3a1077df05c4646ceddd1e7ac63a985083bf3e92537bbb928a3367fb9045a`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e39edebed912723bb7950dfd3d3d5da55ec06fe00f8a567eb8ba1330232639`  
		Last Modified: Fri, 04 Jul 2025 07:03:48 GMT  
		Size: 1.7 MB (1696204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05ef023be33734626ff20dd5acfdef09ebd29285b62d770b5743607eefc42a`  
		Last Modified: Fri, 04 Jul 2025 07:03:48 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cabdc5142d7885096d697dd52e6a05c35183458b0a939fe3d1d09fd7c731c5a`  
		Last Modified: Fri, 04 Jul 2025 07:03:48 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d83664e84a95258371c7d3d36610602e743c9692a3359367cc2c5f5e66be8`  
		Last Modified: Fri, 04 Jul 2025 07:03:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8901a7ff36a27358ade56dfa4fb0d31cb49a81944e513f3aa04028616fb90d4`  
		Last Modified: Fri, 04 Jul 2025 07:03:49 GMT  
		Size: 20.5 MB (20513528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:90a9419fb3557946a7278dc533ed1e36e9e00edc9496bb03e9d96f275a16fd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 KB (411360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d27ff30c8258c3b7b8a307be9cd4951a4130ef0216ea130bb0273e81b88b59`

```dockerfile
```

-	Layers:
	-	`sha256:67d56a3a45d0b427cd91457ddd2c145740b834d448f4a7630151b617631203e7`  
		Last Modified: Fri, 04 Jul 2025 08:02:49 GMT  
		Size: 376.5 KB (376488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce3d05cb36338cf4fead6be81d95014d232b183cb622576ac6295178ff00c82`  
		Last Modified: Fri, 04 Jul 2025 08:02:50 GMT  
		Size: 34.9 KB (34872 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:3d2dafdabe283f879c5034503a82ce3546508b00182a9508d28e5447cf57bcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55256172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0a8df52fa5b468bc59f4215cb7f24f067cca4702bc8d6941c9e7902324386f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
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
	-	`sha256:01a5d92b246a6d60b990cacf09bb2fcc12451ac7c1b17f7396ba16c682667c7f`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91e11dba2e3d8f6f7071f2936da54d2416010d1a7ee5417246d3253bf6623e1`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8195a02efbcbc128ec081a88ee47bec8eef940c0795b5cbc4df768899a7937`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a159d59982da6923f201118958fe2300484b8b87fc234f3931bd53e5ada97eb`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ece48f855cb7df61774667a79b0d041719ad4fa2591e332164c433268fdde9`  
		Last Modified: Thu, 26 Jun 2025 14:35:24 GMT  
		Size: 1.5 MB (1482393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba47c112ae6e351bc2e1b54570ffb73aff9d2ccd129cb95dffebd29d22a1897`  
		Last Modified: Thu, 26 Jun 2025 14:35:23 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5617fcc9523b5e2918cd0df1ce9d0e21461fde0756bdeb01ffc1a6aa5c46bb`  
		Last Modified: Thu, 26 Jun 2025 14:35:24 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223b55671bd0c0db085bb55209522c0e34654d5a00cd2243d75b4b3289f83ae`  
		Last Modified: Thu, 26 Jun 2025 14:35:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c990ace7d39af29de8767de031848cd351b3f6070477805b305de3bcecee4f86`  
		Last Modified: Fri, 27 Jun 2025 00:09:41 GMT  
		Size: 20.5 MB (20515128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:c81e5866c14525dc87c63a9ec89c1d7d5fb389609520445cbf11d2cb50625cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 KB (411356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d1887aaef70b741e7a4d68eb3ad7b706f98f54ee524afeec44382e49f753d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9be9850072615b21b11f6fb679b2b4517ef3f7cac99f4e77bdde81c343e020f`  
		Last Modified: Thu, 26 Jun 2025 23:06:07 GMT  
		Size: 376.5 KB (376484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9771166024a36d712ae12e933344c577fd6732655ce4e92937e2d01bde9bd811`  
		Last Modified: Thu, 26 Jun 2025 23:06:08 GMT  
		Size: 34.9 KB (34872 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:aecdb5cc3f85b36766c3a46c6b664679b41decea8ed7bc8d9f2264a4f978d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58329315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b791cb49af9dda97036fa8bb6c7fe383e1cbda9a9bf9bd268c51d03e102b59e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416dc488e82ac5d95b592019f37aa9b64fdb6535ead41862f2acaa1677ad8e8e`  
		Last Modified: Thu, 03 Jul 2025 23:57:30 GMT  
		Size: 12.6 MB (12599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ba56106dd7084cdbb4d9ab2d30f1b097ce958de942d3197fc708ee1f3e636a`  
		Last Modified: Thu, 03 Jul 2025 23:57:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25d63e1e4d6962369161cd89600b93f34b435063aad41926a421597342eb6e9`  
		Last Modified: Fri, 04 Jul 2025 00:01:25 GMT  
		Size: 13.2 MB (13210606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56deef95c718f1fbe14547d0fcd0e8682120447b39ddcddabbcf51078ea78e27`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4071eca4de4ffe44b642f2d9e429cfb38ffed2ba8f05c01b05987bd9e09168`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b47a68df718bf2a7d4445bdade317550e020b85d2aa4a94525ae1ad4b31a8`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13964924a7e5d79c0c083de7d22047114b2d6303f4218c86261b01153e6269f`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8816c938b3b46dfbeaf5118ec0047759f2db428a6851268ae2447f2939be202`  
		Last Modified: Fri, 04 Jul 2025 04:52:15 GMT  
		Size: 1.6 MB (1618852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a536759b7c30da7b0cbd1343f2d70740c1f61184817347f9a14298edd075dbe`  
		Last Modified: Fri, 04 Jul 2025 04:52:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6a922db06c777a5f97978c7a49465a5bd491269594bda58016b17277a0a2e1`  
		Last Modified: Fri, 04 Jul 2025 04:52:15 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f0743edaaa93508210d9bda8cb59945798a8bd7586a10650afc2a5e7e71894`  
		Last Modified: Fri, 04 Jul 2025 04:52:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da675386dbf0b65a72d9b6ba544ef88c400f404d62bfbea79c6bfb5404f8ebf1`  
		Last Modified: Fri, 04 Jul 2025 04:52:16 GMT  
		Size: 20.5 MB (20514130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:62f40ca434d15f3b5c7cbc86dac3b8f8b02d1d2665d1f3c74255730190de3cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.2 KB (411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6312e3aa676045338339a6c8fd894f3ce1553faa792fd7c79b6ab92297bcf4b3`

```dockerfile
```

-	Layers:
	-	`sha256:ce418ad5c38370d608586eafe36ac1342a919d0540c161499b3578b41252fd46`  
		Last Modified: Fri, 04 Jul 2025 08:02:55 GMT  
		Size: 376.4 KB (376430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac541d972bf90bf965394c5730823941d4fc975adcdea1e166ef4763ed99041d`  
		Last Modified: Fri, 04 Jul 2025 08:02:56 GMT  
		Size: 34.8 KB (34790 bytes)  
		MIME: application/vnd.in-toto+json
