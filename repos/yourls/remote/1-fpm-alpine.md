## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:467dc03a6fff25453ed3d769fedef65e69ef4eb15c35a1077a46eaa3624e9e59
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:12303724e8eeab7ad63834202f193dd4197ea2a3bcd3943ea9f187ccad071e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46087971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992407e702adaf19ea69c8606644a13c6d3aadcb4f755594abffb87b5e83b74e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7296391c090a8ace615ca0ccb4bfc48f26a96de409128520aa0f7c3edfd7cb29`  
		Last Modified: Thu, 03 Jul 2025 23:04:18 GMT  
		Size: 5.9 MB (5944413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec0dd61d1f32dd5e249b8bc422e5d6a5d13078627639e7f22480884284dcd14`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b550848d390f582c78d2107234c0b500a09b8c8502e8e9a5c1bb3019922ce`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0155122bcd1dd94c56b3548bf7ad573a3bee0407c5f3ac019e579f1136d0735`  
		Last Modified: Thu, 03 Jul 2025 23:04:18 GMT  
		Size: 13.6 MB (13647265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d5bebacf7cbf99d00347245602f244d1e0589fc6489a8db30e32206f4fd1b4`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef301ac054b5db0a88d5813a4420533f5ae20ee184eb2b68c949093fa1267b`  
		Last Modified: Thu, 03 Jul 2025 23:04:18 GMT  
		Size: 15.7 MB (15704841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f4cdf8eb248bd05f0a3545ee2997b8e0fd8e32fe58d9d10806991ae9a9970`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc7c3818127edbdae45e5ce7de7ccc12251d62071d0fc0361bda9be28a330fe`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 20.2 KB (20207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8ee3811d08c589ed75107c2eb29e3341400923e6c294df5662e3c3f89ab3e0`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f933e8dd5617df3a7dc96959322f7e933cc163d75999a8a44a7e3eb93843138`  
		Last Modified: Thu, 03 Jul 2025 23:04:17 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0321db635eb80ee53fdb190c59f1f6631825beb406c8321a7bbaa9bb25801d`  
		Last Modified: Thu, 03 Jul 2025 23:12:35 GMT  
		Size: 687.3 KB (687254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9317ffb54d9fb9310ea904c319aae98c30a48a5525346a1a67f8864c5da072b8`  
		Last Modified: Thu, 03 Jul 2025 23:12:35 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9d295c7357d4eccf88b41e61c355d5dafc2424f1dac25d57667181acb3ca2a`  
		Last Modified: Thu, 03 Jul 2025 23:12:36 GMT  
		Size: 481.9 KB (481903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9488af4b80bb60f9f45ef513544fe21afab790377ec3667c503c3b52a8d27`  
		Last Modified: Thu, 03 Jul 2025 23:12:37 GMT  
		Size: 5.8 MB (5767628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304cb7775bbb8c4b3093c96a013368f18386cf93b04698d78c78a8d79bfac107`  
		Last Modified: Thu, 03 Jul 2025 23:12:35 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df4aee13b15b4de3f18b66ac0890b3cfe26f5b0504fdd999ce5bfb810b97ebd`  
		Last Modified: Thu, 03 Jul 2025 23:12:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:a977db323dfa07711e2b68df00b199edca8ee65f8405572f7ca3a0673604f5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a329c387f2a1a7312dbe57abc7d7de7fc4da02ffbdb450990b7ec307dbb39510`

```dockerfile
```

-	Layers:
	-	`sha256:2b33dd0a3b06b9f5f4f3b6ec52b7f68fd0d0feec7956570e9ca3cc504dd49d93`  
		Last Modified: Fri, 04 Jul 2025 01:43:08 GMT  
		Size: 31.6 KB (31597 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:cc28ce4f9566b0264c202824497a6c1c2d3e11e685654a981b665594dc2b2316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44421391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3114145031c52f571f68bb082a4b7201b01a33413b580678ec52c5c822147dd1`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fcfa38d1163783fcd5003a8aaf644ad021dbc06430f65ddface58771cc7554`  
		Last Modified: Thu, 03 Jul 2025 23:06:13 GMT  
		Size: 17.3 MB (17342543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb3a5f1d1aaf7b3c3d64a9ff019845fb879a499b13d81ee81e2f591b87764b`  
		Last Modified: Thu, 03 Jul 2025 23:06:11 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46f8f43f25b03100cdad152a20856f255c8823e6e64b65c95724d7dc7e032bd`  
		Last Modified: Thu, 03 Jul 2025 23:06:11 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c5e45aecddbfdfef89ef9614945b390d10ff805351754bb2659f15c5d4c153`  
		Last Modified: Thu, 03 Jul 2025 23:06:11 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918725c6365d10cbd74daaf7f7412610ba97c606903149009a975221cba96d75`  
		Last Modified: Thu, 03 Jul 2025 23:06:11 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9afdcd0c545614b5f2da2e487d5c22b6b1a8603efb08a9a6c3ead518274b3a`  
		Last Modified: Fri, 04 Jul 2025 01:03:35 GMT  
		Size: 191.8 KB (191762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1d9ad057d8d54ed30ef7684f09f1272a9151bc48373c85611763cce60464ff`  
		Last Modified: Fri, 04 Jul 2025 01:03:35 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a519e20a02645be6078457e239cf4c0a23e931e693f4698ba02dbc2c701fa1e9`  
		Last Modified: Fri, 04 Jul 2025 01:03:35 GMT  
		Size: 481.4 KB (481405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f4f3c157fc415b0007b36cdad6aa4153cc316ad236737b8f09fbc35dcd38b`  
		Last Modified: Fri, 04 Jul 2025 01:03:36 GMT  
		Size: 5.8 MB (5767633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0251b7bc52522f874ea2aad10713d65b0dca3286260dbcd785d1d49fe3bca`  
		Last Modified: Fri, 04 Jul 2025 01:03:35 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79adc2f00c05112d0d9764c680881b5857fb49d092c2595d24255052af96a6b8`  
		Last Modified: Fri, 04 Jul 2025 01:03:35 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:5c2868451704ede6e57b45b21d3cb98975270d508e8f783624739b649ea0964a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7097ae227bfb9179b8557e853cd15584c70c948d8feabbb662596ec87d03f7`

```dockerfile
```

-	Layers:
	-	`sha256:78a93e5786d99d6e86be0e6240d2847a9a5c68a6c17805cb3972eef4ba303acc`  
		Last Modified: Fri, 04 Jul 2025 01:43:11 GMT  
		Size: 31.7 KB (31712 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:62a7d19721fedfb0d92ba4985b2928201c9f9e4d5a50226f6551d4281336f597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42920518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b11d92d25ec2233c3167a1f7194de38ff2c4d4e05be8c50f1f57f6198eec8f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:05f4b8d7b2257f1a6ac3d6d3cc6bf9a4b64ab9fc5d2607c301f7de2c7d6c4f46`  
		Last Modified: Thu, 03 Jul 2025 23:46:20 GMT  
		Size: 13.6 MB (13647249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41d3b4f0ee7936d37a29b00d6599e6c083cdd6c3c1e87cf67e60c78bed722f`  
		Last Modified: Thu, 03 Jul 2025 23:46:17 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0844b4fd292163d0a02861f1b98987686fe8d19804816188e674749be15618a`  
		Last Modified: Thu, 03 Jul 2025 23:52:19 GMT  
		Size: 16.4 MB (16360772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b738953951a2c0822de4033c52c0293e2a0ae0aa8e3e81be47dd2285bd803d`  
		Last Modified: Thu, 03 Jul 2025 23:52:18 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44e9c5759e1479534021c337459895a6533781d8acf8aabc422f4d4251058f3`  
		Last Modified: Thu, 03 Jul 2025 23:52:18 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321836a7945449f6f76bbbd48a787004b4391ede7da525c8635cd7b127d018ec`  
		Last Modified: Thu, 03 Jul 2025 23:52:18 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4680745d7f2c8cde09c83f435833d1be06c38a07a68fb508bac0f5a147f3e15e`  
		Last Modified: Thu, 03 Jul 2025 23:52:18 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9568fdd45fc7d5f620cacb8dbc51abcdc8a416a32894d695a37b5b57b875e8`  
		Last Modified: Fri, 04 Jul 2025 03:22:01 GMT  
		Size: 178.7 KB (178707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56941dcb916ba05f27b6bbfbca5995a097168795f19b677ef01603187e0d7c5a`  
		Last Modified: Fri, 04 Jul 2025 03:22:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaa0c2718eb6e2bfa99fbfba7e711e79a7aee6a943e8614c6f6cdc45bf6c3b4`  
		Last Modified: Fri, 04 Jul 2025 03:22:03 GMT  
		Size: 442.1 KB (442096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812960efa7cfc9b3136ac72a6ee49a3f13014e9ab3ff06b9128f1ac8fcf14ce9`  
		Last Modified: Fri, 04 Jul 2025 03:22:03 GMT  
		Size: 5.8 MB (5767628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0740b1ea45ec0c71d079cd67f9473290527c52d97adeb8ff5994ff0593cd1a`  
		Last Modified: Fri, 04 Jul 2025 03:22:02 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29bcd296a8a58ee5832e18db6bd3cd6f4c08d9dc10485d6898113c0f5923adb`  
		Last Modified: Fri, 04 Jul 2025 03:22:02 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:023d4664d00fd66c91910a813bdd7afde1b2da1227cd26cf78c6cb6fde272c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b511eb144886532b52fa13d8d37227f1b88f8660ab0926c24160b5aaa03172`

```dockerfile
```

-	Layers:
	-	`sha256:156cc6f0bc9a039dea782643cd484b11f7c559e83e3845464ce2d173af5d4ba0`  
		Last Modified: Fri, 04 Jul 2025 04:43:25 GMT  
		Size: 31.7 KB (31712 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:d101b1afafaf0ef0eb35675c4ca280fdfb71409d2f6079e94650b1047c0bc315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46320672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a154b16c00c936c946e0b61013955eb041f510a18ffdcbbd22e0695b584f37`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:8b220f2eaec9520ea981fe044dbd753069e82acc397dfa855f2a332e39b93468`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 13.6 MB (13647248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d569bf8384ea7859bc5bdebb7b303dc9b3a01a31162528b5298988b410fd2ace`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa6f9ea5b6630bf1fa8b27dc2be24f8593ae44564d56d40c3c99371c8aa816f`  
		Last Modified: Thu, 03 Jul 2025 23:30:12 GMT  
		Size: 15.3 MB (15340125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169f5a4f55ab3c20bff7182a6bcdd210d686cd4012eeba9526ed15138837f1b3`  
		Last Modified: Thu, 03 Jul 2025 23:30:07 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a464a1e1080c3a733c49d3c2e2f0e11ac984ed6384176c5abf2e75bb97ed6f`  
		Last Modified: Thu, 03 Jul 2025 23:30:07 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e8507244c9a4c92045129dd270d914d480a05351435a2cdd43733b56792506`  
		Last Modified: Thu, 03 Jul 2025 23:30:08 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e23d78e1f3a909c03ce4f6630118e37a9f8030b5bccec63dea1c36b10d7855`  
		Last Modified: Thu, 03 Jul 2025 23:30:08 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825e4e20db77a7c987a89d276d38ca39d78c0b8ab2d68a355cc06a8c7c9ba69b`  
		Last Modified: Fri, 04 Jul 2025 04:00:09 GMT  
		Size: 603.7 KB (603682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1345f4a5d07560e4b58ad9757edd4ca0a96eb39b77ce8d46c3d1db3ea78b87`  
		Last Modified: Fri, 04 Jul 2025 04:00:08 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdce1e2d2ab1186face8c041ca170c0941281a05fbee0a53b5b1a14a65f1b35`  
		Last Modified: Fri, 04 Jul 2025 04:00:09 GMT  
		Size: 536.7 KB (536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add4940cbb830099334aa1a02832a700dfe7c52d276e8f54f73e066ac3f88647`  
		Last Modified: Fri, 04 Jul 2025 04:00:09 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0bd38b482098b4c7722913d635d2e2ba89fa7a4c7d3c79ee009f61b55f49b6`  
		Last Modified: Fri, 04 Jul 2025 04:00:09 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e81622ca6923c7ebeb7346dc898652da5122f6ef92b192831ed1d923c594226`  
		Last Modified: Fri, 04 Jul 2025 04:00:08 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:ed17069886b61cb35b3c18e55efb8e9b23d48911d0f6474d8b4cc19e32eb8078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0d1886b573bd9ef9fe644a11c530f719da537af895b8371f8d2b55d9663ec1`

```dockerfile
```

-	Layers:
	-	`sha256:c8414222efeb5769f8df4c865305db00659ccebff71c178f484b969798774879`  
		Last Modified: Fri, 04 Jul 2025 04:43:28 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:22a8227958bc272961ce92215e8195e83c50e44252af4cb069bbd12f42f63022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46201073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a324928172e34813cbed09b23dd5e9504579e84e4dc3d1274c93c95f1fb9ae63`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b83c713fd8347285199bb12d3df0f7a96474084100549cd650557c4822889cf`  
		Last Modified: Thu, 03 Jul 2025 23:04:54 GMT  
		Size: 13.6 MB (13647235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e39848c0b88e9516e96d93e647520c7d526d99d1eb662f926bb1516dfdb74d`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed8b502f4a1594d4834bd22c94fef51bfbe1b77b2f88380c626646cef20e5f`  
		Last Modified: Thu, 03 Jul 2025 23:04:54 GMT  
		Size: 16.1 MB (16102665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebda5b774c2af6616a0686981834061c0e979a37d558a68eefab1c048c83315a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9077c09d448f734234cd7c5ba92e80e3045a2d9c0fdbf8f141436b7d0022898`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f9576be547cdd70eb156fe51e8b1ac950de894f800947064f2ad066920975`  
		Last Modified: Thu, 03 Jul 2025 23:04:52 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15af0b5602bfcfce087fa6782ffc80942bb855f5c44d302ec2091c6dec1bc80d`  
		Last Modified: Thu, 03 Jul 2025 23:04:52 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf02f957e2985a0b045baafbd2eee95eafc5edbbfff29538e5dc3e326f4fc4`  
		Last Modified: Thu, 03 Jul 2025 23:12:28 GMT  
		Size: 713.1 KB (713114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a029f45d8b08464f3de883b3a6256df141d2e5ec884b39bd431215a125dab7b9`  
		Last Modified: Thu, 03 Jul 2025 23:12:28 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97b8f141a97cfd1daecb92705d7c7b06e8da3ac9faa93430a1d33753295a40b`  
		Last Modified: Thu, 03 Jul 2025 23:12:29 GMT  
		Size: 489.6 KB (489623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1c2ebbbe26fc598ec3bbc07f050a27ef40074a0b4ace13c6ed984679f13ab7`  
		Last Modified: Thu, 03 Jul 2025 23:12:29 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0caf4f84d189a67dab09c2afddc3c4f77766f22fc71d35f0eb339be87e1acb4`  
		Last Modified: Thu, 03 Jul 2025 23:12:28 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae337c186c4804127abbc5a1d8c63368aec8775e358880c4436152644d800e3c`  
		Last Modified: Thu, 03 Jul 2025 23:12:28 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:1225ce7120062abe84cade271021652005b9d88dd58ea32f6ef24934431c31ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834dc6f7367db3990a7b8d54944b13250ac08e83bee279228b550a45f2e1675b`

```dockerfile
```

-	Layers:
	-	`sha256:a56b214f5c5237aacb276cc21fbd8081382633c06a2c663532c88d21fa71a8ec`  
		Last Modified: Fri, 04 Jul 2025 01:43:21 GMT  
		Size: 31.6 KB (31559 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:a718935c9ecd903c243e28dfca0d505f1def3cf12829edd41871efc8d0417a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46106042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e625b3e37aad610532730d3e5d54844a754f3bc4c75df64ffddce35621459140`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:7da4669ab0266f9dd895304e7c92d52e7df1b0acfdc30e6abf0d73fd20c6d09a`  
		Last Modified: Thu, 03 Jul 2025 23:15:37 GMT  
		Size: 13.6 MB (13647243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdb584c1e59e66bf7047b954cfc1e41ae7df62560b963934f349b9bd0a11fed`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec4c098d64fe970162d27f119fafc79780b52fb7ecd162d800c94abf01e685`  
		Last Modified: Thu, 03 Jul 2025 23:19:36 GMT  
		Size: 16.2 MB (16180101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c51e014cc90f32922752857a7a0467fae4a7abe39ac8d84124b875134391b7`  
		Last Modified: Thu, 03 Jul 2025 23:19:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef4fe6bc3c0dba9b0b0be97b4ac1625304ee2e588768da9946bc9eb914fd100`  
		Last Modified: Thu, 03 Jul 2025 23:19:33 GMT  
		Size: 20.0 KB (20010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c1a037250e339ca28064a76ae07f61a0b41b0bb625d58f85287052f01793ca`  
		Last Modified: Thu, 03 Jul 2025 23:19:33 GMT  
		Size: 20.0 KB (20004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2481dfe4f103b868aab994e5f60d09938996cc3ce5fc4fe20263c9338b0b8f`  
		Last Modified: Thu, 03 Jul 2025 23:19:34 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f3b6beb0f68e839c4a9bf3c4f41d11e70fb37e7f8194ea3dc7e3e988254844`  
		Last Modified: Fri, 04 Jul 2025 02:23:16 GMT  
		Size: 228.8 KB (228763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf72ad354623e9b078eea860949c0df56ed0d55eaf964f496c435d9cc78937`  
		Last Modified: Fri, 04 Jul 2025 02:23:15 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6f41cc2087c9baf4732d532bd4ad5601a3ad707336147b6aadb32dca3f7e4`  
		Last Modified: Fri, 04 Jul 2025 02:23:17 GMT  
		Size: 547.7 KB (547740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e15990caf0b6539005d7971fc1d1a4f84744a6b3c2f0a2379a56c648213f8`  
		Last Modified: Fri, 04 Jul 2025 02:23:16 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ff99fa92cd8c952295a51dfcd26b706044c8af676b86db8b9cbe0e0d3b2df0`  
		Last Modified: Fri, 04 Jul 2025 02:23:16 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413e2dbf0cb52839ed3a92ac2690791afcee2b6ecb81c35bcb56b30a5e8f8f35`  
		Last Modified: Fri, 04 Jul 2025 02:23:16 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:869a9c266f8c5565309177ac334b577b1ba55ebf628d5d60f51d5dc4cc036f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b918543b624ddd7576e197dbe2308c3f808c04a6a8a71ef2960d1be71f3d0b`

```dockerfile
```

-	Layers:
	-	`sha256:c5f96e3f4252bbd0439858b64679eff2e50d8ec9dd31a844a7063b6922b3a722`  
		Last Modified: Fri, 04 Jul 2025 04:43:33 GMT  
		Size: 31.6 KB (31647 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; riscv64

```console
$ docker pull yourls@sha256:98dc2e3ecf0a2a47c44b439cf49ba356f5d056a04b26878cf2995157e3d7be32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45535140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5bd46b388e56b0e4c6b0cf3b5fc4d32c10fd24045efd9eb9c93000591a0af3`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:3fef9af04f77cee78d12af5c916be05fdbafab520d953b27a0e22aabf6917d85`  
		Last Modified: Fri, 04 Jul 2025 00:22:03 GMT  
		Size: 13.6 MB (13647251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae4f98ceb1c3250752dcd6d2b2322a49e9241e8b32b996d4fc611be6bbb87a6`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c669d50b9c8ce3ad5848d6b4b65326dd6c222b336b6e7705ea610607e7c06ec`  
		Last Modified: Fri, 04 Jul 2025 00:22:03 GMT  
		Size: 18.2 MB (18247439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0eba8d0ddcdcf6f9dbf9dc6a0e365d08a0dcb819ceee022ed8c6d74befa08c`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf3048185d9cc4407793de406112a3b8f83f14ce34c850a48d9dc8e0e71c8e9`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9904f49cc61410335ff80ea6fe9ab2fdd8146ed0e6ba8cf9c16fcdc62b6851`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76b953fe83d47b6b40ead94cbd2520e5e26c9721918e7b97ceea55136342a2a`  
		Last Modified: Fri, 04 Jul 2025 00:22:01 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeca3fd43d3b8e979e69dc047c10e44264098299b03b3170b2b3fe8979bd0a49`  
		Last Modified: Fri, 04 Jul 2025 21:25:32 GMT  
		Size: 204.4 KB (204392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54932a6b84129f31ccfcbf3c968ec91f8a3203608a6ca1a146ba44fa8a7a4f89`  
		Last Modified: Fri, 04 Jul 2025 21:25:33 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b8d452ae48f58c19d3be98a12025cac9f3e82a6536e6d1456da9449bb593c`  
		Last Modified: Fri, 04 Jul 2025 21:25:33 GMT  
		Size: 493.8 KB (493845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79799533047382a4f3297f40832a2ac4e4ae555b136ee2c359c2f71ec25d30`  
		Last Modified: Fri, 04 Jul 2025 21:25:34 GMT  
		Size: 5.8 MB (5767628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ed727e5271358cfda0af29463c9b9485f3eed69423afe5d918c870b5c1f38f`  
		Last Modified: Fri, 04 Jul 2025 21:25:32 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ce2f22584cbf4da1087dcd3fa37ff969a36238cf09373bdb18bee08ba21b6f`  
		Last Modified: Fri, 04 Jul 2025 21:25:32 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:f8bceba06a90418a7c711ae6b88f65c2a91ec8f8adde3a92e7c6eccc32dc91a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf6686a7ac70899dd365a494e0d6062e7926d69fedab67a13fbb27e9d862add`

```dockerfile
```

-	Layers:
	-	`sha256:d6bc5d7dae8e2bdea1fa58a3af893b3f97d58f6f0f2bc56452510c03dbc8939c`  
		Last Modified: Fri, 04 Jul 2025 22:42:38 GMT  
		Size: 31.6 KB (31647 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:afae4b94d8c1a10840494f005f5c32732c7d5301af2feb03cf7a464f95914dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45673095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92de9625069938d5c9c7edb613bb321e0df9de5a9d82d85cac0b1acef4aba18f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.10
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
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
	-	`sha256:9da3506587d8ded424a7c5730d972ae6f1735f6afc1a325c7e9f83474f399fde`  
		Last Modified: Thu, 03 Jul 2025 23:16:27 GMT  
		Size: 13.6 MB (13647264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a375a1790dbb9b0d83c7dd0560e7f6e75fb5b06afbc76019557052c897e5a`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703cfd663fc43412b88dfa084b4207ae1143207267240f30900fd46796d51b14`  
		Last Modified: Thu, 03 Jul 2025 23:21:19 GMT  
		Size: 15.9 MB (15889948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cf456d9fe653d20a3441645f93978816d2f3f95d895dcdd44faf0b6145436`  
		Last Modified: Thu, 03 Jul 2025 23:21:17 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c7bcfe1b618f416c55a8d771e45ade44ad7fa9efb85acad4a702a67b47950f`  
		Last Modified: Thu, 03 Jul 2025 23:21:17 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae4563063b30cb9a183dee188a4f7d45a44c915384503adf9d0622b034f113a`  
		Last Modified: Thu, 03 Jul 2025 23:21:17 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43c28256ca920d8f1b9f712b5403facee0d57a3fa394350c125865ee1f9c2e8`  
		Last Modified: Thu, 03 Jul 2025 23:21:17 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6543885589e781cd47138da3729a7101edd44fd0c8184b84ceea19ab4f1e373`  
		Last Modified: Fri, 04 Jul 2025 02:00:27 GMT  
		Size: 220.1 KB (220085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bf85dec5cd478a2a867f249e7e489a4236633df6ff2b3678f312ecbc42eb7f`  
		Last Modified: Fri, 04 Jul 2025 02:00:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94468ce820c8fbd2cfeed01eb6f170e4e3bdbc47635d71649e2792eaa3d7ca7d`  
		Last Modified: Fri, 04 Jul 2025 02:00:25 GMT  
		Size: 510.7 KB (510655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2eaa177460de6561b310c0253e58ec673e380d33f57af21f186f20ae3c92e`  
		Last Modified: Fri, 04 Jul 2025 02:00:26 GMT  
		Size: 5.8 MB (5767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc13ecf5368f7743729d08c1c06a68929f426d21aad99eed0b5bbe92b17622`  
		Last Modified: Fri, 04 Jul 2025 02:00:25 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045917a28f07203eeeb96210257cbbc62aa6b1e9649877e2ea70cf14928fc918`  
		Last Modified: Fri, 04 Jul 2025 02:00:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:08107dd038581132e32e3d4f1564f3113af98c14e1ed1dffb9fe47ced64a1b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b5933e90e90741b6052f9817a4facbb95d390862b878486794c0fad15b75f6`

```dockerfile
```

-	Layers:
	-	`sha256:8bbc73116135a4ec1049f85f744c6faf6283ee7abef6941ce898ecf1a16ec0cc`  
		Last Modified: Fri, 04 Jul 2025 04:43:38 GMT  
		Size: 31.6 KB (31597 bytes)  
		MIME: application/vnd.in-toto+json
