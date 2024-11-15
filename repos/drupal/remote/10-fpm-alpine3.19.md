## `drupal:10-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:4918cebe9d5f13fff65b6005183b8b7512e2037f31484bb6276d077850ac96d8
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
$ docker pull drupal@sha256:54c1408ed9d499f29de18cc865e4b8a888a88a3597345ed55f34c05e657ea6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57473441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c55a744888b371726fde73e31a69e1c5642655fe537379af02965e056c6bc9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6dcacd3e6cda6fe5513f5a664ee8f7dda78033ce431cf26de020e1e7b95dca`  
		Last Modified: Tue, 12 Nov 2024 02:37:14 GMT  
		Size: 4.9 MB (4872471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b6643f029151390e535c5e640ce0d3d26f458c0d93580134974f4abaaff5f`  
		Last Modified: Tue, 12 Nov 2024 02:37:14 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70261bc2be1202c93f5771d51d45151ad487294e26c5b90e5f435adc2953910`  
		Last Modified: Tue, 12 Nov 2024 02:37:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1406868e1cc16a051cfe91a42302a5f079d328e13b62ef285c023911bf2904ce`  
		Last Modified: Tue, 12 Nov 2024 02:37:14 GMT  
		Size: 12.1 MB (12147084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165bb7eee6ce32509a1e918e51e9f2edb3ba0dfe1138e4e604b1d2a3324c2cc2`  
		Last Modified: Tue, 12 Nov 2024 02:37:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a4179a17f8f840d2ac1a5a4221dc3fc26c5a252c1dd829713c5b55eec6a53`  
		Last Modified: Tue, 12 Nov 2024 02:37:15 GMT  
		Size: 12.9 MB (12854846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90abbc0d405989e02b209fa30680858a86662bf761b1165f9777be6d35e6790`  
		Last Modified: Tue, 12 Nov 2024 02:37:15 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51c28f6a0a6fb76173f75e1eb2435e23957bcc4d2f0799118dfaa28cc263`  
		Last Modified: Tue, 12 Nov 2024 02:37:15 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d309d64f2287689f5ce08e64c6eef6f95e31e48f27e7f04835e2f1a02b4449`  
		Last Modified: Tue, 12 Nov 2024 02:37:15 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e3f18ea705780c90467c382875811d001f540502576e19d27b01d52a1c801`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 2.3 MB (2283688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7f1585b037254003e7c0f453d28f80d5baa299f97d83fb9f5e3b5141d437c3`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9897225257788ec4536642794caab395bd993c7f2fd4eb7f812fa208596c1a2`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 739.0 KB (738952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4de9e20dac6f41f33d4600efc72e1efe10cc5340e29340287b67faedb7366f`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b98e47132ca1a9bb9080f9f7b4fdc194975bc33f7f7e680f4d66f82aa9b2b6`  
		Last Modified: Thu, 14 Nov 2024 17:49:04 GMT  
		Size: 21.1 MB (21123157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:14b751247aa61c419343b4df32ebf617059fbcf06cfb56ae57b17b3997c3ac5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 KB (386958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17478da7244cbc2ab39b062e38e9f035fc0d6dd68622b4b414c9ef5799b14479`

```dockerfile
```

-	Layers:
	-	`sha256:345ab64e42c08dbb1eee9adc801dff804b293d470501a7e18809bfc5d43b4448`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 353.9 KB (353919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50f45568fb8bcb3274c16007953c6f1f4ec9664fe4392f06957ca00cf3f8f5a`  
		Last Modified: Thu, 14 Nov 2024 17:49:03 GMT  
		Size: 33.0 KB (33039 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:b9899da4fe5bcf2c220695c03f23f7826fbf53c49119141ae15c4165c3fd6517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55215889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87d18b929782e1a301682b6e260478123bc1b580c97a0f01a98624975bf183`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d506df09dbdf91185add3a7b93df87df3f96e9e86244bb5a36ce976bad384da`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 4.5 MB (4549552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565c5d4979fc78805381ae54974577a69443306d5cd6ce30896d12062df3b5f`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a131775c3bd5253ef21285ac1b265871981ec4c9eb57a1a2dfc43a3072104`  
		Last Modified: Tue, 12 Nov 2024 03:04:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8131f00adf2cc62c43e9c55bbd8a9bc588407d5b914a2df9cb843fa2de7a39c`  
		Last Modified: Tue, 12 Nov 2024 05:01:50 GMT  
		Size: 12.1 MB (12147087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4992f3004e078711c4b2542941a7f8d65bcb010224b0f785d3d48cbd831e027`  
		Last Modified: Tue, 12 Nov 2024 05:01:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2fcffa809d427cc603023faf45732774500decb2d9a3ff786cc0c5c7c25abd`  
		Last Modified: Tue, 12 Nov 2024 05:05:29 GMT  
		Size: 11.7 MB (11706274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236779199912cd2b80ea63784e56a57051bfaba42e451338b1059830b2061ff2`  
		Last Modified: Tue, 12 Nov 2024 05:05:29 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3c5aa42f179d01f447598a60679af6ef88b2b7b83386721f1cb11c65c8f1b4`  
		Last Modified: Tue, 12 Nov 2024 05:05:29 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d9abc82c68dc46092dcba9cee4294ef5adb461ccc02c5a4898171948e71f3`  
		Last Modified: Tue, 12 Nov 2024 05:05:29 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7351dc32d8d7f766ef4d7a2cc8682ba9b728105f23ba69d439f466d6069d2f82`  
		Last Modified: Tue, 12 Nov 2024 16:15:12 GMT  
		Size: 1.7 MB (1740665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c9320ce438a00f72050e7462bb2a7bf1db110f86a4714c3a891fc83353eb2f`  
		Last Modified: Tue, 12 Nov 2024 16:15:11 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbebbe96f8f063b477518afe69fc4b45fae7977dcedb9ee88e28271e5748824`  
		Last Modified: Thu, 14 Nov 2024 17:52:05 GMT  
		Size: 739.0 KB (738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c9f6e7ef39818526cd559626400db81c8ed581a7c810ee8129fadf8f1106df`  
		Last Modified: Thu, 14 Nov 2024 17:52:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068329a4aa59b6e0bc476047a7f5c310294c10caab2826a0ffab72b2ac9f3434`  
		Last Modified: Thu, 14 Nov 2024 17:52:06 GMT  
		Size: 21.1 MB (21123559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:18b6f87099c218fff6d64f0320cdfc3f9359a3c626395659ddbf1b60eece709e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f3c64f808f4b3ae6d2312b6011bb5c730d0fe2e9402ed4e12035a144225aa1`

```dockerfile
```

-	Layers:
	-	`sha256:2c5ea9e57d849d70cc2b61e5a1bd9e4c743671efc35245b2117acdc9d7f42215`  
		Last Modified: Thu, 14 Nov 2024 17:52:04 GMT  
		Size: 33.0 KB (32964 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7f60ccfaa96a762d0f8352fbdfbd9849a92945ef5d70b1fba15706c6359b1566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53820456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18de3e9efbc0e2e090df379ceb85c22ac854ae6630ae2cb068366dcf296d87f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0436284ed3df1ea72ee7578e1acedcb3f1d13662da3f84c96df0f7250b0e65`  
		Last Modified: Tue, 12 Nov 2024 04:13:48 GMT  
		Size: 4.3 MB (4273946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f71fe689f2c66318ac16bb591f4263243d0ee583bf8e58b422159d0e8e5f74`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459364abd934a595a7d02d68c9dbf45d3769fec662e99f1aa3c9c4f8554b53a6`  
		Last Modified: Tue, 12 Nov 2024 04:13:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b59c607fb85282b7fd56e37db2071b82899ba9e963888983edc1d7c1154b3fc`  
		Last Modified: Tue, 12 Nov 2024 09:12:10 GMT  
		Size: 12.1 MB (12147088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc16f427a3c401470eb71a7cfa0163e517133d75ec3a72b313d87164fc79b21`  
		Last Modified: Tue, 12 Nov 2024 09:12:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13117e2f72e9e0fda23641c0354074dd075bbd8633fb62155c098b497fe28cc9`  
		Last Modified: Tue, 12 Nov 2024 09:19:23 GMT  
		Size: 11.0 MB (10970225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42241276b12457a118a7b96f2c8d078225f1b71ea3c32e12f45d9b41503785`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578b8ac96ecdd6b35afb34f93b4c06e77a87b8d0927560f440ec09a3c54c287`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 19.3 KB (19315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c3b3a893135b1e439121e07cb0f05201670f6f6fb5057f9d0b24587fb4d7d0`  
		Last Modified: Tue, 12 Nov 2024 09:19:22 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2596353aeb681d7a3f582dde82273a039a31231876f464fe62f71efe67b1e0`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 1.6 MB (1605434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b79d9f451203f83f31de742c96491b9921a7c3ba4c7914a7f2bfbd892f742a2`  
		Last Modified: Wed, 13 Nov 2024 07:49:51 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d9a18425400d64ce4433e07d3d7c163653e5a1a0201a370b4bb1e216802f72`  
		Last Modified: Thu, 14 Nov 2024 18:06:45 GMT  
		Size: 739.0 KB (738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf58136f243b9cf5a8915c46abcbd569d78b4e7efb8fb28549ccbfe97365dd8`  
		Last Modified: Thu, 14 Nov 2024 18:06:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61f338ca45099602550de522dee57336985ab1ddc7f96182f11875c2c1a9e07`  
		Last Modified: Thu, 14 Nov 2024 18:06:45 GMT  
		Size: 21.1 MB (21123729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:055f65d247bd9727beb8f2dc4482a174a3bcb06afe1090cb85902c9a4cfbf817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 KB (384286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d614e715498bb14d4118a3b122f7d15947ab2b9cb578e56387eed0674a169981`

```dockerfile
```

-	Layers:
	-	`sha256:d6a6ed352c39dedbd952c7d611f41aea3a9afcffd5476f1c89e47304d2086bcf`  
		Last Modified: Thu, 14 Nov 2024 18:06:44 GMT  
		Size: 351.1 KB (351107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432ee7d885f5f217c5aaba18cc79f097801ff1a239f37bcc16922ffe14096bab`  
		Last Modified: Thu, 14 Nov 2024 18:06:44 GMT  
		Size: 33.2 KB (33179 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:f3b12aee4766ea63f455a3789cfd6bb60669a734111d66e8e487e20edd9b17ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57694756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872029042a5f4f5cd6a4958d328d6e0e0ebccf0ea065f11d10af760173d92d00`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aa82fe7cb492df316f7b720cc5bd1cf6a0f0bbf25ec9d0738d8bab76eb6ac8`  
		Last Modified: Tue, 12 Nov 2024 04:11:04 GMT  
		Size: 4.8 MB (4810652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf6e72d90a16f21844fd0a2e0521c81b8bbae7a03922cd2d8afe2243befeeff`  
		Last Modified: Tue, 12 Nov 2024 04:11:03 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a4c00e4542840ffb2d40fc8e730ca3aceef8c5efbd7d8e4d37b0fd2779f28`  
		Last Modified: Tue, 12 Nov 2024 04:11:03 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4f3901e90f8ad2d1ec9761938f97690a80ed59b1f6d60eef866e1b0719888`  
		Last Modified: Tue, 12 Nov 2024 08:02:44 GMT  
		Size: 12.1 MB (12147082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9fa729289d3494c567e2db6ab5f2fcc15006d632a4d73b749ded01e788d3c5`  
		Last Modified: Tue, 12 Nov 2024 08:02:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0dbfabc1ee57f2e92b4e7cbe8dde5eeee7f3c3ee2f807044609525d45ab9d`  
		Last Modified: Tue, 12 Nov 2024 08:07:10 GMT  
		Size: 12.9 MB (12924674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9657457570fb9cb0592f60dceeca662badb15d5f67b25eb70a08feb1f02250aa`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c782869d8ae2eb29ea1d142deabdff2354e614c387a0711f6d81c46967784e92`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa440590fd2ed69d716222e5622a42463f5c6a4b4bbe356a281f7b77969f7105`  
		Last Modified: Tue, 12 Nov 2024 08:07:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce1f4d7d9c1396222e2aaede8905bd65f556e85e8539259ce81500af6f2ff8`  
		Last Modified: Wed, 13 Nov 2024 02:57:34 GMT  
		Size: 2.6 MB (2557050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0fe849d59b1a52a2432932e945bbe20bcfaa247b74955d71f0d44633186b90`  
		Last Modified: Wed, 13 Nov 2024 02:57:33 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bea1537bc578bf7166b1200aaf76d5f41e31eaa1a49ead313baeb7ce238aaa`  
		Last Modified: Thu, 14 Nov 2024 18:09:03 GMT  
		Size: 739.0 KB (738956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd097a68a9ef22bd6b7db68780d6c19ac67dd053ff4d2397af08c1797f2cd2c`  
		Last Modified: Thu, 14 Nov 2024 18:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c33585acbac06d7072aa56c2882c9330ea6c09338e2c4037b4c7631cbd8757`  
		Last Modified: Thu, 14 Nov 2024 18:09:04 GMT  
		Size: 21.1 MB (21123737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:f47c78a376234172b3bb89bdc9045649e23991fd82fa6d7ac532e2e0bae974ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 KB (384358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a0258e4f2ef7c3b6cac76b036c04e9976f451415ca96f971f0dc2f7bc0b242`

```dockerfile
```

-	Layers:
	-	`sha256:9b998d9e872eecf1b600cbf2050fb5709c93f22f7804e2575cc30352d3cb6f0f`  
		Last Modified: Thu, 14 Nov 2024 18:09:03 GMT  
		Size: 351.1 KB (351135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d446b27d1578f1c646f48dc4974021953b2d325228450dbc2bf891d4bbdca9fa`  
		Last Modified: Thu, 14 Nov 2024 18:09:03 GMT  
		Size: 33.2 KB (33223 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:76c6112c1f62460532cdcb0c7eabaeb10d89b4967bddc00383fd77c267246cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57577799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230bcdb800d73167a2782b5dd54211ae22f4fb7a096ed33c8612c782aa0c3d72`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed797b662362a3f569bb7ffd0042265d4f4894db24fe12eb19964313e5a8819a`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 4.8 MB (4760618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d9887db361f79d4a14b88a6128cff8af843ed622329a5f9f7a0d0f4d225c1c`  
		Last Modified: Tue, 12 Nov 2024 02:37:54 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db35bcc1c19d11ce74bad828c08ebf7f50a4ffe0f736b3823e98df1e0a9750e`  
		Last Modified: Tue, 12 Nov 2024 02:37:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546182a8ba61a9ff299ce2a8e941fd2bd241ad18899193aa9d512f8155e292df`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 12.1 MB (12147086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a098f9b8620618c7ce03229de6e0a8c0885854a92626c9859d4c2666b02a112`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27626f5e970ee89dea49a1a8d68bedde52dee817f243cf56a0af5f3effda55bf`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 13.2 MB (13202586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e9b3ac20b7cf75cbea906103ce26f4f8ca481248bda24fcdcedecab8b0dd3e`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8fe52a33e4329996c52943c84d206aad3a0c981708a786cfe1bbca38bd63df`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8cf0caeb5ab150274767baa2433d1cd876b1f6f5146e71299ce89376b9b0d`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ffc680ac7106d152bb6a8f167f87f8a8a9bcaf4ad27915c8dcc66cbb0c37e5`  
		Last Modified: Thu, 14 Nov 2024 20:13:06 GMT  
		Size: 2.3 MB (2317687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff8be9214fcc95f8da4cb7317831649ddb0b452c371078c07ba5e67a5c29bf8`  
		Last Modified: Thu, 14 Nov 2024 20:13:05 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2301298b177504adeadc76ddef13a5cfbe8c29cb42bd7a15003d6fbbf814c6a`  
		Last Modified: Thu, 14 Nov 2024 20:13:06 GMT  
		Size: 739.0 KB (738951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a48b2eb7e5e329269afbb16a3ef354b497ea0ba1f4eb8dbc7c8742bc96376d`  
		Last Modified: Thu, 14 Nov 2024 20:13:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b8e91c8f311fcb207eee8bb615e976d1008571a30a179696355ffbfd59093c`  
		Last Modified: Thu, 14 Nov 2024 20:13:07 GMT  
		Size: 21.1 MB (21123685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:6a498a75b9725ee158a5b2104badb14dbd29f867f973c5a2025eee69273e941b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 KB (386870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccf085b28283a3a1c538157752c2da6136764dc9c22e4b19de31b221f8f4238`

```dockerfile
```

-	Layers:
	-	`sha256:304692d6f19dc398d41f13fbd87cd9fe6ba8d27f68025c65d3c5ac8e50c55313`  
		Last Modified: Thu, 14 Nov 2024 20:13:05 GMT  
		Size: 353.9 KB (353884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7882ba670aefd7fbab82e4f9b0272eef82437c84444183019ae6bb17b7f50813`  
		Last Modified: Thu, 14 Nov 2024 20:13:05 GMT  
		Size: 33.0 KB (32986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:fa674d61a963e60d0c0e6d92db8c501807907410c42254cc6e644e4ebd5a45c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57682651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b5ee65599c7096f1dfa19576013426c8b3bbe116850c565b384911517d967d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b5b574e5e7a1963997e6adc5fc6c41ea62b3d72487780713b6d09006e673c`  
		Last Modified: Tue, 12 Nov 2024 03:49:43 GMT  
		Size: 4.8 MB (4816871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4503eb1a8e49f698eea61c5c4dce1fa0040ce6ceca1d52253836027f00e9d7`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453f6eea919490bc644797b1f6b8249d5e157a311bebf21cec14cdc7315bd97`  
		Last Modified: Tue, 12 Nov 2024 03:49:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb34a1954bb8e077aec75426ca3adeb559dc4cdb53f50ff674502c38993fa2`  
		Last Modified: Tue, 12 Nov 2024 06:12:37 GMT  
		Size: 12.1 MB (12147082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc52540aaccb808d4286076482a85ff933d04c8ff27d7ced025b1b49ef616863`  
		Last Modified: Tue, 12 Nov 2024 06:12:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf188a7a0c68e9cbd682e878d1b05dbaa63d39ea09c1ded0c2578c6c8273800`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 13.4 MB (13352729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f003e7fb73fbe33f0a3cb3c641305a38b0277bb52c2232111e8243526191f08c`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf964a7912f37c2a23b6b679ff502b8421eeeffaad900ddf6cc4a62dd952bd89`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 19.3 KB (19329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98df7149e5827c112b19589b6d82e07f0af68220cdf3de8ec8a6a21cbdd12c`  
		Last Modified: Tue, 12 Nov 2024 06:15:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb3164d58bf5264931beb87d44a234515a6c5b7c884a6b388ef5e42a11881ca`  
		Last Modified: Tue, 12 Nov 2024 16:22:02 GMT  
		Size: 2.1 MB (2105507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5af6028b3cf9dacc1956e361c797019d5f3541e514d3f50a69bf2c180349a2`  
		Last Modified: Tue, 12 Nov 2024 16:22:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3282d247f05d9947d5f806f056c2aff1667b7896867b7bed620b6df59aa85f2a`  
		Last Modified: Thu, 14 Nov 2024 18:05:51 GMT  
		Size: 739.0 KB (738956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bdec9365c27e5e9795231bac89aeb4e72c8be0dd2f6570ed9b8c27332ce64c`  
		Last Modified: Thu, 14 Nov 2024 18:05:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4ccb8879618b5712422747363b0d34cf6b25ae2503e4f0a84096f9399bda1a`  
		Last Modified: Thu, 14 Nov 2024 18:05:52 GMT  
		Size: 21.1 MB (21123639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:522316d4c86a82c68861dc20fcd3e040e40951a50625df1d26f98f9ff35fd0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 KB (382256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d546c6103e307a0e595d0853792e822c11dabdfe5b69823b8cce252617b20b6`

```dockerfile
```

-	Layers:
	-	`sha256:1108863d9fc8c432056cfd3dae8c3b3cae76467bc1c4bcd79675346e4a3fa77d`  
		Last Modified: Thu, 14 Nov 2024 18:05:51 GMT  
		Size: 349.1 KB (349147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabdcc5b8f1491614bcaefb71bc10ba048103edd93e43dddad9e6fb750b616db`  
		Last Modified: Thu, 14 Nov 2024 18:05:51 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:e8371261b29d56517b08f0a099490064bb6acd07ee38aad68c02a59dad59ef72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56919291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b06fbfed092ed84148c3b9094d897e9869c5164c528948ad4469d9560d93944`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["php-fpm"]
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV DRUPAL_VERSION=10.3.8
# Tue, 12 Nov 2024 16:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 12 Nov 2024 16:27:18 GMT
WORKDIR /opt/drupal
# Tue, 12 Nov 2024 16:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 12 Nov 2024 16:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ebb87545715444ed87e790ef4054fd17853711b917372939fcec005a51ddbd`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 4.8 MB (4799270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93607338abaacd48124e4ac15fa9ced5b6d5b12eab2b3a8dede0efab1212c45a`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afbaeae156c89776da7468752d9ee2392816ff4e3ccfeade1d8ecb4f8b6cd24`  
		Last Modified: Tue, 12 Nov 2024 03:53:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a271f5f171f5be7c56b275d054fe96f39f58933c3b54cfe0368a050bfff426f6`  
		Last Modified: Tue, 12 Nov 2024 06:45:59 GMT  
		Size: 12.1 MB (12147079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bcdf93fc1a1d25c560282f775b6e9b808ecef14bea6359c8ce917fc64bb3ce`  
		Last Modified: Tue, 12 Nov 2024 06:45:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e33bb264df7185833f5aef1305938dd1c5716b579bcf698e9af25f7e51829`  
		Last Modified: Tue, 12 Nov 2024 06:49:42 GMT  
		Size: 12.8 MB (12824102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888dc341a8c698cf4720bc793be0a129f8b479d6b3e74e6657dc9e312843a27`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b967bdb6dfc02193909cbe798766157a4ba2854e7ca1fa2a4126f4d6a94a4be`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 19.3 KB (19314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d03f758561d18d2e9bd0605d4ea684d60d2970c57e1b8352396721238837b28`  
		Last Modified: Tue, 12 Nov 2024 06:49:41 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e25b2d0a2eb16490e3d990d94d028b00317a2bea2492f487dddf36a8ba9880`  
		Last Modified: Tue, 12 Nov 2024 23:43:44 GMT  
		Size: 2.0 MB (1999435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9a0d0ee02bcb3c52e3898d9652243dc011fc9bda724cec29220ebc179ac5c`  
		Last Modified: Tue, 12 Nov 2024 23:43:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de452da92ac71894367e874a1cdcb4c8f21d1e322df7b2a0c4496e74c47ca569`  
		Last Modified: Thu, 14 Nov 2024 18:00:26 GMT  
		Size: 739.0 KB (738956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcf2dfe5b68c6235c1c05d19d72e1e023be97df12fabfe76e41ff2ffa69f7c`  
		Last Modified: Thu, 14 Nov 2024 18:00:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e985be8fbeda9713c897f55b4c1169a2a4765c2e0362eb7aa1fd44f544f79f5`  
		Last Modified: Thu, 14 Nov 2024 18:00:26 GMT  
		Size: 21.1 MB (21123708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:f4c1ac8ff373870ef302a0b6b27b2365df80f1c8d7762fe53e3a0083ab5e3642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 KB (382139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b6880a4f0ee61e4c182cca20b17ab18f53cf2a5e9eb7313d039977499e905e`

```dockerfile
```

-	Layers:
	-	`sha256:ba10c400df6de3653fcd0fddf3e906f04b99febed8b6819a9e25fd5fe66d9417`  
		Last Modified: Thu, 14 Nov 2024 18:00:25 GMT  
		Size: 349.1 KB (349101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3865c4a6b2e833fe6c8ad2e4830e445d44eb434fcbf9e038559c186f60fa41d6`  
		Last Modified: Thu, 14 Nov 2024 18:00:25 GMT  
		Size: 33.0 KB (33038 bytes)  
		MIME: application/vnd.in-toto+json
