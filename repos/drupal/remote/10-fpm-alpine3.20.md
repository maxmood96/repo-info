## `drupal:10-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:e1651cc6ddd1f15801794f3998f03a2c3600ecea0b0d7699252ed4dc04f080f3
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

### `drupal:10-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:ae16a93b29ceda25b7096335006c6f4febd63b38c1c7b565a55fa080a15c7895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56704457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daced235390e749b36cb9f36375bec7c33c30fce6d364f183b2b2dce2cb044b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f690cc5dff53b7f3772d63ffe199fb2f3eddfd24672e86ab202b3efe6169474`  
		Last Modified: Tue, 07 Jan 2025 03:30:18 GMT  
		Size: 3.3 MB (3293723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865d24122ef3f248ea53498d2b868d31dd0ef496bdd13d9f4f69f19e82db3d61`  
		Last Modified: Tue, 07 Jan 2025 03:30:17 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d1f9b3dbd0267b54ab42385e854bc3260c854670df50feafe401da118c4827`  
		Last Modified: Tue, 07 Jan 2025 03:30:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe049907d8e55cd4a1516a4cf2a21e29d0d30738ef8c1b8b242d1af40d9adb`  
		Last Modified: Tue, 07 Jan 2025 03:30:18 GMT  
		Size: 12.5 MB (12545519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b64d5bb1a1596194c5c8ad2aa01366b754a5479a6505577bdd7691b03b7609`  
		Last Modified: Tue, 07 Jan 2025 03:30:18 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ebd68e3ae833d8afe00b55482b1736e39089eb9f38e8c3a71c00e7fc6896e0`  
		Last Modified: Tue, 07 Jan 2025 03:30:19 GMT  
		Size: 13.1 MB (13106340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d1bb75461359b4aa2cb3d3878c8e9641482f7f167a80463b74dfbf49ea24f0`  
		Last Modified: Tue, 07 Jan 2025 03:30:19 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3220b0206dbbcd36a7467b8ad0e4383fa270bb3f31197073af8f7611e6ddaea9`  
		Last Modified: Tue, 07 Jan 2025 03:30:19 GMT  
		Size: 19.4 KB (19430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a19637bc5f89c6de60486aec2abb2530bd7baf1791a98dbe823f7f91eff0b`  
		Last Modified: Tue, 07 Jan 2025 03:30:19 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d97df361ffef062045263d8c15fd3317ff3d1871ff7ccb5bee987bed730708`  
		Last Modified: Wed, 08 Jan 2025 00:32:25 GMT  
		Size: 1.9 MB (1902038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6fbdb4a9a19d9530cdf0ebe6c050573515de064651dd49a017e4ff3a426d19`  
		Last Modified: Wed, 08 Jan 2025 00:32:25 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2615d693d0264cfb804e17e811e509736ed2bfd36a2a0da6ba2f2297af91dcd3`  
		Last Modified: Wed, 08 Jan 2025 00:32:25 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5e4eb9479a73aa4486b9469aa2bd6e00d0d67d48cf8dec670019077e54024`  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023d384c02089e0f8858f031bec694f86aad69e9bbf127982ac29b36a0cfe3c5`  
		Last Modified: Wed, 08 Jan 2025 00:32:27 GMT  
		Size: 21.5 MB (21467441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:4c14cf0f158337acc994bb199599a0c112db63f88b49f2b71bdef2096f098c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 KB (377841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f612e8f398614fea081a9006ddeb23c94dd4d8cab7d488825d57b118ca7124e`

```dockerfile
```

-	Layers:
	-	`sha256:0e78c71dfaf652ff966d3656798253749f39977f69fc4047609d66e856292c35`  
		Last Modified: Wed, 08 Jan 2025 00:32:24 GMT  
		Size: 344.8 KB (344809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0caae475efa352ac2c389d5c8175637d25a2ffff6e7be22d8b738a26eb041a67`  
		Last Modified: Wed, 08 Jan 2025 00:32:24 GMT  
		Size: 33.0 KB (33032 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:a796b3f632044cb718ed919564898a61ea0927e953bc1179f4f31843398c11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54748097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ac496d66037cf8cc509d785d3215268477243eb5af25acdbc84e743ad4bb66`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6e5e4c2e68718d1f73ada486908f719d13b227a11f78fc8876bdae65936e`  
		Size: 3.3 MB (3277802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da5effe2170797797df1994313aee89dcd1884282164d0f8a7b2b6624090726`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e18edcb50238487ec3d15c28791318639104f7da84baac7d0aee6de4f24e5`  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cffb409fdea2a1859a8742ddb8c35adcd28f8632330b8c26142412018478762`  
		Last Modified: Tue, 07 Jan 2025 05:29:18 GMT  
		Size: 12.5 MB (12545519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1edb1147b0c96a9d4435502e36bbaafc1c9b93e4b1d244048606deb05f590c`  
		Last Modified: Tue, 07 Jan 2025 05:29:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe23d072727bff6b8ba862d895cde9b557b0406427529680dd8ac33a0963596`  
		Last Modified: Tue, 07 Jan 2025 05:33:10 GMT  
		Size: 11.9 MB (11932931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53789333b37bfb8004b21fd6493d618adf2d0026413d86d137f020354037a02`  
		Last Modified: Tue, 07 Jan 2025 05:33:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1554687d2bf40016390219520869f27fa4a8347a576a492fdf7e78599937182d`  
		Last Modified: Tue, 07 Jan 2025 05:33:09 GMT  
		Size: 19.2 KB (19216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3ae033f114969ea6d8a5b486b3dc950eadd6b7d5edca32e0ddbc9490ce0e15`  
		Last Modified: Tue, 07 Jan 2025 05:33:09 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc58e15b06205d2c6097d52ddc4bbc5bba060bed98f11c92cd7a6b105fe952a`  
		Last Modified: Tue, 07 Jan 2025 20:25:26 GMT  
		Size: 1.4 MB (1385574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93046a029a8f7260177e9c9f1cb68cedda9e8eb467ac5bced8f611737a5d314`  
		Last Modified: Tue, 07 Jan 2025 20:25:26 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad226106c754e0053574e8fbb1f7fae694d672194f3402f1cd3668cdb368d8f2`  
		Last Modified: Tue, 07 Jan 2025 20:25:26 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dd7573a0c00461eb5bc950b6d62930df8b227c05efaa24d67632a290b91184`  
		Last Modified: Tue, 07 Jan 2025 20:25:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05157437dcc0dd868c08dbd420f03a588124a72e6752e1c9b595c97aa1e796a4`  
		Last Modified: Wed, 08 Jan 2025 00:30:46 GMT  
		Size: 21.5 MB (21467131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:e9e8c430b70fb3d0f0c3066878e21472bb64024be6a881c9763a0b59f49008a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca34ba3160ea35920fd9a73745ae77aa7ad736caa85dabb50d070e34958dc74`

```dockerfile
```

-	Layers:
	-	`sha256:65087d35a6021d1e33ac7c2f509c4dcee63599724b8fc7f34b96b2ad7deee467`  
		Size: 33.0 KB (32957 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:dca6ced25c7c3abfa94c30dc41ac3aa052b90a7c766d819547ca7ebde9d1c378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53427265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70dd681d4b85ecdce442f1dd7143ae2af5cc89c86f54ade61954f2af4ed6e754`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666fe9f2778fc13085387269ec8e5a9a92fe5a5cd43a1c04d0550044cef029e5`  
		Last Modified: Tue, 07 Jan 2025 04:03:10 GMT  
		Size: 3.1 MB (3086378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33e8f07354fb119b701cf115f1a2dc9d9e81c9a1d4e577cc25369377d26496`  
		Last Modified: Tue, 07 Jan 2025 04:03:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7628e2f49a6657703e1bf3b16f926b733c3fcfdc62265ce69d5a5b75d985504d`  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c229ade4a8c7b16b02d51e68936bd124294a7d187ff1168b5dabdc96a46ad4`  
		Last Modified: Tue, 07 Jan 2025 05:12:23 GMT  
		Size: 12.5 MB (12545521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d3ce7581051b2b51d3d0d7cd62fec64d243dc93cb14f381a2734529d2f6a78`  
		Last Modified: Tue, 07 Jan 2025 05:12:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677b0030d11cd5e15f8e637279312c0f9fc467acf681cb2c9fcf5880a45b6483`  
		Last Modified: Tue, 07 Jan 2025 05:16:17 GMT  
		Size: 11.2 MB (11187713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f2d670d3f27073da5bf6030d6bae6a0a9be09896a0a2c9ee9dc32d36dbcc0`  
		Last Modified: Tue, 07 Jan 2025 05:16:17 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6573a35403a7d83b79a2b28a3e623b6ff10f69fbd4c918b07d3825ad1047b8a`  
		Last Modified: Tue, 07 Jan 2025 05:16:17 GMT  
		Size: 19.2 KB (19221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9c8ac020413a046ccd8c3d12af754ed8cdef6e65c87068835dd667dc42648`  
		Last Modified: Tue, 07 Jan 2025 05:16:17 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c63b7c81fa3b73a47571d1346561e793e34ceddd422c11b69ecdee61d92aa`  
		Last Modified: Tue, 07 Jan 2025 20:58:49 GMT  
		Size: 1.3 MB (1275486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852cd5e2511ccdbab587d18820acc9670ea996a357eaa917c0356f7956e48f29`  
		Last Modified: Tue, 07 Jan 2025 20:58:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718c31efe12e76a09dd2ca6c8d380984c4ad79ba7d3a6d2bcf01e9c564e57f5`  
		Last Modified: Tue, 07 Jan 2025 20:58:49 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d19a01e665041f46c8ee452ff862091268c6310e232993ea2e3b197047c336`  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad2d0155945bd179c32ff6ef04509620e8d7349f39e5ec28748dc64608de3e`  
		Size: 21.5 MB (21465679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f2bf75cae93e3024f96a0790e18537c068901a6612e98622678479ca395fdd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 KB (375172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7156781abae428ced574ee8492a4d6fd03196bf9f9bc783273c8ada99c8d062e`

```dockerfile
```

-	Layers:
	-	`sha256:97d0b49609d4df0c32425a8096cb3bc1ee9b3ae165950990725a7d229925deec`  
		Last Modified: Tue, 07 Jan 2025 21:08:55 GMT  
		Size: 342.0 KB (342000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8275e93b7904e8d65d609d2f4e568b7ed3a8120706e5001aa012b44cb870ad1`  
		Last Modified: Tue, 07 Jan 2025 21:08:55 GMT  
		Size: 33.2 KB (33172 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ab3b675d0229a56d94ad26c18ca51fe5df898c5eeb084706722374b5a8f102b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57557956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0c30633d2b1e7573d0b5523ea3071c1a555f5dc3412cb8b02e1cdb08ee3d3f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 18 Dec 2024 04:27:27 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12651a1164be1c0ff5ff6b5888077c5a5ce96f08fe1a1eea4c3c70cec19c59`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 3.3 MB (3341946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29137c219172cc292e8d59680364cf3eee1a1e71b5507c0237d302305c00ec3`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c134198c2af672fa5dd2e3639c0be7847f521d9b05277485eaa64a00c4c20fb`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcc80b1ee3d2edc1ba2564131aaaaec09b2845b926a65578aeec496dbd02346`  
		Last Modified: Tue, 07 Jan 2025 05:53:12 GMT  
		Size: 12.5 MB (12545521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d02dcdedac928bf479aadb829c8ce5820f3265e4effb0c3e06a92a92fbda49`  
		Last Modified: Tue, 07 Jan 2025 05:53:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c221958f4538af6ef29155cbb7c3dd84d1de7c5d00e852fdb0e98ce9149210f8`  
		Last Modified: Tue, 07 Jan 2025 05:58:00 GMT  
		Size: 13.2 MB (13164358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b3608c610cfca4525882a726c3f3242afdbccb015902a10c417a9a9c7c8c4`  
		Last Modified: Tue, 07 Jan 2025 05:57:59 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c2c9365ae1416e2ddd19f5dc73632bf28f9d71d97cb24c9b821cb7b2dfe65`  
		Last Modified: Tue, 07 Jan 2025 05:58:00 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072e0ac4a10978a65c662d5928d3cbbd909ef3f8ea91bb3424523d92ddd9c4f`  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7a9282063173e2ca816537b7b5fed54624f8241792760e2543c131084436f5`  
		Last Modified: Tue, 07 Jan 2025 18:51:01 GMT  
		Size: 2.2 MB (2179376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9590f8c734c451015433d0693df366e064ec688b6af05d00929cf4695e39dc`  
		Last Modified: Tue, 07 Jan 2025 18:51:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daabd7ecd5ea1163adbfcdadbdc44e7e5c197532a42db754ff169ef1794f1a0`  
		Last Modified: Tue, 07 Jan 2025 18:51:01 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6ef24497ae36255d85c44ed89e9db50ae1719d302aa13a1f32f9fbc17b107c`  
		Last Modified: Tue, 07 Jan 2025 18:51:01 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14466c1ec64c31bcfa8b7c337f395b559e3893842f70d1a33ea2b7ae425d9948`  
		Last Modified: Tue, 07 Jan 2025 19:00:04 GMT  
		Size: 21.5 MB (21464895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:59420da141c48101c9c7c09913210a8bdef55e831a8ed3bb9a159782b5638d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 KB (375244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da42c531f7c86b44a77974c8a1f9425e08ea53d467d3e9a19c32b93724477ef`

```dockerfile
```

-	Layers:
	-	`sha256:53954b4957cfc89a73566a0ee0f4866e1b0639152f43b94610e597abcc9fa01e`  
		Last Modified: Tue, 07 Jan 2025 19:00:03 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254ff85490a089dabb439a33182074cfb569e5274b2631ef0c656d5af98eba44`  
		Last Modified: Tue, 07 Jan 2025 19:00:03 GMT  
		Size: 33.2 KB (33216 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:43fa8cf531c26c51d5fafccd8b21f785a8fba6f1368215f336e3530a8b918d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56995018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56a5814c39e2384b5d68bdf642e544f3f4666c7713bf3387e991e6ca86d41e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918daacf795a19aae6adaf948f0febb2d904c54e239cebd8c33369e5a3441511`  
		Last Modified: Tue, 07 Jan 2025 03:27:52 GMT  
		Size: 3.3 MB (3339862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3610ee925894c856be26fe360c4774bcaa60a51ec41217063e6905d6b6e4cf`  
		Last Modified: Tue, 07 Jan 2025 03:27:52 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b67e6164a648d2b6da895be498ef644814bf5c93fac33c96a08b67b49bf3328`  
		Last Modified: Tue, 07 Jan 2025 03:27:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7320ce4370fd5c3c73b37ff50976af1d599281deb18a7d5f46e285cd4537a`  
		Last Modified: Tue, 07 Jan 2025 03:27:53 GMT  
		Size: 12.5 MB (12545518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa669ff8881d0d338eca785d23b2f77d7408743ab55fa8d43bd28bb9a8a7b32`  
		Last Modified: Tue, 07 Jan 2025 03:27:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd014f615681424c13e85c4f67dad6e992c9b57112049e9a5ec347ae843c97e`  
		Last Modified: Tue, 07 Jan 2025 03:27:54 GMT  
		Size: 13.4 MB (13441154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6cca70eb8a0ba2bd85169ff488c00be5ed491d8cf68e0b05b2869fb4893582`  
		Last Modified: Tue, 07 Jan 2025 03:27:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa561ec0760ae4a0efeb07a62740d96a228bb589c473d4d3909b61e86a0e0f39`  
		Last Modified: Tue, 07 Jan 2025 03:27:54 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859562fb4dfb55be1a7d7217b11a5cfcf54261ac67fdeb04837ebbd98baf2a4b`  
		Last Modified: Tue, 07 Jan 2025 03:27:55 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34957303874d156c11f3e25901608b304369722bea72ae23c46c8433b90c500a`  
		Last Modified: Wed, 08 Jan 2025 00:30:33 GMT  
		Size: 2.0 MB (1962422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53c31d9bf0f0619dcfe663913b040421abcdcf7ced6fcfb416c143f2a6f0ea7`  
		Last Modified: Wed, 08 Jan 2025 00:30:32 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68d31a18b6a0614790092057d60a0025bb98543f8c060ddf1f58c1a721096f7`  
		Last Modified: Wed, 08 Jan 2025 00:30:33 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5620c314b138ca0f8befc907f4c4bf355d2a577efab49e95b7fec93e74b225`  
		Last Modified: Wed, 08 Jan 2025 00:30:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4b2a2f990a4ee35a3339032e90bf5be3405186197b49073b6b7367a6149d3`  
		Last Modified: Wed, 08 Jan 2025 00:30:34 GMT  
		Size: 21.5 MB (21467489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:be1c49a98837b3677e213a39f00d263e63c18858093d3055978ef1fbabe00cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 KB (377753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e8525cd5c00af670d717aaa4f4a1b386393ace90252d4d8a82bb187abd9a0`

```dockerfile
```

-	Layers:
	-	`sha256:9d540cc2099b8aca9bc9090397ed1dc85d7a6298d74675ce61b375e0a964d511`  
		Last Modified: Wed, 08 Jan 2025 00:30:32 GMT  
		Size: 344.8 KB (344774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4c10941d5b7b7427ab6339896c9ab710d92e5e57f45519efb3e20dd4c9a5e8`  
		Size: 33.0 KB (32979 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:6a8eb132fd35c120df1244b1f9387661848df6233ff959ec0b929b0fcfa4c762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57060915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6fe3a65e4d415fe47f737984105559e6403cf2afca0a44bc42e0c2135aedb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c1c7ca97bd5883ed3428282fc1d95b690329961e07598c989d7cc3e28ab72`  
		Last Modified: Tue, 07 Jan 2025 04:08:03 GMT  
		Size: 3.4 MB (3419545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9082a14288e52e96ed72a73b7cb744d6f4a60665586a1301c8a7d13caadf8`  
		Last Modified: Tue, 07 Jan 2025 04:08:02 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e6835799395b61d043101026bec9208c8d02d4ab267305b04621b87ef4aff2`  
		Last Modified: Tue, 07 Jan 2025 04:08:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a3f82b3084d502282b7c0291e065d15a6295a694dab607af04504cdd1fc2e`  
		Last Modified: Tue, 07 Jan 2025 05:08:24 GMT  
		Size: 12.5 MB (12545504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cb016ca411924c1f86ada674c3a7f8a12a85b1af784b70757549dd5670a2af`  
		Last Modified: Tue, 07 Jan 2025 05:08:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368d50346186977c6ba5f16aade07ad92c49637bfbc12f788408c6e9e012f095`  
		Last Modified: Tue, 07 Jan 2025 05:11:38 GMT  
		Size: 13.6 MB (13604529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08a03140012bb612e445fe05830b1a363fbb17abecd6e361950b9238ad51a0c`  
		Last Modified: Tue, 07 Jan 2025 05:11:38 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a0e28d62bb4c1f4b8ad709bc15cc908fbffebdf83ad7d4682492c1f80f85a`  
		Last Modified: Tue, 07 Jan 2025 05:11:38 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52338ef7fba2476f39af648d727892100e312ccf03c4d55e07e411978b4e49bf`  
		Last Modified: Tue, 07 Jan 2025 05:11:38 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bab5e2e4196597b0deb6a44d3ff24fc4067a96b228c6510aaf0c29443e72af`  
		Last Modified: Tue, 07 Jan 2025 12:06:19 GMT  
		Size: 1.7 MB (1679950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aba51a2e5193fc7162dff6af1f19730148b24aeb2c60b5a4b28e4a68cb90ad`  
		Last Modified: Tue, 07 Jan 2025 12:06:19 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3157f444732cd4c8758ef3500975d41c9dc26e16c9abba2380b79f7c9af1bbfd`  
		Last Modified: Tue, 07 Jan 2025 12:06:19 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5092fbf32c427d5a80a3c702810fccbea075b08cfcb5c848882a615a84651`  
		Last Modified: Tue, 07 Jan 2025 12:06:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcafada483dc88fae97aff60c9504e5c04e54aa6379c8176ef1160a6d35de49`  
		Last Modified: Wed, 08 Jan 2025 04:32:21 GMT  
		Size: 21.5 MB (21467476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:050c1ac3fc858c1faa47131b2422acd3a7b6029154c72448833d668f61ee39c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.1 KB (373145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f29ff9d88e36dd5f002dd6319bb4aeffb0e1d560f347280c426c544536cfa16`

```dockerfile
```

-	Layers:
	-	`sha256:4e803067ed0a70802c00747e1bb81641e4ca698d05ee6e1495413a9b99f6606a`  
		Last Modified: Wed, 08 Jan 2025 00:41:21 GMT  
		Size: 340.0 KB (340043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef4e46dcb3cbe011db4a045a48b831005ce293c7ff99c767f9b55f20ceef4ec`  
		Last Modified: Wed, 08 Jan 2025 00:41:21 GMT  
		Size: 33.1 KB (33102 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:016cb31b7e3233f417900f43f8321aa35546573c5f91ec7767bd2e49c06f2169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959bf21e48f91fea9e938fa2fa90864521c6f14465d3dc5e5393c778e1d91fd5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aea9df96660cb6c7a3ecdd756f8ab70a916f52c0cb0f8ad9ba87fe615c057`  
		Last Modified: Sat, 21 Dec 2024 06:49:48 GMT  
		Size: 12.5 MB (12545648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909475cba016b581c448fea653f807a36f1376665dfbeb2709191818ba994cf4`  
		Last Modified: Sat, 21 Dec 2024 06:49:45 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d096844005402b1fe70127fef09a3e4b9c0ac689657dd6a2d7edbddcf8cfd925`  
		Last Modified: Sat, 21 Dec 2024 07:40:25 GMT  
		Size: 13.2 MB (13152700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965a085d2679550a199b727ae369f24a296ddbe6b6ae6b1cd2a44b9a6ae3504f`  
		Last Modified: Sat, 21 Dec 2024 07:40:23 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2e3ffa1aab30fa8a111fcf68aa7840c88c5bc806344311e426662116359cdc`  
		Last Modified: Sat, 21 Dec 2024 07:40:23 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e529ef423e863b81f4cef6e0c5e42ea1004213b829d0dc331d825618111e74c3`  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dbebd3e343e0ef7e4afcc462e544713323a3b6c291029addeafce275dd6edb`  
		Last Modified: Sat, 21 Dec 2024 18:26:06 GMT  
		Size: 1.5 MB (1483041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945de1784b67a83a3aba34318401702d647b828969a9582949f52cb86e0022f`  
		Last Modified: Sat, 21 Dec 2024 18:26:06 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1e30cfceb2ac49129892a425dc9458aecb8caba3ec49512026380063e6f8bf`  
		Last Modified: Sat, 21 Dec 2024 18:26:06 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa9c1fb846a639722bf3edcab97cb5882e16db5673851177ba95767581d5b4e`  
		Last Modified: Sat, 21 Dec 2024 18:26:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02dd28dc2eb058530fe6d91e2907ea87978a65ea3504ed17ccc92821610f95`  
		Last Modified: Wed, 08 Jan 2025 03:31:56 GMT  
		Size: 21.5 MB (21467016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:98f79de34690ab7e6b40ce775ac4c576f27415834bceca657f7649497c4973b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 KB (377768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e296f1480a818530a8d4c01d16c4e076600e7baef8caa8a513661f6692a0926f`

```dockerfile
```

-	Layers:
	-	`sha256:918ead18bc2bb220f0ba395339819226fa12082565d00c6f01de58a2c3c6699b`  
		Last Modified: Sat, 21 Dec 2024 18:40:20 GMT  
		Size: 344.7 KB (344665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913543b701c9f8e8ed820b6d501ade94f9718157392c80c0ed4210bcb3434e3e`  
		Last Modified: Sat, 21 Dec 2024 18:40:20 GMT  
		Size: 33.1 KB (33103 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:8b17239e692930f35fb53e62135e62d56490b6bc1b23e3b38ed4a5851379d50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56397018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57d0cadb3eae3fc2722aabc6cd0023c9b6bd82ff43a13155b3c9c659322d044`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcacb882a5db1e743c34cc92815e2f3aab3e188ee2522e3208a1ed1657316319`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 3.5 MB (3485610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c95db3928cf5b057875d0344bcbb766164738b63d3ec9f076fd1b10abd46e`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17161d12eebb02d227b9e5af0a2feca4cb2817d393db01e188518657f245ce3`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c2050f484c9af7008ba83abc6ce7a010848edf6ad571a533ae73e0a90dbd`  
		Last Modified: Tue, 07 Jan 2025 05:11:20 GMT  
		Size: 12.5 MB (12545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ae2880b0747a609c8902f536ef1ec04422094651f892a4bf87ca362025084e`  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4946acdd8da5d94ce380e25c98c4cb2e6cc8c7f07180da54f8712619be39fce`  
		Last Modified: Tue, 07 Jan 2025 05:14:54 GMT  
		Size: 13.1 MB (13067183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab0346c74a235320ef204a8f1b83416913ddde772b2d036336bb225cff443ea`  
		Last Modified: Tue, 07 Jan 2025 05:14:54 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53216e192d2d31e0fed038d330ff26607712e1a1d8cf698cb88632f6c9506c67`  
		Last Modified: Tue, 07 Jan 2025 05:14:54 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e84f168090a37da8d88a59b075495a33cec5759c8b2217f0b1249999d799f`  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7544d7cabddbcb7cef6f9a33c741d386e388f089694abc61513595a11cecc595`  
		Last Modified: Tue, 07 Jan 2025 19:29:17 GMT  
		Size: 1.6 MB (1596734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f70b941d26ba3ede3bf796c8ae0446630ad6c602e2c1956de39631cb24d3e2e`  
		Last Modified: Tue, 07 Jan 2025 19:29:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d37f1b5c92beb7e48196a64d4173719cc9f33f1a1b194fa96e9176ba60b0eaa`  
		Last Modified: Tue, 07 Jan 2025 19:29:18 GMT  
		Size: 742.2 KB (742236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d5aa9a498e847db14cc2ce9235b7ded415ece46a6839996404d04cb5c7634`  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0a6aaebf62be361e588896996a9a6367d667b79b8c88d2145617bca6080895`  
		Last Modified: Wed, 08 Jan 2025 00:38:41 GMT  
		Size: 21.5 MB (21467618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:94bc006b0adb2703fd1324d29a0c93465a97be7e844c8411d65ad3421088910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 KB (373029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f547de7dddf2b53f0a1b3ae540658b201e24b984aa28b5b9d01d5549a912370`

```dockerfile
```

-	Layers:
	-	`sha256:570727d6ef47cd04d8d1deac50fd1e9a28b9f8f8b9af4ea70893cfbd52803380`  
		Last Modified: Wed, 08 Jan 2025 00:38:40 GMT  
		Size: 340.0 KB (339997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a63745720847651d72c7d4f63e75b420f9223c791f3beafec2b8a67afb5c077`  
		Size: 33.0 KB (33032 bytes)  
		MIME: application/vnd.in-toto+json
