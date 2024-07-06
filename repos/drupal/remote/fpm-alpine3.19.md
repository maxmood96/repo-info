## `drupal:fpm-alpine3.19`

```console
$ docker pull drupal@sha256:7fbca292fe893e543963d2eb1e05e64cf1fd48965a90b32597245b662169fbb5
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

### `drupal:fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:877d131f0ad6ffdb6f387e618d2bbab1b28452afca5611db2706ebec3141129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57800990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a75a8a05086743fb2d951ef72b8080b317a93559025425b102764b56dbe3a5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:13:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 21 Jun 2024 01:13:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 21 Jun 2024 01:13:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 21 Jun 2024 01:13:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Jun 2024 01:13:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 21 Jun 2024 01:13:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 01:13:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 01:13:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Jun 2024 01:39:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523087b9c271ae77d92e944ca833899bac59254ff834ca6106f2b0008f864382`  
		Last Modified: Fri, 21 Jun 2024 02:21:54 GMT  
		Size: 2.8 MB (2775517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d060ecc216f23e008efa4494a28853d924be900e357c22e573c279a319af6a4`  
		Last Modified: Fri, 21 Jun 2024 02:21:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597315652e0b3a62ece26492f0cc07086c503fddccf28f6b8cb0f3cf5632068`  
		Last Modified: Fri, 21 Jun 2024 02:21:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cf55575b77cb8cfe9d488d820bc8edea1f1a23c1ce548118f43fe309ba73ad`  
		Last Modified: Sat, 06 Jul 2024 02:32:36 GMT  
		Size: 12.1 MB (12128106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a09060bf37a118d1b7473012663ae0befdb26ee738e8a948ee1ebe85fa5f09`  
		Last Modified: Sat, 06 Jul 2024 02:32:35 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8760940fb00ec7d4794f9d268ceb4fad99c6da55e5ebbbad738a8c82fcae957d`  
		Last Modified: Sat, 06 Jul 2024 02:32:52 GMT  
		Size: 15.4 MB (15368899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7220a708423dca8263ffb3f3c1de83940763ad9423d8b0e1a8122f536f140`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfd7673daa8e5237059d12a313133f65eb3a913bf77c345a6ec3c667477fb52`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9861f228f6e591089eff7192817b138cfb73d4ab8ce6f661859d101a3b88e68e`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053ef06d1f0bea25cf9fce50f7ff3a7640d25367a671317f8678996643e0aa54`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 2.3 MB (2282636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59de2703bbccf218bdcdfd0f8d0afff2e6fbcc88e000a151da6948a0f3e7d9e`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f92ed3a4b7ecb6d902529a4afa99ecf9debbc0e216fa937dd897c822a42ed15`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 726.3 KB (726329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfdb2770b04e9387b098e484ba02308ba35ad353674be01583eb0e5f10d0d14`  
		Last Modified: Sat, 06 Jul 2024 05:55:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38932969ff625bcc279759169654c58d60991261cdf138b92f718c8dfa486db`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 21.1 MB (21068607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:b3b8741f084b458fad299f0c3943977c1fda7662b30fee5407bd804f9bc1f0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 KB (365471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18642c327a451687e3d73d50d07cfa336a7fef1b7524b9017eb71e86193f7b99`

```dockerfile
```

-	Layers:
	-	`sha256:b18bab4fdf6e8caf60afe568246a198ac5738ce02fa09527e2452168e7928cbe`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 332.8 KB (332833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24378990255d89a8530d6999a31f79af9b42b2b88ec56613b0fd7a8f565f9b42`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 32.6 KB (32638 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:a184d288d2c054f5c3c076ae367a77c56deca824b15980815a216899b52bf258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55568254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0814b26b177a23ddd723b5534de6df642691ee68ed112be270e557f404704f4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:14:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 22:14:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 22:14:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 22:14:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 22:34:53 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fe3503923312700d0ad215db61ad54d143feac25bfc14ba0b4eb2cd554730`  
		Last Modified: Thu, 20 Jun 2024 23:11:30 GMT  
		Size: 2.8 MB (2782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e727f9d3c5208e6085f44fcc1802704b726a7b2b884ee795f8ceeb3594b9e6`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49ddfbb89fe4110ef4b151edfe03948f99fe5bf8d637ef0657bd9bb46d10c9`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2368e5ce245a66b896fdca2929871af7aea500be9686a338a63f5df6ec25a9`  
		Last Modified: Sat, 06 Jul 2024 01:50:35 GMT  
		Size: 12.1 MB (12128120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e5c686c402b03f8de8ea90c0332f36c642d3a80f2af6f929f82cab057f5f6a`  
		Last Modified: Sat, 06 Jul 2024 01:50:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964b4ee7ab28d81fe832aea7eb1e0c9c7bae22beb6f1185126c66b1c76d0b4df`  
		Last Modified: Sat, 06 Jul 2024 01:50:52 GMT  
		Size: 13.9 MB (13914969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f6b07a343e4756289bb0abde600492d458eb65b8cab249779c203ee46bd944`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43145b115e3f355c0cbd6bd777a936eff9d2e1a5f7d7a30fbb84aab8245feb7`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 19.4 KB (19407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f2c13b4cf2b71b2b85e3b525c0703a273cf920bab32bba19986152178e5`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a233c8619da452e0af3215592a8048e51003ce0e3093b777dd127260bf4b17`  
		Last Modified: Sat, 06 Jul 2024 03:10:45 GMT  
		Size: 1.7 MB (1740113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e363bccce11f18646d5b5884a6470b3948bd2e0ba3ceef932e6c834cb706f`  
		Last Modified: Sat, 06 Jul 2024 03:10:45 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f59f97f5f583e5c2db7663acdd8302f806e758fc7efbe3e7818c6f37089f5`  
		Last Modified: Sat, 06 Jul 2024 03:53:34 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf5d374fb2035adba7616c4d4de5594a4bb8871b0f3f34012c44e4343138b1c`  
		Last Modified: Sat, 06 Jul 2024 03:53:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dda07ef08c94f86e680ce8e833a89d9e7a68cc87430c6acbf4501f87cd5de96`  
		Last Modified: Sat, 06 Jul 2024 03:55:49 GMT  
		Size: 21.1 MB (21069198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:6ac1500fe42e04ed27e17bab61b170e863d470dc22e634294848daf8b8abccb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144fbb40028cc9cd3e454a26ea1d4f770c88826625a6b2fe75cfa0d202472275`

```dockerfile
```

-	Layers:
	-	`sha256:f294cef411fc26bbbb8fc5d6647ee8631772f651c4d1f369798bd841f16896bf`  
		Last Modified: Sat, 06 Jul 2024 03:55:48 GMT  
		Size: 32.6 KB (32623 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6f91d64dc9b10196cc4349ef10a1836a9113d92ba6e6291d8e3d681c0ca37e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54148176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3c900d766f8e035e2daaa015b3d5fa4160ad29b8269847cf2c5f823c2fa437`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:36:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:36:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:36:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:36:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:36:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 19:11:23 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd2f7314fb5a1bddd9717973873845b50c0071affc1e794041d120c75898de`  
		Last Modified: Thu, 20 Jun 2024 20:09:38 GMT  
		Size: 2.6 MB (2624592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f23dd8be0ad44d730123eaa34961b21523892832d003182b0254c0a46ac650`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd5cf20011ab84a0de7e85853e1003271ddd0a307016623fddf7d0a902750d5`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3077ca3d521190f3f7a94174e2f924f518e43d9049ecc081774f4048adcfe74c`  
		Last Modified: Sat, 06 Jul 2024 02:52:22 GMT  
		Size: 12.1 MB (12128109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0298efb242bd0b948f75ffbe3a86f7af0f5c65e39808e38b26de6324084d096`  
		Last Modified: Sat, 06 Jul 2024 02:52:21 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a86f23bc8b0c44fd51bd26d8a4cff4a566312cf68764f0dd77af5b05a3170`  
		Last Modified: Sat, 06 Jul 2024 02:52:38 GMT  
		Size: 13.0 MB (13035223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbe0ea5db2c0c23f3bbcec66845754f2033888affde2530f5bbe8be2ed770e`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783404d469d5fa09aca9164a4eaaddd9bcf5800a690ef8aa025f48e9e190105`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 19.4 KB (19378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3908eb7915b269be27d59fdec0c83a0c59672f76ad3411ff9e5c283cea47f29c`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f9f38b080183b0003beda026b119253ce2e8a6a4c7096864805fb4a64b831c`  
		Last Modified: Sat, 06 Jul 2024 05:29:47 GMT  
		Size: 1.6 MB (1604849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1429d71e6e906e8b58e8936ad7387cc9c4c0948dfadbdb4611206251914b9a`  
		Last Modified: Sat, 06 Jul 2024 05:29:47 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0585463d436b63027a6445f240370fc6b4e47fbaa52f7aa0cc6ee17fb6c20a24`  
		Last Modified: Sat, 06 Jul 2024 06:06:55 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2dedbfdf180812e3fc53804f05d9f98aa45c6ce0fe1c12dd741e66a9483a19`  
		Last Modified: Sat, 06 Jul 2024 06:06:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46ad5f02ec93e302559a87d33c7bf241aeca75b8814ac186406fd520176d414`  
		Last Modified: Sat, 06 Jul 2024 06:16:45 GMT  
		Size: 21.1 MB (21069176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:c8d376d57add8d575e870709020b9c3ccedb5528c6a72db8cc2e40ef7727f669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 KB (363165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafb813306df30b5aefcb2f6216fd372e3f0088aa7503a17e52f251fcc915bdf`

```dockerfile
```

-	Layers:
	-	`sha256:e01e534e6554f7f4894186c534d43a428938a2dc18eb18f44fff157bccceb99b`  
		Last Modified: Sat, 06 Jul 2024 06:16:44 GMT  
		Size: 330.3 KB (330323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad9dc9cea4fe550daebe7530294bb78e7673e590b15a394abbdc08a4ac4ffe0`  
		Last Modified: Sat, 06 Jul 2024 06:16:44 GMT  
		Size: 32.8 KB (32842 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ea88100a2e03e616c1baa019e882fa358e6377a6474a17a6f9537345f8249996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (58036905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1de4828ea3615b43976cd9f7b3d1684c9570288c857a8ca8be4e48e1852bc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:51:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 22:51:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 22:51:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 22:51:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 22:51:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 22:51:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:51:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 23:18:07 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01446ea5918cdf1fe1b865bb8d7330b56410ce93061441cfcbd2f22e4a75c328`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 2.8 MB (2829133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121d7c7e80736da27a924b7bbc4c7d347f8de1e1e5d1227f2732342fd44df0a3`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858568419b94cae9ac32ee0afc3ecfeb070d2bf79da8598e2e9e20e51a82578`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d71d56eb6f4c2ce28105392f6cf227d8a82996c669bd7bd86ab5866364faa`  
		Last Modified: Sat, 06 Jul 2024 02:36:40 GMT  
		Size: 12.1 MB (12128108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770369fbd5b29ca943ac0dbe894618b0b9333e51cb983fdb5e8c7db952b155ee`  
		Last Modified: Sat, 06 Jul 2024 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96085ecbe366fb5e86ce7dd6ce3d341a1dd64a2f9dc7a5366bc9afc31a20b6a`  
		Last Modified: Sat, 06 Jul 2024 02:36:55 GMT  
		Size: 15.3 MB (15338893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f209e65a29485ca2b9af2ba729c4e595bca9aee74bc446def577ecbd4ac64ae`  
		Last Modified: Sat, 06 Jul 2024 02:36:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127a6f40955a853109b0eaa87c0b3a9ef3f7cda68760a5be0e860b501f893cdf`  
		Last Modified: Sat, 06 Jul 2024 02:36:54 GMT  
		Size: 19.4 KB (19387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb89b7821a6c6c707248a4eb0054f2460771b2ad0fd107f07849712869edcf2`  
		Last Modified: Sat, 06 Jul 2024 02:36:53 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa7b2bc17e66b5b5a1a107778cfbbc80321ab64b42db02545aad7beb14b5b6`  
		Last Modified: Sat, 06 Jul 2024 05:17:23 GMT  
		Size: 2.6 MB (2554982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b989d72e912e8b4de0299c59ce86cc4e571e58068caef5d2e2cd64d5c0d55`  
		Last Modified: Sat, 06 Jul 2024 05:17:23 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d8a674a2a6683bc81eee0879f2195c854646b7b050bc8973382ae0c130153`  
		Last Modified: Sat, 06 Jul 2024 06:09:20 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3091b5a38af2d56718d46f9d83c30f9251ca4610348e80ecd3778fb357bb8c2f`  
		Last Modified: Sat, 06 Jul 2024 06:09:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9341363e6b2eda941df53a3f9a7bfdb449d9ab0a64dda21880b4f14099a301`  
		Last Modified: Sat, 06 Jul 2024 06:17:00 GMT  
		Size: 21.1 MB (21068858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:02ad58f6148b62e627087bb20d365279d1dc7f5e79a8b061beaaa292bf574c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 KB (363731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00c5b4221384df6eae8153938e2826990da1dfb61429c022097d0c816972f10`

```dockerfile
```

-	Layers:
	-	`sha256:ff24dfbb7ed79b8696a24dad8c4c2c0adf4c332b0540649da16a5bde50d2de17`  
		Last Modified: Sat, 06 Jul 2024 06:16:57 GMT  
		Size: 330.4 KB (330359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2822fb26cdd12eb51dab9ffd20b11dd458c748babfd1154f322cdd2f4bee156`  
		Last Modified: Sat, 06 Jul 2024 06:16:57 GMT  
		Size: 33.4 KB (33372 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:cee0cacdf4010fa2b30932647d8111882a7f6c0f3c0174a58eb6825780d32007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57890820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f112a0cc59997f050efac12b7196251b9d209b4b29cee7d78f3124dfcefb2db`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:29 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 20 Jun 2024 17:38:29 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 21:18:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 21:18:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 21:18:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 21:18:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 21:18:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 21:18:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 21:18:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 21:18:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 21:58:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 20 Jun 2024 21:58:29 GMT
ENV PHP_VERSION=8.2.20
# Thu, 20 Jun 2024 21:58:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 20 Jun 2024 21:58:29 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 20 Jun 2024 21:58:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 21:58:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 22:11:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 22:11:27 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 22:11:28 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 22:11:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 22:11:28 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 22:11:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 22:11:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 22:11:29 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 22:11:29 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee93461fb0affa26ec63de4968aec9b190a692f67387914ce5413631503cfc9`  
		Last Modified: Thu, 20 Jun 2024 23:00:58 GMT  
		Size: 2.8 MB (2839145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce563d818438283f6ad202048afaf917002b477ed8e9f7cf92f702cb6e107ec`  
		Last Modified: Thu, 20 Jun 2024 23:00:57 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bd536aafcd34aa58a5e1fbb549c18ea11942f80f21b693f10fb0b654c9cfeb`  
		Last Modified: Thu, 20 Jun 2024 23:00:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c7e95739d8f5c8d81755a873a59d74d2905411c06af77b2981de91c33122ca`  
		Last Modified: Thu, 20 Jun 2024 23:02:55 GMT  
		Size: 12.1 MB (12118923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44816f1dd08a0f66a6b875e917b58226828bb008cafdefc14b3282678abc2c6f`  
		Last Modified: Thu, 20 Jun 2024 23:02:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ab909de62441379d34b0415a0dd37e152c39a30d7dfac2f964c37a86ff92a4`  
		Last Modified: Thu, 20 Jun 2024 23:03:14 GMT  
		Size: 13.2 MB (13197972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb63279887715fab90f40fe719b0b96b93e046c178d4dfe837dd6f2b2c6b7ba`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f6da55977bb8c6b6ecbb9526a234fa1494d9d8cca528158154417b9d1d835`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 19.6 KB (19558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4afed3e155dcfacf8c0734ff110722b493d217d7461a166247f5ec0fb90ca`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab8b6cde17c325d98971ca8484f61b57556ae2d62addfc65626a4cc9f88e406`  
		Last Modified: Sat, 06 Jul 2024 00:57:40 GMT  
		Size: 4.7 MB (4654950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133f74d5babf8314590a0f1f63b1ab75ba58d94cfb79522a9973aa375d199895`  
		Last Modified: Sat, 06 Jul 2024 00:57:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74051baea21409fa3ba664b5334ecf95f0ae3eafedd10ea2f96b18609db9abf`  
		Last Modified: Sat, 06 Jul 2024 00:57:40 GMT  
		Size: 726.3 KB (726334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03699d3f369e9931755d9b9c86ec0da57cb3c1241af566086cdd2f5a6cbe716`  
		Last Modified: Sat, 06 Jul 2024 00:57:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e471e3a0097ddb581e637e677a04dcefbca776ea263808f94e93e9e30bb1e770`  
		Last Modified: Sat, 06 Jul 2024 00:57:41 GMT  
		Size: 21.1 MB (21069042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:e4aad3eed91a1edfc699eb5e26401604175a339fbeb10e2dec4b57e603396643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 KB (365366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cb1cb6fbb98d4068911c5a6e396e7a1b9fae8bce557174be34e84e1fa8e80b`

```dockerfile
```

-	Layers:
	-	`sha256:4eaee3247034a5f7a79b8c9f028373600eb0924f619534c590cc59afe7d9e3f2`  
		Last Modified: Sat, 06 Jul 2024 00:57:39 GMT  
		Size: 332.8 KB (332788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3df08e508a0c62b7f2e9ce0fedf45008f4b6c0cca7f7f266e03ef63215d7ef`  
		Last Modified: Sat, 06 Jul 2024 00:57:39 GMT  
		Size: 32.6 KB (32578 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:5fd00b6b51ba802b277e1b896d15e46af6553ab2b024786bb1f8949f1920f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55613234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2164d19e39a70d584285622f197b0b5fd0c426a20979d483bd85c2d365a92779`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:51:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:51:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:51:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:52:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:52:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:52:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:52:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:52:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 19:09:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 20 Jun 2024 19:09:46 GMT
ENV PHP_VERSION=8.2.20
# Thu, 20 Jun 2024 19:09:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 20 Jun 2024 19:09:47 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 20 Jun 2024 19:09:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 19:09:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:15:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 19:15:13 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:15:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 19:15:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 19:15:16 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 19:15:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 19:15:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 19:15:18 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 19:15:18 GMT
CMD ["php-fpm"]
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
ENV DRUPAL_VERSION=10.3.0
# Thu, 20 Jun 2024 21:27:23 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 21:27:23 GMT
WORKDIR /opt/drupal
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb9ede040a8629a36c19a1019af3a33bdcab0e9b16dd4e50894df992e2bc57`  
		Last Modified: Thu, 20 Jun 2024 19:40:08 GMT  
		Size: 2.9 MB (2858706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1732b6eaedabe72854b318d620f62ca5985f9320a089bd90b6c760234d0c540`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4078b4ab583744a8a16db200a1b0a44450c6b122867ead7a14b2a395921cd4`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401f7ec3a545a393748afd413b96edc1d1a7d1a96a15d02f1ffaf1d652e4d686`  
		Last Modified: Thu, 20 Jun 2024 19:42:04 GMT  
		Size: 12.1 MB (12118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5d8169172cbb51d4754bdfb510f495754ed53d9795cc0877906721d1bee64`  
		Last Modified: Thu, 20 Jun 2024 19:42:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24502c03f9ac65a961c293a00f80fac893912909f98471dddd1c27c0174139d3`  
		Last Modified: Thu, 20 Jun 2024 19:42:21 GMT  
		Size: 13.3 MB (13342070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff6274fe7275ae6cf86fe95c2dffb6db1f570bf5b7f3730264b5509dd834da`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7bfe2f4b618a2635b70dd457dcc5ac235ac4fda212c48a6d49c3e129ebc81c`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 19.4 KB (19380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb6b5ccc954a4b32ee891a9b0b8d6a1ed5585e580c8ff92ca21ec1d6be5a744`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ccae45e04dda068c03b20dd3654329bceeddeaa6c4ce516edb407a922e251`  
		Last Modified: Fri, 21 Jun 2024 03:29:59 GMT  
		Size: 2.1 MB (2105092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd52057e424ada2c8ef9b5a7a5d0f4c230a9c5ff250e7556e9beeeffd34b7798`  
		Last Modified: Fri, 21 Jun 2024 03:29:59 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c3e4b6363e1de83bc894bb44098a677c81607d7f2e372de51395e5e99b7b1f`  
		Last Modified: Fri, 21 Jun 2024 06:25:29 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366f3fe7fa87154a1e1ca78a004dc0244f78585a706458fca221bebf16a38b43`  
		Last Modified: Fri, 21 Jun 2024 06:25:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e2512f5be79406740be084094e6e010706aa697f0a406669cc00e2e74ef57`  
		Last Modified: Mon, 24 Jun 2024 18:09:40 GMT  
		Size: 21.1 MB (21068080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:a2d793bffa5714d24ecd8db1851737623555bc60efe6271bb26edca4f3b59fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.1 KB (361127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a0c6acd2ce2fb2c1ee1307a6be8e1cb4c8c12f090a0d0fe1a6be32c35960a`

```dockerfile
```

-	Layers:
	-	`sha256:8f5551dae1d672550017ea40b4abb4ff2774d303a69b56cf1442fc371694dd6c`  
		Last Modified: Mon, 24 Jun 2024 18:09:38 GMT  
		Size: 328.4 KB (328359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9df85ab3155e7f859f2bcae7b1551c8a98ddc78adbf6ee807965ee69c347cc4`  
		Last Modified: Mon, 24 Jun 2024 18:09:38 GMT  
		Size: 32.8 KB (32768 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:6be53b5408e79ba3969023c70007481b8e936fca37f3a5493e608580268a82e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57286797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9e227a2a956b96b5bef000400b168da73c7fd77dd4d334c1d566b759e18b82`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:57:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 21 Jun 2024 00:57:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 21 Jun 2024 00:57:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 21 Jun 2024 00:57:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Jun 2024 00:57:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 21 Jun 2024 00:57:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:57:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:57:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Jun 2024 01:29:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7206a1bfab077fd781ea2f1bff4245da6a985c14e5ac529be337f2a603bfe2`  
		Last Modified: Fri, 21 Jun 2024 02:03:40 GMT  
		Size: 3.0 MB (2956393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127507485549677fb9d01f808d1e93e9bd9c50738e97f7d5f24eb6c5c0177d39`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d9ac49dc0992d0026684046dc69d1afde3acf6907aaf78e13654907905c8b7`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b26240051cb075d6cd566fba9974144bc239fa9494331cb750ea06d0a086a`  
		Last Modified: Sat, 06 Jul 2024 02:12:57 GMT  
		Size: 12.1 MB (12128107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c35ce0196eb7f7970b7a5aace64fc45d316c99012e6458a500a0cb038f886aa`  
		Last Modified: Sat, 06 Jul 2024 02:12:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af49b55935a663258837d86c7c79e62c88b5118378b767a2104eca7cdedb6e70`  
		Last Modified: Sat, 06 Jul 2024 02:13:09 GMT  
		Size: 15.1 MB (15122311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad75a227691311b10f98d104a1d99fe699846182c3c440b46747994d0da5f58`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf273803a6e8761d4182808f91636c7ef245c6643be3c1cb2e99e5a859215e94`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295aa649f23a1813f18118fd39becd982caa78f641b1d358c03b3e8506d58416`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c21577ba51ac5e5ff82dc61428614fcb3f8f8db643b1f55e7a1c63dca72fdb`  
		Last Modified: Sat, 06 Jul 2024 04:19:02 GMT  
		Size: 2.0 MB (1998725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f9f7eb9e9e7f896eb9486364b3143d1d174055b70a9f1dfc8853bbe67160d`  
		Last Modified: Sat, 06 Jul 2024 04:19:02 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb093a8e32bef309ab3fc51f402d6bd52a7a182778cc65144ebbbf423b206b`  
		Last Modified: Sat, 06 Jul 2024 06:05:52 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680c65776939655e172050e3c1c6d39fbb62ef0adc81a37eeea7850d7fd5d5e`  
		Last Modified: Sat, 06 Jul 2024 06:05:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875fc4978f1b0a651c0453d28f18298be359edc7fde0526ac19da6d8389a3957`  
		Last Modified: Sat, 06 Jul 2024 06:16:07 GMT  
		Size: 21.1 MB (21069053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:153eb590ec4b581cc743d37fe0b61b37fb74e6aed2801132e7d220ef6e37b726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 KB (360992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b832f412a13a4582a97e37aac68c81f0de3bbad9de6ca97a52bdcfe2242270f3`

```dockerfile
```

-	Layers:
	-	`sha256:16d8f9b6639e7d0df0aa4344ae214f0bc2690538ab367565982c8ac916766504`  
		Last Modified: Sat, 06 Jul 2024 06:16:06 GMT  
		Size: 328.3 KB (328301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5a4e2d0127b552f598317feb12916e0de593ca4d94655805089629f895ed86`  
		Last Modified: Sat, 06 Jul 2024 06:16:06 GMT  
		Size: 32.7 KB (32691 bytes)  
		MIME: application/vnd.in-toto+json
