## `drupal:php8.5-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:6f8f1b99b2d76f45902eb5f2d36e55cc010637e2e449eeb903327ad069ab042e
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

### `drupal:php8.5-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:9934caa939bef1ca271ca32bc1b958e2658ae0ac73a97b10c13ed453ba6f17b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65630510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe58f50ff6a750eea7b004f7cbeca6c8e93ee42a69d963f3f2d794e23ccb57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:15:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:15:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:15:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:15:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:15:49 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:15:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:15:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:18:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:18:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:18:42 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:18:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:18:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:18:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:18:42 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 22:13:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 22:13:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:13:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:13:02 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:13:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:13:02 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:13:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:13:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1b91efc881f03194ca5ce23fa120cf07af1fd1cf7ca7739de3e5209dbb9d`  
		Last Modified: Thu, 09 Apr 2026 22:18:49 GMT  
		Size: 3.5 MB (3464803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987748fe1cbea95f65bca08149d906f2f11bb652bbe293e8d84fbdef7631e698`  
		Last Modified: Thu, 09 Apr 2026 22:18:49 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2f4efe85432d91145d3a98a3b29af8dc45a55eceeb2f53e796066646a3d321`  
		Last Modified: Thu, 09 Apr 2026 22:18:49 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd66c962c724fcbe0646a83aef91d4e813c5db4bdc2fb7a0a24be8f5e07e1a7`  
		Last Modified: Thu, 09 Apr 2026 22:18:49 GMT  
		Size: 14.4 MB (14376835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24bca05f64da291b2f170a85e70175cb8afeb114a95b395204d974a90124e9`  
		Last Modified: Thu, 09 Apr 2026 22:18:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8a7bf647d7260bac0e738704929ee95b9284cb3300a7fadf5561e4bb8a642a`  
		Last Modified: Thu, 09 Apr 2026 22:18:51 GMT  
		Size: 16.9 MB (16903133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b68650bd6315ab7801a5be67c8dc3fd79a60acd4da1cbc021269523e0c3af8`  
		Last Modified: Thu, 09 Apr 2026 22:18:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4af1adb811651e09e0aee2841d05e09a44ca368d1a09b510a5294ac2f42839d`  
		Last Modified: Thu, 09 Apr 2026 22:18:51 GMT  
		Size: 20.1 KB (20110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3879d3a2cb109cbbe1ceaaf1d8982011ff3683fefcf2f1abcf89790a33035a`  
		Last Modified: Thu, 09 Apr 2026 22:18:51 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380399bf4b771c94f8e5d75de0e60ff31367876de6c3ec8bd7963feb135bb7d9`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 4.9 MB (4922838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffffd1a758c9a7aacd1a1090ccee4b3cbc24234034e07faac3521cc0cd07569`  
		Last Modified: Wed, 15 Apr 2026 22:13:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2840134ca4293a483de5a9e5f0d6e5f2d354f499b56f1af31369618df3bf6b`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 790.8 KB (790770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece6bc74eae526f41ab6c2850e31b8fd4b76895ef7366e5a615a39fcc2671fc0`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d0cf0ef55f634a22ea1095fcaa743b3a5e0bf124bb66f44b301c11104df388`  
		Last Modified: Wed, 15 Apr 2026 22:13:25 GMT  
		Size: 21.3 MB (21333338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:6f0085c242ef1be70efd27c48eafd57f8c8db62163d236f23a9d58b330a0aafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.1 KB (408065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cb94be95362265b08c1511b09e6cd789bda5f9ace25485284b430ecf753f67`

```dockerfile
```

-	Layers:
	-	`sha256:4623d0ac759506fbc210f0551676a20db43d67f90bc3f25c1b7e0ad5bf98bbb2`  
		Last Modified: Wed, 15 Apr 2026 22:13:23 GMT  
		Size: 375.8 KB (375796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a629aa38b62bd2d06c636027ae3d84b74b05fadc8ab5caaac18bd6d5268659`  
		Last Modified: Wed, 15 Apr 2026 22:13:23 GMT  
		Size: 32.3 KB (32269 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:9374d1614f6bea7aea6efe137b36ff00c0d0ba82924cdb135b2e703a39335027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62744380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95aa9c844dc4aca4a5c8b0adc01e5905b686177111ab02d4ae989eaba57ae5ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:12:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:12:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:12:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:12:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:15:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:15:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:15:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:15:34 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:15:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:15:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:15:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:15:34 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:42:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:42:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:42:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:42:49 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 21:42:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:42:49 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 21:42:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 21:42:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ea279ecd0622aada20637a59ba54b46230d0656d6e893aeb1ee5cfcac3990`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 3.4 MB (3428886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d73f80330efb23e6103a6dc569942b96ab7c5d6cd3f68512bdcc759b9bbb7c`  
		Last Modified: Thu, 09 Apr 2026 22:15:39 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c889f4c4f1ceeb5b6f1cee6f8e7b3f641d8f57fdc317672846df9c2c0e9b0810`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69111cfb621b923f9fe5ecc7f4f000ce4e91f65fb4036221ad4f00e12ac67093`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 14.4 MB (14376826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86ce46506d12851c95471eda7ca808f4eef98439a52f5926d744e3ceea78ecf`  
		Last Modified: Thu, 09 Apr 2026 22:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2943078ed708c762dd5f8567afaeca37d219fb608386ae32694e4031d93b39`  
		Last Modified: Thu, 09 Apr 2026 22:15:41 GMT  
		Size: 14.9 MB (14854238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fbaf960fab7b808477b70d2505ad717d9a25135020c17560e95401d9958aeb`  
		Last Modified: Thu, 09 Apr 2026 22:15:41 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d7ee40eba9054524fa1cfd2d83339ed8597d6716da679fe2c6d42510e006f`  
		Last Modified: Thu, 09 Apr 2026 22:15:41 GMT  
		Size: 19.9 KB (19900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dee4233688caa3f91435fdb54f502d88cbd32e0b38844f8b1fa576f6a3896e`  
		Last Modified: Thu, 09 Apr 2026 22:15:42 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d0da91233c2403663ab67a5e9ed1ab260fc6104bf27b8042fc98f193ba97f2`  
		Last Modified: Wed, 15 Apr 2026 21:43:06 GMT  
		Size: 4.4 MB (4420464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78434ce2811d2bf3b1f78490f968d12714fe9a6fe7d7d0e2b87b50d0d5725b1`  
		Last Modified: Wed, 15 Apr 2026 21:43:06 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e964c113366203fb78f02f7050f943e9612565139376eca37a4a029aa266a6`  
		Last Modified: Wed, 15 Apr 2026 21:43:06 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa47939db2e04c518477572653578a9e104417d92fe3fbd5c23e08a65de8afa`  
		Last Modified: Wed, 15 Apr 2026 21:43:06 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50085f82a1613eeab1238703e6fc7083e4c27ce9145e76cf73dbf2ddad0f335`  
		Last Modified: Wed, 15 Apr 2026 21:43:08 GMT  
		Size: 21.3 MB (21334449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:f637b2df39cde9bceb083e65b3885457384147fa102da02d0b79a0f3465d4911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455ddc00a815bf2de678795fca1ddf3821be9fba75606f1490de3a553e3d46bd`

```dockerfile
```

-	Layers:
	-	`sha256:71569c73f16694414fc15a351689db7772fe3dcb831a21388fe5b6a408cfe02e`  
		Last Modified: Wed, 15 Apr 2026 21:43:05 GMT  
		Size: 32.2 KB (32182 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:0e9c834f5076d241ff7a949ba3d3c171cd530391d689214cdfdf943883a62055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61139989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93e903274e25a6c6858106b918570b252a7f6db8bdebcc7558082be52b42223`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:22:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:22:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:22:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:22:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:22:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:22:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:22:25 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:22:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:22:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:25:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:25:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:25:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:25:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:25:42 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:25:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:25:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:25:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:25:42 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 22:20:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 22:20:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:20:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:20:55 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:20:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:20:55 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:21:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2372db80b6bdf5cc06e7d13637a6af64fcfe85650ec8281428952677065a3e20`  
		Last Modified: Thu, 09 Apr 2026 22:25:48 GMT  
		Size: 3.2 MB (3244512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc527a2475f4119d95b18339370aa289c68c33350cbf4b9c3d4bf3e61598964`  
		Last Modified: Thu, 09 Apr 2026 22:25:48 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c2d13afbb4d45c69fc2d3dcd73e002e736b1bf0462ca5bcc00ce4c86015ed`  
		Last Modified: Thu, 09 Apr 2026 22:25:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea317624e7716ac96ca3b9060f7b2d4713bb8af1b8e3a675f222d47db6f78b48`  
		Last Modified: Thu, 09 Apr 2026 22:25:48 GMT  
		Size: 14.4 MB (14376836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851ad20143c963b9e413c4095b52a61124c8cc658724ba6f89643fa68d0ed94`  
		Last Modified: Thu, 09 Apr 2026 22:25:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59874d61bb2497daafa113d15913092b8dbc24f43e9231216db6bf07a509a7`  
		Last Modified: Thu, 09 Apr 2026 22:25:49 GMT  
		Size: 14.0 MB (14039184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf473f47ecc897229d536abd3949c40fa576f53951312b8882d03c02c8b664f`  
		Last Modified: Thu, 09 Apr 2026 22:25:49 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6688f347438344d1b09f1f6862370b995379aa10984dd6b9b592f752a46616b`  
		Last Modified: Thu, 09 Apr 2026 22:25:50 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe2e840fa6955690155043e5a10e85602df5a293dca40410f0b23d5d5bf2a5b`  
		Last Modified: Thu, 09 Apr 2026 22:25:50 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d60e97a8a7b3e23b265fb8da4d8a475833eb34a3803670b64664df35c151809`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 4.1 MB (4097317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8462a760a206bbc6abeb77bbf693cd02077f17e7fd883363a2b7a85a935e6de`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef153583eca007639d007ea772fafe3a7aecca485f031170ac544e1bfc34f6b`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d86b84729601d865b6fb621343b17618caa4e33c5ff85389e69e1b8dc9857`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09614837f1ea3a77f4409e8a954044f4565316cb046fd1e56d690bd43f2fb262`  
		Last Modified: Wed, 15 Apr 2026 22:21:17 GMT  
		Size: 21.3 MB (21334037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:f9ec320d0abe85383d2e75458515a09c2f94725d4151cf492a504eae01eb2af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.2 KB (405239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0066c20d1601fdf231af368ae1f7670df0eca808e4d6c0d80bc579bce30b433`

```dockerfile
```

-	Layers:
	-	`sha256:8af8936e9872e27bcafed6a0cb33b5b32f57dfd27c3c9845e98fef9c76e64fc1`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 372.8 KB (372842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c1b24ec7f1bf3aa307bfdb5404f24c3ed25cf33a3370d3da12e085f5e6dd774`  
		Last Modified: Wed, 15 Apr 2026 22:21:15 GMT  
		Size: 32.4 KB (32397 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:76f0221c84a57fb36613d79fb8603767947a6d17220c2022c98b7d47a13aa25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65785837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e611c7853eb89fa551e02342026da3f25e0e4d16734e05a7d0a02b291f938c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:16:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:16:18 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:16:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:19:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:19:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:20:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:20:00 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:20:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:20:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:20:00 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:20:00 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 22:25:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 22:25:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:25:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:25:03 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:25:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:25:03 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:25:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:25:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f1a71eeafcb389fcb804d748848c3399bf9e4bd5647437d69b38b29271c9c8`  
		Last Modified: Thu, 09 Apr 2026 22:20:07 GMT  
		Size: 3.5 MB (3467258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c079efddd4e9d59760913641656de716cdcae9926077bd9df1d9aad83de1327`  
		Last Modified: Thu, 09 Apr 2026 22:20:06 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ccedff6018b2249c0224bf3a7da506cac90242d5f1bb29ad1749de35b142ef`  
		Last Modified: Thu, 09 Apr 2026 22:19:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9697f63f743e702e659947b0bada88504e774a9493389dc666950ddcbf88747`  
		Last Modified: Thu, 09 Apr 2026 22:20:07 GMT  
		Size: 14.4 MB (14376827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee1590f235bf45796937942d905777bc81195fe116aafb9e889105b6a658ff5`  
		Last Modified: Thu, 09 Apr 2026 22:20:08 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbd8934a68914ffccdca5ce61c240d3aa03b6afa12ec04a3a8ac2d939ea4679`  
		Last Modified: Thu, 09 Apr 2026 22:20:08 GMT  
		Size: 16.4 MB (16437630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f1dbb056bc330264ba9c605726dbd0b2a62c446b7b9aa3859167641a4eb87`  
		Last Modified: Thu, 09 Apr 2026 22:20:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405ae466e08d01b3ef6b1fde3093493cc3673771157107068f5d97732f0032d7`  
		Last Modified: Thu, 09 Apr 2026 22:20:09 GMT  
		Size: 19.9 KB (19906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e885891ea6bd8433a94a9670a1a90abed18e5ede896e59251ce5fa696c2453c4`  
		Last Modified: Thu, 09 Apr 2026 22:20:09 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b12094d8f4ef12ba2df27027ab778c2b0c56b685715e2b5f5fcf7ad3a566fa5`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 5.2 MB (5206279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206314f72a9da763e34372597c32041cf692e9b4746bf8506ab2afbc446ee2c0`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1566635634bb6a76aca6585f64af238b25f173c2e0ff1d9c48ae7707b7c269ed`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 790.8 KB (790758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf8456bf7479375f1c0e95a66d67ff107f6d2fbfdac2e6e8edb7ff6b82ff333`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d06ca31481e403a38cfe36ab1d0219c860ffe67b86c890567ca24847bd9c3b`  
		Last Modified: Wed, 15 Apr 2026 22:25:26 GMT  
		Size: 21.3 MB (21333851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:13941114d346f26a7518f585faac1b81d7039f1325b0fd020f4fc23f52e6867d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.3 KB (405291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc86fdb2aa8945800d12418a096f6151ab1d53df3b77c695d77e2b9b97405dd`

```dockerfile
```

-	Layers:
	-	`sha256:b003df3ed733cc8b9a96ebc7a4008de031a1ad5f132ab23d4d25f9b1b7573480`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 372.9 KB (372862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d96c61071eb688663a6ec5f279a76041d65763b7050761a8f82fecbc66ec23`  
		Last Modified: Wed, 15 Apr 2026 22:25:24 GMT  
		Size: 32.4 KB (32429 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:5e0ea69f738a49404b04b5b9e53642d9bb6798e8fc77aee8bc63a0d1e50e52fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65359437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89134625e911d0604da64d9f53336661fe0bf1b2222c157fce2190439746901f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:16:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:16:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:16:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:16:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:16:48 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:16:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:16:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:20:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:20:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:20:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:20:28 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 00:20:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 00:20:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 00:20:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 00:20:28 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 00:13:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 00:13:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:13:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:13:27 GMT
ENV DRUPAL_VERSION=11.3.6
# Thu, 16 Apr 2026 00:13:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 16 Apr 2026 00:13:27 GMT
WORKDIR /opt/drupal
# Thu, 16 Apr 2026 00:13:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 16 Apr 2026 00:13:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcf5ef7b1191983b2bc720948e9af8cceb205f717ef3a998d3cfe343e4dba26`  
		Last Modified: Fri, 10 Apr 2026 00:20:36 GMT  
		Size: 5.8 MB (5807174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f44f433fb8a31687dc2de9e88ffa88b53e69e3ebe1728c7daa2b92fa7fcd5`  
		Last Modified: Fri, 10 Apr 2026 00:20:35 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449cc8e6e45c3a193462a7653f861b66b6a7ce0be6d2998fb61d343d533a856`  
		Last Modified: Fri, 10 Apr 2026 00:20:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1d360e97c3175cd0daecbbb4b4db85c9fe28816a21b4cd9b7c616f646ce164`  
		Last Modified: Fri, 10 Apr 2026 00:20:36 GMT  
		Size: 14.4 MB (14376833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e8d4c1711daa5f6aad1183f7a15fcf712e9526270a78ccd09d45a548393f4`  
		Last Modified: Fri, 10 Apr 2026 00:20:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0114f895accc1a52d1650f5167a5200a5fef9738e55b9fce08703301fa6a9690`  
		Last Modified: Fri, 10 Apr 2026 00:20:37 GMT  
		Size: 17.3 MB (17341430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a377da92b5f2e29ed3fd82cf083402b8cfef8fb689df5e0862a4a65b9c024be`  
		Last Modified: Fri, 10 Apr 2026 00:20:37 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e365794955b7c086ef2b4f8d6b4a8294de41d95b19e38cab16fbfd34617e6`  
		Last Modified: Fri, 10 Apr 2026 00:20:38 GMT  
		Size: 20.1 KB (20087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ab9d993aad36f84d0337422a096c2ca9bae7490845aef4eb260316a74c4a4`  
		Last Modified: Fri, 10 Apr 2026 00:20:38 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a409dbfed8a0aa67b25a1b77124423f1718b8c60cee4c224bc23cfd677d43`  
		Last Modified: Thu, 16 Apr 2026 00:13:44 GMT  
		Size: 2.1 MB (2054426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864e31de51dbe641f86728567cd87bd9b09246592133081bc41878a5b39b26f6`  
		Last Modified: Thu, 16 Apr 2026 00:13:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5e71d55d3362608254ec7a8d9454ad01a5b9cd74487d06af530dbc5123fe5`  
		Last Modified: Thu, 16 Apr 2026 00:13:45 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1d76a4cf29d40bbcd066af58e9966c3e6a56e72105927e4f9d29878d8a716`  
		Last Modified: Thu, 16 Apr 2026 00:13:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ccb010eb90951378f5c492da73dc1a2d6238c2f81a8f3a8b82965fd017c28`  
		Last Modified: Thu, 16 Apr 2026 00:13:46 GMT  
		Size: 21.3 MB (21334185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:aeee4e5ed1dcc76ed4b0be296ffb789bc3208830a658c61c4058e3e1a6b64010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 KB (407997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13565867fff9e79beedc316108df932a070e5ef3daa38bfda9f25fcab313f907`

```dockerfile
```

-	Layers:
	-	`sha256:41dd63db32394bed7ddbcee76034742d73ede4013a9a9ba5aa1149bcd8d04506`  
		Last Modified: Thu, 16 Apr 2026 00:13:44 GMT  
		Size: 375.8 KB (375771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1586faec0cd9b0db4cc231dc90105e39fe06f8ce7b808222ce32ee94d5217b12`  
		Last Modified: Thu, 16 Apr 2026 00:13:44 GMT  
		Size: 32.2 KB (32226 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:841b423e6d21c5c21b6d3fc2df521a7aae523f171e0e78494147d3596043992b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64795133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecd533af5f38b6f7fdd2c1303e7c87939f14153334958b23106942c20de12e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:40:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:40:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:40:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:40:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:40:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:40:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:48:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:48:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:48:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:48:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:48:16 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:48:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:48:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:48:17 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:48:17 GMT
CMD ["php-fpm"]
# Fri, 10 Apr 2026 01:16:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Apr 2026 01:16:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:57:08 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:57:08 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:57:08 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:57:08 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:57:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:57:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f75f0d68fec15e86a66bb1163cc325a06b9f5675b56ea20c405cce5e7adb7a`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 5.9 MB (5945783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7eb72ca6c1423ccd1a389d0bbdcacbefca48fa8957dce2abc28e75dd020a9c`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2109b462465754c71efb3d3c36c4659284495e4e79c59797b775c9caa59c469c`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f13bcac7bf61abf25a28b90a21275081584a7865424b10b02b8f7ab47b9fbc`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 14.4 MB (14376865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a36dd963263d7ab52a46e41d6b079d208e3d3a22b1449a2b4fe3afed333e92`  
		Last Modified: Thu, 09 Apr 2026 22:45:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0bdec1cf90dae27b358272272f5cfb0c94718a2bb382fe2e1309c7078a88ef`  
		Last Modified: Thu, 09 Apr 2026 22:48:33 GMT  
		Size: 17.0 MB (16963984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f8e248dd4b627e2ccc8177298cc666a71ae7a2801db7c93f429394d4a6fa6`  
		Last Modified: Thu, 09 Apr 2026 22:48:32 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d32dbbf59cfcaf40dae8c4e03df1244b8c16a6c6be1f680cee1ca4d257c3904`  
		Last Modified: Thu, 09 Apr 2026 22:48:32 GMT  
		Size: 19.9 KB (19916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8359b3b249012d0cb05909277107971934c2a8897f7c9cdb185456e4becf6cf`  
		Last Modified: Thu, 09 Apr 2026 22:48:33 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a11c0515e8cb0c7d2bfa4a4aa4c16b40de95d2e860e28dfb8af8b985fff3c9`  
		Last Modified: Fri, 10 Apr 2026 01:17:47 GMT  
		Size: 1.6 MB (1615338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61b8f74f5958ce490c2229fd83fefa98f45e0bf014c049af9740f4bdfc280fe`  
		Last Modified: Fri, 10 Apr 2026 01:17:46 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19246ae9d3736ef7de266c532bddad6bc5f6f447b591778d0d9540d9f1767d`  
		Last Modified: Tue, 14 Apr 2026 18:57:56 GMT  
		Size: 790.8 KB (790767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bd441593ab771a54bb2f79d9121a654c8b5ba08b16a404da235edec53279eb`  
		Last Modified: Tue, 14 Apr 2026 18:57:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6262eddd16f0bf7d20e1922f971aad280edafb693a1a8c014bb76223646625d`  
		Last Modified: Tue, 14 Apr 2026 18:57:57 GMT  
		Size: 21.3 MB (21334364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:92c04b60efd5b3edd732cdd1280aade534dabb3acf535106e2c824b5aedc72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.2 KB (403216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14e8fd92808ff755a1b3e568648e582a79cbd68a49d6d3080abe9bf594e1ef2`

```dockerfile
```

-	Layers:
	-	`sha256:013b0eb3818540ca431f859491a717ceac9a1850911b5acbbffeb32e05514d31`  
		Last Modified: Thu, 16 Apr 2026 03:51:41 GMT  
		Size: 370.9 KB (370889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6ec5e496ecb2a6325d617cbd00264625d01cbcd4b8b6124f453e9e7930ffb4`  
		Last Modified: Thu, 16 Apr 2026 03:51:40 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:b9173ee9d411357c74e0e2d569112f6b3ae432997d6e24fb031de9fd5c4df8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60446415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92b52c4fccbe8aa35d6e5823c744760e1bcde044a1dc80660b3267ac5e38ffc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 02:06:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Mar 2026 02:06:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Mar 2026 02:06:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_VERSION=8.5.5
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 12:34:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 12:34:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 14:33:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 14:33:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 14:33:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 14:33:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 14:33:47 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 14:33:47 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 14:33:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 14:33:47 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 14:33:47 GMT
CMD ["php-fpm"]
# Sun, 12 Apr 2026 23:49:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 12 Apr 2026 23:49:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 19:11:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:11:40 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 19:11:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 19:11:40 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 19:12:21 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 19:12:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcec5e28255dc0e86ab83e16a74b5c1c525134a3732aee9e431f8cc84bce27`  
		Last Modified: Fri, 27 Mar 2026 14:21:20 GMT  
		Size: 3.6 MB (3600619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570e48bf7a46da44ec0d6ff793a75c8aba195204deaed906886b9c3172e561d`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a134d0a16baab5e83185028e3a86fe467859436a2b79af399201c18fdf43c`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8809d113e7278087420df60ad8c2e846e373c947dd4c9ae8a8d3774d62e10854`  
		Last Modified: Fri, 10 Apr 2026 13:33:59 GMT  
		Size: 14.4 MB (14376825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8ef0a328b411214db4b3c0e9c57449fa68317df2e1dd876b27a19438009101`  
		Last Modified: Fri, 10 Apr 2026 13:33:55 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4037e3d3cae75ea2b5964e40b25a066d484edfca2c7920dc81a3d530cfef085`  
		Last Modified: Fri, 10 Apr 2026 14:34:45 GMT  
		Size: 15.4 MB (15376036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662298cf2d8eb732ce4dc42c1736b2971dbbcfc059c42fb8f1f0a87f3ab9717d`  
		Last Modified: Fri, 10 Apr 2026 14:34:43 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfacc4d35e3bb8e595f2f993f061cd6436164c7ce4e0309d7a4f1650d5e2e97`  
		Last Modified: Fri, 10 Apr 2026 14:34:43 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c987a1b102cb67842f09058c5ee6673be5c5924bea4118d6ee67e9f66b392fb`  
		Last Modified: Fri, 10 Apr 2026 14:34:43 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ad202f151a753e719d86e545bba4a27e049dd79effa297f5a5fc9240cde4a`  
		Last Modified: Sun, 12 Apr 2026 23:52:37 GMT  
		Size: 1.4 MB (1415770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893daeaa9f3a59ce9c362fe15303fead1e33669b1c7e660bf5da9168a2bb6e6`  
		Last Modified: Sun, 12 Apr 2026 23:52:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233beaa6267e1b3f040db67a1e63c1ab02efaa5770f52a7f4cf3422b821e7f82`  
		Last Modified: Tue, 14 Apr 2026 19:15:03 GMT  
		Size: 790.8 KB (790767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed8846f5dded645fe1a9b150967b17bdc11ac50f5c686cc7680b0115961c43`  
		Last Modified: Tue, 14 Apr 2026 19:15:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96edc2bb507c16e507ed2cb4f9b262508ae0f87ab952ddddc77df99161823a61`  
		Last Modified: Tue, 14 Apr 2026 19:15:06 GMT  
		Size: 21.3 MB (21335291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:cd43f5fd1d0bf15689fac82e6bd9e9f0684b2245690a81a15dbeb2ae10c51e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 KB (402189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00e88cd3813d7ddb718b4f323707559a0988531199396899442dda1b3740c2`

```dockerfile
```

-	Layers:
	-	`sha256:51639f340f265ee3fd3ec13b6591e12b3935865a31213c3f188ede3ff0f6ebe0`  
		Last Modified: Tue, 14 Apr 2026 19:15:02 GMT  
		Size: 369.9 KB (369862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68a27541fd9207c87175871926cb23a33038c7262418b9a0c6dda2907cf0404`  
		Last Modified: Tue, 14 Apr 2026 19:15:02 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:768a20e76358bd2909e27fa0fbcb816134cc5fa29af08b6d16059cfa129a25b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64502854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8376e92da15b6840998e3067e89288409d664f0f9c83bb642eec9118b8931`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:27:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:27:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:27:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_VERSION=8.5.5
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:27:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:27:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:33:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:33:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:33:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:33:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:33:09 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:33:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:33:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:33:10 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:33:10 GMT
CMD ["php-fpm"]
# Thu, 09 Apr 2026 23:33:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Apr 2026 23:33:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:59:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:59:34 GMT
ENV DRUPAL_VERSION=11.3.6
# Thu, 16 Apr 2026 00:59:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 16 Apr 2026 00:59:34 GMT
WORKDIR /opt/drupal
# Thu, 16 Apr 2026 00:59:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 16 Apr 2026 00:59:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03f78560b492a6a896fc1de4f8b2a22350e0783e19d18796a0368ece29fe5a9`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 3.7 MB (3693214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c5c3db78af4ad975f687ea0000215b60b8309556794377c339f416f692db1c`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7da6b53b99bf8fc44dba62cc974863447aca25c57f7278ab7db5bc687338c`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da43aa84f8f4d4981def1dca2b99ce7a66048869e8ba8d889abf542096a03af`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 14.4 MB (14376850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7207cb3c4e21204d529910faa86c738557e94d48027c6938441a29d64d74bf5`  
		Last Modified: Thu, 09 Apr 2026 22:33:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c335bb7ab94bcd9adbf7a8ba8fbf8264246fa0fa1b58a197c763adc59b06ce`  
		Last Modified: Thu, 09 Apr 2026 22:33:23 GMT  
		Size: 16.3 MB (16311466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f508f84bee50119416f89500ff4d9efd0a5785846109e13907116a7b7477a19`  
		Last Modified: Thu, 09 Apr 2026 22:33:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc52f8acc10f5ce6c27a44be1a8c21b4b79a7e61557ea74c17b2a6a410babcc4`  
		Last Modified: Thu, 09 Apr 2026 22:33:24 GMT  
		Size: 19.9 KB (19906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d18715f83f8741fcbf1884695386ed8d1ead5b1d97a392ad15197bdfba1bf54`  
		Last Modified: Thu, 09 Apr 2026 22:33:24 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f389c315c06677c1b96bd3cfe7576f884c3571dccaea0697d788479e2f23c7f0`  
		Last Modified: Thu, 09 Apr 2026 23:33:38 GMT  
		Size: 4.3 MB (4311975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a198e6affeda01ce189f8b1747758dc2b90cfe3c2bd4215ba7f7c51b2ed7103`  
		Last Modified: Thu, 09 Apr 2026 23:33:38 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe27e749f0df991fbadce3d997ee88447fe684474b215ecd11e31775733ece5`  
		Last Modified: Thu, 16 Apr 2026 01:00:01 GMT  
		Size: 790.8 KB (790774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944f271da520f86eee92037cb67c3960253b6d037a52a12b58475244a3e5496`  
		Last Modified: Thu, 16 Apr 2026 01:00:01 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2366dfced72f59381607e69481f828908cb79e1ec2317bc057b075c4d37ffef`  
		Last Modified: Thu, 16 Apr 2026 01:00:01 GMT  
		Size: 21.3 MB (21334429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:1fca16bd33d6392cfa9c5a0c4ca6f93638ec3c7591c5339ee2dac511e92f53c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 KB (403124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7303c080d21a80c744ac31d4981bb61bd0146dd0c5e67014402505dcb28177c8`

```dockerfile
```

-	Layers:
	-	`sha256:70498f4087e992e0d8c3f73bbb13482634cc0ca8da9d5fd645c13f16c344d1fc`  
		Last Modified: Thu, 16 Apr 2026 01:00:01 GMT  
		Size: 370.9 KB (370855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9626d0954f4856d47829e5344692ec90d6a8c98bc10cd39d4eb8c34bbbdeb9a2`  
		Last Modified: Thu, 16 Apr 2026 01:00:01 GMT  
		Size: 32.3 KB (32269 bytes)  
		MIME: application/vnd.in-toto+json
