## `drupal:11-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:3dcc95b4cf16dcff8ddc631338caf6897f3ee30e894f76dd05909bbee74ef678
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
$ docker pull drupal@sha256:1ea62f74cf51bb3e8d43aab3636a072a4359b7dced7380f4fe0191cc0d932970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55452411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897e3fce96c7d858c00a65d62cec783df76fa1a74ebb739aad0aeb0c4f552152`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106470e729a24f3e2d4265d4edc6afbc4261b3905e4c2b555acf3777482b0d85`  
		Last Modified: Wed, 08 Jan 2025 18:09:47 GMT  
		Size: 3.3 MB (3333628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fedc8f9807fae0f538982fb50fd1369bbfb4422d01ffe2eb54d750f289508f`  
		Last Modified: Wed, 08 Jan 2025 18:09:46 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e94941220008160a693a6ed8bbb5090ec8ab016743488815afc6a8ef99535`  
		Last Modified: Wed, 08 Jan 2025 18:09:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda1feaa8cc69f98764222ffb9345c8a4fb9be7c38b8724633919bfdbb920702`  
		Last Modified: Wed, 08 Jan 2025 18:09:47 GMT  
		Size: 12.5 MB (12545866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0a133f9d8fd552dee3364cc157b82c6b4af978105ae81541620414bee80a3c`  
		Last Modified: Wed, 08 Jan 2025 18:09:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae557fdd973fb84a2a6493b2199273be3b39e45623fb94ffd8a4761116b6091`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 13.2 MB (13200160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa2151730701658fc581377c3040604bee18c6c6360155b7efcae08d3805256`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83b326d773723be57950c37a385454330cb11f1a9baefc932d365a9d318f88f`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 20.0 KB (20030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1051c554667d3494c747d113ac9dbaa9bab0d1ec1e03ef853f5b3c82f36cc844`  
		Last Modified: Wed, 08 Jan 2025 18:09:49 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aec43dd71a9a1b2b07f16ee4bdd18c75b722cada84307593683bb57fddfc244`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 1.9 MB (1921849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33244ef4446a91f798e47cea8df37dd7420b2a1961a8e618eef4ea5e32a9e0c`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b214a5de9a0a17bdfcceac1b6d379be2f30b32c9158bf74f574b09ebb3f3893`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 742.2 KB (742235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5a1a31c62bfe2cfd225cf63c433b0cce4300adb67b64d278b68f527e1f79b`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244c667ad8073fe65e343573aa1b4476d56a4d370d7dcd1922cf76b08784629`  
		Last Modified: Wed, 08 Jan 2025 19:15:48 GMT  
		Size: 20.0 MB (20033199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:9f81b3c115fdf772f60387ea080b09f785cd5601dfe3faa578ff49a591758e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 KB (401052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828fbdbf87b6c389b78f07a77a5fe9cf6eb061b78ec260f4fe0841f7cf9e3e48`

```dockerfile
```

-	Layers:
	-	`sha256:598b0c59c2d40103575e4ef960fc3ab22dc5713a239f93c255308d28f3a03444`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 364.8 KB (364815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ce1be27382a23d2ebbb1e663fe5e2f0a07b32cb027d7b72f78b96962ff3450`  
		Last Modified: Wed, 08 Jan 2025 19:15:47 GMT  
		Size: 36.2 KB (36237 bytes)  
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
		Last Modified: Tue, 07 Jan 2025 04:04:45 GMT  
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
		Last Modified: Tue, 07 Jan 2025 05:21:31 GMT  
		Size: 11.9 MB (11932135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a5d6383779af0bb0de20a36cfbd98c24ceb42607ad110cb2d3e4a5d11c709`  
		Last Modified: Tue, 07 Jan 2025 05:21:30 GMT  
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
		Last Modified: Tue, 07 Jan 2025 05:00:01 GMT  
		Size: 12.5 MB (12545715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f95167d47aeb3a435077aceb7d8705c818b486632725b186c95787b67034b1`  
		Last Modified: Tue, 07 Jan 2025 05:00:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b950f93713574e66a68a9cf5c594595e585411adbb3fc9154187609b8f69aa44`  
		Last Modified: Tue, 07 Jan 2025 05:04:01 GMT  
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
		Last Modified: Tue, 07 Jan 2025 05:04:01 GMT  
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
		Last Modified: Tue, 07 Jan 2025 20:57:31 GMT  
		Size: 36.5 KB (36457 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6bb39756858171e37a63c342c6c5b964a4fdcfeead0655a83b20555b067d106f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56054064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a87c426bfcecaf51d1aff35b8a101a3a40d0334362d52c754f2fb65fac579e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56d572749242eca00678614bd6256b30f2e360d0b7715160972ff2da91198e`  
		Last Modified: Wed, 08 Jan 2025 19:58:39 GMT  
		Size: 12.5 MB (12545912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b83f72f0bae608817f70381a155b26f4984a12188d30f475b1470402a02e27`  
		Last Modified: Wed, 08 Jan 2025 19:58:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000840a86e7ef49d75ab76eade246f989f842764b252a56caf24f6f8b05c368d`  
		Last Modified: Wed, 08 Jan 2025 20:03:39 GMT  
		Size: 13.2 MB (13189070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849dc6774750c44cc056e2c1b44a01c5e314fb6678ba73f58a06cb10d4983ce5`  
		Last Modified: Wed, 08 Jan 2025 20:03:38 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab5fefc99da7ec61bc13afeb6ec46292edd7facd248b95d9af1b86849769fec`  
		Last Modified: Wed, 08 Jan 2025 20:03:39 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ddf4c589c51f874ec6253ed419fbc7496ccba03e70fcc611e887cdb04c25c`  
		Last Modified: Wed, 08 Jan 2025 20:03:39 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875d6652cdc39c8a83c1e3c627802eef0ea472680ede5fae94df75624ad1898e`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 2.2 MB (2190119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ee62919160ac5faddc9c03ae5a9c2282b577ef92ac67b6377f6986b944120`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a265ab39b1168df14159988748844b408e7b06315dc9794533ce3a89fc4e891`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ec0b5c862d06b903446662681fd7d7724604588ac89fa45693c86acf12b83`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e008e80771175361675f325733191dab6ac0a785ccd532df4001190c85480`  
		Last Modified: Thu, 09 Jan 2025 08:55:42 GMT  
		Size: 20.0 MB (20033119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:72e2c7fb8c74cd982ce678a41aaef0ccffcf2766acfccd4664dbdfda4cc8e5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e00abdf44076bd2d8bdc6fb8bd9ebac4bfc6b7632f1ea338e5bde9b61be243d`

```dockerfile
```

-	Layers:
	-	`sha256:46c9047080ca2a299307cd7e6dcf7825338ee3bb089b63e53d5fa2880361ddb6`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 362.2 KB (362202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811c3f17d6b2a0d4ca0f64fa6d9568134770acb3ecbb16ad2882846ce9977595`  
		Last Modified: Thu, 09 Jan 2025 08:55:40 GMT  
		Size: 36.5 KB (36542 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:0862bf64dda740ee2e516f3af06c3a8267fd48ff6c7797118c113c5586529005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55681939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39044e390eea65545e9143bc49a1315d5f48a6f8e30a16b6cdd41a8ba3d7e1e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7fa4d99b1e859b3c4325b9be71ba00b5023f760d1e926b42da9504a799af88`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 3.4 MB (3373756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3828ba51a833db2280a4af94c556ce7ad65f58bff57cb9be564783eb7161a6d`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc37f570843e3859b287a52af11f772a42df7432723179072dcfd9293d827a`  
		Last Modified: Wed, 08 Jan 2025 18:04:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a97740a96617588f5f2be6436a3fbe9d14e6a8d4093df6d11b0437477e6a156`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 12.5 MB (12545854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b0830843f10ae59c964fc7eadbdd4b933a59c1a03c1126adfacbfac5185a39`  
		Last Modified: Wed, 08 Jan 2025 18:05:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130a7e3bbab59b6bdf2bcd43bea3161635afd7ca3e1c2517a7402ec5992574f`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 13.5 MB (13505507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f774b322726acdb67018b15e04e4f1dc02a48e7c58acdac736c018e672c29259`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e93eddf983f2fb2841cd1db055c982bf7b969ebd185ebec27990f19a8cbd787`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 20.0 KB (20020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53614d7132d9ff691184f2ce1d795c021e20f76da8e29861a642b324c2585300`  
		Last Modified: Wed, 08 Jan 2025 18:05:22 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65633ac808e2bca61c6f87a5735b372f698a4fbcfb38859c1ecd9df94fdb56`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 2.0 MB (1984595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3b2aff08f283d1a19e0a4c46909ab066326ddcb237e46b6b7ae295568445c5`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f97aaa3877525defdde7dd4b40e8ec8a721d894ff7343bb4becf0f6e924c9`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f5792c151de9bc35e2b045fda1d12cb81cda29ef9d6704a4003ecd6f1ac74c`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30272c69f75735959b94795ec63664dcf3e9e16555c8055a2669c7cb6e17e67f`  
		Last Modified: Wed, 08 Jan 2025 19:15:36 GMT  
		Size: 20.0 MB (20033123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:2025916b619c62e2ab163616e8e3ea4a103a510e7d3b4f31c64b9d5fa7703789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbe396e996fb1415a70b541dadcb0c60c642277b3d18069816077e2a982a21d`

```dockerfile
```

-	Layers:
	-	`sha256:b4c574fe44e8ee1a5019701ddb8bc3857e5fb88feb95d8ceaed4c69215211c0c`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 364.7 KB (364730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c2811aa0d31767e77c83b90976bd04ec6b18f811c00035a3649c67a4a6e812`  
		Last Modified: Wed, 08 Jan 2025 19:15:35 GMT  
		Size: 36.1 KB (36135 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:43a46e0673a1d8cf1c58b91b873dc4b784f044f93b01972efe526d0e4d507966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55767469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fc0fac4af78ce68c5cff1103cca4bd7800b90e6adabd6ac91241919aaa9f39`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4595b78858f46be4deb7eaed8c79d1cbcbfabeb43ebac735f8d3329090df27`  
		Last Modified: Wed, 08 Jan 2025 19:44:13 GMT  
		Size: 12.5 MB (12545911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8fc6ecc53933bebb5897bc5c8d34ce1e1b1aea5b1a19ccf070e06af648e51d`  
		Last Modified: Wed, 08 Jan 2025 19:44:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270cdedbcf838a9f1ab9ff4db15ef4bc94e980ff8c2e24bbe822d97f2a01ad85`  
		Last Modified: Wed, 08 Jan 2025 19:47:36 GMT  
		Size: 13.7 MB (13670576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4895684444f9b13cca27548793db2ca1fb861547942e83cb0fa09590e6ee97`  
		Last Modified: Wed, 08 Jan 2025 19:47:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf31ff048823b9baf9813b48d7f9a21e4c57cceab1fb2804067d0322e7524f6`  
		Last Modified: Wed, 08 Jan 2025 19:47:35 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871d2dd58861495982e967deb89e1cd0f8678f4058c0d527bf744d8ccb3cbac5`  
		Last Modified: Wed, 08 Jan 2025 19:47:35 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6d8d1dd2dec5344a5a1fbcb571025baaafa0822508c7e6bf94bf4141d9bee`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
		Size: 1.7 MB (1691964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ffd17c3dc952aac67d550082bea829ec201eda3a556294ffd88947318b9f43`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bcdb2dcff5944513522bf1545dfd713cf023f3e72fe93d55e83723079358da`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
		Size: 742.2 KB (742238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c786e991f7c40cea6b7381b634186f8a8caf7bf7a8ad1c35caddf4473c4b7029`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22e165b37677f1027e6eada87b89b305452212745378fac20fc2678f6a9a34a`  
		Last Modified: Thu, 09 Jan 2025 04:02:58 GMT  
		Size: 20.0 MB (20033250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:26b8e81687297f6c906b38e2913afeca4a39444957be2e16e0751d0f68b3424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0dfe18bc36d5c265be25382d6d940cca1c8725b87edf95bc874aa7490a2f58`

```dockerfile
```

-	Layers:
	-	`sha256:73a0580eff61719279415bf54b16a11026d6287eb15a0b9416d95b653eaae2c8`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
		Size: 360.2 KB (360157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c9f19ba6607fbdb7cc5647f0d199d2fa2569325f4665778f75fea9cee2d398`  
		Last Modified: Thu, 09 Jan 2025 04:02:56 GMT  
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
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
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
	-	`sha256:57f6a000aefb554fcf8c079110c6293bd9550b2e3a29709b1ce9b336e6ca76df`  
		Last Modified: Sat, 21 Dec 2024 18:17:05 GMT  
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
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 361.5 KB (361453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac031ed217d75108db5c0c649b9647a9707fc5fff8d6bb32ec1a8d302e24e96`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 36.4 KB (36369 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:15cbbcaa5791ecbc073fc6630c7cac162a0dc3384b7fee23af56dd602beb8d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55144211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1322c3c73d4660364251f34db1505f0eaaf48728c2f31a440c92ff53edf05e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651166e22fdcb9885b2dcc4f5dca968e967705564de4484ba3e50812e646a069`  
		Last Modified: Wed, 08 Jan 2025 20:15:53 GMT  
		Size: 12.5 MB (12545896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18d2a1dcc4c3b243f550656f50e5197cb25b1fff9270de981e8ea5243db64a`  
		Last Modified: Wed, 08 Jan 2025 20:15:53 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39fac6777deb05465f51536a2338cb8f1d7a4a4f254fe34b077d53c1ee7d772`  
		Last Modified: Wed, 08 Jan 2025 20:15:53 GMT  
		Size: 13.2 MB (13150249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e581955982b2555c865bea84abe49fd2b01fc08ed7a308ffaa2275e060cef49`  
		Last Modified: Wed, 08 Jan 2025 20:15:53 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ae8a66b5fc831d8a06e3bdc32f9a8b20f8f2ffdfd5a38e04576ff624be9e`  
		Last Modified: Wed, 08 Jan 2025 20:15:54 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb10cecb430c53f22408940466a3cb7d799cdc223fa8b04d5020d3b763aca37`  
		Last Modified: Wed, 08 Jan 2025 20:15:54 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a0db9b65dc90ef6a21404e593c4814775e48f3668fddb13b38aad11b56e165`  
		Last Modified: Thu, 09 Jan 2025 10:25:29 GMT  
		Size: 1.6 MB (1611507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00f5b9a51d4eb5d4dfbb5d071871383055bc396e13f0d23c9b6b8b1ef0f361c`  
		Last Modified: Thu, 09 Jan 2025 10:25:29 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b24be5a91fa91b3023d99d1586b681d19b9a5163eaa9cb2daaeb4196090076`  
		Last Modified: Thu, 09 Jan 2025 10:25:29 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4285d89337bf953484f3aed614b127ea5c8cbd626343588fa2b6b897c9c100e9`  
		Last Modified: Thu, 09 Jan 2025 10:25:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fa12de3573d55ac2f4651a1fbee0d10033343856c124abc175c7688990737a`  
		Last Modified: Thu, 09 Jan 2025 10:25:30 GMT  
		Size: 20.0 MB (20032603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:faa357bdc4e32a6cf5550dddbac12a2e0f4d20dce81390dd583ac9fdb879d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 KB (396289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03887c4baebc10732051d5860e2446f3a027ab63d178a2eed8be5a3ba5391343`

```dockerfile
```

-	Layers:
	-	`sha256:73026c4e40618ff5ce20c7dff6ac363cefbe16ebd279bf8473c04da2ec08ae7a`  
		Last Modified: Thu, 09 Jan 2025 10:25:28 GMT  
		Size: 360.1 KB (360051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6b630f4b21994382200f215069c91d573923c0ea86142ad97388283b08636f`  
		Last Modified: Thu, 09 Jan 2025 10:25:28 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json
