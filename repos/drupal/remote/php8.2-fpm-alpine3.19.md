## `drupal:php8.2-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:671728bc6e0113937354978c966059dbc8c56d33c9c1545fc2a7eef9871e9ff9
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

### `drupal:php8.2-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:ab5e3232f1d6a0e0add7eb7128d78525da5f0fbc1e92494399d463dff31e9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55885928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f334dd35ff66ea5ce2c9af2689d1f074d81fb48cd0dfd10796854e8358cb6c0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:39:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:39:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:39:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:39:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:39:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:39:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:39:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:39:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 21:36:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 23:52:53 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 23:52:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 23:52:53 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 23:52:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 23:53:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:00:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:00:46 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:00:47 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:00:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:00:47 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:00:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:00:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:00:48 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:00:48 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99979baa6760dc40a927f812328a1431e3870d0f166b035365166ef2cf8d4`  
		Last Modified: Tue, 12 Dec 2023 23:24:24 GMT  
		Size: 2.8 MB (2755737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47536423e0797b82f7a737a4efeb29297c96a33e8662ddcd121d728a01eac477`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6d4fc569fcdbdb835c5ee3607367e6ba4779809c0fad97de75045144220f8`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d5f73e08f0d6f47a6d68c93eb6dda6aed5fda619b27a0543328708f69a3a4a`  
		Last Modified: Thu, 28 Dec 2023 01:21:30 GMT  
		Size: 12.1 MB (12101522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72253ce4e5f473139968ddb4f9a5dd5980d0fadf3ad88dcf92660f6461ad5f47`  
		Last Modified: Thu, 28 Dec 2023 01:21:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989df9c2dc530e9abf5dfbc22c6c7cbf9fcaa3010ad89231be796d2038caa5c`  
		Last Modified: Thu, 28 Dec 2023 01:21:57 GMT  
		Size: 12.9 MB (12881126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8e54beadbb740524dd743196580399313ae9efa448f90ed065260fe6531caa`  
		Last Modified: Thu, 28 Dec 2023 01:21:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a8b8db10b40ea43f278bb4be217c1db1c09c854eb61939637fb86e2bcd2e18`  
		Last Modified: Thu, 28 Dec 2023 01:21:54 GMT  
		Size: 19.3 KB (19290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e739aaa9a63202a8e844a8eb9c231d9ec8d9b56f5a5fb02f51a28a0f727e0f74`  
		Last Modified: Thu, 28 Dec 2023 01:21:54 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7e9ed66ca2b44900b7c2a71bef79a41bdfe78a2e42469b5829a2d92acb2fe`  
		Last Modified: Thu, 18 Jan 2024 01:01:13 GMT  
		Size: 4.8 MB (4785536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73d6fde4eee0c5f64298f82afdf9010c76ff8ed1ddb0b5676cf3f9b2bdbec8`  
		Last Modified: Thu, 18 Jan 2024 01:01:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736cbbdfce8616609be4155bcb04628d1ac6a647bfc283e79bc5999f5863dbf2`  
		Last Modified: Thu, 18 Jan 2024 01:01:12 GMT  
		Size: 705.2 KB (705209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0342fda5968a4aad3ab1545f0d8d530301844cc140a6f251f50f1122d6f009`  
		Last Modified: Thu, 18 Jan 2024 01:01:12 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c590a456926bb6fbf626fe0f4cb72c31b252f012ad41acc5be1c577e3288ba`  
		Last Modified: Thu, 18 Jan 2024 01:01:14 GMT  
		Size: 19.2 MB (19214942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:7a29bbb36f7989366f9baa7d4ccd488ca993241b011f37663143372ba4ef140a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 KB (326607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884b2ced7589836365d4aa9a06481d722b0429bb537f585a9bd7546583cae396`

```dockerfile
```

-	Layers:
	-	`sha256:029c03077361e128e2b123c718a55a3f0f9a513cd68950e3953bd9d8573a33bd`  
		Last Modified: Thu, 18 Jan 2024 01:01:12 GMT  
		Size: 288.2 KB (288216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3493c7241216cfb95fbaf00b8f708b38b7ceb5bccf07826065212d52b12c67cf`  
		Last Modified: Thu, 18 Jan 2024 01:01:12 GMT  
		Size: 38.4 KB (38391 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:4f7c4546e3dba934c936437bedcc68b44278ad85d7d21701e25421db3f2d633d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51440661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffecdcc8807818219940404f104fd66009c8ebf0c8139c97a8b3869e1bd5ef4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:01:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:01:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:01:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:01:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:01:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:01:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:01:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:01:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 20:49:57 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 28 Dec 2023 03:02:18 GMT
ENV PHP_VERSION=8.2.14
# Thu, 28 Dec 2023 03:02:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 28 Dec 2023 03:02:18 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 28 Dec 2023 03:02:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 03:02:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 03:08:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 03:08:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 03:08:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 03:08:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 03:08:24 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 03:08:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 03:08:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 03:08:25 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 03:08:25 GMT
CMD ["php-fpm"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6157a5053a6ba5646a1361153760014335e77813c8792b60d226dedefbb229`  
		Last Modified: Tue, 12 Dec 2023 22:10:24 GMT  
		Size: 2.8 MB (2761045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682a06d9f91bef66466bcb1b37715dc344282ac9f062ffff8405cf448d71f51`  
		Last Modified: Tue, 12 Dec 2023 22:10:23 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982a61382f7fcec3d428935d516ac99bf603d105e72ebe0c2952b860f329675f`  
		Last Modified: Tue, 12 Dec 2023 22:10:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cdd604279ad384783d61fc0a61964b7261cc9e8304180faa7df167e087c660`  
		Last Modified: Thu, 28 Dec 2023 03:41:14 GMT  
		Size: 12.1 MB (12101539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607a7d9f29ab788170913d1b9bc5ff323b05ab432c9c019403110aee118d4127`  
		Last Modified: Thu, 28 Dec 2023 03:41:13 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae0dcc698b2973af6b3b3990c4603d1a19de9510646c82a31f3a9b193be577`  
		Last Modified: Thu, 28 Dec 2023 03:41:42 GMT  
		Size: 11.7 MB (11722896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4fee5187453aee8192b6642326b072e2c9aefe8a131d4df65456837fdd49e0`  
		Last Modified: Thu, 28 Dec 2023 03:41:39 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ead70c331d76cd6395d9390d84ac1c75cbf020719209e7b854ccd5ab6916ecb`  
		Last Modified: Thu, 28 Dec 2023 03:41:39 GMT  
		Size: 19.1 KB (19123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da4cd14bd5aa0935716c61f1e6cd94abd6ea350134523623d46269a28cb9083`  
		Last Modified: Thu, 28 Dec 2023 03:41:39 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022925cd669d30da2301cba713380c175b1433105365847d96fcbb68bb1b5dd1`  
		Last Modified: Mon, 08 Jan 2024 10:44:30 GMT  
		Size: 1.7 MB (1739733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f633df481d8666e988efeb96ead47ae416d0ae37eb70ca8a0e55ed8f48ba8`  
		Last Modified: Mon, 08 Jan 2024 10:44:29 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839ecbe0f9421fc0fd982b62f989209da653550e9ae29574b2b3f2e272bed6a`  
		Last Modified: Mon, 08 Jan 2024 10:44:30 GMT  
		Size: 705.2 KB (705210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f766a35a866aa05f585b585ef74112060796cf11eecf898270d676e2f1236de`  
		Last Modified: Mon, 08 Jan 2024 10:44:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e78b81109b31b66dc59182a21d30dfad47d27d0d2e3f87c22d1197d44f5ea`  
		Last Modified: Mon, 08 Jan 2024 10:44:31 GMT  
		Size: 19.2 MB (19211890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:61a771f687f9a551793b33d13df0af0477a4657ccd6e6b353198687a90299e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 KB (36062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b555417a2ff4cb09a4ff0bfaac89bfac4b63080e2b323711ff63f119f0e197`

```dockerfile
```

-	Layers:
	-	`sha256:ff7bf289cadb8f4f3f885513bf089c000a4eb97d593795958c0b5d09ac6be307`  
		Last Modified: Mon, 08 Jan 2024 10:44:29 GMT  
		Size: 36.1 KB (36062 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:dbfedacc85b8a9cb916cbda260fd0745a0c5f391a23cf31e36095799d551cec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50177188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e178d5eb8f28aa6a77f0e6157bfb489db4320f0d3d2adf4d84ebb5f0efa79327`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:17:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:17:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:17:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:17:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:17:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:17:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:17:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 21:09:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 28 Dec 2023 00:39:41 GMT
ENV PHP_VERSION=8.2.14
# Thu, 28 Dec 2023 00:39:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 28 Dec 2023 00:39:42 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 28 Dec 2023 00:39:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 00:39:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:53:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:53:15 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:53:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:53:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:53:18 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:53:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:53:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:53:21 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:53:21 GMT
CMD ["php-fpm"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fcdc554dd7b708317247ba5731b0d76bc06dc68a48af57f662820d33c665cc`  
		Last Modified: Tue, 12 Dec 2023 22:36:17 GMT  
		Size: 2.6 MB (2608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4717604343f2899832c4417228ef3cdb02080f72378a4152eb72083f09c96e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a6a05c32e2329e654bc633b417da36b7c74ed6bf626231bf0e900f912838e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8e310a28362f149eda79e811306a7d91d36f17409facbd7689f4597d1b2ea`  
		Last Modified: Thu, 28 Dec 2023 02:53:52 GMT  
		Size: 12.1 MB (12101534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903683171fb30acca9f6eda7a4b4b0fea5f6d25b7b3a91e4178ca70687d5cee6`  
		Last Modified: Thu, 28 Dec 2023 02:53:50 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768f39e622e527524eb69dd8cc727be2bfcddde8e489912c4bedd27bba6c096e`  
		Last Modified: Thu, 28 Dec 2023 02:54:20 GMT  
		Size: 11.0 MB (10990942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0e33104c14fbe82add4f31f086d1840f9df03b50c5455b421fa98fea0717b`  
		Last Modified: Thu, 28 Dec 2023 02:54:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7e006b22076762b0173d45f1a4ceb4ad6efe15c12057ae07c4467af52f3c3c`  
		Last Modified: Thu, 28 Dec 2023 02:54:17 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7535fb14b49a3e96552ba8b14556970b13708ba0d14d237c9a28e77b6b6e41d`  
		Last Modified: Thu, 28 Dec 2023 02:54:18 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31810c97b23c308fb53713151227be051db5112751b891d5a272616145e063c`  
		Last Modified: Thu, 28 Dec 2023 08:40:11 GMT  
		Size: 1.6 MB (1604332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276416dc935caf948efb987e65c1df5d8f15bf3d48edc4763891ac0e9e199c79`  
		Last Modified: Thu, 28 Dec 2023 08:40:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ad06e31500fe2c990cea679b8372fd2a4d28635bd15f449aedaa2b691c2f7`  
		Last Modified: Thu, 28 Dec 2023 08:40:11 GMT  
		Size: 705.2 KB (705207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c568a5ef19dc63ac5341f613b3308da5b5eb863a7e39943898c510b5d83e377`  
		Last Modified: Thu, 28 Dec 2023 08:40:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09408e01221e4995c71dd2882e2ef5fe35f385f972437b3e055d8d8c3bd7908f`  
		Last Modified: Sat, 06 Jan 2024 00:38:24 GMT  
		Size: 19.2 MB (19214621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:9aa5fc82dd1f5897b5015204225b3bfdcc137385bc67c6a520e44d8c40bc050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 KB (317430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ecbfc43f3f5da85181daea1169ec803a7c1ef773844af2224541c99ff2442e`

```dockerfile
```

-	Layers:
	-	`sha256:9b797ec985b8fc09fa23b9e89d31c7f97de8b24e48057d47a8299b8e7915385a`  
		Last Modified: Sat, 06 Jan 2024 00:38:23 GMT  
		Size: 285.0 KB (285016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8fbee31dd8453f35da66d67349fa51135c674e2544f844d793ba7614057f55`  
		Last Modified: Sat, 06 Jan 2024 00:38:22 GMT  
		Size: 32.4 KB (32414 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:67aaf680476031bbf198a3542d9d82dafa6960bf38191dff32997dcaa9e62b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53711628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c7a16b449364ad34292a4974ed10cd1ff14fe7b8cf833b2fde046e44f12903`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:09:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:09:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:09:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:09:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:09:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:09:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:09:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:09:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 21:09:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 23:12:03 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 23:12:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 23:12:03 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 23:12:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 23:12:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 23:20:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:20:06 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 23:20:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 23:20:06 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 23:20:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 27 Dec 2023 23:20:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 27 Dec 2023 23:20:06 GMT
EXPOSE 9000
# Wed, 27 Dec 2023 23:20:06 GMT
CMD ["php-fpm"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a19b0853c69aaf4e0a33f42601f1bddea728304bef39e2fc08f66f3d518576`  
		Last Modified: Tue, 12 Dec 2023 23:00:29 GMT  
		Size: 2.8 MB (2810204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ba87116831a71587816ab8564d1a2b7137e1163524eb7e5abf40966e6882c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a9508fcdd73dc8c678f841adc3269e9919da38f14917ddaa2162b636d4661c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761824eeb66a1bceeb5e0739c46c0dfb7f07e77a61f9d061966efad19767058c`  
		Last Modified: Thu, 28 Dec 2023 00:37:34 GMT  
		Size: 12.1 MB (12101537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56dad5070e8cec6dbd0376421e15fb8baf8b9fa7d1a9b20449f4d4d8752e91e`  
		Last Modified: Thu, 28 Dec 2023 00:37:32 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfb08faf44d1ee9c2955abb850e4357bd1f5854c34952fff8b2a8e104ef5daa`  
		Last Modified: Thu, 28 Dec 2023 00:37:59 GMT  
		Size: 12.9 MB (12946628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc20601176095bbb7e47a5e07bad5a42f5b3b84576b5586ae2881ece573d96a`  
		Last Modified: Thu, 28 Dec 2023 00:37:58 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d194bad833596395d07582ba633e3733c4d44dec2073db00c3f6943ec7e3d0`  
		Last Modified: Thu, 28 Dec 2023 00:37:58 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e3abcdc6cf7d085a8ffb5ca548d9bb4d47da9888c3d80b6d8c4fe2d231015f`  
		Last Modified: Thu, 28 Dec 2023 00:37:58 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2def3baae64af6b7d223686dcd9b493dc04216d9535eb1f744dc599b0bf830a7`  
		Last Modified: Thu, 28 Dec 2023 05:39:21 GMT  
		Size: 2.6 MB (2552916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616645bea9cae8ac60949089998dfdc5f24c0ea3253987623716fc86fa64e920`  
		Last Modified: Thu, 28 Dec 2023 05:39:21 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f46a555f10cd2344f398dd926dc744ba9bbcd5ba633551a75296611e2bb921`  
		Last Modified: Thu, 28 Dec 2023 05:39:21 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fdb8cf6020a3c337dc6e8379c64f3524499a200e779db9fe4dea3e40de02`  
		Last Modified: Thu, 28 Dec 2023 05:39:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1e4235e63bf5d1739fba9545fabe7e99868fe97ff82d09b270e259b97a293a`  
		Last Modified: Sat, 06 Jan 2024 00:20:15 GMT  
		Size: 19.2 MB (19214175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:159704d6515be4e3524a9cc6ff8294803baa09fdf463df0aeb46641c15eab97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 KB (317161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edce573fc258aee30fee6af3094fcdf485894357bc1b2d5aa846a8666ededf3d`

```dockerfile
```

-	Layers:
	-	`sha256:d8ba33200522a4bd6019dee32d32707991d1b4e816e600c99e1db38ada8d05ed`  
		Last Modified: Sat, 06 Jan 2024 00:20:15 GMT  
		Size: 284.9 KB (284919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68642f443cedab6702b49db9a7e5a0293fd019a20c635a6a74be5f0c0467b8ad`  
		Last Modified: Sat, 06 Jan 2024 00:20:14 GMT  
		Size: 32.2 KB (32242 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:03efeb69a7a517878ffbcfb87e133cc82ea1e596d9d235c209040351618cc2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55992261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc01d50f7aa9cf9418642474f9a9d8cce047c575740470f878d8763fbffe4dc6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:00:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:00:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:00:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:00:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:00:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:00:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:00:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:00:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 21:33:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 23:59:34 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 23:59:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 23:59:34 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 23:59:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 23:59:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:13:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:13:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:13:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:13:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:13:10 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:13:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:13:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:13:11 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:13:11 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35c853c51aa63c9f21d6c91fa6948b8160ed6a90764a48e7b1891c38e016590`  
		Last Modified: Wed, 13 Dec 2023 00:34:22 GMT  
		Size: 2.8 MB (2820917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6af7fb9ea0ea850c653027fa7b1b18f1d4c405aade35df3c3ec2151bb8251f`  
		Last Modified: Wed, 13 Dec 2023 00:34:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233674231d3f63e2099e1d4253bf67fd488ef3d4fcd72e3e741ffb7a41f385e`  
		Last Modified: Wed, 13 Dec 2023 00:34:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47d5e9ef894b4813fdff313f6505023018dd7c50f8a06e3d17096cffa1552ad`  
		Last Modified: Thu, 28 Dec 2023 02:21:51 GMT  
		Size: 12.1 MB (12101534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26bce96edd16d86eff8fb73e4df4d021c21fc7b3853dbcf17aa54c694e2f13f`  
		Last Modified: Thu, 28 Dec 2023 02:21:50 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195900465d26fd6460dcded36947e2916134a9aca8c20a6f523009dbda678583`  
		Last Modified: Thu, 28 Dec 2023 02:22:20 GMT  
		Size: 13.2 MB (13228250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f86fa0bef92796a6019981b222b580bb561fbd9281be9ba7854b32545d49d13`  
		Last Modified: Thu, 28 Dec 2023 02:22:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55863e49df9e79c775355f0e0c3364e76eb7ad0b8c2fab395dc1cab2b6313a`  
		Last Modified: Thu, 28 Dec 2023 02:22:16 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d1689b3ed687f522933d83484b2b756c317c12fd4312514ee7bbcf001745bc`  
		Last Modified: Thu, 28 Dec 2023 02:22:16 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f56e8b8d6ecdcf906400e6fc064dc7575a385d23257a0cd5a47fe7f5220d7d`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 4.6 MB (4644379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a83a5fa0f2753403152b664fa1d120a984763e013eb4192a913124732616776`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9b1bde84bda39fc4274eaee18c83c19a6c98f4b2f9bd7c4af264e6c5b27c8`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 705.2 KB (705208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ff7f226ad58e74dfb2cf3832baea78994e04f9049eb6c03c72cdc270932b3`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c7b40d5614c19da1ee1af0f83875481982cd97c87da154543b477c769d409`  
		Last Modified: Thu, 18 Jan 2024 01:00:43 GMT  
		Size: 19.2 MB (19214476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:38fc9a7596d8e433d204b98e3b5c47060b6e84c018753e96d227644c43ed4f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 KB (326424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24328a06ec9a558f8a5c2aace9cdb9c24f89dec0f615c75f9e5bf42ab91aea0c`

```dockerfile
```

-	Layers:
	-	`sha256:5b97e9a4bd8757789523cda4e38c76f900ff11541a22157d2d181714158c6730`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 288.1 KB (288131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78475f6408df02daabb5a33d74d3db0fc8bf692835e3b56ed2a4e178f0d57609`  
		Last Modified: Thu, 18 Jan 2024 01:00:41 GMT  
		Size: 38.3 KB (38293 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:b1499c764778f290362b4f80647a946e01d276022e32a4b88792af70fa6f995e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53735417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e3291fd5e6d57614bd0a76275335d366ed8f1f462d761a048304c293ac71ad`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 20:31:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 20:31:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 20:31:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 20:31:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 20:31:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 20:31:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:31:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 20:31:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 21:17:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 23:50:30 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 23:50:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 23:50:31 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 23:50:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 23:50:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:57:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 23:57:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:57:38 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 23:57:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 23:57:39 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 23:57:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 27 Dec 2023 23:57:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 27 Dec 2023 23:57:42 GMT
EXPOSE 9000
# Wed, 27 Dec 2023 23:57:43 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89935d2f947cbd3585545f82639d347027ef82fbbf413f8684101953ea74bd6`  
		Last Modified: Tue, 12 Dec 2023 22:41:51 GMT  
		Size: 2.8 MB (2838539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208bea042d5cdcbe6436f88d2f7ea51b03a91df91ae099118f57b644b87bdb2`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb83a14858379fd485cb474c02417cd209b148b775365e9bae3ab90f5fe798`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c6be4cac9dacdfd1c8eac6494a01abde16c8520309970babd8ddd7f58a7db5`  
		Last Modified: Thu, 28 Dec 2023 01:05:28 GMT  
		Size: 12.1 MB (12101539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cbdc56dfac4901b8272b7326b5e7da21b3ff6c2f0393d777924a899531f073`  
		Last Modified: Thu, 28 Dec 2023 01:05:27 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5038942ae064b70f7e6554fb91eba3c15cf1702760f980eb8f393dd89b14794`  
		Last Modified: Thu, 28 Dec 2023 01:05:59 GMT  
		Size: 13.4 MB (13379214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805de5d1c05f8a44edab61a0335857cdca1b14bf155d5eed2c41a2e41a33673c`  
		Last Modified: Thu, 28 Dec 2023 01:05:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fbc35ae751f556b96229787bee3392ebfe7f39e0e3f8fb22d588805f9af632`  
		Last Modified: Thu, 28 Dec 2023 01:05:56 GMT  
		Size: 19.1 KB (19102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708212f9dc749cd67a0fe8c2fc1ef048ad2998f36a0e39a4ef6e6aa0b2374d02`  
		Last Modified: Thu, 28 Dec 2023 01:05:56 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c438d10ce61632c2fd68849fadd01339a9984d6b83e05c13d33e407afb0d39`  
		Last Modified: Thu, 28 Dec 2023 05:39:37 GMT  
		Size: 2.1 MB (2104487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5745fe52557b7f5230724c6c8747a74e542b825e4b94e295fb72749a358395cb`  
		Last Modified: Thu, 28 Dec 2023 05:39:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec02d4f6faedb581e40d07ed1bab5bc78d0f5320652b4ecf6573d2cb5f646cb`  
		Last Modified: Thu, 28 Dec 2023 05:39:37 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b0b27bc21a89f9b0e982c1e38cd72cc0601a1c1b2a47a7f62948ab72e5f175`  
		Last Modified: Thu, 28 Dec 2023 05:39:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d01a8ef704fdef3b41f4ec56ce59559ae727724e0187b1ec64a3878026f16d`  
		Last Modified: Thu, 18 Jan 2024 01:31:08 GMT  
		Size: 19.2 MB (19215002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:4901cf9bca695748d80abbfde8674edf43c18250257eb0990d61f4ab82726bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 KB (316540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54197e1cfd6e2b4558c0e11f2406015038bf46d8705f63e2daaa0a6a67c7bcc7`

```dockerfile
```

-	Layers:
	-	`sha256:b6db114e6a5e5e705c381babb52c8d50cfe8bf78dd297058bd1528b439fd146c`  
		Last Modified: Thu, 18 Jan 2024 01:31:06 GMT  
		Size: 284.2 KB (284214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276c74f5ac6958e3b7783322e648e872326ce2212cd9a4fa4e32030f34ffce32`  
		Last Modified: Thu, 18 Jan 2024 01:31:05 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:6da4c968e0eb7173f333a971b82e527a6803cf6d3f1d7838171ca2d6df39bf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52861942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af67897f787516700803aaf3e01973fd05eab9d84d8e2db733df6e92a86d6932`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 19:58:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 19:58:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 19:58:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 19:58:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 19:58:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 20:42:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 22:42:24 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 22:42:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 22:42:24 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 22:42:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 22:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:47:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 22:47:57 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 27 Dec 2023 22:47:58 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 22:47:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 22:47:59 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 22:47:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 27 Dec 2023 22:47:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 27 Dec 2023 22:47:59 GMT
EXPOSE 9000
# Wed, 27 Dec 2023 22:47:59 GMT
CMD ["php-fpm"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e288a28783d4cd969dd1990881bb3af72dea005727b0a012c1e2d6dbd56480`  
		Last Modified: Wed, 27 Dec 2023 23:44:35 GMT  
		Size: 12.1 MB (12101547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96590b2061bbd5bbca94ba50cfaacba3e750437b5f8ac4724e3b6a4d7a1e8cd5`  
		Last Modified: Wed, 27 Dec 2023 23:44:34 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e18a3d85df266d100130ddc7ce78b9f74f1a3aee60e3e97c8d7aa27101d34`  
		Last Modified: Wed, 27 Dec 2023 23:44:51 GMT  
		Size: 12.6 MB (12628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f866d0a2cde38af476f96897f01fb36ce3506c1dff64aa74b8b56d32ed6ef09d`  
		Last Modified: Wed, 27 Dec 2023 23:44:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcfea8e2ae0f6c2d41ec6fd3fda4eb06707ed7058822f8bdc5dd7aa783da71`  
		Last Modified: Wed, 27 Dec 2023 23:44:50 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2158e8142f744b77999ce9de8c062bf5fe260d3632ee916150371bb7831d2785`  
		Last Modified: Wed, 27 Dec 2023 23:44:50 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31423e97af7eea46b09341b961d91f4dcbf5ca80ef23098a9a76aefe3be5da2`  
		Last Modified: Thu, 28 Dec 2023 03:08:23 GMT  
		Size: 2.0 MB (1998228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a53358dd1a4f5baec0001fe30822217afd718b62fcbe24c584af24ce4d99f7`  
		Last Modified: Thu, 28 Dec 2023 03:08:23 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886190163af3ce20f0ef54a5ea16cb28c4397a1eb5040637a8ba62ddaa4c0e43`  
		Last Modified: Thu, 28 Dec 2023 03:08:23 GMT  
		Size: 705.2 KB (705208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceab70044dd758d1c2bdb08b712dabbf29bae791bd69fc282667115ad3cf57`  
		Last Modified: Thu, 28 Dec 2023 03:08:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5015883838e8ee53aea1efff9c7abbb167df0179bbffd8fb3418aff375981a6e`  
		Last Modified: Sat, 06 Jan 2024 00:12:00 GMT  
		Size: 19.2 MB (19214563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:89a2de424ac4fbd152ca3962fd4f4d8b80bb0ee77bd2cf2b3902ad6bab683730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 KB (315456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1f8b02523edd5166dc5bb62d30c67f90a6e6c9502cbcffdefcd336e1492746`

```dockerfile
```

-	Layers:
	-	`sha256:061557af3ac253ae12415f114b47a98171603920f735151b9935d846a653c191`  
		Last Modified: Sat, 06 Jan 2024 00:11:59 GMT  
		Size: 283.2 KB (283248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca76a34bbde5e25e49a4b4cc91d31a908fedff557aeec0809251d83564e9e7d`  
		Last Modified: Sat, 06 Jan 2024 00:11:59 GMT  
		Size: 32.2 KB (32208 bytes)  
		MIME: application/vnd.in-toto+json
