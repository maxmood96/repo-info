## `drupal:10-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:3184dcbf25948d4c5e39317058108cee0fe65b4f6b8c722f9191d4a358a1b4c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `drupal:10-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:ab2f7fad26f91e3bb704329f21a6af93f024d9f4fb5f2db513cfe1fb746efb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57469456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94af8408bd52ed92e1a41a197578f228fb829322cbd31ee712da529e829cac68`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 15:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 15:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e4337a6664d4a1d4cd87ed9de51a8f8f777ce351338c8a7ed9f863a1f98b0b`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 4.9 MB (4872464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b465b0b8b8abc315f6cf868e51dd76877d99bf75005cbc8f508c6d2701a1d`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbcb20a410c9f0b47a1d40e0d423cfb12132e926c8cc0800a993c37dd77f20a`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98874e5eb68690207cb56b2bab94b373731652f0fed7da27383fccaa66fd7a33`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 12.1 MB (12147077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930168d0f53f275e805d6b4cecabfeca6bfcd7bac653e644f813e918dc7a5f7e`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315dc47477842432045c845c1a7c2cef8bb5fc76f422399f4c561922877293a2`  
		Last Modified: Mon, 28 Oct 2024 22:12:56 GMT  
		Size: 12.9 MB (12854821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b9295661d93b92abe852ae01873f4b41d19b96aa8afb656d7dbc2fbbfa86f4`  
		Last Modified: Mon, 28 Oct 2024 22:12:56 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b6b777c45620b2b50707acd7f79887aa7d77fcb366b7ce4adebaa9954b33b0`  
		Last Modified: Mon, 28 Oct 2024 22:12:56 GMT  
		Size: 19.5 KB (19485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419509065e5134b62c437e2c77b5ae0f5ceae8e62a73d71432a5ec3f4e445493`  
		Last Modified: Mon, 28 Oct 2024 22:12:56 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae279c2dc92b34c1fb1d64e37a81eeb5270f3f1d6e13ee070ad139bb1c8ba579`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 2.3 MB (2283692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90deebf646287543652c53169bc4d5df37a8029def30f1b90ce7db7999602d64`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9c4a94a3829c94dcf96febe96eb0bf45e7da810fcd1aafc9ae9c8fb47101b`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 738.7 KB (738712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff3c6f0b506ba47c735d10946aa6c25c73d61870afc3e9799f30fd412e66d3`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c2e813958aa6aa1ec0983595c6aaf0ff614bac78ab6b71814f266e9e1a2b22`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 21.1 MB (21119479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:b3a17f562f326c0e1f6b148205ebebd3a5aa2c6835f7eb8a7684e51d5141fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 KB (386952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deda18931516d93655f1c78a3886551ac4b3d011a1c7b85880281fcd2b0567b`

```dockerfile
```

-	Layers:
	-	`sha256:d2f192156de9515865359274ebd59c63a0b1eb9df08be0668fd7807efa8b3d54`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 353.9 KB (353915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517862184aa7ff78588446f8c07729db62d80c4601b630959f4f43717eb5709e`  
		Last Modified: Mon, 28 Oct 2024 23:24:16 GMT  
		Size: 33.0 KB (33037 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:d028f52856411606410758ed2a17dc13cb489c9c6d5f9705dea689e952d1ff79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55211320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63634dabd99367f0379d37e5b3fd2a75b5d8d4fa47f83b3405aa54a2a100266`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 15:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 15:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f5582f8510632131a7738e0b931539dcee5de1991cb3b56befa5e9dea19109`  
		Last Modified: Mon, 28 Oct 2024 22:20:46 GMT  
		Size: 4.5 MB (4549494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5985e06088ddc92fc7b3102ac2f694add2ad7d33b83f40481ddb73895f89ab51`  
		Last Modified: Mon, 28 Oct 2024 22:20:45 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f32b709a7cddecf643a6a97fe1f1299b1ebc138fd03f749b4e2331e9580ff1`  
		Last Modified: Mon, 28 Oct 2024 22:20:45 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f5090585fdd4eaf3660b4af47c7dd9b9915bd3232e45b6d4c1e2c7dbef883`  
		Last Modified: Mon, 28 Oct 2024 23:22:17 GMT  
		Size: 12.1 MB (12147089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c752ae041429afd83836b7790bd97a03f52a49e4ad6e1bcf650f1ec84a81ee`  
		Last Modified: Mon, 28 Oct 2024 23:22:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331c7743efa586f092b8099560ea3f43c6289acb199e982ef1c27a4383814d5`  
		Last Modified: Mon, 28 Oct 2024 23:26:37 GMT  
		Size: 11.7 MB (11706259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238d2a1f0df1d633126bc8c8e2d1a6b7cb66919fa211ce5822b04bbbfd0abdc0`  
		Last Modified: Mon, 28 Oct 2024 23:26:36 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478c7609ef2df574bd767e94da427b9ad13566ef7c11b210daea94724aa967a2`  
		Last Modified: Mon, 28 Oct 2024 23:26:36 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eff4f6b39e7ba08dbbe6ba5553b4d650e608191b44458aaa944d6543bf448b`  
		Last Modified: Mon, 28 Oct 2024 23:26:37 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d867879039b853642edbac36a0573454bb37859f50a3dc2eb5b3bb3ac8bad43`  
		Last Modified: Tue, 29 Oct 2024 00:18:22 GMT  
		Size: 1.7 MB (1740652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25a7da77b96a1fa48625dae66c06f910b08acf319678aec7f5aac0b9545130`  
		Last Modified: Tue, 29 Oct 2024 00:18:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcacb3564071fadf74544ee6e5fe9fb2b803913c160280b1b64e82b405d4ac3a`  
		Last Modified: Tue, 29 Oct 2024 01:11:50 GMT  
		Size: 738.7 KB (738708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94742ae2e97fb08dc4c9278483c9ffa5470dc5548e4359d09409cf984a09b24`  
		Last Modified: Tue, 29 Oct 2024 01:11:50 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106a226085de15ef5741eb65c0358e8311b6068266f8da9d0854fc05305fd433`  
		Last Modified: Tue, 29 Oct 2024 01:11:51 GMT  
		Size: 21.1 MB (21119378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:47fe6291c23488b7199c1e7be3d23d96883b7082ad8a79d6e2c46d8a6d15422a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a228f4f6484d09465d65c919ae29425a07afe1b92de63055ce7f4349e8dbf11`

```dockerfile
```

-	Layers:
	-	`sha256:d9cf9e1602dcb489346183f6074c881cd661a30a38a0e0b5bf18ec2dd37fe56a`  
		Last Modified: Tue, 29 Oct 2024 01:11:49 GMT  
		Size: 33.0 KB (33006 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:9f989afc999355dfa66717aaf0e15eca5102eecbc27eb6e18a74bf7397db7c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53815783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5b2a43757c1037fb5281e16eca7a4f8c83e601b0124d21bf2215cbdc10714d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 15:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 15:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb95ffa9127becc3e273fc383338f28ee241a7004aa2fb678c74b6c24e6cdd2`  
		Last Modified: Mon, 28 Oct 2024 23:09:26 GMT  
		Size: 4.3 MB (4273952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f67e54f0fd76d9ac183a984ede56462d325cddef03a1615886d6cfe439565`  
		Last Modified: Mon, 28 Oct 2024 23:09:26 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcc1fefe1b3dec0dd6d68e75a4213b6c95fdfa6fb5ed2cde40c7fbf7b469f05`  
		Last Modified: Mon, 28 Oct 2024 23:09:26 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7c3f40b3632bee6fa1a8747f3443a883baadec7666448324b989329f434b07`  
		Last Modified: Tue, 29 Oct 2024 00:59:01 GMT  
		Size: 12.1 MB (12147091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a928f7a93cb4752a08407564beb32d4d51da693e6b87afc3c3ae7f40d4d36e1`  
		Last Modified: Tue, 29 Oct 2024 00:59:01 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d51ba711098927a9f556d4d4a85f414f24a6bc9ffca4158e0ecffa4e4dcd3`  
		Last Modified: Tue, 29 Oct 2024 01:02:45 GMT  
		Size: 11.0 MB (10970228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038c711d0b11d64509a133ec516f4fcfee284f219bd2d2412626269c35583797`  
		Last Modified: Tue, 29 Oct 2024 01:02:44 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6f4b0a0f0def50364199cf05e4cab08d1f8f557b093085c56407d32caa1e8f`  
		Last Modified: Tue, 29 Oct 2024 01:02:44 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42824dbbbdff58810f912c241ebf27fbdaa981b0d991d2b0814b06ecb45ee8d5`  
		Last Modified: Tue, 29 Oct 2024 01:02:45 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1143c238f585f5252d29d40860ad42486fd130a701db75d1a9ffad8e4079c97`  
		Last Modified: Tue, 29 Oct 2024 02:38:59 GMT  
		Size: 1.6 MB (1605406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e063610d5a1bccb71d217b5205614f6a7c5f18a5b733dfbc9e114ef8185af14`  
		Last Modified: Tue, 29 Oct 2024 02:38:58 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797e2cb3865b64879f24aaf3736831b2ed099bb9e6b0e90b4128359d1563223`  
		Last Modified: Tue, 29 Oct 2024 05:21:08 GMT  
		Size: 738.7 KB (738719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3746fda9dabb93166e49ac5e43aebfac58aab9bb836a49d611befc7836b16df`  
		Last Modified: Tue, 29 Oct 2024 05:21:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9824342007f2bc406ee0d022da8ee37af0c2b9aaa7786b1f8966f95ec67e08`  
		Last Modified: Tue, 29 Oct 2024 05:21:08 GMT  
		Size: 21.1 MB (21119391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:8614f6bc0924187fcffb6db1bb2c136593745942cd6400f6c5f81be9353a9d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 KB (384324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc79ca29c289c6b43be6b83bae201c99eed45ff5d1e6f429f68e5aecd13f756c`

```dockerfile
```

-	Layers:
	-	`sha256:0c04c41fd0370c0bc4f903ec4f2d2083f847bc04aa758a488a6c91d1202696b7`  
		Last Modified: Tue, 29 Oct 2024 05:21:07 GMT  
		Size: 351.1 KB (351103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f883d0f95835a56784d22d00d9c204585ad232cfb789911839eb0e68c200a5c9`  
		Last Modified: Tue, 29 Oct 2024 05:21:07 GMT  
		Size: 33.2 KB (33221 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:3e8e399e1c9940e98cb7928805dd6a4b60fd77c05ebb2fea212fa4ed39af912a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57689568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26a1fc00b1ff3c8ace815cddc585e25ac07b4197cc4a89aab8643c465aaf1b9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 15:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 15:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40695ca4960fb06f2beb21ebb72341baf9a80b06208c8787f3afd70cf0f115d2`  
		Last Modified: Mon, 28 Oct 2024 22:43:30 GMT  
		Size: 4.8 MB (4810647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8888fd67e4103a97949e4e53bede0efbfa8c99737af1d64e776178a263d0407d`  
		Last Modified: Mon, 28 Oct 2024 22:43:29 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186eed04373107222bc0e0a328397074efe93ad77c5374ec9c0f099992edee8`  
		Last Modified: Mon, 28 Oct 2024 22:43:29 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c69d1fb19881332634b2954b3c657ca469d04e09a14855c2fa72938f79a75d`  
		Last Modified: Tue, 29 Oct 2024 00:41:16 GMT  
		Size: 12.1 MB (12147085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af3dc37dbfe4bba274d17dbce2112936f9b5b2769203093659965dab544406e`  
		Last Modified: Tue, 29 Oct 2024 00:41:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1c86d84c9551a1d9cacd951724712525715b2c0e6b52dd31911d7b74b3e666`  
		Last Modified: Tue, 29 Oct 2024 00:45:44 GMT  
		Size: 12.9 MB (12924571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e141bcf9895c13551d16dcd478c1c535f0b5bd407bdc8d261d5841957c3317`  
		Last Modified: Tue, 29 Oct 2024 00:45:43 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef1fa3303ee0a17c1820128a6ff3102d6695b18904f98a4237bceecaffe1008`  
		Last Modified: Tue, 29 Oct 2024 00:45:44 GMT  
		Size: 19.3 KB (19316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad796bf65b0a0371cbb71525de322d9f0aeb69ab87ffc08b6f7e7d978ab795c`  
		Last Modified: Tue, 29 Oct 2024 00:45:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de559e0eb67f163f59ee1e35bfc857daa1da2a1c9c8c8d64132c28773658e754`  
		Last Modified: Tue, 29 Oct 2024 02:48:43 GMT  
		Size: 2.6 MB (2557013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ca73f44403854596e1d3a4d6fb474ce830c0c4c129b28f9d8b3dbebf328d2`  
		Last Modified: Tue, 29 Oct 2024 02:48:43 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b216e1e269724afc559600998456c3a4be34c9f5be053bf6929f5c1b60cd1f6b`  
		Last Modified: Tue, 29 Oct 2024 06:23:27 GMT  
		Size: 738.7 KB (738718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851275cf224869947431f37c695a439324e57ba055eb222bf0074e17e400875`  
		Last Modified: Tue, 29 Oct 2024 06:23:26 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd641b917231fd1c4f78bc433be31eff0801799dffc537e5b326e79bf7974a9`  
		Last Modified: Tue, 29 Oct 2024 06:23:27 GMT  
		Size: 21.1 MB (21119091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:f7c6c8afafaf509ce08965698e082108ae8bdc3a32fb0860fa325603afaf1c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 KB (384396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ccb4c0959906f37ca6be4b1d7d41ca327f590b72e6fe9fc0606eb0caf7111`

```dockerfile
```

-	Layers:
	-	`sha256:e146d62923ab23fc16f9f2e32c90a11f185aa1e2d690b15a283cecf2a60f5163`  
		Last Modified: Tue, 29 Oct 2024 06:23:26 GMT  
		Size: 351.1 KB (351131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea780c189b6f2aa7687bc183e8cfb17357f01667c57dbb1d301b29d9bea5b5e`  
		Last Modified: Tue, 29 Oct 2024 06:23:26 GMT  
		Size: 33.3 KB (33265 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:6e568114b6b7df8a8c712869a0295366506a31125b8379524e76e7b3588b2138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57573213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1783691b5461127dc3e232ce409c43c4b3b6f8b9368273d4ad560da4a3028b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 15:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 15:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8266887db3ddbb4387f253f4fcd74acda325c77a04aa6a51cdb6ac91fdbc1764`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 4.8 MB (4760524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64432d4d0b92f4f08b855f5622698b4a06c7aba8eadaf96f165bd07e9b9881ca`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9d7baa853d5dc190378ef3f76d7ca6c50e9fa4215afc59341e093d2129b95`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111c101c007394bcc55a242771f82d87fa001960c5e932f9532e48fab66ce16f`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 12.1 MB (12147080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055c2c269afa21e46b3d881cd5f8801f5e42860a741e07b90b6938fac8896114`  
		Last Modified: Mon, 28 Oct 2024 22:12:54 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfd0895d412feecf5f93f92e78bf1d047032f5b435b6af712701d05b55963f`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 13.2 MB (13202753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ce83fb5e78ed59820cbe872f33852ce82f535a66e64c102cbe94a68c077e66`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22924f00d8262dffe78d5405e7450768dca738f4addbffbfcb5a82b2f80adbcc`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c3d6e68766bd4fb2c54c01021299dc911f9a889ccfe8a38404eb8fb0ed0f1b`  
		Last Modified: Mon, 28 Oct 2024 22:12:55 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c7326bac30d8e83ddbf9af3ed4a101926e2b1fbf6c2ca438a0618ae5c1720`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 2.3 MB (2317730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a50a05fa07b8aebfad079cfeb0889a99fd202c3ab0339f3d0d1038b38ed0d4`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e261b2978de7c00506fbf8c8119554d4ffe4379967c07f7fd7841ecc69f3b`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 738.7 KB (738712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415c55f67b13fb0705abb2aef8cc7ada5d448b126dc2eeb6d20e2efee488f8d3`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1407da86464b9cf2f259f0ab9c6995e2277a8ebb8104ede4212af9646fd41`  
		Last Modified: Mon, 28 Oct 2024 23:24:18 GMT  
		Size: 21.1 MB (21119292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:20e4598f3acf4d2f243c1b1780a8902661fe4aef002017548685c35019b8b4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 KB (386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ac0b38f23ccac5427cb00ef7fe8e2acafd9ce4119015577dd5c79e773ce2e1`

```dockerfile
```

-	Layers:
	-	`sha256:0d2d625004f93408c052123b0d95aac85ad8e2c7e051ef2fcc225175633eddb4`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 353.9 KB (353880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd9bcf1d88666bb71b84bda69c196f4598eb6adca18663f2df4032a51d89ae4`  
		Last Modified: Mon, 28 Oct 2024 23:24:17 GMT  
		Size: 33.0 KB (32986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:6f9f0c2a66de2e068801c9eb40da593ed99872ec0e2485a1ab8b519e84c07633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58608732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b44f64a253ef8285a627480fad5b46c80ee1957e0e5189546d2185d312dca94`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:24:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:24:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:24:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:24:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:24:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:24:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:25:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:50:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 15:27:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 15:27:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4514a75734a8a2c464727a1d2643b6ffc19526edfbc2100de62e45284ef3699a`  
		Last Modified: Sat, 07 Sep 2024 01:45:56 GMT  
		Size: 2.9 MB (2882579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946f8448bd3215cc0574597d31b6c547a6035486812c2fcbfc8e931d6279885`  
		Last Modified: Sat, 07 Sep 2024 01:45:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903ff2eae36c9cf63d249425e3f7bd588d8fcd648ecf498db42a9c9c09ab6a2`  
		Last Modified: Sat, 07 Sep 2024 01:45:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012d90ee22189b6da179dd5a29cf4434b3e21b370a5f43c48e12885f023dde`  
		Last Modified: Fri, 25 Oct 2024 01:02:13 GMT  
		Size: 12.1 MB (12147181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e5091abd710bf905c39e97dcbc4f8cbf3ec01565f4179fbeedbcddc78e6aa`  
		Last Modified: Fri, 25 Oct 2024 01:02:12 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23629b53bbad5e3e091c6cf8ad2c8ed76437d8b9110d58a19ddac34d5801bc5f`  
		Last Modified: Fri, 25 Oct 2024 01:02:30 GMT  
		Size: 16.2 MB (16217288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd36b038b19874ade3f96c13540f556cf4a6eee08845eace5c8c01bd3db1747c`  
		Last Modified: Fri, 25 Oct 2024 01:02:27 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235d65d2d28fbe6273b91693c4543606af6d8da4650255b6e381a1a92166674`  
		Last Modified: Fri, 25 Oct 2024 01:02:27 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19847499c86f886f0d81c56823ba3771a41df44b0bd248213f21643112fc9fcb`  
		Last Modified: Fri, 25 Oct 2024 01:02:27 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35de7e011b3a729a41ca2cb4ffa4e52102a64047c4c5ed59cb01a1b7bed96511`  
		Last Modified: Fri, 25 Oct 2024 03:19:07 GMT  
		Size: 2.1 MB (2105514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb680bb67b214f97376760c79abcf408ba476eda9723f478631f2f5e85ed57`  
		Last Modified: Fri, 25 Oct 2024 03:19:07 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fff4ce46fb30413a2524f6307fbd3e46466bf2525f04fd902f214bdf8663eb3`  
		Last Modified: Fri, 25 Oct 2024 04:12:06 GMT  
		Size: 738.7 KB (738718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4058901969c27e65482b901036ff1c1a8ea9f7c975323ba5bfae3b0fe51a26fc`  
		Last Modified: Fri, 25 Oct 2024 04:12:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb8d0372bd64687c9ff1a35e1a02e772898f5bcba89450bc76d65ce0c12ab3d`  
		Last Modified: Fri, 25 Oct 2024 04:12:07 GMT  
		Size: 21.1 MB (21119607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:608ca725b59ba163b79d950726bd1a38df4bf2b067373c21466291911a0cf1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 KB (381552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652fa0e8d6137bd0c14439e38189fa5a72aeec2a86a59b16f81bf653cd7513a2`

```dockerfile
```

-	Layers:
	-	`sha256:4986c090a87a5071406c4c18d1c8ded195e700b9bf993866eb4db4511b35a543`  
		Last Modified: Fri, 25 Oct 2024 04:12:05 GMT  
		Size: 349.1 KB (349143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee48c25488849d1c8f00415d021d0f64153402f82082222c2fcb29711a375e6`  
		Last Modified: Fri, 25 Oct 2024 04:12:05 GMT  
		Size: 32.4 KB (32409 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:0659eb8eeaffcca1f42acfcff60b74754ca0dd207211a16cb9e5f2d204ff67c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d519a0b8b4aeed8bd024e1850a27fc3d3c9cc20c2cf312295918c4be82d3674`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:31:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:31:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:31:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:31:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:31:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:31:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:31:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:31:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:11:47 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_VERSION=8.2.25
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 15:27:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 15:27:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 15:27:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 15:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 15:27:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 15:27:16 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 15:27:16 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252a16b4a3f1ff8b7342597a1478d555f90a9466c5c0b4390a680b41165487a5`  
		Last Modified: Sat, 07 Sep 2024 00:43:13 GMT  
		Size: 3.0 MB (2976667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f2ec96a13f97950cd572f6ba53cd2b32756a6b0fbbab2578461fca19ef5a`  
		Last Modified: Sat, 07 Sep 2024 00:43:12 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a33bb433d3ff1f94ee0dbb35f0d25b17087375b1397e429df7974ffd56abf9f`  
		Last Modified: Sat, 07 Sep 2024 00:43:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717f42bbfdda321265e6df7cf9c5eb80b144ac4bede551974686af614a8ca8eb`  
		Last Modified: Fri, 25 Oct 2024 02:50:17 GMT  
		Size: 12.1 MB (12147180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4736ee6729cbf94860ec8467e7bac1383cdb8427d9d46ee74226ec09a8bf1873`  
		Last Modified: Fri, 25 Oct 2024 02:50:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4dbf300c964f8723508846294cc264e3fefc94508dda898b3ec7cc470e720`  
		Last Modified: Fri, 25 Oct 2024 02:50:32 GMT  
		Size: 15.6 MB (15619838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a2cf3c3922a5a885e71465fc4480474f5bf4f49ff86f76ebd690d2b413169f`  
		Last Modified: Fri, 25 Oct 2024 02:50:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbbb00ec5185e7cdbe4a39318f4fe9131782abb9c479537da2d2ce6edb6ed9`  
		Last Modified: Fri, 25 Oct 2024 02:50:29 GMT  
		Size: 19.4 KB (19379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23328158342fb34a9dbfaf888126c51e546e139cf17ad358f382202b1861da3b`  
		Last Modified: Fri, 25 Oct 2024 02:50:29 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77706e84627e28ad9541262f8babacf7048fea5359e77d3d5b5937cf208cc5b`  
		Last Modified: Fri, 25 Oct 2024 06:54:30 GMT  
		Size: 2.0 MB (1999482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d110028be777a37d49260ccc79f2babf94fa13574654a8360d9584a73e80c3`  
		Last Modified: Fri, 25 Oct 2024 06:54:30 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cac91f03917797b80fb2b35aadfc1192b6496b60ae4cb790fab26986d17a4e`  
		Last Modified: Fri, 25 Oct 2024 08:32:08 GMT  
		Size: 738.7 KB (738719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c6aa475501e51b013577b860c9a0641ba3d6fc4d36180c67b657458e50a807`  
		Last Modified: Fri, 25 Oct 2024 08:32:08 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6786849f845a2728135d7a83be81ce77f503e6158b7d64253223a72618d4d99`  
		Last Modified: Fri, 25 Oct 2024 08:32:09 GMT  
		Size: 21.1 MB (21119475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:7a57800fdda296d6b2d807c2344ed0f02d93b1f64bd30e086d0079f81af1baca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 KB (381441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4dfc9182fae0c766b3b83c31eda648ad285f721a51e91ab5f9906ff473a8bf8`

```dockerfile
```

-	Layers:
	-	`sha256:df54bce0c57a690157c4014e38ac75f6fcf49f545aa7b1a002bce76560435ef2`  
		Last Modified: Fri, 25 Oct 2024 08:32:08 GMT  
		Size: 349.1 KB (349097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c2f6b056390de011838460f157b88c5a10036c1916572ce75a87582eaf9722`  
		Last Modified: Fri, 25 Oct 2024 08:32:08 GMT  
		Size: 32.3 KB (32344 bytes)  
		MIME: application/vnd.in-toto+json
